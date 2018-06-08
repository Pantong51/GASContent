# Binding Attribute Delegates To Update Your UI
One common issue for developers trying to implement the Gameplay Ability System for the first time is getting those updates
from the system about Attribute changes.  In most games this is a core feature in order to keep the players UI responsive to changes
about their health, mana etc.

This is a very breif tutorial that assumes you have already followed guides to set up your AttributeSet and Character for the Gameplay Ability System.

First in your MyCharacter.h file we need to add a delegate which will be accessible to the UI in BP and C++

```
DECLARE_DYNAMIC_MULTICAST_DELEGATE_OneParam(FHealthChange, float, CharacterHealth);
UPROPERTY(BlueprintAssignable, Category = "Delegates")
FHealthChange OnHealthChange;
```
  
Then we want to declare a function that will be called by the Attribute's delegate to fire our delegate (or do what ever kind of processing you need to)
  
``'
void HealthAttributeUpdated(const FOnAttributeChangeData& Data);
{
	OnHealthChange.Broadcast(Data.NewValue);
{
```

Finally we need to bind to the actual Attribute delegate, which we will do in the BeginPlay() function of your character's cpp file.
  
```
void AMyCharacter::BeginPlay()
{
	Super::BeginPlay();

	if (AbilitySystem)
	{
    AbilitySystem->GetGameplayAttributeValueChangeDelegate(UMyAttributeSet::HealthAttribute()).AddUObject(this, &MyCharacter::HealthAttributeUpdated);
  }
}
```

Note that the MyAttributeSet has a static function that returns the health attribute, you should have one for every attribute.

Thats it, now all you need to do is bind to your delegate in the UI to get updates any time the ability system changes your health.

Written By DeadlyMidnight

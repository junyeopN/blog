# C++ For Unreal

## Timer

- Use FTimerHandle to handle events that happen periodically.

```cpp
void ATower::BeginPlay()
{
    Super::BeginPlay();
    tank_ = Cast<ATank>(UGameplayStatics::GetPlayerPawn(GetWorld(), 0));

	// FTimerHandle, Trigger Class, Trigger Function when timer is up, repeat
    GetWorldTimerManager().SetTimer(fire_rate_timer_handle_, this, &ATower::CheckFireCondition, fire_rate_, true);
}
```

- The example executes CheckFireCondition() function every time fire*rate* period timer is up.
- Because last argument is true, the timer repeats every time. Else it ends after first timer is over.

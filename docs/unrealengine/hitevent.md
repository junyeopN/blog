# Hit Event

# OnComponentHit.AddDynamic()

- Can bind hit events with a function
- **needs to be bound on BeginPlay; constructor is too early**.

```cpp
// binding function needs to take the following 5 parameters
// also needs UFUNCTION()
UFUNCTION()
void OnHit(UPrimitiveComponent* HitComp, AActor* OtherActor, UPrimitiveComponent* OtherComp, FVector NormalImpulse,
    const FHitResult& Hit);
```

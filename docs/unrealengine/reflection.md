# Unreal Engine Reflection Functions

## 1. TSubClassOf<T>, SpawnActor<T>

- Used when we want to **dynamically load a blueprint class that inherits a C++ class**

### ex)

1. class A is c++ class
2. class B is a blueprint class inheriting B, has static mesh.
3. class C is a c++ class that wants to use B because of its static mesh.

then we use TSubClassOf to declare the class we want in blueprint editor, and SpawnActor to spawn the dynamically declared class.

```cpp
// BasePawn.h

TSubClassOf<class AProjectile> projectile_class_;


// BasePawn.cpp
GetWorld()->SpawnActor<AProjectile>(projectile_class_->GetClass(), projectile_spawn_point_->GetComponentLocation(),
    projectile_spawn_point_->GetComponentRotation());
```

## 2. CreateDefaultSubobject<T>(TEXT({object_name}))

- Creates subobject belonging to Actor/Pawn
- Only can be used in Constructor because it needs to initialize in Blueprint.
- Can assign as root component, or declare as child of another component by using `SetupAttachment`

```cpp
// Sets default values
ABasePawn::ABasePawn()
{
    // Set this pawn to call Tick() every frame.  You can turn this off to improve performance if you don't need it.
    PrimaryActorTick.bCanEverTick = true;

    capsule_component_ = CreateDefaultSubobject<UCapsuleComponent>(TEXT("Capsule Component"));

    if (capsule_component_)
    {
        RootComponent = capsule_component_;
    }

    base_mesh_ = CreateDefaultSubobject<UStaticMeshComponent>(TEXT("Base Mesh"));

    if (base_mesh_)
    {
        base_mesh_->SetupAttachment(RootComponent);
    }

    turret_mesh_ = CreateDefaultSubobject<UStaticMeshComponent>(TEXT("Turret Mesh"));

    if (turret_mesh_)
    {
        turret_mesh_->SetupAttachment(base_mesh_);
    }

    projectile_spawn_point_ = CreateDefaultSubobject<USceneComponent>(TEXT("Projectile Spawn Point"));

    if (projectile_spawn_point_)
    {
        projectile_spawn_point_->SetupAttachment(turret_mesh_);
    }
}
```

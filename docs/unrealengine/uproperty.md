# UPROPERTY

Used to define Blueprint properties for C++ class members.

## 1. Editability

- EditAnywhere/VisibleAnywhere/EditDefaultsOnly

## 2. Blueprint Access

- BlueprintReadOnly, BlueprintReadWriteOnly

## 3. Category

- Used to categorize members in blueprint editor

```cpp
UPROPERTY(Category = "Components")
```

## 4. meta

```cpp
UPROPERTY(meta = (AllowPrivateAccess = "true"))
```

- Can edit private members in Blueprint if this is added.

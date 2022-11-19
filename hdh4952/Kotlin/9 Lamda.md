# 9. Lamda

- Lamda (익명함수)
    - 메소드의 파라미터로 넘겨줄 수 있다.
    - return 값으로 사용할 수 있다.

- 기본 형태

```kotlin
val 람다함수명 : Type = {argument : Type -> statement}
```

- 예시1

```kotlin
val square : (Int) -> (Int) = {number -> number * number}
println(square(3)) // -> 9
```

- 예시2

```kotlin
val nameAge = {name : String, age : Int -> "my name is ${name}, ${age} years old"}
println(nameAge("Kotlin", 10)) // -> my name is Kotlin, 10 years old
```

- 확장함수
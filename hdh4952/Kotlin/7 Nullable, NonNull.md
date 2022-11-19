# 7. Nullable, NonNull

- Nullable로 선언하려면 type뒤에 ?를 붙인다

```kotlin
var name : String = "Kotiln" // NonNull
var nullName : String? = null // Nullable
var nameToUpperCase = name.toUpperCase() // -> KOTLIN
var nullNameToUpperCase = nullName?.toUpperCase() // 만약 nullName이 null이면 null 반환
```

- ?:

```kotlin
val name : String? = null
val hello = "Hello "   (name? : "Kotiln") // -> Hello Kotlin
```

만약 null일 경우 콜론(:) 뒤에 있는 Expression이 적용

- !!

```kotlin
fun ignoreNull(str : String?) {
	val notNull : String = str!!
	val upper = notNull.toUpperCase()
}
```

컴파일러에게 null이 아니라는 것을 알려줌

- let

```kotlin
val name : String? = "Kotlin"
name?.let {
	println("Hello ${name}") // -> Hello Kotlin
}
```

name이 null이 아닐 경우 println 실행
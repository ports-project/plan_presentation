# 8. class

```kotlin
class Human {
	val name = "Kotlin"

	fun hello() {
		println("Hello!")
	}
}

fun main() {
	val human = Human()
	human.hello() // -> Hello!
	println("my name is ${human.name}") // -> my name is Kotiln
}
```

- 주생성자

```kotlin
class Human constructor(val name : String = "noname"){

	fun hello() {
		println("Hello!")
	}
}

fun main() {
	val human = Human("Kotlin")
	val human2 = Human()
	human.hello() // -> Hello!
	println("my name is ${human.name}") // -> my name is Kotiln
	println("my name is ${human2.name}") // -> my name is noname
}
```

constructor 생략 가능

- init

```kotlin
class Human constructor(val name : String = "noname"){

	init {
		println("New human has been born!")
	}

	fun hello() {
		println("Hello!")
	}
}

fun main() {
	val human = Human("Kotlin")
	val human2 = Human()
	human.hello() // -> Hello!
	println("my name is ${human.name}") // -> my name is Kotiln
	println("my name is ${human2.name}") // -> my name is noname
}
```

init은 클래스 객체가 생성될 때 한번만 실행된다.

- 부생성자

```kotlin
class Human(val name : String = "noname"){

	constructor(name : String, age : Int) : this(name) {
		println("my name is ${name}, ${age} years old")
	}

	init {
		println("New human has been born!")
	}

	fun hello() {
		println("Hello!")
	}
}

fun main() {
	val human = Human("Kotlin", 10)
	// -> New human has been born!
	// -> my name is Kotiln, 10 years old
}
```

- 상속

```kotlin
open class Human(val name : String) {
	fun hello() {
		println("Hello!")
	}
}

class Korean : Human() {
	
}

fun main() {
	val korean = Korean()
	korean.hello() // -> Hello!
}
```

- 오버라이딩

```kotlin
open class Human(val name : String) {
	open fun hello() {
		println("Hello!")
	}
}

class Korean : Human() {
	override fun hello() {
		println("Hi!")
	}
}

fun main() {
	val korean = Korean()
	korean.hello() // -> Hi!
}
```

- super

```kotlin
open class Human(val name : String = "Kotlin") {
	open fun hello() {
		println("Hello!")
	}
}

class Korean : Human() {
	override fun hello() {
		super.hello()
		println("Hi!")
		println("my name is ${name}")
	}
}

fun main() {
	val korean = Korean()
	korean.hello()
	// -> Hello!
	// -> Hi!
	// -> my name is Kotlin
}
```

super는 상위 클래스의 메서드, 프로퍼티, 생성자를 사용하는 키워드
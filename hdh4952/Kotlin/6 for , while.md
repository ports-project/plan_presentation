# 6. for , while

- for

```kotlin
val num = arrayListOf(1, 2, 3, 4, 5)

for (n in num) {
	println(n)
}

var sum = 0

for (i in 1..10) sum  = i
println(sum) // -> 55

sum = 0
for (i in 1..10 step 2) sum  = i
println(sum) // -> 25 

sum = 0
for(i in 10 downTo 1) sum  = i
println(sum) // -> 55

sum = 0
for(i in 1 until 10) sum  = i
println(sum) // -> 45

for((index, n) in num.withIndex()) {
	println("${index} ${n}, ") // ->0 1, 1 2, 2 3, 3 4, 4 5 
}
```

- while

```kotlin
var index = 0
while(index < 10) {
	println(index  )
}
// -> 0 1 2 3 4 5 6 7 8 9
```
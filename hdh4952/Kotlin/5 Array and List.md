# 5. Array and List

```kotlin
val array = arrayOf(1, 2, 3) // Array<Int>
val array2 = arrayOf(1, "a", 3.4f) // Array<Any>
val list = listOf(1, 2, 3) // List<Int>
val list2 = listOf(1, "a", 3.4f) // List<Any>

val arrayList = arrayListOf<Int>() // ArrayList<Int>
arrayList.add(10)
arrayList.add(20)
```

기본적으로 array는 mutable, list는 nonmutable

- Array
    - 배열 크기 변경 불가, 값 수정 가능
- List
    - 읽기 전용
- ArrayList
    - 크기 변경 가능, 값 수정가능
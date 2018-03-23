# Array - Chuỗi trong Kotlin

```
class Array<T> private constructor() {
    val size: Int
    operator fun get(index: Int): T
    operator fun set(index: Int, value: T): Unit

    operator fun iterator(): Iterator<T>
    // ...
}
```

## Khởi tạo:

```
arrayOf(1, 2, 3)
arrayOfNulls(3) - Khởi tạo một array gồm 3 phần tử có giá trị Nulls

// tạo một Array<String> với giá trị ["0", "1", "4", "9", "16"]
val asc = Array(5, { i -> (i * i).toString() })
```

## Phép gán cho một array khác - Cast down
```
Array<Any> = Array<String>  // error
```

Trên là interface của lớp Array, chúng ta còn có class **ByteArray, ShortArray, IntArray** cũng biểu diễn chuỗi của các lại dữ liệu căn bản. Chúng không có mối 
quan hệ kế thừa từ **Array**, có cùng tập các phương thức và thuộc tính giống nhau.

```
val x: IntArray = intArrayOf(1, 2, 3)
x[0] = x[1] + x[2] 
// x[0] = 5

```



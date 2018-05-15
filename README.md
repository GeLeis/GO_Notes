# GO_Notes
GO study note 
sublime的build path 路径配置
/Users/Mac/Library/Application Support/Sublime Text 2/Packages/User

## 1.printf打印参数需要占位符,println打印参数不需要
## 2.每个go程序都是一个包，惯例
包名与导入路径的最后一个目录一致，例如math/rand包由 packgge rand语句开始

## 3.组合导入
```
import(
	“xx”
	“xx”
)
```

## 4.在go语言中，首字母大写的都是要被导出的
当连续的函数命名参数是同一类型，则除了最后一个类型之外，其他可省略
```
func add(x, y int) int {
	return x + y
}
```

## 5.go语言字符串用””，函数可以返回任意数量的返回值
```
func swap(x, y string) (string, string) {
	return y, x
}
——>
a, b := swap("hello", "world")
```

## 6.没有参数的return语句返回结果的当前值，
go的返回值可以被命名，并且像变量那样使用，返回值的名称应当具有一定的意义，可以作为文档使用
```
func split(sum int) (x, y int) {
	x = sum * 4 / 9
	y = sum - x
	return
}
```

## 7.与c语言不通的是，go在不同类型之间的转换需要现实转换

## 8.常量的定义与变量类似，只不过使用const关键字，常量可以是字符，字符串，布尔或数字类型，不能使用 := 语法定义,未指定类型的常量由上下文来决定
```
const Pi = 3.14
```

## 9.go的for循环,没有()，其他和java一样,跟c或者java中一样，可以让前置/后置语句为空，相当于while
```
for i := 0; i < 10; i++ {
    sum += i
}
	
sum := 1
for sum < 1000 {
    sum += sum
}
```

## 10.if也是没有(),必须要用{},在if的便捷语句定义的变量同样可以在任何对应的else中使用

## 11.go语言保存了变量的内存地址，类型*T是指向类型T的值的指针，其零值是nil，与c不通，go没有指针运算

## 12.结构体字段可以通过结构体指针来访问,通过指针间接访问是透明的,特殊的前缀 & 返回一个指向结构体的指针

## 13.slice切片[lo:li],从lo开始到li-1结束，包含lo和li-1，从0开始

## 14.函数也是一个返回值，go函数也可以是闭包的，闭包是一个函数值，他来自函数体的外部的变量引用，函数可以对这个引用值进行访问和赋值。换句话说这个函数被绑定在这个变量上

## 15.goroutine是由Go运行时环境管理的轻量级线程，开启一个新的goroutine执行,go f(x,y,z)，goroutine在相同的地址空间中运行，因此访问共享内存必须进行同步

## 16.channel是有类型的管道，可以用channel操作符<-对其发送或者接收值
ch <- v

## 17.for range不仅能遍历map,slice,array还可以去除channel中数据

## 18.time.Tick()返回的是一个channel






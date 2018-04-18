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

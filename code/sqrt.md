    package main

    import (
        "fmt"
        "math"
    )

    //一个整数，它加上100后是一个完全平方数，再加上168又是一个完全平方数，请问该数是多少？

    func main() {
        var i float64
        //定义一个最大范围1万以内
        for i = 10000; i > 0; i-- {
            x := int32(math.Sqrt(i + 100))
            y := int32(math.Sqrt(i + 268))

            if x*x == int32(i+100) && y*y == int32(i+268) {
                fmt.Println(i)
            }
        }

    }


math.Sqrt(x)  这里的参数必须是一个float64的类型

x == int32(x) //这个在golang中是无法比较的，所以在前面获得x的值的时候
先进行类型转换到int32，再笔记


//结果：
1581

261

21



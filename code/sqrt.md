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
            x := math.Sqrt(i + 100)
            y := math.Sqrt(i + 268)

            if x*x == i+100 && y*y == i+368 {
                fmt.Println(i)
            }
        }

    }

    //zhe个数暂时没有求解出来

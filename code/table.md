输出乘法表

    package main

    import "fmt"

    func main() {
        for i := 1; i <= 9; i++ {
            for j := 1; j <= 9; j++ {
                if j <= i {
                    //交换i和j将会出现不同的形式的乘法表
                    fmt.Printf("%d * %d = %d  ", i, j, i*j)
                }
            }
            fmt.Println("\n")
        }
    }

    note:printf()里面的第一个参数和c一致

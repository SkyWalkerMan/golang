输出国际象棋棋盘。

    package main

    import "fmt"

    func main() {
        var i, j, k int32

        for i = 1; i <= 8; i++ {
            fmt.Println("---------------------------------------")
            for j = 1; j <= 8; j++ {
                k = i + j
                if is_sushu(k) {
                    fmt.Printf("|白| ")
                } else {
                    fmt.Printf("|黑| ")
                }
            }
            fmt.Println("\n")
        }
        fmt.Println("---------------------------------------")
    }

    //判断一个数是否是素数
    func is_sushu(n int32) bool {
        if n%2 == 0 {
            return true
        } else {
            return false
        }
    }

    note:国际象棋的棋盘式黑白相间的，i+j是偶数的是所在位置是黑格，为基数的时候所在位置为白格

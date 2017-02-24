输入三个整数x,y,z，请把这三个数由小到大输出。


    package main

    import "fmt"

    func main() {
        var x, y, z, temp int
        fmt.Print("请输入三个数:")
        fmt.Scanf("%d %d %d", &x, &y, &z)

        if x > y {
            temp = x
            x = y
            y = temp
        }

        if x > z {
            temp = z
            x = z
            z = temp
        }

        if y > z {
            temp = y
            y = z
            z = temp
        }

        fmt.Println(x, y, z)
    }


    //最终排序结果是下x <y <z
    //假定x是最小值，用最小的值和其他的值进行比较保证x始终是最小，通过交换的方式。
    //fmt.Scanf() //获取多个值


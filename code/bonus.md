企业发放的奖金根据利润提成。利润(I)低于或等于10万元时，奖金可提10%；利润高
于10万元，低于20万元时，低于10万元的部分按10%提成，高于10万元的部分，可可提
成7.5%；20万到40万之间时，高于20万元的部分，可提成5%；40万到60万之间时高于
40万元的部分，可提成3%；60万到100万之间时，高于60万元的部分，可提成1.5%，高于
100万元时，超过100万元的部分按1%提成，从键盘输入当月利润I，求应发放奖金总数？

    package main

    import (
        "fmt"
    )

    func main() {
        var bonus1, bonus2, bonus4, bonus6, bonus10, bonus float64

        var money float64
        fmt.Printf("请输入内容：")
        fmt.Scanf("%f", &money)
        //	money := strconv.Atoi(s)

        bonus1 = 100000 * 0.1
        bonus2 = bonus1 + 100000*0.075
        bonus4 = bonus2 + 200000*0.05
        bonus6 = bonus4 + 200000*0.03
        bonus10 = bonus6 + 400000*0.015

        if money <= 100000 {
            bonus = money * 0.1
        } else if money <= 200000 {
            bonus = bonus1 + (money-100000)*0.075
        } else if money <= 400000 {
            bonus = bonus2 + (money-200000)*0.05
        } else if money <= 600000 {
            bonus = bonus4 + (money-400000)*0.03
        } else if money <= 1000000 {
            bonus = bonus6 + (money-600000)*0.015
        } else {
            bonus = bonus10 + (money-1000000)*0.01
        }

        fmt.Println(bonus)
    }

//note:
//不同不类型的变现不能直接进行运算，float64和int进行运算时非法的

//获取命令行的输入使用fmt.Scanf('参数类型',&接收值),还可以使用os.Stdin获取命令行的输入

//

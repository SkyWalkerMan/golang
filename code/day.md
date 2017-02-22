    package main

    import (
        "fmt"
        "strconv"
        "strings" //调用Split字符串分割函数
    )

    //判断用户输入的年月日是这一年的第几天，闰年的时候考虑多加一天

    func main() {
        var date string
        var sum int
        fmt.Print("请输入年月日格式（年-月-日）:")
        fmt.Scanf("%s", &date)

        //	handler_after := strings.Fields() //按空格分隔为数组
        handler_after := strings.Split(date, "-") // 2017-10-5  ---->[2017 10 5]

        //转换为数字
        year, _ := strconv.ParseInt(handler_after[0], 10, 0) //strconv 把字符串转换为int64
        month, _ := strconv.ParseInt(handler_after[1], 10, 0)
        day, _ := strconv.ParseInt(handler_after[2], 10, 0)

        //计算某个月之前的天数
        switch month {
        case 1:
            sum = 0
        case 2:
            sum = 31
        case 3:
            sum = 59
        case 4:
            sum = 90
        case 5:
            sum = 120
        case 6:
            sum = 151
        case 7:
            sum = 182
        case 8:
            sum = 213
        case 9:
            sum = 243
        case 10:
            sum = 274
        case 11:
            sum = 304
        case 12:
            sum = 335
        }

        if isleap(year) {
            sum = sum + int(day) + 1 //这里sum定义的是int类型，所以需要对类型转换
        } else {
            sum = sum + int(day)
        }

        fmt.Println("您输入的日期是该年的第:" + strconv.Itoa(sum) + "天，" + strconv.Itoa(int(year)) + "年都过去了这么多天，你TM的都干了些啥") //数字转换字符串strconv.Atoi(sum)

    }

    func isleap(year int64) bool {
        if (year%4 == 0 && year%100 != 0) || (year%400 == 0) {
            return true
        } else {
            return false
        }
    }

    //go和php中02==2

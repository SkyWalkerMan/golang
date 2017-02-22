1、给定一些数字，组合出多少个不同的三位数

code:

    package main

    import "fmt"
    import "strconv" //用于数字转字符串，方便使用+连接字符串

    //1,2,3,4这4个数组成多少个每个位置不重复的3位数

    var num = []int{1, 2, 3, 4, 5} //定义一个list，需要处理这个数组组成一个不重复的单个数字

    func main() {
    	len := len(num)
    	for i := 0; i < len; i++ {
    		for j := 0; j < len; j++ {
    			for k := 0; k < len; k++ {
    				if i != j && j != k && k != i {
    					//满足的唯一条件三个索引不相同即可
    					fmt.Println(strconv.Itoa(num[i]) + strconv.Itoa(num[j]) + strconv.Itoa(num[k]))
    				}
    			}
    		}
    	}
    }


note:
golang：字符串的链接可以使用+号，类似php
golang：数字转字符串，需要引入strconv包，字符串的转换
不同的三位数只要数组的所以不同所获得三位数就是不同的。。


# 2024091203030-吴芳玉-JAVA-04

## java04(1)
```java
package com.glimmer04;

import java.util.Scanner;

public class ifelse {
    //这个函数用于判断传入的年份是否为闰年
    //是闰年返回1，不是闰年返回2
    //则该程序需要两部分完成，第一部分完成传入，第二部分完成判断是否闰年
    public static void main(String[] args) {
        //以下是一个用于用户传入年份的方法
        Scanner sc = new Scanner(System.in);
        System.out.println("请输入年份：");
        int year = sc.nextInt();

        //以下方法用于判断传入的年份是否为闰年
        //是闰年返回1，不是闰年返回2
        if (year % 4 == 0) {
            System.out.println(1);
        } else {
            System.out.println(2);
        }
    }
}
```
## java04(2)
```java
package com.glimmer04;

import java.util.Scanner;

public class forwhile {
    public static void main(String[] args) {
    //以下用于让用户键入所打印的图形高度区间
    Scanner sc = new Scanner(System.in);
    System.out.println("请输入一个数值C，以打印出高度为【3，C】中所有奇数的空心菱形"+'\n'+"C:");
    int C = sc.nextInt();
        //以下用来保证n为奇数的语句
        for(int n = 3;n <=C;n+=2){
            //以下创建一个长度为n的数组，用于每一行的编写
            String[] a =new String[n];
            //以下代码用于写第1到（n+1）/2行的图形
            int i = (n+1)/2-1;
            int j = (n+1)/2-1;
            while (i>=0&&j<=a.length){
                a[i] = "*";
                a[j] = "*";
                //以下代码使得输出的null转为空格符
                for (int m = 0; m < a.length; m++) {
                    if(a[m] ==null){
                        a[m] = " ";
                    }
                    System.out.print(a[m]);  //这一步遍历数组，输出一行图形
                }
                //以下代码用于行与行之间的换行
                String newLine = System.lineSeparator();
                System.out.println(System.lineSeparator());
                //以下代码使数组a存储的数据回到null，以便于下一次循环的赋值
                a[i] = null;
                a[j] = null;

                i--;j++;
            }
            //以下代码用于写第（n+1）/2+1行到第n行的图形，基本流程与上一部分代码相同
            int k =1;
            int p =n-2;
            while (k<=p){
                a[k] = "*";
                a[p] = "*";
                //以下使得输出的null转为空格符
                for (int m = 0; m < a.length; m++) {
                    if(a[m] ==null){
                        a[m] = " ";
                    }
                    System.out.print(a[m]);//这一步遍历数组，输出一行图形
                }
                //以下用于行与行之间的换行
                String newLine = System.lineSeparator();
                System.out.println(System.lineSeparator());
                //以下使数组a存储的数据回到null，以便于下一次循环的赋值
                a[k] = null;
                a[p] = null;
                k++;p--;

            }
            //以下用于n取值不同时便于观察的分割线
            System.out.println("-------------------------------------");

            
        }


    }
}
```
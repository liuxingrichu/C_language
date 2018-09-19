### 简单成绩评价系统 ###
/*
C语言经典程序之：简单成绩评价系统
C语言编程要求：

    要求编写一个简单的成绩评价系统

      1  要求循环对若干（未知数）学生的百分制成绩进行评价；

      2  90分以上（包括100分），等级为A；

          80分以上（包括80分，但不包括90分），等级为B；

          70分以上（包括70分，但不包括80分），等级为C；

          60分以上（包括60分，但不包括70分），等级为D；

          60分以下（不包括60分，包括0分），等级为E；

      3  健壮性判断：超过100分或低于0分，程序报错。

      参考：https://www.cnblogs.com/Joynic/archive/2013/01/27/2879201.html

*/

#include "stdio.h"
void main()
{
   int n;                   /*定义整数n*/
   float score;         /*把score设为浮点型，因为成绩有可能是小数，例如86.5*/

    printf("Please Enter Your Score:");       /*用户提示信息*/
    scanf("%f",&score);                             /*从键盘读取score*/

    if(score<0||score>100)
    {

         printf("The score you input is illegal!\n");      /*假如输入分数大于100或小于0，报错*/
    }
  else         /*输入成绩合法的情况*/
  {

      n=(int)score/10;     /*score处以10，并强制转换成整形，赋给n，方便switch判断*/
      switch(n)               /*Switch语句*/
      {
       case 10:
       case 9:printf("A\n");break;        /*10跟9相同，都为A*/
       case 8:printf("B\n");break;
       case 7:printf("C\n");break;
       case 6:printf("D\n");break;
       default:                                      /*缺省的值，即n=5、4、3、2、1、0等值的情况*/
          printf("E\n");break;
        }
    }
}

### 歌星大奖赛 ###

	/*
	歌星大奖赛
	
	在歌星大奖赛中，有10个评委为参赛的选手打分，分数为1~100分。
	选手最后得分为：去掉一个最高分和一个最低分后其余8个分数的平均值（四舍五入）。
	请编写一个程序实现。
	
	*/
	
	#include<stdio.h>
	
	int main()
	{
	    int integer,i,max,min,sum;
	//   max=-32768; /*先假设当前的最大值max为C语言整型数的最小值*/
	//   min=32767; /*先假设当前的最小值min为C语言整型数的最大值*/
	    max = 0;
	    min = 100;
	    sum=0; /*将求累加和变量的初值置为0*/
	    for(i=1;i<=4;i++)
	    {
	        printf("Input number %d=", i);
	        scanf("%d",&integer); /*输入评委的评分*/
	        sum+=integer; /*计算总分*/
	        if(integer>max)
	            max=integer; /*通过比较筛选出其中的最高分*/
	        if(integer<min)
	            min=integer; /*通过比较筛选出其中的最低分*/
	    }
	    printf("Canceled max score:%d\nCanceled min score:%d\n",max,min);
	    printf("Average score:%f\n", (sum-max-min)/8.0); /*输出结果*/
	    printf("Average score:%d\n", (int)((sum-max-min)/8.0 + 0.5)); /*输出结果*/
	}



### 数据格式化输出不配套  ###
	#include <stdio.h>
	
	int main()
	{
	    float p;
	    float oa1[11]={12,156,1,51,145,1,32};
	    float ar(float array[10]);
	    p=ar(oa1);
	    return 0;
	}
	
	float ar(float array[10])
	{
	    int a,b,min,max,i;
	    //float i;
	    i=array[0];
	    for(a=1;a<10;a++)
	        if(i<array[a]) i=array[a];
	    printf("%.1f\n", i);
	    printf("%d", i);
	    return 0;
	}

浮点型数据格式化，输入整型数时，输出0.

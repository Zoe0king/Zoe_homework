# Zoe_homework
项目一
#include <stdio.h>
void main()
{
	int N,n,M=1,m;  //定义N（层数）n（储存N的值），M（每层*号数量）m（储存M的值）
	char k;   //定义k（每层*前的空）
	k='   ';
	printf("不应只是追求5层，应该追求自定义层数\n");
	printf("输入*号金字塔层数");
	scanf("%d",&N);   //设定*号金字塔层数
	while(N>0)   //每层*号输出循环
	{
		n=N;  //储存N的值于n中
		m=M;  //储存M的值于m中
		A: if(n>0)   //每层*前的空格多少，越在金字塔尖部空格越多
		{
			printf("%c",k);
			n--;
			goto A;  //使用该函数返回if函数实现多空格的效果
		}
		else if(m>0)  //层数越多*号越多
		{
			printf("* ");
			m--;
			goto A;  //使用该函数返回if函数实现随层数增加*数增加的效果
		   }
		   N--;    //减为0时结束while循环
		   M++;    //增加下一层*数
		   printf("\n");  //下一层
	}
}

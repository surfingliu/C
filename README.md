# C
学习C语言
#define _CRT_SECURE_NO_WARNINGS

//#include<stdio.h>
//void reverse_string(char* string)
//{
//	if (*string != '\0')
//	{
//		reverse_string(string+1);
//	
//	printf("%c ", *string);
//	}
//	else
//	{
//		printf("");
//	}
//}
//int main()
//{
//	char arr[10];
//	scanf("%s", arr);
//	reverse_string(arr);
//	return 0;
//}
//#include<stdio.h>
//int DigitSum(n)
//{
//	int sum=n%10;
//	if (n > 9)
//	{
//		sum+=DigitSum(n/10);
//	}
//	return sum;
//}
//int main()
//{
//	int n;
//	int ret;
//	scanf("%d", &n);
//	ret=DigitSum(n);
//	printf("%d", ret);
//	return 0;
//}
//#include<stdio.h>
//int calculate(int n,int k)
//{
//	if(k>0)
//	return n * calculate(n, k - 1);
//	if (k == 0)
//		return 1;
//}
//int main()
//{
//	int n;
//	int k;
//	int ret;
//	scanf("%d %d",&n, &k);
//	ret = calculate(n, k);
//	printf("%d", ret);
//	return 0;
//}
//#include<stdio.h>
//int fab(int n)
//{
//	int i;
//	int a = 1, b = 1, temp = 0;
//	if (n < 3)
//		return 1;
//	else
//	{
//		for (i = 0; i <= n - 3; i++)
//		{
//			temp = a + b;
//			a = b;
//			b = temp;
//		}
//		return temp;
//	}
//}
//int main()
//{
//	int n;
//	int ret;
//	scanf("%d", &n);
//	ret=fab(n);
//	printf("%d", ret);
//	return 0;
//}
//#include<stdio.h>
//#include<assert.h>
//int my_strlen(const char* str)
//{
//	assert(str);
//	int count = 0;
//	while (*str++)
//	{
//		count++;
//	}
//	return count;
//}
//int main()
//{
//	char str[10] = { 0 };
//	scanf("%s", str);
//	printf("%d", my_strlen(str));
//	return 0;
//}
#include<stdio.h>
#include<assert.h>
void  my_strcpy( char*a, char*b)
{
	assert(a);
	assert(b);
	int i = 0;
	for (i = 0; i < 10; i++)
	{
		a[i] = b[i];

	}
}
int main()
{
	char a[] = { 0 };
	char b[] = { 0 };
	scanf("%s", a);
	scanf("%s", b);
	my_strcpy(a, b);
	printf("%s", a);
	return 0;
}

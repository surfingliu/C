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

#define _CRT_SECURE_NO_WARNINGS

//#include<stdio.h>
//#include<string.h>
//void pre(char* a)
//{
//	int sz = 0;
//	sz = strlen(a);
//	int left = 0;
//	int right = sz - 1;
//	while (right > left)
//	{
//		int  temp = 0;
//		temp = a[right];
//		a[right] = a[left];
//		a[left] = temp;
//		right--;
//		left++;
//	};
//}
//int main(){
//	char arr[100] = { 0 };
//	gets(arr);
//	pre(arr);
//	printf("%s", arr);
//	return 0;
//}
//#include<stdio.h>
//void print(int n)
//{
//	int i = 0;
//	int j;
//	for (i = 0; i < n; i++)
//	{
//		for (j = 0; j < n - 1 - i; j++)
//		{
//			printf(" ");
//		}
//		for (j = 0; j < 2*i + 1; j++)
//		{
//			printf("*");
//		}
//		printf("\n");
//	}
//	for (i = 0; i < n - 1; i++)
//	{
//		for (j = 0; j < i + 1; j++)
//		{
//			printf(" ");
//		}
//		for (j = 0; j < 2 * n - 3 - 2 * i; j++)
//		{
//			printf("*");
//		}
//		printf("\n");
//	}
//}
//int main()
//{
//	int n;
//	scanf("%d", &n);
//	print(n);
//	return 0;
//}
#include<stdio.h>

int main()
{
	int money=0;
	int empty = 0;
	scanf("%d", &money);
	int total = 0;
	total+= money;
	empty = money;
	while (empty >= 2)
	{
		total += empty / 2;
		empty = empty / 2 + empty % 2;
	}
	printf("%d", total);
	return 0;
}
#include<stdio.h>
int main()
{
	int  b, c;
	int a = 1;
	while (a)
	{
		scanf("%d %d %d", &a, &b, &c);
		if ((a + b <= c) || (a + c <= b) || (b + c <= a))
		{
			printf("Not a triangle!");
			printf("\n");
		}
		else
		{
			if (a == b && a == c)
			{
				printf("Equilateral triangle!");
				printf("\n");
			}
			else if (a == b || a == c || b == c)
			{
				printf("Isosceles triangle!");
				printf("\n");
			}
			else 
			{
				printf("Ordinary triangle!");
				printf("\n");
			}
		}
		
	}
	return 0;
}
//#include<stdio.h>
//int main()
//{
//	int i, j;
//	int temp;
//	int arr[8] = { 2,3,5,7,4,1,5,7 };
//	for (i = 0; i < 7; i++)
//	{
//		for (j = 0; j < 7 - i; j++)
//		{
//			if (arr[j] > arr[j + 1])
//			{
//				temp = arr[j];
//				arr[j] = arr[j + 1];
//				arr[j + 1] = temp;
//			}
//		}
//	}
//	for (i = 0; i < 8; i++)
//	{
//		printf("%d", arr[i]);
//	}
//	return 0;
//
//		
//}
//#include<stdio.h>
//int main()
//{
//	int arr1[5] = { 1,2,3,4,5 };
//	int arr2[5] = { 6,7,8,9,10 };
//	int i;
//	
//	for (i = 0; i < 5; i++)
//	{
//		arr1[i] = arr1[i] ^ arr2[i];
//		arr2[i] = arr1[i] ^ arr2[i];
//		arr1[i] = arr1[i] ^ arr2[i];
//	}
//	for (i = 0; i < 5; i++)
//	{
//		printf("%d", arr1[i]);
//	}
//	printf("\n");
//	for (i = 0; i < 5; i++)
//	{
//		printf("%d", arr2[i]);
//	}
//	return 0;
//}
#include<stdio.h>
void init(int arr[])
{
	int i = 0;
	for (i = 0; i < 10; i++)
	{
		arr[i] = 0;
	}
}
void print(int arr[])
{
	int i;
	for (i = 0; i < 10; i++)
	{
		printf("%d", arr[i]);
	}
	printf("\n");
}
void reverse(int arr[])
{
	int i;
	int temp;
	for (i = 0; i < 5; i++)
	{
		temp = arr[i];
		arr[i] = arr[9 - i];
		arr[9 - i] = temp;
	}
}
int main()
{
	int i;
	int arr[10] = { 1 };
	init(arr);
	print(arr);
	for (i = 0; i < 10; i++)
	{
		arr[i] = i;
	}
	print(arr);
	reverse(arr);
	print(arr);
	return 0;
}

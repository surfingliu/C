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
#include<stdio.h>
#include<math.h>
int  isprime(int number)
{
	int j;
	for (j = 0; j < sqrt(number); j++)
	{
		if (number % j == 0)
		{
			return 0;
		}
	}
	return 1;
}
int main()
{
	int i;
	for (i = 100; i <= 200; i++)
	{
		if(isprime(i));
		{
			printf("%d ", i);
		}
	}
	return 0;
}
#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>
#include<stdlib.h>
#include<string.h>

typedef struct node {
    char StuID[11];
    int Grade;
    struct node* next;
}StudentLinkedListNode;


/* 创建相交链表 */
void createCrossLink(StudentLinkedListNode* a, StudentLinkedListNode* b, int beforeCross1, int beforeCross2) {
    // a和b后面若干结点值相同
    // beforeCross1为跳过的a中的个数，从第beforeCross1 + 1个结点开始相交
    // beforeCross2为跳过的b中的个数，从第beforeCross2 + 1个结点开始相交
    // 相交方法是将b中的前一结点指向a中的首个相交结点
    StudentLinkedListNode* p, * q;
    while (beforeCross1--)a = a->next;
    while (--beforeCross2)b = b->next;
    p = b->next;
    b->next = a;
    //销毁野指针结点
    while (p) {
        q = p->next;
        free(p);
        p = q;
    }
}

void destroyCrossLink(StudentLinkedListNode* a, StudentLinkedListNode* b, StudentLinkedListNode* crossNode) {
    StudentLinkedListNode* p = crossNode->next, * q;
    while (p) {
        q = p->next;
        free(p);
        p = q;
    }
    while (a != crossNode) {
        q = a->next;
        free(a);
        a = q;
    }
    while (b != crossNode) {
        q = b->next;
        free(b);
        b = q;
    }
    free(crossNode);
}

/* 打印单个节点 */
void printLinkedListNode(StudentLinkedListNode* node) {
    printf("{ID:%s, Grade:%d}", node->StuID, node->Grade);
    if (node->next != NULL) {
        printf("->");
    }
    else {
        printf("\n");
    }

}

/** 输出该表的成绩情况 */
void outputStudentLinkedList(StudentLinkedListNode* head) {
    StudentLinkedListNode* node = head;
    while (node)
    {
        printLinkedListNode(node);
        node = node->next;
    }
    // 用于单个节点输出的函数printLinkedListNode已提供
    //请你实现遍历链表的逻辑
    //TODO
}


/** 新建一个链表node并返回 */
StudentLinkedListNode* studentLinkedListCreate(char student_id[], int grade){
    StudentLinkedListNode* node = (StudentLinkedListNode*)malloc(sizeof(StudentLinkedListNode));
         node->Grade = grade;
         strcpy(node->StuID, student_id);
    return node;
    //tips:malloc的时候记得为转化为结构体指针
    //TODO
}


/** 按照降序插入学生的成绩情况,并返回链表头指针 */
StudentLinkedListNode* studentLinkedListAdd(StudentLinkedListNode* head, StudentLinkedListNode* node) {
    node->next = head;
    head = node;
    return head;//TODO
}


/** 反转链表 */
StudentLinkedListNode* reverseLinkedList(StudentLinkedListNode* head) {
    StudentLinkedListNode* pnode = NULL;
    StudentLinkedListNode* node = head->next;
    head->next = NULL;
    while (node)
    {
        pnode = node->next;
        head=studentLinkedListAdd(head, node);
        node = pnode;
    }
    //TODO
    return head;
}

/** 找到相交的第一个结点 */
StudentLinkedListNode* findCrossBeginNode(StudentLinkedListNode* class1, StudentLinkedListNode* class2) {
    int len1 = 0, len2 = 0;
    int dl = 0,i=0;
    StudentLinkedListNode* node=class1;
    StudentLinkedListNode* pnode=class2;
    for (; node != NULL; node = node->next)
    {
        len1++;
    }
    for (; pnode != NULL; pnode = pnode->next)
    {
        len2++;
    }
    StudentLinkedListNode* plong = class1;
    StudentLinkedListNode* pshort = class2;
    dl = len1 - len2;
    if (len1 < len2)//判断两联表长度，并剪去多余长度 
    {
        plong = class2;
        pshort = class1;
        dl = len2 - len1;
    }
    for (i = 0; i < dl; i++)
    {
        plong = plong->next;
    }
    while ((plong != NULL) && (pshort != NULL) && (plong != pshort))
    {
        plong = plong->next;
        pshort = pshort->next;
    }
    return plong;
    //class1和class2在后一部分完全重合（结点的内存地址相同），请找出并返回开始相交的第一个结点。
    //请不要简单地通过结点结构体的成员来判断。
    //TODO
}

int main() {
	freopen("./gradeImport.in","r",stdin);

  StudentLinkedListNode* class1 = NULL, * class2 = NULL;
    int num1, num2, i;
    char student_id[11];
    int grade;
    int beforeCross1, beforeCross2;
    StudentLinkedListNode* node;
    while (~scanf("%d %d", &num1, &num2)) {//用户输入总人数 
        class1 = class2 = NULL;
        // 存储数据到链表
        for (i = 0; i < num1; i++){
            scanf("%s %d", student_id,&grade);
            node = studentLinkedListCreate(student_id,grade);
            class1 = studentLinkedListAdd(class1,node);
        }
        for (i = 0; i < num2; i++) {
            scanf("%s %d", student_id,&grade);
            node = studentLinkedListCreate(student_id,grade);
            class2 = studentLinkedListAdd(class2, node);
        }
        printf("* part1:\nclass1:\n");
        outputStudentLinkedList(class1);
        printf("class2:\n");
        outputStudentLinkedList(class2);

        // 反转链表
        class1 = reverseLinkedList(class1);
        class2 = reverseLinkedList(class2);
        printf("* part2:\nclass1:\n");
        outputStudentLinkedList(class1);//打印反转链表 
        printf("class2:\n");
        outputStudentLinkedList(class2);

        // 生成相交链表
        scanf("%d %d", &beforeCross1, &beforeCross2);
        createCrossLink(class1, class2, beforeCross1, beforeCross2);

        // 打印相交结点
        node = findCrossBeginNode(class1, class2);//寻找节点 
        printf("* part3:\n");
        printf("{ID:%s, Grade:%d}\n", node->StuID, node->Grade);

        //销毁相交链表
        destroyCrossLink(class1, class2, node);

        printf("\n");
    }
    return 0;
}
#include <stdlib.h>
#include <stdio.h>
#include "queue.h"

void testStack(Stack S);
void testQueue(Queue Q);

int main(int argc, char **argv)
{
    Stack *S = (Stack *)malloc(sizeof(Stack));
    Queue *Q = (Queue *)malloc(sizeof(Queue));
    InitStack(S);
    InitQueue(Q);
    FILE *fp_in;
    char in_file[] = "./test_stu.in";
    fp_in = freopen(in_file, "r", stdin);
    if (fp_in == NULL)
    {
        printf("can not load file!");
        return 1;
    }
    int mode, num, e, status;
    while (~scanf("%d", &mode))
    {
        switch (mode)
        {
        case 0:
            num = 0;
            scanf("%d", &num);
            while (num > 0)
            {
                num--;
                scanf("%d", &e);
                status = Push(S, e);
                if(status)
                {
                    printf("Push:%d\n", e);
                }
                testStack(*S);
            }
            break;
        case 1:
            num = 0;
            scanf("%d", &num);
            while (num > 0)
            {
                num--;
                status = Pop(S, &e);
                if(status)
                {
                    printf("Pop:%d\n", e);
                }
                else
                {
                    printf("Pop failed\n");
                }
                testStack(*S);
            }
            break;
        case 2:
            status = GetTop(*S, &e);
            if(status)
            {
                printf("GetTop:%d\n", e);
            }
            else
            {
                printf("GetTop failed\n");
            }
            testStack(*S);
            break;
        case 3:
            status = StackEmpty(*S);
            if(status)
            {
                printf("The Stack is Empty\n");
            }
            else
            {
                printf("The Stack is not Empty\n");
            }
            testStack(*S);
            break;
        case 4:
            num = 0;
            scanf("%d", &num);
            while (num > 0)
            {
                num--;
                scanf("%d", &e);
                status = EnQueue(Q, e);
                if(status)
                {
                    printf("EnQueue:%d\n", e);
                }
                else
                {
                    printf("EnQueue failed\n");
                }
                testQueue(*Q);
            }
            break;
        case 5:
            num = 0;
            scanf("%d", &num);
            while (num > 0)
            {
                num--;
                status = DeQueue(Q, &e);
                if(status)
                {
                    printf("DeQueue:%d\n", e);
                }
                else
                {
                    printf("DeQueue failed\n");
                }
                testQueue(*Q);
            }
            break;
        case 6:
            status = GetHead(*Q, &e);
            if(status)
            {
                printf("GetHead:%d\n", e);
            }
            else
            {
                printf("GetHead failed\n");
            }
            testQueue(*Q);
            break;
        case 7:
            status = QueueEmpty(*Q);
            if(status)
            {
                printf("The Queue is Empty\n");
            }
            else
            {
                printf("The Queue is not Empty\n");
            }
            testQueue(*Q);
            break;
        default:
            break;
        }
    }
    return 0;
}

void testStack(Stack S)
{
    int seq[MaxSize], i = 0;
    StackToArray(S, seq);
    printf("Stack contains:");
    for (i = 0; i < StackLength(S); i++)
    {
        printf("%d ", seq[i]);
    }
    printf("\n\n");
}

void testQueue(Queue Q)
{
    int seq[MaxSize], i = 0;
    QueueToArray(Q, seq);
    printf("Queue contains:");
    for (i = 0; i < QueueLength(Q); i++)
    {
        printf("%d ", seq[i]);
    }
    printf("\n\n");
}

#define  _CRT_SECURE_NO_WARNINGS
//#include<stdio.h>
//int main()
//{
//	int a, b;
//	int i;
//	int count=0;
//	int m, n;
//	scanf("%d %d", &a, &b);
//	for (i = 0; i < 32; i++)
//	{
//		m = a & 1;
//		n = b & 1;
//		if (m == n)
//		{
//			count++;
//		}
//		a=a >> 1;
//		b = b >> 1;
//	}
//	printf("%d", 32-count);
//	return 0;
//
//#include<stdio.h>
//int main()
//{
//	int number;
//	int a,b;
//	scanf("%d", &number);
//	a = number;
//	b = number;
//	int i;
//	int arr1[16] = { 0 };
//	int arr2[16] = { 0 };
//	for (i = 0; i < 16; i++)
//	{
//		if ((a & 1) == 1)
//		{
//			arr1[i] = 1;
//		}
//		a = a >> 2;
//	}
//	b = b >> 1;
//	for (i = 0; i < 16; i++)
//	{
//	
//		if ((b & 1) == 1)
//		{
//			arr2[i] = 1;
//		}
//		b = b >> 2;
//	}
//	for (i = 0; i < 16; i++)
//	{
//		printf("%d", arr1[i]);
//	}
//	printf("\n");
//	for (i = 0; i < 16; i++)
//	{
//		printf("%d", arr2[i]);
//	}
//	return 0;
//}
//#include<stdio.h>
//int main()
//{
//	int a;
//	scanf("%d", &a);
//	int count = 0;
//	int i;
//	for (i = 0; i < 32; i++)
//	{
//		if ((a & 1) == 1)
//		{
//			count++;
//		}
//		a = a >> 1;
//	}
//	printf("%d", count);
//	return 0;
//}
//#include<stdio.h>
//int main()
//{
//int a, b;
//scanf("%d %d", &a, &b);
//a = a ^ b;
//b = a ^ b;
//a = a ^ b;
//printf("%d %d", a, b);
//return 0;
//}
#include <stdio.h>
#include <stdlib.h>
#define N 10000

int a[N]; // 用于存储奶牛产奶量

//Todo
//需要返回中位数奶牛产奶量。
//可以自行添加其他辅助函数,可以修改传参的数量
int solve1(int *a,int n){
	int i,j,temp,mid;
	if(n==1)
	{
		return a[0];
	}//如果n为1则返回第一个值 
	else{
for(i=1;i<n;i++)
{
	for(j=0;j<n-i;j++)
	{
		if(a[j]>a[j+1])
		{
			temp=a[j+1];
			a[j+1]=a[j];
			a[j]=temp;
		}
	}
}//冒泡排序 
if(n%2==0)
{
	mid=(a[n/2]+a[n/2+1])/2;	
}
else
{
	mid=a[n/2];
}
return mid;
}}
void test1(){
    int caseNum; //表示测试轮数
    int n;
    int ans[N];
    if (freopen("5_1_input_5.in", "r", stdin) == NULL) {
		printf("There is an error in reading file 5_1_input_5.in");
    }
    scanf("%d", &caseNum);
    for (int case1 = 0; case1 < caseNum; case1++) {
        printf("==== Case %d ====\n", case1 + 1);
        scanf("%d", &n);
        for (int i = 0; i < n; i++) {
            scanf("%d", &a[i]);
        }
        ans[case1] = solve1(a,n);
        printf("ans is:%d\n", ans[case1]);
        printf("\n");
    }
    fclose(stdin);
}

int main() {
    test1();
    return 0;
}
#include<stdio.h>
int main()
{
	/*int arr[10] = { 1,2,3,4,5,6,7,8,9,0 };
	printf("%d", &arr[9] - &arr[0]);
	return 0;*/
	int arr[10] = { 0 };
	printf("%p\n", arr);
	printf("%p\n", &arr);
	printf("%p\n", arr + 1);
	printf("%p\n", &arr + 1);
	return 0;

}
#include<stdio.h>
void test()
{
	printf("hehe\n");
}
int main()
{
	int arr[10] = { 0 };
	test();
	int i;
	for (i = 0; i < 10; i++)
	{
		arr[i] = i;
	}
	for (i = 0; i < 10; i++)
	{
		printf("%d ", arr[i]);
	}
	return 0;
}
//void test1()
//{
//	printf("haha\n");
//}
//void test2()
//{
//	test1();
//}
//void test3()
//{
//	test2();
//}
//int main()
//{
//	test1();
//	test3();
//	return 0;
//}
//#include<stdio.h>
//int main()
//{
//	int arr1[] = { 1,2,3,4,5 };
//	int arr2[] = { 2,3,4,5,6 };
//	int arr3[] = { 3,4,5,6,7 };
//	int* arr4[] = {arr1,arr2,arr3};
//	int i,j;
//	for (i = 0; i < 3; i++)
//	{
//		for (j = 0; j < 5; j++)
//		{
//			printf("%d ", arr4[i][j]);
//		}
//		printf("\n");
//	}
//	return 0;
//}
//#include<stdio.h>
//void print1(int* p, int sz)
//{
//	int i;
//	for (i = 0; i < 10; i++)
//	{
//		printf("%d ", *(p + i));
//	}
//}
//void print2(int(*p)[10], int sz)
//{
//	int i;
//	for (i = 0; i < 10; i++)
//	{
//		printf("%d ", *(*p + i));
//	}
//}
//int main()
//{
//	int arr[10] = { 1,2,3,4,5,6,7,8,9,0 };
//	int sz = sizeof(arr) / sizeof(arr[0]);
//	print1(arr, sz);
//	printf("\n");
//	print2(&arr, sz);
//	return 0;
//}
#include<stdio.h>
void print1(int arr[3][5], int r, int c)
{
	int i, j;
	for (i = 0; i < r; i++)
	{
		for (j = 0; j < c; j++)
		{
			printf("%d ", arr[i][j]);
		}
		printf("\n");
	}
}
void print2(int(*p)[5], int r, int c)
{
	int i, j;
	for (i = 0; i < r; i++)
	{
		for (j = 0; j < c; j++)
		{
			printf("%d ", *(*(p + i) + j));
		}
		printf("\n");
	}
}
int main()
{
	int arr[3][5] = { 1,2,3,4,5,2,3,4,5,6,3,4,5,6,7 };
	print1(arr, 3, 5);
	printf("\n\n");
	print2(arr, 3, 5);
	return 0;
}

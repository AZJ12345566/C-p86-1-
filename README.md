# C-p86-1-
C语言学习笔记 p86分支与循环(1)接上
#include<stdio.h>
int main()
{
    int n=1;
    int m=2;
    switch(n)
    {
        case1:
              m++;
        case2:
              n++;
        case3:
              switch(n)
              {//switch允许嵌套使用
                  case1:
                        n++;//这里的case1不会执行，因为n的值为2；直接跳到case2
                  case2:
                        m++;
                        n++;
                        break;
              }
         case4:m++;
            break;
         default:
            break;
    }
    printf("m=%d,n=%d\n",m,n);
    
    return 0;
}



//循环语句
int main()
{
    while(1)//恒为真
        printf("hehe\n");//死循环打印hehe
    return 0;
}

int main()
{
    int i=1;
    while(i<=10)
    {
        printf("%d",i);
        i++;
    }
    return 0;
}

int main()
{
    int i=1;
    while(i<=10)
    {
        if(i==5)
          break;
        printf("%d",i);
        i++;
    }
    return 0;
}//输出为1，2，3，4，5,break在循环中也可以使用，用于跳出循环

int main()
{
    int i=1;
    while(i<=10)
    {
        if(i==5)
          continue;
        printf("%d",i);
        i++;
    }
    return 0;
}//输出1，2，3，4然后进行死循环，因为continue之后直接返回while，i一直在等于4与5的循环中

int main()
{
    int i=1;
    while(i<=10)
    {
        i++;
        if(i==5)
          continue;
        printf("%d",i);
    }
    return 0;
}//输出1，2，3，4，6，7，8，9，10
//在循环中遇到break，就停止后期的所有循环，直接终止循环，所以，while中的break用于永久终止循环
//在while循环中，continue是用于终止本次循环的，也就是本次循环continue后面的代码不在执行，直接跳转到while语句的判断部分，进行下一次循环的入口判断

int main()
{
    int ch=getchar();
    putchar(ch);
    printf("%c\n",ch);
    return 0;
}//输出你输入的字符

int main()
{
    int ch=0;
    while((ch=getchar())!EOF)
    {
        putchar(ch);
    }//EOF是end of file的简写，其值为-1
    return 0;
}


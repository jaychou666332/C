# C
/*一辆卡车违反交通规则，撞人逃跑。现场3人目击事件，但都没记住车号，只记下车号的一些特征。甲说牌照的前两位数字是相同的；乙说：牌照的后两位数字是相同的，但和头两位数字不同；丙是位数学家，他说，四位的车号刚好是一个整数的平方。请根据以上线索编写程序求出车号。*/
#include <stdio.h>
main()
{
  int  i,j,k,c;
  for(i=1;i<=9;i++)
    for(j=0;j<=9;j++)
      if(i!=j)
      {
        k=i*1000+i*100+j*10+j;
        for(c=31;c*c<k;c++);    /*此行命令不是循环结构，for结尾处带有分号，该命令的用处为增加c的值，为接下来判断c*c==k做准备*/
        if(c*c==k)
          printf("Lorry_No. is %d . \n",k);
       }
 }

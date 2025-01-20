# rotation
#include <stdio.h>
int rotation(int a[4][4])
{
    int new[4][4];
    int c,b;
    for(b=0;b<4;b++)
    {
        for(c=0;c<4;c++)
        {
            new[b][c]=a[3-c][b];
        }
    }
    for(b=0;b<4;b++)
    {
        for(c=0;c<4;c++)
        {
            a[b][c]=new[b][c];
        }
    }
}
int main(void)
{
    int i,j;
    int number;
    int a[4][4]=
    {
        {1,2,3,4},{5,6,7,8},{9,10,11,12},{13,14,15,16}
    };
    for(i=0;i<4;i++)
    {
        for(j=0;j<4;j++)
        {
            printf("%d ",a[i][j]);
        }
        printf("\n");
    }
    scanf("%d",&number);
    for(i=0;i<number;i++)
    {
        rotation(a);
    }
    for(i=0;i<4;i++)
    {
        for(j=0;j<4;j++)
        {
            printf("%d ",a[i][j]);
        }
        printf("\n");
    }
}

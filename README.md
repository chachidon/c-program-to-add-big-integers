# c-program-to-add-big-integers
#include <stdio.h>

int main()
{
    int i,carry=0,n,d=0,l=0,j=0;
    printf("enter the number of digit you want to add: ");
    scanf("%d",&n);
    int a[20000];
    int b[20000];
    int c[20000];
    printf("enter the digit for first element: ");
    for(i=0; i<n; i++){
        scanf("%d",&a[i]);
    }
    printf("enter the digit for seconf element: ");
    for(i=0; i<n; i++){
        scanf("%d",&b[i]);
    }
    c[0]=0;
    l=1;
    for(i=0;i<n;i++){
    
            d=a[i]+b[i]+c[i];
            c[i]=d%10;
            carry=d/10;
        
        while(carry>0){
            c[l++]=carry%10;
            carry=carry/10;
                          }
        
    }
    for(i=n; i>=0;i--){
        printf("%d",c[i]);
    }
    return 0;
}

#include <stdio.h>
int main()
{
    int n=10 ,a[n] ,i ,j ,temp;
    printf("Enter The Array Elements ");
    scanf("%d",&n);
    for(i=0;i<n;i++){
        scanf("%d",&a[i]);
    }
    for(i=1;i<n;i++){
        for(j=0;j<n;j++){
            if(a[j]>a[i]){
             temp = a[i];
                for(int k=i-1;k>=j;k--){
                    a[k+1]=a[k];
                }
                a[j]=temp;
            } 
        }
    }
    printf("array after sorting \n");
   for(i=0;i<n;i++){
            printf("%d\t",a[i]);
        }
return 0;
}

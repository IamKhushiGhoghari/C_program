// Online C compiler to run C program online
#include <stdio.h>

void main() {
    
    int i,j,s,p = 1,n;
    float diff1 = 1,diff2 = 1;
    
    printf("Enter number:");
    scanf("%d",&n);
    
    for(i=1; i<=n; i++)
    {
        //Reset the diff2
        diff2 = 1;
        //Space loop
        for(s=1; s<i; s++) {
            printf("   ");
        }
        //Patterm 1 starting calculation
        p = i * diff1;
        //Pattern 1 loop
        for(j=i; j<=n; p += j,j++) {
            printf("%3d",p);
        }
        //Pattern 2 diff calculation for each step
        for(j=1; j<n; j++) {
            diff2 += 0.5;
        }
        //Pattern 2 starting calculation
        p = i + n * diff2;
        //Pattern 2 loop
        for(j=n-1; j>=i;p += j,j--) {
            printf("%3d",p);
        }
        //diff1 updatatio 
        diff1 += 0.5;
        printf("\n");
    }
}

#include<stdio.h>
#include<limits.h>
int main() {

       int n;
       printf("enter the size of the array:");
       scanf("%d",&n);
       if(n<2)
       {
           printf("minimum of 2 numbers required");
       }

       int arr[n];
       printf("enter %d elements:\n");
       for(int i=0;i<n;i++)
       {
           scanf("%d",&arr[i]);
       }
       int large=INT_MIN,large2=INT_MIN;
       for(int i=0;i<n;i++)
       {
           if(arr[i] > large) {
            large2 = large;
            large=arr[i];
           } else if(arr[i]>large2 && arr[i]!=large){
           large2=arr[i];
           }

       }

       if(large2 == INT_MIN)
       {
           printf("2nd largest number not found");
       }
       else
       {
           printf("2nd largest number:%d", large2);
       }
       return 0;
}

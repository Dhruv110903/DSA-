#include <iostream>
using namespace std;

int pivot(int arr[], int n)
{
    int s=0;
    int e=n-1;
    int mid=(s+e)/2;
    
    while(s<e)
    {
        if(arr[mid]>=arr[0]){
            s=mid+1;
        }
        
        else
        {
            e=mid;
        }
        
         mid=(s+e)/2;
    }
    return s;
}


int binary(int arr[], int s, int e, int key)
{
    int start=s;
    int end=e;
    int mid=(start+end)/2;
    
    while(start<=end)
    {
        if(arr[mid]==key){
            return mid;
        }
        
        if (arr[mid]<key)
        {
            start=mid+1;
        }
        
        else
        {
            end=mid-1;
        }
        
    }
    return -1;
}




int findpos(int arr[],int n , int key)
{
    int pivotno=pivot(arr,n);
    int k=0;
    if(k>=arr[pivotno] && k<=arr[n-1])
    {
        return binary(arr,pivotno,n-1,k);
    }
    
    else
    {
        return binary(arr,0,pivotno-1,k);
    }
}

int main()
{
    int even[6]={10,12,13,1,2,3};
    
    int k;
    cout<<"Enter the value of k : "<<endl;
    cin>>k;
    
    cout<<"The index of k in rotated search array is : "<<findpos(even,6,k)<<endl;
    
    return 0;
}

# SORTING-USING-BUBBLE-SORT-AND-THEN-MERGING

#include <iostream>

using namespace std;
void sort(int a[],int n)
{
    int i,j,temp;
    for(i=0;i<n;i++)
    {
        for(j=0;j<n-i-1;j++)
        {
            if(a[j] > a[j+1])
            {
                temp=a[j];
                a[j]=a[j+1];
                a[j+1]=temp;
            }
        }
    }
}

int main()
{
     int m,n,i,j,k=0;
    cout<<"Enter the number of elements for array 1 \n";
    cin>>m;
    int a[m];
    cout<<"Enter "<<m<<" numbers  \n";
    for(i=0;i<m;i++)
    cin>>a[i];
    sort(a,m);
    cout<<"Array 1 after sorting \n";
    for(i=0;i<m;i++)
    cout<<a[i]<<" ";
    
    cout<<"\n Enter the number of elements for array 2 \n";
    cin>>n;
    int b[n],c[m+n];
     cout<<"Enter "<<n<<" numbers  \n";
    for(i=0;i<n;i++)
    cin>>b[i];
     sort(b,n);
    cout<<"Array 2 after sorting \n";
    for(i=0;i<n;i++)
    cout<<b[i]<<" ";
    
     i=0;
    j=0;
    while(i<m || j<n)
    {
        if(a[i]<b[j])
        {
            c[k++]=a[i++];
        }
        else
        {
            c[k++]=b[j++];
        }
    }
    
    cout<<"\n Merged Array : \n";
    for(i=0;i<m+n;i++)
    cout<<c[i]<<" ";

    return 0;
}

# baitapmang1e
giải các bài tập mảng 1e
#include<iostream>
#include<math.h>
using namespace std;

void nhapmang(int a[], int n)
{
    for(int i = 0; i < n ; i++)
    {
        cout<<"Nhap vao phan tu a["<<i<<"]:";
        cin>>a[i];
    }
}
void xuatmang(int a[],int n)
{
    for(int i = 0; i < n ; i++)
    {
        cout<<a[i]<<"    ";
    }
    
}
bool scp(int n){
    int sqr = sqrt(n);
    return (sqr*sqr == n);
}
void sapxeplaimang(int a[],int n)
{
    for(int i=0;i<n;i++)
    {
        int gan=a[0];
        for(int i=0;i<n-1;i++)
        {
            if(a[i]>a[i+1])
            {
                gan=a[i];
                a[i]=a[i+1];
                a[i+1]=gan;
            }
        }
    }
}
int tongcacsochinhphuong(int a[],int n)
{
    int tong=0;
    for(int i=0;i<n;i++)
    {
        if(scp(a[i])==1)
        {
            tong+=a[i];
        }
    }
        cout<<"\n Tong cac so chinh phuong co trong mang la :"<<tong;
        cout<<endl;
}
int main()
{
    int a[1000];
    int n;
    cout<<"Nhap n :";
    cin>>n;
    nhapmang(a,n);
    xuatmang(a,n);
    tongcacsochinhphuong(a,n);
    sapxeplaimang(a,n);
    xuatmang(a,n);
    return 1;
}

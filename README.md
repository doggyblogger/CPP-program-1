# CPP-program-1
CPP program to move all elements 
#include<bits/stdc++.h>
using namespace std;
// To moves all -ve element to end of array in same order.
void segregateElements(int arr[], int n)
{
// Create an empty array to store result
int temp[n];
//Traversal array and store +ve element temp array
int j = 0; //index of temp
for (int i=0; i<n;i++)
if (arr[i] >= 0)
temp[j++] = arr[i];
// If array contains all positive or all negative.
if (j==n || j == 0)
return;
// Store -ve element in temp array
for (int i = 0; i <n; i++)
if (arr[i] < 0)
temp[j++] = arr[i];
// Copy contents of temp[] to arr[]
memcpy(arr, temp, sizeof(temp));}
// Driver program
int main()
{
int arr[100],N;
cout << "Enter the length of array: "<< endl;
cin>>N; 
cout<<"Enter the array elements of the array:"<< endl;
for(int i=0 ;i<N; i++) 
cin>>arr[i];
segregateElements(arr,N); //Calling the function
for (int i = 0; i< N; i++)
cout<<arr[i] <<" "; 
return 0;
}

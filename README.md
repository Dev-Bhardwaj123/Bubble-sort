# Bubble-sort
Given an unsorted array sort the array using bubble sort technique
//Bubble sort
#include<iostream>
using namespace std;

int main(){
	int n;
	cout<<"Enter the size: ";
	cin>>n;
	int arr[n];
	for(int i=0;i<n;i++){
		cin>>arr[i];
	}
	for(int i=0;i<n;i++){
		int flag=0;
		for(int j=0;j<n-i-1;j++){
			if(arr[j]>arr[j+1]){
				//if want in decreasing order just replace arr[j]>arr[j+1] to arr[j]<arr[j+1]
				swap(arr[j],arr[j+1]);
				flag=1;
			}
		}
		if(flag==0){
			break;
		}
	}
	cout<<endl;
	for(int i=0;i<n;i++){
		cout<<arr[i]<<" ";
	}
}

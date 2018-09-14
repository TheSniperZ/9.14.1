# 9.14.1
数组的使用
// 9.14.1.cpp : 定义控制台应用程序的入口点。
//数组的使用

#include "stdafx.h"
#include<iostream>

using namespace std;


int _tmain(int argc, _TCHAR* argv[])
{
	int a[10],b[10];
	
	for (int i=0;i<10;i++){
		a[i]=i*2+5;
		b[10-i-1]=a[i];
	}
	for (int i=0;i<10;i++){
		if (i%5==0) cout<<endl; //每输出5个数据进行一次换行
		cout.width(6); //设置输出宽度为6
		cout<<"a["<<i<<"]="<<a[i]<<" ";
		
	}
	cout<<endl;
	for (int i=0;i<10;i++){
		if (i%5==0) cout<<endl;
		cout.width(6);
		cout<<"b["<<i<<"]="<<b[i]<<" ";
	}
	return 0;
}


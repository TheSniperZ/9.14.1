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

// 9.14.2数组的使用和交互.cpp : 定义控制台应用程序的入口点。
//

#include "stdafx.h"
#include<iostream>
using namespace std;


int _tmain(int argc, _TCHAR* argv[])
{
	const char Key[]={'a','b','c','b','a'};
	const int Num_Qus=5;
	char c;
	int q=0,corr=0;
	while(cin.get(c)) //输入ctrl+z时，while(cin.get(c))判断为假，跳出循环。
	{
		if(c!='\n'){
			if(c==Key[q]){
				cout<<" ";
				corr++;
			}
			else
				cout<<"*";
			q++;
		}
		else{
			cout<<"Score"<<static_cast<float>(corr)/Num_Qus*100<<"%";
			q=0;corr=0;cout<<endl;
		}
	}
	return 0;
}


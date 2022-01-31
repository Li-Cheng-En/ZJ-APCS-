# ZJ-APCS-三角形辨別
#include<bits/stdc++.h>
using namespace std;
#define IOS ios::sync_with_stdio(false),cin.tie(0),cout.tie(0)

int main() {
	IOS; 
	int s[3];
	int i, j, tmp;
	for(i=0;i<3;i++){
		cin >> s[i];
	}
	for(i=0;i<3;i++){
		for(j=i+1;j<3;j++){
			if(s[i]>s[j]){
				tmp=s[i];
				s[i]=s[j];
				s[j]=tmp;
			}
		}	
	}
	for(i=0;i<3;i++){
		if(i != 2){
			cout << s[i] <<" ";
		}
		else
			cout << s[i]<<"\n";
	}
	
	if(s[0]+s[1]<=s[2]){
	cout << "No";
	}
	else if(pow(s[0],2)+pow(s[1],2)==pow(s[2],2)){
		cout << "Right";
	}
	else if(pow(s[0],2)+pow(s[1],2)>pow(s[2],2)){
		cout << "Acute";
	}
	else if(pow(s[0],2)+pow(s[1],2)<pow(s[2],2)){
		cout << "Obtuse";
	}
	return 0;
}

# Codeforcescpp-34A
#include <bits/stdc++.h>
using namespace std;

int main() {
	int n, nums[101],tmp1,tmp2;
	cin >> n;
  cin >> nums[0] >> nums[1];
  tmp1 = 1;
  tmp2 = 2;
  int min = abs(nums[0] - nums[1]);
	for (int i = 2; i < n; i++) {
		cin >> nums[i];
    if(abs(nums[i] - nums[i-1]) < min){
      min = abs(nums[i] - nums[i-1]);
      tmp1 = i;
      tmp2 = i+1;
    }
	}
  if(min > abs(nums[0] - nums[n-1])){
    min = abs(nums[0] - nums[n-1]);
    tmp1 = n;
    tmp2 = 1;
  }
  cout << tmp1 << " " << tmp2;
	return 0;
}

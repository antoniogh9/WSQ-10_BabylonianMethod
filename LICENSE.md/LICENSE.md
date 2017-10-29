#include<iostream>
#include<cmath>
using namespace std;

float babylonian_square(float a) {
  float ans, b=0, dif=0;
  ans = a/2;
  do {
    b = ans;
    ans = (ans+a/ans)/2;
    dif=b-ans;
  } while (dif>0.001);

  return ans;
}

int main() {
  int val;
cout << "Enter your value: ";
cin >> val;
cout << "The square root of that number is " <<babylonian_square(val) << endl;
return 0;
}

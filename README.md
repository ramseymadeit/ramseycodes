# ramseycodes
#include <iostream>
using namespace std;
int main() {

    int num, i, end, sum = 0;

    // Take input from user
    cout << "Find sum of prime numbers upto : ";
    cin >> end;

    for(num = 2; num <= end; num++) {

        for(i = 2; i <= (num / 2); i++) {

            if(num % i == 0) {
                i = num;
                break;
            }
        }

        // If the number is prime then add it.
        if(i != num) {
            sum += num;
                 }
    }

    cout << endl << "Sum of all prime numbers upto " << end << "is  : " << sum;

    return 0;
}

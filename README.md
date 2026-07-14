#include <iostream>

using namespace std;

int main()
{
    cout << "Enter the total number of Kilometers driven this month: ";
    const double Commission_rate = 0.25;
    double Kilometers =0;
    double Earnings =0;
    double Commission =0;
    double Bonus =0;
    double Final_payout =0;

    cin >> Kilometers;

    if
    ( Kilometers <= 1000){
          Earnings = (Kilometers * 4.50);
    }
      else if
        ( Kilometers <= 2000)
        {
        Earnings = (1000 * 4.50) + (Kilometers - 1000) * 5.20;
        }
        else
            {
            Earnings =  (1000 * 4.50) + (1000 * 5.20) + (Kilometers - 2000)* 6.10;
            }
    Commission = (Commission_rate * Earnings);

            if
                (Kilometers > 2500)
            {
              Bonus = (Kilometers - 2500)* 0.50;
            }
    Final_payout = (Earnings - Commission + Bonus);
    cout << "Earnings before commission: R"<< Earnings << endl;
    cout << "Commission amount: R"<< Commission << endl;
    cout << "Bonus amount: R"<< Bonus << endl;
    cout << "Final payout to the driver: R"<< Final_payout<< endl;


    return 0;
}

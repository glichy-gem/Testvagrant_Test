#include <iostream>
#include <vector>
#include <algorithm>
#include <climits>
using namespace std;
class example {
public:
    string maximumgstproduct(string product[],int price[],int gst[],int quan[]) {
        int maxigst = INT_MIN;
        int maxindex = -1;
        for (int i=0;i<4;i++) {
            int currentmaxigst = price[i]*quan[i]*gst[i];
            if (currentmaxigst > maxigst) {
                maxigst=currentmaxigst;
                maxindex=i; 
            }
        }
        return product[maxindex];
    }
    int totalamount(int price[], int gst[], int quan[]) {
        int total = 0;
        for (int i=0;i<4;i++) {
            int current;
            if (price[i]>500) {
                current=((price[i]*(100+gst[i])*quan[i])/100)-0.05*((price[i]*(100+gst[i])*quan[i])/100);
            } 
            else 
            {
                current=(price[i]*(100+gst[i])*quan[i])/100;
            }
            total = total+current;
        }
        return total;
    }
};

int main() {
    example e;
    string product[] ={"Leather Wallet", "Umbrella", "Cigarette", "Honey"};
    int price[] ={1100,900,200,100};
    int gst[] ={18,12,28,0};
    int quan[] ={1,4,3,2};
    cout <<"Maximum GST product is: "<< e.maximumgstproduct(product, price, gst, quan) << endl;
    cout <<"Total Amount Paid to Shopkeeper is: "<< e.totalamount(price, gst, quan) << endl;
    return 0;
}

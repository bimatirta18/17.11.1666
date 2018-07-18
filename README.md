# 17.11.1666
tugas pemrograman

#include <iostream>
#include <string>
#include <conio.h>

using namespace std;

class Berat{
       friend ostream& operator<<(ostream&, Berat&);
       friend istream& operator>>(istream&, Berat&);
 public:
        Berat();
        void berat_badan(){
             bbideal=tb-110;
             }
 private:
         int tb;
         int bbideal;
         };
Berat::Berat(){
                  cout<<"Menghitung Berat Badan Ideal"<<endl;
                  cout<<"==========================================="<<endl<<endl;
				  }
         istream& operator>>(istream& in, Berat& input){
                  cout<<"Masukkan Tinggi badan anda :";
                  in>>input.tb;
                 
                  return in;
                  
                  }
         ostream& operator<<(ostream& out, Berat& output){
                     
                    cout<<"=======================================\n";
                    cout<<"Tinggi Badan Anda:"<<output.tb<<endl;
                    cout<<"Berat Badan Ideal Anda :"<<output.bbideal<<endl;
                   	cout<<"=======================================\n";
                	cout<<"Terima Kasih"<<endl;
                  return out;
                   
                  }
 int main(int argc, char *argv)
 {
     Berat b;
     cin>>b;
     b.berat_badan();
     cout<<b;
        cout<<endl;
        
      cout<<"Tekan Enter untuk cExit";
     getch();

}

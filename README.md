# karmas-kSay-lar-
#include <iostream>
  using namespace std;
  

class karmasıkSayılar
{
private:
	int gercek, sanal;
public:
	karmasıkSayılar(int g = 0, int s= 0);
	~karmasıkSayılar();
	karmasıkSayılar(const karmasıkSayılar& oth);
	int getGercek() {
		return gercek;
	}
	int getSanal()
	{
		return sanal;
	}
	void setdeger(int g = 0, int s = 0);
	void displaykarmasıkSayılar();
};
karmasıkSayılar::karmasıkSayılar(int g = 0, int s = 0)
{
	gercek = g;
	sanal = s;
	cout << " copy constructor olusturuldu!" << endl;

}
karmasıkSayılar::~karmasıkSayılar()
{
	cout << "distructor gerceklesti!" << endl;

}
karmasıkSayılar::karmasıkSayılar(const karmasıkSayılar& oth)
{
	gercek = oth.gercek;
	sanal = oth.sanal;
	cout << " copy constructor gerceklesti!" << endl;

}
void  karmasıkSayılar ::setdeger(int g = 0, int s = 0)
{
	gercek = g;
	sanal = s;
}
void karmasıkSayılar::displaykarmasıkSayılar()
{
	if (sanal >= 0)
	{
		cout << gercek << "+" << sanal << "i" << endl;
	}
	else
	{
		cout << gercek << sanal << "i" << endl;
	}
}



int main()
{
	karmasıkSayılar karmasıkSayılar1(6 , 4);
	cout << "gercek:" << karmasıkSayılar1.getGercek();
	cout << "sanal:" << karmasıkSayılar1.getSanal();
	karmasıkSayılar1.displaykarmasıkSayılar();

	karmasıkSayılar karmasıkSayılar2(5, -7);
	cout << "gercek:" << karmasıkSayılar2.getGercek();
	cout << "sanal:" << karmasıkSayılar2.getSanal();
	karmasıkSayılar2.displaykarmasıkSayılar();

	karmasıkSayılar karmasıkSayılar3(karmasıkSayılar2);
	karmasıkSayılar3.displaykarmasıkSayılar();
	karmasıkSayılar3.setdeger(7, 9);
	karmasıkSayılar3.displaykarmasıkSayılar();


	return 0;
}

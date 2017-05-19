# lab2k-n
Coffee/chocolate/hair styling

lab1
#include <iostream>

using namespace std;
class coffee{
public:
	int sugar, water, amount_coffee;
protected:
	coffee(){
		sugar = 3;
		water = 200;
		amount_coffee = 1;
	}
};
class hotchocolate : public coffee {
private:
	int sug, wat, a_s;

public: 
	hotchocolate(){
		sug = sugar;
		wat = water;
		a_s = amount_coffee;
	}
	void first(){
		cout << "sug = " << sug << endl;
		cout << "wat = " << wat << endl;
		cout << "a_s = " << a_s << endl;
	}

};

int main(){
	hotchocolate objHotchocolate;
	objHotchocolate.first();
	
	int a;
	cin >> a;
	return 0;
}



lab2
#include <iostream>

using namespace std;


class cup_coffee{
private:

public:
	cup_coffee(int p_x = 0, int p_y =0): x(p_x), y(p_y){}
	int x; int y;

};
cup_coffee operator+ (cup_coffee left, cup_coffee right){
	return cup_coffee(left.x + right.x, left.y + right.y);
}

int main(){
	cup_coffee Cup1;

	cup_coffee p1(30, 20);
	cup_coffee  p2(-40 , -50);

	cup_coffee  p4 = p1 + p2;

	cout << p4.x << ' ' << p4.y <<endl;

	int a;
	cin >> a;
	return 0;
}



lab3
#include <iostream>

using namespace std;

class coffee{
private:
	int sugar, water, amount_spoons;
public:
	class taste{
	public:
		taste(){
			cout << "Chocolate" <<endl;
		}
	};
};

int main(){
	coffee::taste(); 

	int a; cin >>a;
	return 0;
}



lab4
#include <iostream>

using namespace std;

class Girl{
private:

public:
	virtual void hair(){
		cout << "Do styling" <<endl;
	}


};

class hairdryer : public Girl{
private:

public:
	void hair(){
		cout << "Drying hair" <<endl;
	}
};

class rectifier : public Girl{
private:

public:
	void hair(){
		cout << "Straighten hair" <<endl;
	}
};

class curling : public Girl{
private:

public:
	void hair(){
		cout << "Curl hair" <<endl;
	}
};


int main(){
	Girl* grl;

	hairdryer* dryer= new hairdryer;
	rectifier * rectify = new rectifier;
	curling* curl = new curling;

	Girl* mas[3];
	mas[0] = dryer;
	mas[1] = rectify;
	mas[2] = curl;

	for(int i =0 ; i<3 ; i++){
		mas[i] -> hair();
	};

	int a; cin >> a;
	return 0;
}

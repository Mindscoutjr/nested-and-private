#include <iostream>

using namespace std;
class A
{
private:
    class B
    {
    public:
        void f()
        {
            cout<<"\nTest";
        }
    };
public:
    B g() 
    {
        return B(); 
    }
};


int main()
{
    A a;
    A::B b; 
    A::B b1 = a.g(); 
    auto b2 = a.g(); 
    a.g(); 
    b2.f(); 
}

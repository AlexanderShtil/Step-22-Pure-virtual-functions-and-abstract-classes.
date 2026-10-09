# Step-22-Pure-virtual-functions-and-abstract-classes.
#include <iostream>
#include <windows.h>
#include <string>
#include <memory> 

class Unit {
public:

    virtual void attack() = 0;

    virtual ~Unit() {};
};

class Soldier : public Unit {
public :

    void attack() override {
        std::cout << "Солдат ведет огонь из автомата!";
    }
};

int main()
{
    SetConsoleCP(1251);
    SetConsoleOutputCP(1251);
  
    Unit* my_unit = new Soldier();

  
    my_unit->attack();

    delete my_unit;

    my_unit = nullptr;

    return 0;
}

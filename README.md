# CPP RANDOM

This repository demonstrates the usage of using cpp random engine to generate random int or float number.

## Quick Peak
```cpp
#include <iostream>
#include <random>


int main(int argc, char ** argv)
{
    // Instantiate random engine to generate random number
    std::random_device rd;                              // Random device will generate a random unsigned int
    std::mt19937 eng(rd());                               // mt19937 is one of the random engine provided by C++, we seed it with the value from rd()
    std::uniform_int_distribution<> distr_int(-3, 5);       // uniform_int_distribution make sure the int value is within a range you set
    std::uniform_real_distribution<> distr_double(-3.0, 5.0);   // uniform_real_distribution make sure the double value is within a range you set

    // Using the random generator
    std::cout << "Random int: " << distr_int(eng) << std::endl;
    std::cout << "Random double: " << distr_double(eng) << std::endl;

    return 0;
}
```

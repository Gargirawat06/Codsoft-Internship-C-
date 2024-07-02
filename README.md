# Codsoft-Internship-C++
 
This is my Task 1-Simple Number Guessing Game using C++.
#include <iostream>
#include <cstdlib>
#include <ctime>

int main() {
    srand(time(0)); 
    int randomNumber = rand() % 200 + 1; 
    int userGuess, attempts = 0;

    std::cout << "Welcome to the Number Guessing Game!\n";

    do {
        std::cout << "Guess the number between 1 and 200:";
        std::cin >> userGuess;
        attempts++;

        if (userGuess > randomNumber) {
            std::cout << "Guess too high! Try a lower number.\n";
        } else if (userGuess < randomNumber) {
            std::cout << "Guess too low! Try a higher number.\n";
        } else {
            std::cout << "Congratulations! You guessed the number " << randomNumber << " correctly in " << attempts << " attempts.\n";
        }
    } while (userGuess != randomNumber);

    return 0;
}
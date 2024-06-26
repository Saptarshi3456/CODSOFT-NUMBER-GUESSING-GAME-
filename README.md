# CODSOFT-NUMBER-GUESSING-GAME-
Create a C++ program that generates a random number and asks the user to guess it. Provide feedback on whether the guess is too high or too low until the user guesses the correct number.

#include <iostream>
#include <cstdlib>
#include <ctime>

using namespace std;

int main() {
  srand(time(0)); 
  int numberToGuess = rand() % 100 + 1;
  int guess;

  cout << "Guess a number between 1 and 100: ";

  while (true) {
    cin >> guess;

    if (guess < numberToGuess) {
      cout << "Too low! Try again: ";
    } else if (guess > numberToGuess) {
      cout << "Too high! Try again: ";
    } else {
      cout << "Congratulations! You guessed the correct number.";
      break;
    }
  }

  return 0;
}

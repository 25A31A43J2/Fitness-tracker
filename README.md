# Fitness-tracker
This Fitness App project in C++ is designed to calculate a user’s BMI (Body Mass Index) using height and weight details. The program takes user input, processes BMI calculations, and displays the fitness status such as underweight, normal, or overweight. It uses basic OOP concepts like classes, functions, and conditional statements.


#include <iostream>
using namespace std;

class FitnessApp {
private:
    string name;
    int age;
    float weight, height, bmi;

public:
    void getDetails() {
        cout << "===== FITNESS APP =====\n";

        cout << "Enter Name: ";
        cin >> name;

        cout << "Enter Age: ";
        cin >> age;

        cout << "Enter Weight (kg): ";
        cin >> weight;

        cout << "Enter Height (m): ";
        cin >> height;
    }

    void calculateBMI() {
        bmi = weight / (height * height);
    }

    void displayReport() {
        cout << "\n===== FITNESS REPORT =====\n";

        cout << "Name   : " << name << endl;
        cout << "Age    : " << age << endl;
        cout << "Weight : " << weight << " kg" << endl;
        cout << "Height : " << height << " m" << endl;
        cout << "BMI    : " << bmi << endl;

        if (bmi < 18.5)
            cout << "Status : Underweight" << endl;
        else if (bmi >= 18.5 && bmi < 25)
            cout << "Status : Normal Weight" << endl;
        else
            cout << "Status : Overweight" << endl;
    }
};

int main() {
    FitnessApp user;

    user.getDetails();
    user.calculateBMI();
    user.displayReport();

    return 0;
}

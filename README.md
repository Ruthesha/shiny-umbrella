#include <iostream>
#include <vector>

// Function to calculate the average of an array of numbers

double calculateAverage(const std::vector<int>& numbers) {
    
    int sum = 0;
    for (int number : numbers) {
        sum += number;
    }
    return static_cast<double>(sum) / numbers.size();
}

int main() {
    int size;

    std::cout << "Enter the number of elements: ";
    std::cin >> size;

    std::vector<int> numbers(size);
    
    std::cout << "Enter " << size << " numbers:" << std::endl;
    for (int i = 0; i < size; ++i) {
        std::cin >> numbers[i];
    }

    double average = calculateAverage(numbers);

    std::cout << "The average is: " << average << std::endl;

    return 0;
}

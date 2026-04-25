# Student: Faruk Haral  
# Institution: International Balkan University (IBU)  
# Assignment: Introduction to Python - Session 1  
  
import random  
  
# --- PROJECT 1: TEMPERATURE CONVERTER ---  
def temperature_converter():  
    """Converts Celsius to Fahrenheit."""  
    print("\n[Project 1: Temperature Converter]")  
    try:  
        celsius = float(input("Enter temperature in Celsius: "))  
        fahrenheit = (celsius * 9/5) + 32  
        print(f"Result: {celsius}°C = {fahrenheit:.2f}°F")  
    except ValueError:  
        print("Error: Please enter a valid number.")  
  
# --- PROJECT 2: NUMBER GUESSING GAME ---  
def number_guessing_game():  
    """A simple game to guess a number between 1 and 100."""  
    print("\n[Project 2: Number Guessing Game]")  
    target = random.randint(1, 100)  
    attempts = 0  
      
    while True:  
        try:  
            guess = int(input("Guess a number (1-100): "))  
            attempts += 1  
            if guess < target:  
                print("Higher!")  
            elif guess > target:  
                print("Lower!")  
            else:  
                print(f"Correct! You found it in {attempts} attempts.")  
                break  
        except ValueError:  
            print("Error: Please enter an integer.")  
  
# --- PROJECT 3: GRADE CALCULATOR ---  
def grade_calculator():  
    """Calculates average and status from a list of grades."""  
    print("\n[Project 3: Grade Calculator]")  
    grades = []  
    while True:  
        entry = input("Enter grade (or 'q' to finish): ")  
        if entry.lower() == 'q':  
            break  
        try:  
            val = float(entry)  
            grades.append(val)  
        except ValueError:  
            print("Error: Invalid input.")  
  
    if grades:  
        avg = sum(grades) / len(grades)  
        status = "Pass" if avg >= 60 else "Fail"  
        print(f"Average: {avg:.2f} | Status: {status}")  
    else:  
        print("No grades entered.")  
  
# --- MAIN EXECUTION ---  
if __name__ == "__main__":  
    # You can call whichever project you want to run here  
    temperature_converter()  
    grade_calculator()  

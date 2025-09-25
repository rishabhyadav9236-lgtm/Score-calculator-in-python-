def get_valid_score(exam_number):
    """Prompts for and validates a single exam score."""
    while True:
        try:
            score = float(input(f"Enter the score for Exam {exam_number}: "))
            if 0 <= score <= 100:
                return score
            else:
                print("Error: Score must be between 0 and 100. Please try again.")
        except ValueError:
            print("Error: Invalid input. Please enter a number.")

def calculate_grade():
    """Main function to run the grade calculation program."""
    print("Grade Calculator 📝")
    print("------------------")
    
    # Get scores with validation
    score1 = get_valid_score(1)
    score2 = get_valid_score(2)
    score3 = get_valid_score(3)
    
    # Calculate the average
    average_score = (score1 + score2 + score3) / 3
    
    # Determine the letter grade
    if average_score >= 90:
        grade = 'A'
    elif average_score >= 80:
        grade = 'B'
    elif average_score >= 70:
        grade = 'C'
    elif average_score >= 60:
        grade = 'D'
    else:
        grade = 'F'
    
    # Display the results
    print("\nResults:")
    print(f"Average Score: {average_score:.1f}")
    print(f"Letter Grade: {grade}")

# Run the program
calculate_grade()
# Score-calculator-in-python-

# Quiz
questions = [
    {
        "prompt": "What is the capital of France? ",
        "options": ["A. Paris","B.London","C.Berlin","D.Madrid"],
        "answer": "A"   
    },
    {
        "prompt": "Which language is primarily spoken in Brazil?",
        "options": ["A. Spanish","B. Portuguese","C. English","D. French"],
        "answer": "B"
    },
    {
        "prompt": "What is smallest prime number?",
        "options": ["A. 1","B. 2","C. 3","D. 5"],
            "answer": "B"    
    },
    {
        "prompt": "Who wrote 'TO Kill a MockingBird'?",
        "options": ["A. Harper Leo","B. Mark Twain", "C. J.K. Rowling","D. Ernest Heningway"],
        "answer": "A"
    }
]

def run_quiz(questions):
    score = 0
    for question in questions: 
        print(question["prompt"])
        for option in question["options"]:
            print(option)
        answer = input("Enter your answer (A, B, C, D): ").upper()
        if answer == question["answer"]:
                print("Horray! Correct Answer!!\n")
                score += 1   
        else:
                print("Wrong! The correct answer was",question["answer"],"\n")
                                        
    print(f"You got {score} out of {len(questions)} questions correct.")
run_quiz(questions)

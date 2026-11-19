# ==============================================================================
# PYTHON LEARNING SYSTEM (WITH BREAK STATEMENTS + 20-ITEM QUIZ)
# Built using while loops, if/elif/else conditionals, .strip()/.lower(), and break
# ==============================================================================

print("==========================================================")
print("************🐍 PYTHON LEARNING COMPANION 🐍*************")
print("==========================================================")
print("      Complete Study & Quiz System (Prelim - Finals)      ")
print("==========================================================")

raw_name = input("Enter your student name or username: ").strip()
if raw_name == "":
    learner_name = "Student"
else:
    learner_name = raw_name

# Main system loop
while True:
    print("\n==========================================================")
    print(f"WELCOME, {learner_name}!")
    print("----------------------------------------------------------")
    print("MAIN MENU:")
    print("  [1] Prelim Module  (Ch. 1-4: Intro, Syntax, Vars, Types, Ops, I/O)")
    print("  [2] Midterm Module (Conditionals, Nested If, Relational & Logical Ops)")
    print("  [3] Finals Module  (Iteration, for Loop, range(), while & break)")
    print("  [4] Take Final 20-Item Comprehensive Quiz (All Lessons)")
    print("  [5] Exit System")
    print("==========================================================")

    main_menu_choice = input("Choose an option (1-5): ").strip()

    # --------------------------------------------------------------------------
    # [1] PRELIM MODULE
    # --------------------------------------------------------------------------
    if main_menu_choice == "1":
        prelim_page = 1

        while True:
            if prelim_page == 1:
                print("\n----------------------------------------------------------")
                print("PRELIM - PAGE 1: CHAPTER 1 - INTRODUCTION TO PROGRAMMING")
                print("----------------------------------------------------------")
                print("• Programming Language: A special language that computers")
                print("  understand and use to perform tasks.")
                print("• Common Programming Languages:")
                print("  - Python    : Easy to learn and read; great for beginners,")
                print("                data science, and automation.")
                print("  - C / C++   : High performance and efficient; used in system")
                print("                programming, games, and applications.")
                print("  - PHP       : Used for web development; works well with")
                print("                databases and server-side scripting.")
                print("  - Java      : Platform-independent and widely used for apps")
                print("                and systems.")
                print("  - JavaScript: The language of the web; adds interactivity to")
                print("                websites.")
                print("  - Ruby      : Known for simplicity and productivity; used in")
                print("                web development.")
                print("• Python Programming:")
                print("  - Created by Guido van Rossum (Dutch software engineer) in 1991.")
                print("  - Designed to make programming simple, readable, and easy to")
                print("    learn while remaining powerful for professional development.")
                print("  - High-level, interpreted, and general-purpose language.")
                print("• Why Learn Python?")
                print("  1. Simple and easy to learn - Great for beginners")
                print("  2. Readable syntax - Code looks almost like English")
                print("  3. Versatile - Used in many fields (AI, web, automation, games)")
                print("  4. Huge community - Lots of support, tutorials, and libraries")
                print("• Professional IDEs / Code Editors to Start:")
                print("  - PyCharm (by JetBrains), VS Code, Jupyter Notebook/JupyterLab")

                print("\nNext Action:")
                print("  [1] Continue to Page 2 (Syntax, Case-Sensitivity, Indentation, print, Comments)")
                print("  [2] Return to Main Menu")
                step_p1 = input("Select (1-2): ").strip()

                if step_p1 == "1":
                    prelim_page = 2
                else:
                    break

            elif prelim_page == 2:
                print("\n----------------------------------------------------------")
                print("PRELIM - PAGE 2: CHAPTER 2 - SYNTAX, PRINT & COMMENTS")
                print("----------------------------------------------------------")
                print("• Syntax: The set of rules that tells us how to correctly write")
                print("  a program in Python.")
                print("• Rule 1 - Case-Sensitive:")
                print("  - Uppercase and lowercase letters are treated differently.")
                print("  - name = 'John' -> print(name) works, print(Name) causes Error.")
                print("• Rule 2 - Indentation:")
                print("  - Python uses indentation (spaces) to define code blocks.")
                print("  - Example: age = 18")
                print("             if age >= 18:")
                print("                 print('Adult')  # Indented inside block")
                print("• print() Statement: Displays information on the screen.")
                print("  - Syntax: print(value)")
                print("  - Text (str) needs quotes: print('Hello, World!')")
                print("    (Without quotes, Python treats words as variable names.)")
                print("  - Numbers (int/float) need no quotes: print(100), print(25.5)")
                print("  - print(100) is <class 'int'>, while print('100') is <class 'str'>.")
                print("• Python Comments (Ignored by Python; used to explain code):")
                print("  - Single-Line Comment: Starts with '#' until end of line.")
                print("  - Multi-Line Comment: Uses triple quotes for longer notes/docs.")

                print("\nNext Action:")
                print("  [1] Continue to Page 3 (Variables, Naming Rules & Outputting Variables)")
                print("  [2] Return to Main Menu")
                step_p2 = input("Select (1-2): ").strip()

                if step_p2 == "1":
                    prelim_page = 3
                else:
                    break

            elif prelim_page == 3:
                print("\n----------------------------------------------------------")
                print("PRELIM - PAGE 3: VARIABLES, NAMING RULES & OUTPUT")
                print("----------------------------------------------------------")
                print("• Variable: A named storage location used to keep data in a")
                print("  program; its value can change while the program runs.")
                print("• Assignment: Uses '=' (assignment operator).")
                print("  - Example: first_name = 'John'  (variable name = value)")
                print("• Variable Naming Rules:")
                print("  - Short names (x, y) vs. descriptive names (age, carname,")
                print("    total_volume, student_score).")
                print("  - GOOD names start with a letter or underscore (_) and may")
                print("    contain letters, numbers, underscores: number, NUMBER,")
                print("    bread, spam23, _speed.")
                print("  - BAD names start with a number or have spaces/special chars:")
                print("    1number, 1stValue, 2total, 123name, #bread, var.12,")
                print("    space name, @value.")
                print("  - Case-sensitive: age = 18 and AGE = 25 are different variables.")
                print("• Outputting Variables with print():")
                print("  - Single variable: school = 'Clark College' -> print(school)")
                print("  - Comma separator: a = 'I'; b = 'LOVE'; c = 'CCST'")
                print("    print(a, b, c)  -> outputs: I LOVE CCST")
                print("  - Plus operator (+): x = 'I '; y = 'LOVE '; z = 'CCST'")
                print("    print(x + y + z) -> joins (concatenates) strings in order")

                print("\nNext Action:")
                print("  [1] Continue to Page 4 (Basic Data Types & Declaration)")
                print("  [2] Return to Main Menu")
                step_p3 = input("Select (1-2): ").strip()

                if step_p3 == "1":
                    prelim_page = 4
                else:
                    break

            elif prelim_page == 4:
                print("\n----------------------------------------------------------")
                print("PRELIM - PAGE 4: BASIC DATA TYPES IN PYTHON")
                print("----------------------------------------------------------")
                print("• Data Types: Categories that tell Python what kind of data")
                print("  a variable stores and what operations can be done on it.")
                print("• Core Data Types:")
                print("  - int   (Integer) : Whole numbers without decimal part")
                print("                    (e.g., 10, 25, -7, 100)")
                print("  - float (Float)   : Numbers with a decimal point")
                print("                    (e.g., 12.5, 3.14, -0.001, 2.0)")
                print("  - str   (String)  : Text or characters inside quotes")
                print("                    (e.g., 'Hello', 'Juan', 'CCST')")
                print("  - bool  (Boolean) : One of two values: True or False")
                print("• Declaration & Output Example:")
                print("  name = 'Maria'       # str (string)")
                print("  age = 20             # int (integer)")
                print("  grade = 89.5         # float (decimal)")
                print("  is_enrolled = True   # bool (boolean)")
                print("  print(name); print(age); print(grade); print(is_enrolled)")

                print("\nNext Action:")
                print("  [1] Continue to Page 5 (Ch. 3 Arithmetic & PEMDAS; Ch. 4 Input & Conversion)")
                print("  [2] Return to Main Menu")
                step_p4 = input("Select (1-2): ").strip()

                if step_p4 == "1":
                    prelim_page = 5
                else:
                    break

            elif prelim_page == 5:
                print("\n----------------------------------------------------------")
                print("PRELIM - PAGE 5: CH. 3 OPERATORS/PEMDAS & CH. 4 INPUT/OUTPUT")
                print("----------------------------------------------------------")
                print("• Arithmetic Operators (Mathematical calculations on numbers):")
                print("  - +  : Addition        -> 5 + 3  = 8")
                print("  - -  : Subtraction     -> 10 - 4 = 6")
                print("  - *  : Multiplication  -> 7 * 2  = 14")
                print("  - /  : Division(float) -> 15 / 3 = 5.0")
                print("  - // : Floor Division  -> 17 // 3 = 5 (whole number part)")
                print("  - %  : Modulus         -> 10 % 3 = 1 (remainder)")
                print("  - ** : Exponentiation  -> 2 ** 3 = 8 (power)")
                print("• Expressions & PEMDAS (Order of Operations):")
                print("  - Expression: Combination of values, variables, and operators")
                print("    that evaluates to a result (e.g., a = 10; b = 5; result = a + b).")
                print("  - PEMDAS: Parentheses (First) -> Exponents -> Multiplication ->")
                print("            Division -> Addition -> Subtraction (Last).")
                print("• Accepting Input (Chapter 4):")
                print("  - Syntax: variable = input('Prompt message: ')")
                print("  - All input is string (str) type by default.")
                print("  - Formatting output with comma: print('Name: ', name)")
                print("• Converting Input to Other Data Types:")
                print("  - Integer: age = int(input('Enter your age: '))")
                print("  - Float  : grade = float(input('Enter your grade: '))")
                print("  - Boolean: is_student = answer.lower() == 'yes'")

                print("\n==========================================================")
                print("YOU HAVE FINISHED THE PRELIM MODULE!")
                print("==========================================================")
                print("  [1] Proceed to Midterm Module")
                print("  [2] Take the 20-Item Comprehensive Quiz Now")
                print("  [3] Return to Main Menu")
                step_p5 = input("Select (1-3): ").strip()

                if step_p5 == "1":
                    main_menu_choice = "2"
                    break
                elif step_p5 == "2":
                    main_menu_choice = "4"
                    break
                else:
                    break

    # --------------------------------------------------------------------------
    # [2] MIDTERM MODULE
    # --------------------------------------------------------------------------
    if main_menu_choice == "2":
        midterm_page = 1

        while True:
            if midterm_page == 1:
                print("\n----------------------------------------------------------")
                print("MIDTERM - PAGE 1: CONDITIONALS & RELATIONAL OPERATORS")
                print("----------------------------------------------------------")
                print("• Conditional Statement: Lets a program make decisions based on")
                print("  whether a condition is True or False.")
                print("• Relational (Comparison) Operators (Always return True or False):")
                print("  - == : Equal to                 (10 == 10 -> True)")
                print("  - != : Not equal to             (10 != 5  -> True)")
                print("  - >  : Greater than             (10 > 5   -> True)")
                print("  - <  : Less than                (5 < 10   -> True)")
                print("  - >= : Greater than or equal to (10 >= 10 -> True)")
                print("  - <= : Less than or equal to    (5 <= 10  -> True)")
                print("  - Example: score = 85 -> print(score >= 75)  # True")
                print("• Conditional Forms:")
                print("  - if condition: runs indented block only when True.")
                print("    (age = 18; if age >= 18: print('You are an adult.'))")
                print("  - if-else: runs else block when if condition is False.")
                print("    (score = 65; if score >= 75: print('Passed') else: print('Failed'))")
                print("  - if-elif-else: checks top to bottom; runs FIRST True block")
                print("    and skips the rest; else runs if none are True.")
                print("    (score = 85 -> 85>=90 False, 85>=80 True -> 'Very Good')")

                print("\nNext Action:")
                print("  [1] Continue to Page 2 (Nested Conditions)")
                print("  [2] Return to Main Menu")
                step_m1 = input("Select (1-2): ").strip()

                if step_m1 == "1":
                    midterm_page = 2
                else:
                    break

            elif midterm_page == 2:
                print("\n----------------------------------------------------------")
                print("MIDTERM - PAGE 2: NESTED CONDITION IN PYTHON")
                print("----------------------------------------------------------")
                print("• Nested Condition: A condition placed inside another condition.")
                print("• Flow Rule: Inner condition is checked ONLY if the outer")
                print("  condition is True.")
                print("• Syntax:")
                print("  if condition1:")
                print("      if condition2:")
                print("          # block of code")
                print("      else:")
                print("          # block of code")
                print("  else:")
                print("      # runs if condition1 is False")
                print("• Debutant Age Rules by Gender Example:")
                print("  - Male (M): age >= 21 -> 'You are a MALE DEBUTANT.'")
                print("              else      -> 'You are a male, but not a debutant yet.'")
                print("  - Female (F): age >= 18 -> 'You are a FEMALE DEBUTANT.'")
                print("                else    -> 'You are a female, but not a debutant yet.'")

                print("\nNext Action:")
                print("  [1] Continue to Page 3 (Logical Operators & Truth Tables)")
                print("  [2] Return to Main Menu")
                step_m2 = input("Select (1-2): ").strip()

                if step_m2 == "1":
                    midterm_page = 3
                else:
                    break

            elif midterm_page == 3:
                print("\n----------------------------------------------------------")
                print("MIDTERM - PAGE 3: LOGICAL OPERATORS & TRUTH TABLES")
                print("----------------------------------------------------------")
                print("• Logical Operators: Combine or reverse conditions (used with")
                print("  if, elif, else).")
                print("• 1. and (AND = KAILANGAN LAHAT TRUE):")
                print("  - Both/all conditions must be True.")
                print("  - True & True -> True | True & False -> False")
                print("  - False & True -> False | False & False -> False")
                print("  - Example: if age >= 18 and has_id: print('You are allowed to enter.')")
                print("• 2. or (OR = KAHIT ISA LANG TRUE):")
                print("  - At least one condition must be True.")
                print("  - True | True -> True | True | False -> True")
                print("  - False | True -> True | False | False -> False")
                print("  - Example: if day == 'Saturday' or day == 'Sunday': print(\"It's the weekend!\")")
                print("• 3. not (NOT = BALIKTARIN ANG RESULT):")
                print("  - Reverses the result: True -> False, False -> True.")
                print("  - Example: is_raining = False")
                print("    if not is_raining: print('You can go outside.') else: print('Bring an umbrella.')")

                print("\n==========================================================")
                print("YOU HAVE FINISHED THE MIDTERM MODULE!")
                print("==========================================================")
                print("  [1] Proceed to Finals Module")
                print("  [2] Take the 20-Item Comprehensive Quiz Now")
                print("  [3] Return to Main Menu")
                step_m3 = input("Select (1-3): ").strip()

                if step_m3 == "1":
                    main_menu_choice = "3"
                    break
                elif step_m3 == "2":
                    main_menu_choice = "4"
                    break
                else:
                    break

    # --------------------------------------------------------------------------
    # [3] FINALS MODULE
    # --------------------------------------------------------------------------
    if main_menu_choice == "3":
        finals_page = 1

        while True:
            if finals_page == 1:
                print("\n----------------------------------------------------------")
                print("FINALS - PAGE 1: ITERATION & PYTHON FOR LOOP")
                print("----------------------------------------------------------")
                print("• Iteration: Repeating a process or repeatedly executing")
                print("  a set of instructions; each repetition is an iteration.")
                print("• Why use loops instead of repeating print() lines?")
                print("  - Makes code shorter and easier to modify (e.g., changing")
                print("    range(4) to range(100) instead of copying 100 lines).")
                print("• Two Main Loop Types:")
                print("  - for loop  : Repeats for each item in a sequence (known")
                print("                number of repetitions).")
                print("  - while loop: Repeats while a condition is True.")
                print("• for Loop Syntax:")
                print("  for variable in sequence:")
                print("      statement(s)")
                print("• range() Examples:")
                print("  - for number in range(3): print('Welcome to Python!')")
                print("    (Runs 3 iterations; print() runs once per iteration)")
                print("  - for number in range(1, 6): print(number)")
                print("    (Start 1 included, stop 6 excluded -> prints 1 to 5, 5 iterations)")
                print("  - for number in range(5, 0, -1): print(number)")
                print("    (Starts at 5, stops before 0, step -1 -> prints 5, 4, 3, 2, 1)")

                print("\nNext Action:")
                print("  [1] Continue to Page 2 (while Loop & while True with break)")
                print("  [2] Return to Main Menu")
                step_f1 = input("Select (1-2): ").strip()

                if step_f1 == "1":
                    finals_page = 2
                else:
                    break

            elif finals_page == 2:
                print("\n----------------------------------------------------------")
                print("FINALS - PAGE 2: WHILE LOOP & WHILE TRUE WITH BREAK")
                print("----------------------------------------------------------")
                print("• while Loop Syntax:")
                print("  while condition:")
                print("      statement(s)")
                print("• Counting 1 to 5 Example:")
                print("  count = 1")
                print("  while count <= 5:")
                print("      print(count)")
                print("      count += 1")
                print("  - count += 1 adds 1 each iteration; when count becomes 6,")
                print("    the condition is False and the loop stops.")
                print("• Repeating a Program with while True:")
                print("  while True:")
                print("      name = input('Enter your name (X to exit): ')")
                print("      if name.upper() == 'X':")
                print("          print('Program stopped.')")
                print("          break")
                print("      print('Hello,', name)")
                print("  - break stops the loop when user types X or x.")

                print("\n==========================================================")
                print("YOU HAVE FINISHED ALL LESSONS (PRELIM, MIDTERM & FINALS)!")
                print("==========================================================")
                take_quiz_now = input("Do you want to take the 20-Item Comprehensive Quiz now? (yes/no): ").strip().lower()

                if take_quiz_now == "yes" or take_quiz_now == "y":
                    main_menu_choice = "4"
                    break
                else:
                    print("Okay! Returning to Main Menu. You can take the quiz anytime via Option [4].")
                    break

    # --------------------------------------------------------------------------
    # [4] 20-ITEM COMPREHENSIVE QUIZ (COVERS ALL LESSONS)
    # --------------------------------------------------------------------------
    if main_menu_choice == "4":
        while True:
            print("\n==========================================================")
            print("      COMPREHENSIVE PYTHON QUIZ (20 ITEMS - ALL LESSONS)  ")
            print("==========================================================")
            print("Instructions: Type the letter of your choice (a, b, or c).")
            print("----------------------------------------------------------")

            quiz_score = 0

            # --- PART 1: PRELIM QUESTIONS (Items 1-8) ---
            print("\n1. Who created the Python programming language in 1991?")
            print("   a) James Gosling   b) Guido van Rossum   c) Bjarne Stroustrup")
            if input("   Answer: ").strip().lower() == "b":
                quiz_score += 1

            print("\n2. Which programming language is described as 'The language of the web; adds interactivity to websites'?")
            print("   a) JavaScript   b) C++   c) Ruby")
            if input("   Answer: ").strip().lower() == "a":
                quiz_score += 1

            print("\n3. Why does print(Name) cause an error if the variable was created as name = 'John'?")
            print("   a) Missing quotes   b) Python is case-sensitive   c) Wrong indentation")
            if input("   Answer: ").strip().lower() == "b":
                quiz_score += 1

            print("\n4. Which symbol is used to start a single-line comment in Python?")
            print("   a) //   b) /*   c) #")
            if input("   Answer: ").strip().lower() == "c":
                quiz_score += 1

            print("\n5. Which of the following is a VALID variable name in Python?")
            print("   a) 1stValue   b) _speed   c) space name")
            if input("   Answer: ").strip().lower() == "b":
                quiz_score += 1

            print("\n6. What is the data type of the value 89.5?")
            print("   a) int   b) str   c) float")
            if input("   Answer: ").strip().lower() == "c":
                quiz_score += 1

            print("\n7. What is the result of the floor division expression 17 // 3?")
            print("   a) 5   b) 5.66   c) 2")
            if input("   Answer: ").strip().lower() == "a":
                quiz_score += 1

            print("\n8. According to PEMDAS, which operation is evaluated FIRST in Python?")
            print("   a) Multiplication   b) Addition   c) Parentheses")
            if input("   Answer: ").strip().lower() == "c":
                quiz_score += 1

            # --- PART 2: MIDTERM QUESTIONS (Items 9-14) ---
            print("\n9. What type of value do relational operators (==, !=, >, <, >=, <=) always return?")
            print("   a) Integer   b) String   c) True or False")
            if input("   Answer: ").strip().lower() == "c":
                quiz_score += 1

            print("\n10. In an if-elif-else structure, what happens if multiple conditions are True?")
            print("   a) Only the FIRST True block runs   b) All True blocks run   c) The else block runs")
            if input("   Answer: ").strip().lower() == "a":
                quiz_score += 1

            print("\n11. When is the inner condition inside a nested 'if' statement checked?")
            print("   a) Always   b) Only if the outer condition is True   c) Only if the outer condition is False")
            if input("   Answer: ").strip().lower() == "b":
                quiz_score += 1

            print("\n12. Which logical operator returns True ONLY when ALL conditions are True?")
            print("   a) or   b) not   c) and")
            if input("   Answer: ").strip().lower() == "c":
                quiz_score += 1

            print("\n13. What is the result of: True or False?")
            print("   a) True   b) False   c) None")
            if input("   Answer: ").strip().lower() == "a":
                quiz_score += 1

            print("\n14. If is_raining = False, what does 'not is_raining' evaluate to?")
            print("   a) False   b) True   c) Error")
            if input("   Answer: ").strip().lower() == "b":
                quiz_score += 1

            # --- PART 3: FINALS QUESTIONS (Items 15-20) ---
            print("\n15. In programming, what is each single repetition of a loop called?")
            print("   a) iteration   b) indentation   c) concatenation")
            if input("   Answer: ").strip().lower() == "a":
                quiz_score += 1

            print("\n16. Which loop is best used when the number of repetitions is already known?")
            print("   a) while loop   b) for loop   c) if-else")
            if input("   Answer: ").strip().lower() == "b":
                quiz_score += 1

            print("\n17. What numbers are printed by: for number in range(1, 6): print(number)?")
            print("   a) 1, 2, 3, 4, 5, 6   b) 0, 1, 2, 3, 4, 5   c) 1, 2, 3, 4, 5")
            if input("   Answer: ").strip().lower() == "c":
                quiz_score += 1

            print("\n18. What is the first number printed by: for number in range(5, 0, -1)?")
            print("   a) 5   b) 0   c) -1")
            if input("   Answer: ").strip().lower() == "a":
                quiz_score += 1

            print("\n19. In a while loop with 'count = 1' and 'while count <= 5:', at what value of count does the loop stop?")
            print("   a) 5   b) 6   c) 0")
            if input("   Answer: ").strip().lower() == "b":
                quiz_score += 1

            print("\n20. Which keyword is used to immediately stop a 'while True' loop when the user enters 'X'?")
            print("   a) stop   b) exit   c) break")
            if input("   Answer: ").strip().lower() == "c":
                quiz_score += 1

            # --- QUIZ RESULTS ---
            print("\n==========================================================")
            print(f"QUIZ COMPLETED! {learner_name}, your score is: {quiz_score} / 20")
            if quiz_score == 20:
                print("REMARKS: PERFECT SCORE! Outstanding mastery of all lessons!")
            elif quiz_score >= 15:
                print("REMARKS: PASSED WITH HONORS! Great job!")
            elif quiz_score >= 12:
                print("REMARKS: PASSED! Good understanding of the lessons.")
            else:
                print("REMARKS: NEEDS REVIEW. Go back to the modules and try again!")
            print("==========================================================")
            break

    # --------------------------------------------------------------------------
    # [5] EXIT SYSTEM
    # --------------------------------------------------------------------------
    elif main_menu_choice == "5":
        print("\n==========================================================")
        print(f"Thank you for studying, {learner_name}! Happy coding!")
        print("==========================================================")
        break

    # --------------------------------------------------------------------------
    # INVALID OPTION HANDLER
    # --------------------------------------------------------------------------
    elif main_menu_choice != "1" and main_menu_choice != "2" and main_menu_choice != "3" and main_menu_choice != "4":
        print("\nInvalid choice! Please select an option from 1 to 5.")

import os
import time

# ==============================================================================
# Enhanced UI Design with Box-Drawing Borders, ANSI Colors & Error Handling
# ==============================================================================

# ANSI Color Codes for Clean Terminal Styling
RESET = "\033[0m"
BOLD = "\033[1m"
CYAN = "\033[96m"
GREEN = "\033[92m"
YELLOW = "\033[93m"
RED = "\033[91m"
BLUE = "\033[94m"
MAGENTA = "\033[95m"
DIM = "\033[2m"

WIDTH = 74


def clear_screen():
    """Clears the terminal screen for a clean, slide-by-slide experience."""
    os.system("cls" if os.name == "nt" else "clear")


def print_banner(title, subtitle="", color=CYAN):
    """Renders a sleek double-lined box header."""
    print(f"\n{color}{BOLD}╔{'═' * (WIDTH - 2)}╗")
    print(f"║ {title.center(WIDTH - 4)} ║")
    if subtitle:
        print(f"║ {subtitle.center(WIDTH - 4)} ║")
    print(f"╚{'═' * (WIDTH - 2)}╝{RESET}")


def print_section(header_text, color=YELLOW):
    """Renders a clean sub-section divider."""
    print(f"\n{color}{BOLD}┌─ {header_text} {'─' * (WIDTH - len(header_text) - 5)}┐{RESET}")


def print_code_box(lines):
    """Displays Python syntax inside a W3Schools-style code block."""
    print(f"{DIM}  ┌{'─' * (WIDTH - 6)}┐{RESET}")
    for line in lines:
        print(f"{DIM}  │{RESET} {GREEN}{line:<{WIDTH - 8}}{RESET} {DIM}│{RESET}")
    print(f"{DIM}  └{'─' * (WIDTH - 6)}┘{RESET}")


def pause(menu_name="Menu"):
    """Waits for user confirmation before returning to the previous menu."""
    print(f"\n{DIM}{'─' * WIDTH}{RESET}")
    input(f"{CYAN}  Press [Enter] to return to {menu_name}...{RESET}")


# ==============================================================================
# MAIN PROGRAM LOOP
# ==============================================================================
running = True

while running:
    clear_screen()
    print_banner(
        "W3SCHOOLS x CCST PYTHON TUTORIAL",
        "CLARK COLLEGE OF SCIENCE & TECHNOLOGY | IT DEPARTMENT",
        CYAN,
    )

    print(f"\n  {BOLD}SELECT A TERM TO STUDY:{RESET}\n")
    print(f"   {GREEN}[1]{RESET} {BOLD}PRELIM{RESET}   │ Chapters 1–4 (Intro, Syntax, Operators, Input/Output)")
    print(f"   {YELLOW}[2]{RESET} {BOLD}MIDTERM{RESET}  │ Chapter 5    (If, Elif, Else & Nested Conditions)")
    print(f"   {MAGENTA}[3]{RESET} {BOLD}FINALS{RESET}   │ Chapter 6    (While Loops & Loop Controls)")
    print(f"   {RED}[0]{RESET} {BOLD}EXIT{RESET}     │ Quit Tutorial")
    print(f"\n{DIM}{'─' * WIDTH}{RESET}")

    term_choice = input(f"  {BOLD}Enter Term Number (0-3): {RESET}").strip()

    # ==========================================================================
    # TERM 1: PRELIM LESSONS
    # ==========================================================================
    if term_choice == "1":
        in_prelim = True
        while in_prelim:
            clear_screen()
            print_banner("PRELIM MODULE", "Chapters 1 to 4 | Python Fundamentals", GREEN)
            print(f"\n  {BOLD}SELECT A CHAPTER:{RESET}\n")
            print(f"   {GREEN}[1]{RESET} Chapter 1: Introduction to Python & IDEs")
            print(f"   {GREEN}[2]{RESET} Chapter 2: Basic Syntax, Comments, Variables & Data Types")
            print(f"   {GREEN}[3]{RESET} Chapter 3: Arithmetic Operators & PEMDAS Expressions")
            print(f"   {GREEN}[4]{RESET} Chapter 4: Accepting User Input & Type Casting")
            print(f"   {RED}[0]{RESET} Back to Main Term Menu")
            print(f"\n{DIM}{'─' * WIDTH}{RESET}")

            lesson = input(f"  {BOLD}Select Prelim Lesson (0-4): {RESET}").strip()

            if lesson == "1":
                clear_screen()
                print_banner("CHAPTER 1: INTRODUCTION TO PROGRAMMING", "Prelim Slide View", GREEN)

                print_section("DEFINITION")
                print("  • Python is a high-level, interpreted, general-purpose language.")
                print("  • Created by Guido van Rossum in 1991 (simple & readable).")

                print_section("WHY LEARN PYTHON?")
                print("  1. Simple & Beginner-Friendly  - Easy to read and write")
                print("  2. English-Like Syntax         - Clean, minimal punctuation")
                print("  3. Versatile & High Demand     - Used in AI, Web, Data & Automation")

                print_section("PROFESSIONAL IDEs / CODE EDITORS")
                print("  • PyCharm (by JetBrains)  • VS Code  • Jupyter Notebook / JupyterLab")

                print_section("W3SCHOOLS EXAMPLE", CYAN)
                print_code_box(['print("Welcome to CCST Python Programming!")'])
                print(f"  {BOLD}Output:{RESET} Welcome to CCST Python Programming!")
                pause("Prelim Menu")

            elif lesson == "2":
                clear_screen()
                print_banner("CHAPTER 2: SYNTAX, VARIABLES & DATA TYPES", "Prelim Slide View", GREEN)

                print_section("1. SYNTAX & COMMENTS")
                print("  • Case-Sensitive : 'name' and 'Name' are two different variables.")
                print("  • Indentation    : Uses spaces (4 spaces standard) to define blocks.")
                print("  • Single Comment : # This is a single-line comment")
                print('  • Multi-line     : """ This is a multi-line comment """')

                print_section("2. VARIABLE NAMING RULES")
                print(f"  {GREEN}✔ Valid:{RESET}   student_name, _speed, age2")
                print(f"  {RED}✘ Invalid:{RESET} 1number (starts with digit), my-var (contains hyphen)")

                print_section("3. BASIC DATA TYPES")
                print('  • str   (String)  -> name = "Maria"')
                print("  • int   (Integer) -> age = 20")
                print("  • float (Decimal) -> grade = 89.5")
                print("  • bool  (Boolean) -> is_enrolled = True")

                print_section("W3SCHOOLS TRY IT YOURSELF", CYAN)
                print_code_box([
                    'a, b, c = "I", "LOVE", "CCST"',
                    "print(a, b, c)"
                ])
                a, b, c = "I", "LOVE", "CCST"
                print(f"  {BOLD}Live Output:{RESET} {a} {b} {c}")
                pause("Prelim Menu")

            elif lesson == "3":
                clear_screen()
                print_banner("CHAPTER 3: ARITHMETIC OPERATORS & PEMDAS", "Prelim Slide View", GREEN)

                print_section("OPERATOR REFERENCE TABLE")
                print(f"  {BOLD}{'Operator':<10} {'Name':<18} {'Example':<14} {'Result'}{RESET}")
                print(f"  {'─' * 52}")
                print(f"  {'+':<10} {'Addition':<18} {'5 + 3':<14} 8")
                print(f"  {'-':<10} {'Subtraction':<18} {'10 - 4':<14} 6")
                print(f"  {'*':<10} {'Multiplication':<18} {'7 * 2':<14} 14")
                print(f"  {'/':<10} {'Division (float)':<18} {'15 / 3':<14} 5.0")
                print(f"  {'//':<10} {'Floor Division':<18} {'17 // 3':<14} 5")
                print(f"  {'%':<10} {'Modulus':<18} {'10 % 3':<14} 1")
                print(f"  {'**':<10} {'Exponentiation':<18} {'2 ** 3':<14} 8")

                print_section("ORDER OF OPERATIONS: PEMDAS")
                print("  Parentheses -> Exponents -> Multiplication/Division -> Add/Subtract")

                print_section("LIVE DEMO", CYAN)
                print_code_box(["print(10 + 5 * 2)"])
                print(f"  {BOLD}Live Output:{RESET} {10 + 5 * 2}")
                pause("Prelim Menu")

            elif lesson == "4":
                clear_screen()
                print_banner("CHAPTER 4: USER INPUT & TYPE CASTING", "Prelim Slide View", GREEN)

                print_section("KEY CONCEPTS")
                print("  • input() ALWAYS returns data as a string (str) by default.")
                print("  • Use int() to convert to whole numbers and float() for decimals.")

                print_section("INTERACTIVE TRY IT YOURSELF", CYAN)
                print_code_box([
                    'name = input("Enter your name: ")',
                    'age = int(input("Enter your age: "))',
                    'grade = float(input("Enter your final grade: "))'
                ])

                try_ch4 = input(f"\n  {YELLOW}Do you want to test live input? (yes/no): {RESET}").strip().lower()
                if try_ch4 == "yes":
                    try:
                        u_name = input("  Enter your name: ").strip()
                        u_age = int(input("  Enter your age: "))
                        u_grade = float(input("  Enter your final grade: "))
                        print(f"\n  {GREEN}{BOLD}OUTPUT -> Student: {u_name} | Age: {u_age} | Final Grade: {u_grade}{RESET}")
                    except ValueError:
                        print(f"\n  {RED}[!] Error: Please enter valid numbers for Age and Final Grade.{RESET}")
                else:
                    print(f"  {DIM}Skipped live demo.{RESET}")
                pause("Prelim Menu")

            elif lesson == "0":
                in_prelim = False
            else:
                print(f"\n  {RED}[!] Invalid choice. Please enter 0 to 4.{RESET}")
                time.sleep(1.2)

    # ==========================================================================
    # TERM 2: MIDTERM LESSONS
    # ==========================================================================
    elif term_choice == "2":
        in_midterm = True
        while in_midterm:
            clear_screen()
            print_banner("MIDTERM MODULE", "Chapter 5 | Conditional Statements", YELLOW)
            print(f"\n  {BOLD}SELECT A LESSON:{RESET}\n")
            print(f"   {YELLOW}[1]{RESET} Lesson 1: If, Elif, and Else Statements")
            print(f"   {YELLOW}[2]{RESET} Lesson 2: Nested If Conditions (Interactive Grade Checker)")
            print(f"   {RED}[0]{RESET} Back to Main Term Menu")
            print(f"\n{DIM}{'─' * WIDTH}{RESET}")

            mid_choice = input(f"  {BOLD}Select Midterm Lesson (0-2): {RESET}").strip()

            if mid_choice == "1":
                clear_screen()
                print_banner("LESSON 1: PYTHON IF ... ELIF ... ELSE", "Midterm Slide View", YELLOW)

                print_section("HOW IT WORKS")
                print("  • Conditional statements let Python make decisions based on True/False.")
                print("  • Only the FIRST matching condition block will run.")

                print_section("SYNTAX STRUCTURE", CYAN)
                print_code_box([
                    "if condition1:",
                    "    # runs if condition1 is True",
                    "elif condition2:",
                    "    # runs if condition1 is False and condition2 is True",
                    "else:",
                    "    # runs if all conditions above are False"
                ])
                pause("Midterm Menu")

            elif mid_choice == "2":
                clear_screen()
                print_banner("LESSON 2: NESTED IF STATEMENTS", "Interactive Grade Checker", YELLOW)

                print_section("CONCEPT")
                print("  • A nested 'if' is an if statement placed inside another if statement.")

                print_section("LIVE TRY IT YOURSELF", CYAN)
                enrolled = input("  Are you enrolled at CCST? (yes/no): ").strip().lower()

                if enrolled == "yes":
                    try:
                        score = float(input("  Enter your exam score (0-100): "))
                        if score < 0 or score > 100:
                            print(f"  {RED}[!] Please enter a score between 0 and 100.{RESET}")
                        elif score >= 90:
                            print(f"  {GREEN}{BOLD}RESULT: Passed with Honors (Excellent!){RESET}")
                        elif score >= 75:
                            print(f"  {GREEN}RESULT: Passed!{RESET}")
                        else:
                            print(f"  {RED}RESULT: Failed. Needs remedial exam.{RESET}")
                    except ValueError:
                        print(f"  {RED}[!] Invalid input. Please enter a numeric score.{RESET}")
                else:
                    print(f"  {RED}RESULT: Access denied. Please enroll first.{RESET}")
                pause("Midterm Menu")

            elif mid_choice == "0":
                in_midterm = False
            else:
                print(f"\n  {RED}[!] Invalid choice. Please enter 0 to 2.{RESET}")
                time.sleep(1.2)

    # ==========================================================================
    # TERM 3: FINALS LESSONS
    # ==========================================================================
    elif term_choice == "3":
        in_finals = True
        while in_finals:
            clear_screen()
            print_banner("FINALS MODULE", "Chapter 6 | Python While Loops", MAGENTA)
            print(f"\n  {BOLD}SELECT A LESSON:{RESET}\n")
            print(f"   {MAGENTA}[1]{RESET} Lesson 1: While Loop Syntax & Counter")
            print(f"   {MAGENTA}[2]{RESET} Lesson 2: Break & Continue Statements (Live Demo)")
            print(f"   {RED}[0]{RESET} Back to Main Term Menu")
            print(f"\n{DIM}{'─' * WIDTH}{RESET}")

            fin_choice = input(f"  {BOLD}Select Finals Lesson (0-2): {RESET}").strip()

            if fin_choice == "1":
                clear_screen()
                print_banner("LESSON 1: PYTHON WHILE LOOPS", "Finals Slide View", MAGENTA)

                print_section("DEFINITION")
                print("  • A while loop repeatedly executes a block of code as long as")
                print("    a given condition evaluates to True.")
                print("  • Always update your counter variable to prevent infinite loops!")

                print_section("EXAMPLE CODE", CYAN)
                print_code_box([
                    "i = 1",
                    "while i <= 5:",
                    "    print(f'Count: {i}')",
                    "    i += 1"
                ])

                print_section("LIVE OUTPUT", GREEN)
                i = 1
                while i <= 5:
                    print(f"  Count: {i}")
                    i += 1
                pause("Finals Menu")

            elif fin_choice == "2":
                clear_screen()
                print_banner("LESSON 2: BREAK & CONTINUE STATEMENTS", "Finals Slide View", MAGENTA)

                print_section("LOOP CONTROL KEYWORDS")
                print(f"  • {BOLD}break{RESET}    : Immediately stops the loop even if condition is True.")
                print(f"  • {BOLD}continue{RESET} : Skips the current iteration and jumps to the next.")

                print_section("LIVE DEMO (Count 1–6, Skip 3, Stop at 5)", CYAN)
                print_code_box([
                    "num = 0",
                    "while num < 6:",
                    "    num += 1",
                    "    if num == 3:",
                    "        continue  # skips 3",
                    "    if num == 5:",
                    "        break     # stops loop",
                    "    print('Number:', num)"
                ])

                print_section("LIVE OUTPUT", GREEN)
                num = 0
                while num < 6:
                    num += 1
                    if num == 3:
                        print(f"  {DIM}(Skipped 3 via continue){RESET}")
                        continue
                    if num == 5:
                        print(f"  {YELLOW}Reached 5 -> break! Loop stopped.{RESET}")
                        break
                    print(f"  Number: {num}")
                pause("Finals Menu")

            elif fin_choice == "0":
                in_finals = False
            else:
                print(f"\n  {RED}[!] Invalid choice. Please enter 0 to 2.{RESET}")
                time.sleep(1.2)

    # ==========================================================================
    # EXIT PROGRAM
    # ==========================================================================
    elif term_choice == "0":
        clear_screen()
        print_banner(
            "THANK YOU FOR STUDYING!",
            "CCST IT DEPARTMENT x W3SCHOOLS PYTHON TUTORIAL",
            CYAN,
        )
        print(f"\n  {GREEN}Keep coding and good luck with your Python journey!{RESET}\n")
        running = False

    else:
        print(f"\n  {RED}[!] Invalid selection. Please choose 1, 2, 3, or 0.{RESET}")
        time.sleep(1.2)

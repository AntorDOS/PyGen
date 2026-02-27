#!/usr/bin/env python3
"""
PYGEN - Advanced Password Generator & Strength Checker
Author: Jahid Hasan
Version: 1.0
"""
import random
import math
from time import sleep

# ANSI color codes
WHITE = '\033[97m'
ORANGE = '\033[38;2;255;165;0m'
RESET = "\033[0m"
RED = '\033[91m'
GREEN = '\033[92m'
YELLOW = '\033[93m'
BLUE = '\033[94m'
MAGENTA = '\033[95m'
CYAN = '\033[96m'
RESET = '\033[0m'  # Reset color


def show_banner():
    # ANSI color codes
    ORANGE = '\033[38;2;255;165;0m'
    RED = '\033[91m'
    CYAN = '\033[96m'
    YELLOW = '\033[93m'
    RESET = '\033[0m'

    banner_width = 40

    # Main Banner
    print(RED + r"""
██████╗ ██╗   ██╗ ██████╗ ███████╗███╗   ██╗
██╔══██╗╚██╗ ██╔╝██╔════╝ ██╔════╝████╗  ██║
██████╔╝ ╚████╔╝ ██║  ███╗█████╗  ██╔██╗ ██║
██╔═══╝   ╚██╔╝  ██║   ██║██╔══╝  ██║╚██╗██║
██║        ██║   ╚██████╔╝███████╗██║ ╚████║
╚═╝        ╚═╝    ╚═════╝ ╚══════╝╚═╝  ╚═══╝
""" + RESET)

    print(CYAN + "=" * 70 + RESET)

    # Title
    print(YELLOW + "        🔑 PYGEN - Advanced Password Generator & Strength Checker" + RESET)

    # Right-side small signature (banner er niche, dan pashe)
    creator = "By JAHID HASAN"
    print(" " * (banner_width - len(creator)) + ORANGE + creator + RESET)

    print(CYAN + "=" * 70 + RESET)


def show_menu():
    print(GREEN + "\nPlease Select an Option:")
    print(ORANGE + "-" * 40)
    print("  1️⃣   Generate Strong Password")
    print("  2️⃣   Check Password Strength")
    print("  3️⃣   Exit Program")
    print(ORANGE + "-" * 40)


def entropy(passlen):
    e = passlen * math.log2(92)
    print(CYAN + "Your password entropy is: ", int(e), "bit")
    if e < 28:
        print(GREEN + "Strength Level: 🔴  Very Weak")
    elif (e > 27 and e < 36):
        print(GREEN + "Strength Level: 🔴  Weak")
    elif (e > 35 and e < 60):
        print(GREEN + "Strength Level: 🟡  Moderate")
    elif (e > 59 and e < 80):
        print(GREEN + "Strength Level: 🟢  Strong")
    elif (e > 79 and e < 100):
        print(GREEN + "Strength Level: 🟢  Very Strong")
    elif (e > 100):
        print(GREEN + "Strength Level: 🔵  Extremely Strong")


try:
    n = 1
    while n != 0:
        show_banner()
        show_menu()

        choice = int(input(WHITE + "Enter Your Choice: "))

        sletters = list("abcdefghijklmnopqrstuvwxyz")
        capletters = list("ABCDEFGHIJKLMNOPQRSTUVWXYZ")
        numbers = list("0123456789")
        spsymbols = list("!#$%&()*+,-./:;<=>?@[]^_{|}~")

        if choice == 1:
            try:
                n = 0
                while n != 1:

                    print(GREEN + "\n" + "=" * 40)
                    print(BLUE + "        🔑 PASSWORD GENERATOR")
                    print(GREEN + "=" * 40)

                    passlen = int(input(WHITE + "How Many Password Length You Want: "))
                    password_list = []
                    password_list += list(random.choice(sletters))
                    password_list += list(random.choice(capletters))
                    password_list += list(random.choice(numbers))
                    password_list += list(random.choice(spsymbols))
                    random.shuffle(password_list)
                    all_chrc = sletters + capletters + numbers + spsymbols

                    while len(password_list) != passlen:
                        password_list += random.choice(all_chrc)

                    random.shuffle(password_list)
                    password = "".join(password_list)
                    print(CYAN + "Generating Password...")
                    sleep(2)
                    print()
                    print(ORANGE + "Your Password is: ", GREEN + password)
                    entropy(passlen)
                    print()

                    exit = input(RED + "Are You Want You Exit (y/n)? ")
                    if exit == "y":
                        n = 1

                    elif exit == "n":
                        n = 0
                        print()
            except KeyboardInterrupt:
                quit()
            except EOFError:
                quit()

        elif choice == 3:
            print(RED + "Quit....")
            sleep(2)
            print()
            print(GREEN + "====== Thanks For Using passgen ======")
            print()
            break

        elif choice == 2:

            try:
                n = 0
                while n != 1:
                    print(GREEN + "\n" + "=" * 40)
                    print(BLUE + "      📊 PASSWORD STRENGTH CHECKER")
                    print(GREEN + "=" * 40)
                    print()

                    passwd = input(ORANGE + "Enter Your Password: ")

                    has_small = False
                    has_cap = False
                    has_nums = False
                    has_spsym = False
                    for c in passwd:
                        if c in sletters:
                            has_small = True
                        elif c in capletters:
                            has_cap = True
                        elif c in numbers:
                            has_nums = True
                        elif c in spsymbols:
                            has_spsym = True

                    r = 0
                    if has_small:
                        r += len(sletters)
                    if has_cap:
                        r += len(capletters)
                    if has_nums:
                        r += len(numbers)
                    if has_spsym:
                        r += len(spsymbols)
                    l = len(passwd)
                    e = l * math.log2(r)
                    print(MAGENTA + "Calculating....")
                    sleep(2)
                    print()
                    print(CYAN + "Your password entropy is: ", int(e), "bit")
                    if e < 28:
                        print(GREEN + "Strength Level: 🔴  Very Weak")
                    elif (e > 27 and e < 36):
                        print(GREEN + "Strength Level: 🔴  Weak")
                    elif (e > 35 and e < 60):
                        print(GREEN + "Strength Level: 🟡  Moderate")
                    elif (e > 59 and e < 80):
                        print(GREEN + "Strength Level: 🟢  Strong")
                    elif (e > 79 and e < 100):
                        print(GREEN + "Strength Level: 🟢  Very Strong")
                    elif (e > 100):
                        print(GREEN + "Strength Level: 🔵  Extremely Strong")

                    print()
                    qt = input(RED + "Are You Want You Exit (y/n)? ")
                    if qt == "y":
                        n = 1
                        print()
                    elif qt == "n":
                        n = 0
                        print()
                    else:
                        print(RED + "Wrong Input!")
            except KeyboardInterrupt:
                quit()
            except EOFError:
                quit()
except KeyboardInterrupt:
    quit()
except EOFError:

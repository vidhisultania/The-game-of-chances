# The-game-of-chances
Python project
# importing library file tkinter
from tkinter import *
import tkinter as tk
import random

# creating windows
window = tk.Tk()
window1 = tk.Toplevel()
window1.withdraw()
window2 = tk.Toplevel()
window2.withdraw()

# defining global variables
global computer_point
computer_point = 0
global player_point
player_point = 0
global final_point
final_point = 0

# Content to be shown in the first window...
window.title("THE GAME OF CHANCES")
window.geometry("550x250")

label1 = tk.Label(window, text="THE GAME OF CHANCES", font=("Arial Bold", 18), bg="plum1", fg="deep pink")
label1.place(x=110, y=20, bordermode=OUTSIDE)

label2 = tk.Label(window, text="Player's Name", font=("Arial Bold", 12), bg="cyan2", fg="PaleGreen4")
label2.place(x=40, y=70)

txt = Entry(window, text="player name", width=30)
txt.place(x=160, y=70)

# creating dictionary for default value for computer..
computer_choice = {
    "0": "Rock",
    "1": "Paper",
    "2": "scissor",
    "3": "Lizard",
    "4": "Spock"
}

# Main driving code...
# defining function x for second window...


def x():
    window.withdraw()
    window2.withdraw()
    window1.deiconify()
    window1.geometry("800x450")

    # defining global variable...
    global computer_point
    global player_point
    global final_point
    player_point = 0
    computer_point = 0
    # Adding names of both the  player's ...
    label7 = Label(window1, text="player's name-->" + txt.get(), width=18)
    label7.place(x=500, y=320)
    label8 = Label(window1, text="Computer-->", width=18)
    label8.place(x=50, y=320)

    # defining function for rock...
    def rock():
        global computer_point
        global player_point
        global final_point
        # taking value as a variable for computer choices and for comparing it with players choice...
        value = computer_choice[str(random.randint(0, 4))]
        if value == "Rock":
            result = "Match Draw"
        elif value == "Scissor":
            result = "you won"
            player_point += 1
        elif value == "Lizard":
            result = "you won"
            player_point += 1
        elif value == "Paper":
            result = "computer won"
            computer_point += 1
        else:
            result = "computer won"
            computer_point += 1
        label5.config(text="player point " + str(player_point))
        label6.config(text="computer point " + str(computer_point))
        # showing both player's point...
        if computer_point == 3:
            final_point = player_point
            player_point = 0
            computer_point = 0
            label5.config(text="player point " + str(player_point))
            label6.config(text="computer point " + str(computer_point))
            x1()

    # defining function for paper
    def paper():
        global computer_point
        global player_point
        global final_point
        # taking value as a variable for computer choices and for comparing it with players choice...
        value = computer_choice[str(random.randint(0, 4))]
        if value == "Paper":
            result = "Match Draw"
        elif value == "Lizard":
            result = "computer won"
            computer_point += 1
        elif value == "Spock":
            result = "you won"
            player_point += 1
        elif value == "Scissor":
            result = "computer won"
            computer_point += 1
        else:
            result = "you won"
            player_point += 1
        label5.config(text="player point " + str(player_point))
        label6.config(text="computer point " + str(computer_point))
        # showing both player's point...
        if computer_point == 3:
            final_point = player_point
            player_point = 0
            computer_point = 0
            label5.config(text="player point " + str(player_point))
            label6.config(text="computer point " + str(computer_point))
            x1()

    # defining function of scissor
    def scissor():
        global computer_point
        global player_point
        global final_point
        # taking value as a variable for computer choices and for comparing it with players choice...
        value = computer_choice[str(random.randint(0, 4))]
        if value == "Scissor":
            result = "Match Draw"
        elif value == "Paper":
            result = "You won"
            player_point += 1
        elif value == "Spock":
            result = "computer won"
            computer_point += 1
        elif value == "Rock":
            result = "computer won"
            computer_point += 1
        else:
            result = "you won"
            player_point += 1
        label5.config(text="player point " + str(player_point))
        label6.config(text="computer point " + str(computer_point))
        # showing both player's point...
        if computer_point == 3:
            final_point = player_point
            player_point = 0
            computer_point = 0
            label5.config(text="player point " + str(player_point))
            label6.config(text="computer point " + str(computer_point))
            x1()

    # defining function of Lizard
    def lizard():
        global computer_point
        global player_point
        global final_point
        # taking value as a variable for computer choices and for comparing it with players choice...
        value = computer_choice[str(random.randint(0, 4))]
        if value == "Lizard":
            result = "Match Draw"
        elif value == "Rock":
            result = "computer won"
            computer_point += 1
        elif value == "Scissor":
            result = "computer won"
            computer_point += 1
        elif value == "Paper":
            result = "you won"
            player_point += 1
        else:
            result = "you won"
            player_point += 1
        label5.config(text="player point " + str(player_point))
        label6.config(text="computer point " + str(computer_point))
        # showing both player's point...
        if computer_point == 3:
            final_point = player_point
            player_point = 0
            computer_point = 0
            label5.config(text="player point " + str(player_point))
            label6.config(text="computer point " + str(computer_point))
            x1()

    # defining function for spock
    def spock():
        global computer_point
        global player_point
        global final_point
        # taking value as a variable for computer choices and for comparing it with players choice...
        value = computer_choice[str(random.randint(0, 4))]
        if value == "Spock":
            result = "Match Draw"
        elif value == "Rock":
            result = "you won"
            player_point += 1
        elif value == "Scissor":
            result = "you won"
            player_point += 1
        elif value == "Paper":
            result = "computer won"
            computer_point += 1
        else:
            result = "computer won"
            computer_point += 1
        label5.config(text="player point " + str(player_point))
        label6.config(text="computer point " + str(computer_point))
        # showing both player's point...
        if computer_point == 3:
            final_point = player_point
            player_point = 0
            computer_point = 0
            label5.config(text="player point " + str(player_point))
            label6.config(text="computer point " + str(computer_point))
            x1()

    # setting button for player
    b5 = Button(window1, text="Rock", command=rock, font=("Arial Bold", 8), width=15, bg="saddle brown")
    b5.place(x=550, y=40)
    b6 = Button(window1, text="Paper", command=paper, font=("Arial Bold", 8), width=15, bg="misty rose")
    b6.place(x=550, y=100)
    b7 = Button(window1, text="Scissor", command=scissor, font=("Arial Bold", 8), width=15, bg="gray")
    b7.place(x=550, y=160)
    b8 = Button(window1, text="Lizard", command=lizard, font=("Arial Bold", 8), width=15, bg="green2")
    b8.place(x=550, y=220)
    b9 = Button(window1, text="Spock", command=spock, font=("Arial Bold", 8), width=15, bg="tan1")
    b9.place(x=550, y=280)

    window1.mainloop()


def x1():
    window1.withdraw()
    window2.deiconify()
    window2.geometry("550x250")
    global computer_point
    global player_point
    global final_point
    label4 = Label(window2, text="your point is " + str(final_point))
    label4.pack(fill=BOTH)
    window2.mainloop()


def x3():
    window2.destroy()
    window2.mainloop()


# setting button for first window to start game
b1 = Button(window, text="START", command=x, width=15, font=("Bold", 8), bg="yellow")
b1.place(x=170, y=110)

# setting button for third window
b3 = Button(window2, text="START NEW", command=x, width=15, font=("Bold", 8), bg="firebrick1")
b3.place(x=230, y=110)
b4 = Button(window2, text="EXIT", command=x3, width=15, font=("Bold", 8), bg="orange red")
b4.place(x=230, y=150)

# DEFINING BUTTONS FOR COMPUTER
b2 = Button(window1, text="Rock", font=("Arial Bold", 8), width=15, bg="saddle brown")
b2.place(x=30, y=40)
b10 = Button(window1, text="Paper", font=("Arial Bold", 8), width=15, bg="misty rose")
b10.place(x=30, y=100)
b11 = Button(window1, text="Scissor", font=("Arial Bold", 8), width=15, bg="gray")
b11.place(x=30, y=160)
b12 = Button(window1, text="Lizard", font=("Arial Bold", 8), width=15, bg="green2")
b12.place(x=30, y=220)
b13 = Button(window1, text="Spock", font=("Arial Bold", 8), width=15, bg="tan1")
b13.place(x=30, y=280)

# getting score in second window
label5 = Label(window1, text="")
label5.place(x=300, y=350, anchor=CENTER)
label6 = Label(window1, text="")
label6.place(x=300, y=400, anchor=CENTER)

window.mainloop()

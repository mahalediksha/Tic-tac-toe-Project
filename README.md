# Tic-tac-toe-Project

import tkinter as to
import tkinter.messagebox

#to display the game board
game=tk.Tk
game.resizable(0,0)
game.title("TIC-TAC-TOE Using Python")
tk.Label(game,text="TIC-TAC-TOE",font="Calibri 20 bold")

#to take the player names
playerA=tk.StringVar()
playerB=tk.StringVar()
p1=tk.StringVar()
p2=tk.StringVar()

player1_name=tk.Entry(game, textvariable=p1, bd=5)
player1_name.grid(row=1, column=1, columnspan=8)
player2_name=tk.Entry(game, textvariable=p2, bd=5)
player2_name.grid(row=2, column=1, columnspan=8)

bclick=True
flag=0

buttons=tk.StringVar()

#function to disable the button
def disable_Button():
    button1.configure(state="disabled")
    button2.configure(state="disabled")
    button3.configure(state="disabled")
    button4.configure(state="disabled")
    button5.configure(state="disabled")
    button6.configure(state="disabled")
    button7.configure(state="disabled")
    button8.configure(state="disabled")
    button9.configure(state="disabled")

#function for button click
def button_click(buttons):
    global bclick,flag, player1_name, player2_name, playerB, playerA

    if buttons["text"]==" " and bclick==True:
        buttons["text"]=="X"
        bclick=False
        playerB=p2.get()+" is the winner!"
        playerA=p1.get()+" is the winner!"
        CheckForWin()
        flag+=1

     elif buttons["text"]==" " and bclick==False:
        buttons["text"]=="O"
        bclick=True
        CheckForWin()
        flag+=1

     else:
         tkinter.messagebox.showinfo("TIC-TAC-TOE Using Python","Button is already clicked")
    
#function with condition to check the winner
def CheckForWin():
    if(button1["text"]=='X' and button2["text"]=='X' and button3["text"]=='X' or
          button4["text"]=='X' and button5["text"]=='X' and button6["text"]=='X' or
          button7["text"]=='X' and button8["text"]=='X' and button9["text"]=='X' or
          button1["text"]=='X' and button4["text"]=='X' and button7["text"]=='X' or
          button2["text"]=='X' and button5["text"]=='X' and button8["text"]=='X' or
          button3["text"]=='X' and button6["text"]=='X' and button9["text"]=='X' or
          button1["text"]=='X' and button5["text"]=='X' and button9["text"]=='X' or
          button3["text"]=='X' and button5["text"]=='X' and button7["text"]=='X'):
        disable_Button()
        tkinter.messagebox.showinfo(TIC-TAC-TOE Using Python", playerA)

     elif flag==8:
         tkinter.messagebox.showinfo(TIC-TAC-TOE Using Python","It's a tie")

     elif(button1["text"]=='O' and button2["text"]=='O' and button3["text"]=='O' or
          button4["text"]=='O' and button5["text"]=='O' and button6["text"]=='O' or
          button7["text"]=='O' and button8["text"]=='O' and button9["text"]=='O' or
          button1["text"]=='O' and button4["text"]=='O' and button7["text"]=='O' or
          button2["text"]=='O' and button5["text"]=='O' and button8["text"]=='O' or
          button3["text"]=='O' and button6["text"]=='O' and button9["text"]=='O' or
          button1["text"]=='O' and button5["text"]=='O' and button9["text"]=='O' or
          button3["text"]=='O' and button5["text"]=='O' and button7["text"]=='O'):
        disable_Button()
        tkinter.messagebox.showinfo(TIC-TAC-TOE Using Python", playerB)
    
label=tk.Label(game,text="Player 1:",font="Cambria 15 bold",bg="white",fg="black",height=1,width=8)
label.grid(row=1, column=0)

label=tk.Label(game,text="Player 2:",font="Cambria 15 bold",bg="white",fg="black",height=1,width=8)
label.grid(row=2, column=0)

button1=tk.Button(game,text=" ",font="Cambria 15 bold",bg="grey",fg="black",height=4,width=8,command=lambda:button_click(button1))
button1.grid(row=3, column=0)

button2=tk.Button(game,text=" ",font="Cambria 15 bold",bg="grey",fg="black",height=4,width=8, command=lambda:button_click(button2))
button2.grid(row=3, column=1)

button3=tk.Button(game,text=" ",font="Cambria 15 bold",bg="grey",fg="black",height=4,width=8, command=lambda:button_click(button3))
button3.grid(row=3, column=2)

button4=tk.Button(game,text=" ",font="Cambria 15 bold",bg="grey",fg="black",height=4,width=8, command=lambda:button_click(button4))
button4.grid(row=4, column=0)

button5=tk.Button(game,text=" ",font="Cambria 15 bold",bg="grey",fg="black",height=4,width=8, command=lambda:button_click(button5))
button5.grid(row=4, column=1)

button6=tk.Button(game,text=" ",font="Cambria 15 bold",bg="grey",fg="black",height=4,width=8, command=lambda:button_click(button6))
button6.grid(row=4, column=2)

button7=tk.Button(game,text=" ",font="Cambria 15 bold",bg="grey",fg="black",height=4,width=8, command=lambda:button_click(button7))
button7.grid(row=5, column=0)

button8=tk.Button(game,text=" ",font="Cambria 15 bold",bg="grey",fg="black",height=4,width=8, command=lambda:button_click(button8))
button8.grid(row=5, column=1)

button9=tk.Button(game,text=" ",font="Cambria 15 bold",bg="grey",fg="black",height=4,width=8, command=lambda:button_click(button9))
button9.grid(row=5, column=2)

game.mainloop()







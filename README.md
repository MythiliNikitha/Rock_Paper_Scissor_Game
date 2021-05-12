# Rock_Paper_Scissor_Game
import random
from tkinter import * 

def press():
	result = Label(root, text = "Rock")
	result.place(x = 290, y = 180)
	res = "Rock"
	tools = ['Rock','Paper','Scissor']
	choose = random.choice(tools)
	computer = Label(root, text = choose)
	computer.place(x =290 , y =240)

	if(res == choose):
		test = Label(root, text ="DRAW")
		test.place(x = 220, y = 300)
	elif(choose == 'Paper'):
		test = Label(root, text ="COMPUTER WON")
		test.place(x = 220, y = 300)
	elif(choose == 'Scissor'):
		test = Label(root, text ="YOU WON")
		test.place(x = 220, y = 300)
	
def pap():
	result = Label(root, text = "Paper")
	result.place(x=290, y = 180)
	res = "Paper"
	tools = ['Rock','Paper','Scissor']
	choose = random.choice(tools)
	computer = Label(root, text = choose)
	computer.place(x =290 , y =240)
	if(res == choose):
		test = Label(root, text ="DRAW")
		test.place(x = 220, y = 300)
	elif(choose == 'Rock'):
		test = Label(root, text ="YOU WON")
		test.place(x = 220, y = 300)
	elif(choose == 'Scissor'):
		test = Label(root, text ="COMPUTER WON")
		test.place(x = 220, y = 300)

def sci():
	result = Label(root, text = "SCISSOR")
	result.place(x = 290, y = 180)
	res = "Scissor"
	tools = ['Rock','Paper','Scissor']
	choose = random.choice(tools)
	computer = Label(root, text = choose)
	computer.place(x =290 , y =240)
	if(res == choose):
		test = Label(root, text ="DRAW")
		test.place(x = 220, y = 300)
	elif(choose == 'Rock'):
		test = Label(root, text ="COMPUTER WON")
		test.place(x = 220, y = 300)
	elif(choose == 'Paper'):
		test = Label(root, text ="YOU WON")
		test.place(x = 220, y = 300)

root = Tk()
root.geometry("500x500")
root.title("GAME")

rock = Button(root, text = "ROCK", height = 2, width = 7, fg ='black', bg = 'pink', font = ('bold',10), command = press)
rock.place(x = 80, y = 90)

paper = Button(root, text = "PAPER", height = 2, width = 7, fg ='black', bg = 'lightblue', font = ('bold',10), command = pap)
paper.place(x = 190, y = 90)

scissor = Button(root, text = "SCISSOR", height = 2, width = 7, fg ='black', bg = 'yellow', font = ('bold',10), command = sci)
scissor.place(x = 290, y = 90)

player = Label(root, text = "Your choice is:", font = ('bold', 13))
player.place(x =110, y =177)

comp = Label(root, text = "Computer Choice is:", font = ('bold', 13))
comp.place(x =110 , y =237)

status = Label(root, text = "STATUS:", font = ('bold', 13))
status.place(x =138 , y =300)

root.mainloop()

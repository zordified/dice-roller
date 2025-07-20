# dice-roller

import random
import tkinter as tk

root = tk.Tk()
root.geometry('500x400')

root.title("Dice Roller")


label= tk.Label(root, font=('helvetica', 250, 'bold'), text='\u2680')
label.pack()

def rolldice():
    dice = ['\u2680','\u2681','\u2682','\u2683','\u2684','\u2685']
    choice=random.choice(dice)
    label.config(text=choice)
    


button = tk.Button(root, font=('helvetica', 25, 'bold'), text='Roll Dice', command=rolldice)
button.pack(pady=20)

root.mainloop()

from tkinter import *
from time import strftime

root = Tk()
root.title("Clock")
label = Label(root, font=("Arial", 48), bg="black", fg="white")
label.pack()
def update():
    label.config(text=strftime("%H:%M:%S"))
    label.after(1000, update)
update()
root.mainloop()
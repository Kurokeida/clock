# clock

from tkinter import *
import time
from datetime import datetime
from playsound import playsound
import sys

def tick():
    time_string = time.strftime("%H:%M")
    clock.config(text = time_string)
    clock.after(200, tick)

root = Tk()
clock = Label(root, font = ("text", 100, "bold"),  bg = "white", foreground = "blue")
clock.grid(row = 0, column = 1)

alarm_time = "21:32"


while True:
    to_alarm = datetime.now().strftime('%H:%M')

    if to_alarm == alarm_time:
            print("Wake up")

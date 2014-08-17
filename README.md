#Text Based RPG
#11/08/2014
#Adrian Yong

import sys
import os
import random
import pickle
import tkinter


#TODO
#Make start on game
  #Make Intro work
  #Naming System for saves and loads
#Make a GUI so it is easily playable and aesthetically pleasing
#RNG




#Used for clearing Console
def clear():
  os.system('cls')

#Menu (Need to make a GUI for menu and game)
def mainMenu():
    print("------WELCOME TO THIS TEXT BASED RPG-------")
    print("Please Enter an option")
    print("1. New Game")
    print("2. Resume Most Recent Save")

    print("3. Load Save")
    print("4. Options")
    option = int(input())
    if option == 1:
        new = False
        while new == False:
          new = input("Save data may have been found, do you want to start again? (Enter Y or N)").upper
          if new == "Y":
            new == True
            print("gg no re")
          elif new == "N":
            new == True
            mainMenu()
          else:
             new = input("Try again, input not recognised (Enter Y or N)").upper
    elif option == 2:
        clear()
        print(">Game Loads Here<")
    elif option == 3:
        clear()
        print("-----------SAVE GAMES LIST-------------")
    elif option == 4:
        print("-------------OPTIONS-------------------")
    
if __name__=="__main__":
    mainMenu()


# ragnorr_coding.github.com
import random
def gameWin(com , you , chance):
    if (randNo == you ):
        return None 
    elif randNo == 's':
        if you == 'w':
            print("Snake drink the water")
            return False
        elif you == 'g':
            print("Gun Kill The Snake ")
            return True
    elif randNo == 'w':
        if you == 'g':
            print("Gun drwan in the water ")
            return False
        elif you == 's':
            print("Snake drink the water")
            return True
    elif randNo == 'g':
        if you == 's':
            print("Gun Kill The Snake ")
            return False
        elif you == 'w':
            print("Gun drwan in the water ")
            return True
print("----------------------------------------------------")   
print("Wlecome To (Snake , Water , Gun)  Game")
print("___________________________________________________") 
print("****************************************************") 
chance = int(input("How many round you want to play : "))
com = ["s" , "w" , "g"]
randNo = random.choice(com)
n1 = 0
n2 = 0
n3 = 0
n4 = 0
i = 1
while i <=chance:
    print("##################################################")
    print(f"Round {i} :")
    you = str(input("Player Turn : Snake (s) Water (w) Gun (g)\n "))
    if you in com:
        a = gameWin (com  , you , chance)
        if a == None:
            n1+=1
            print(f"Match is tie ")
        elif a == True:
            n2 += 1
            print(f"Congrats! You won the match ")
        elif a == False:
            n3 += 1
            print(f"Sorry! You losse ")
    else :
        n4 += 1
        print("Invalid Input")
    i = i+1
print("=====================================================")
print(f"You Played {chance} Times ")
print("=====================================================")
print("Match summary is : ")
print(f"\t\tMatch Tie {n1} Times ")
print(f"\t\tYou won {n2} Times ")
print(f"\t\tYou loose  {n3} Times \n")
print(":::::::::::::::::::::::::::::::::::::::::::")
print(f"Your score is {chance - (n3 + n1 + n4)} ")
com_score = (chance  - (n2 + n1 + n4))
print(f"Computer score is {com_score}")
print(">>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>")
win = (chance-(n3 + n1 + n4))
if (win < com_score): 
    print("||Your score is less than Computer|| ")
    print(">>>You lost The Match<<<")
    print("BETTER LUCK NEXT TIME")
elif(win == com_score):
    print("Match is Draw")
else:
    print("Congratulation! You won the Match ")
print("*******************************************************")

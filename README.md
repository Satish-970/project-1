# code for python cake dividing project:
'''this project will explain how a cake can be divided into  n equal pieces and pieces of any size and no two pieces are same when they are divided'''
import math
n=int(input("number of parts required:"))
ang=360/n
def Equalpieces(n):
    ''' this program will explain about that a cake can be divided into n equal pieces\
which was done by my group :simha,satish ,hari\
On the date :20-11-2022'''
    if n<=0:
        print("cutting is not possible")
    elif n%2 == 0 :
        print("cake can be cut into {} equal pieces with an angle of {}".format(n,"%.6f"%ang) + " degrees")
    else :
        print("cake can not be divided into odd number of pieces as we are drawing a straight line, which always divide evenly")
def Possibleways_of_AnySize(n):
    if n<=0:
        print("cutting in {} ways is not possible".format(n))
    elif n%2==0:
        a=math.factorial(n-1)
        x=a//2
        if x>0:
            print("cake can be cut into {} pieces is possible such that a piece can be of any size ".format(n))
        else:
            print("cake can not be divided in such a way because for {} pieces cake can divide in {} equal pieces".format(n,n))
    else:
        print("cake can not be divided into odd number of pieces as we are drawing a straight line, which always divide evenly")
def PossibleWays_NoTwoPiecesSame(n):
    if n<=0:
        print("cutting in {} ways is not possible".format(n))
    elif n%2==0:
        a=math.factorial(n-1)
        x=a//4
        if x>0:
            print("cake can be cut into {} pieces is possible such that no two of them are same".format(n))
        else:
            print("cake can not be divided in such a way because two pieces are equal")
    else:
        print("cake can not be divided into odd number of pieces as we are drawing a straight line , which always divide evenly")
        

Equalpieces(n)
Possibleways_of_AnySize(n)
PossibleWays_NoTwoPiecesSame(n)

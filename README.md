# projet-python
def Nim():
    from random import randint
    import sys
    from functools import reduce
    tas = [randint(1, 50), randint(1, 50), randint(1, 50),randint(1, 50)]

    print("Bienvenue au NIM!!")
    joueur1=input("entrez le nom de 1er joueur \n")
    joueur2=input("entrez le nom de 2eme joueur \n")

    print("Les tas sont {}" .format(tas))

    joueur = joueur1
    i=0;
    i=int(i)
    while True:
            i+=1
            print("le joueur ", joueur)
            while True:
                tass = input("choisir un tas\n")
                tass = int(tass)
            
            
                deplacement = input("quel est votre deplacement,choisir entre [1,2,3]\n")

                deplacement = int(deplacement)
            
                if tas[tass-1]>1 and  0 < deplacement  <= 3 :
                  

                      tas[tass-1] =tas[tass-1] - deplacement
                      print("Les tas maintenant contenir {}" .format(tas))
            
                  
                break
              
            if tas[tass-1] == 1 and i==1:
                print(" le joueur ", joueur, "a perdu")
                
                break
            elif tas[tass-1] == 1:
                print(" le joueur ", joueur, "a gagné")
                break
            if joueur == joueur1:
                joueur = joueur2
            else:
                joueur = joueur1
                
    n=1
    score=0
    while n<i+1:
       score=score+n*((10)**n )
       n=n+1
    print("le score de",joueur,"est",score)

    print("game over")
    rep =input("faire une autre partie?[1/0]\n")
    if rep == '1' :
        Nim()
    else :
        print("see you next time")
Nim()

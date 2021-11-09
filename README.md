# LCG
a = 1140
c = 1282
m = 2**24
import datetime
import time
# Function inside theres a loop that runs 50 times
def lcg():
    answer = str(input("Enter U for user input or Enter A for system time:"))
    if answer ==  'u' :
        while True:
            seed = int(input("Enter a seed:"))
            for i in range(50) :
                seed = (a*seed + c) % m
                print(seed)
            else:
                break
        
    if answer ==  'a' :
                    while True:
                        seed = int(datetime.datetime.now().strftime("%S"))
                        for i in range(50) :
                            seed = (a*seed + c) % m
                            print(seed)
                        else: 
                            break
lcg()

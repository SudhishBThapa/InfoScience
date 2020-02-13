# Dice modification program #


```.py

#These variables are to count the rolls of thhe dice 
ones = 0
twos = 0
threes = 0
fours = 0
fives = 0
sixes = 0

def setup():
    size (600,600)
    background (255)
    
    
    
def draw():
    x=0
    delay(14)
    mouseClick()
    bargraph()
    
def bargraph():
    global ones,twos,threes,fours,fives,sixes
    fill(0)
    textSize(20)
    for x in range (6):
        text(x+1,50+50*x,590)
    
    rect(50,550 - ones, 15, ones)
    fill(10,20,0)
    rect(100,550 - twos,15,twos)
    stroke(125)
    rect(150,550 - threes,15,threes)
    stroke(50)
    rect(200,550 - fours,15,fours)
    stroke(45)
    rect(250,550 - fives,15,fives)
    stroke(25)
    rect(300,550 - sixes,15,sixes)
    stroke(5,45,10)
    
def mouseClick():
    global ones, twos, threes, fours, fives, sixes
    background(255)
    stroke(0)
    fill(250)
    rect(100,100, 400, 400, 10)
    stroke(255,0,0)
    strokeWeight(10)

    
    
    n=random(0,6)
    print(n)
    if 0<=n<0.5:
        circle(300,300,50)
        ones = ones + 1
        print ("Number of times one has been rolled: ", ones)
    if 0.5<=n<1.0:
        circle(200,200,50)
        circle(400,400,50)
        twos = twos + 1
        print ("Number of times two has been rolled: ", twos)
    if 1.0<=n<1.5:
        circle(200,200,50)
        circle(400,400,50)
        circle(300,300,50)
        threes = threes + 1
        print ("Number of times three has been rolled: ", threes)
    if 1.5<=n<2.0: 
        circle(200,200,50)
        circle(400,200,50)
        circle(200,400,50)
        circle(400,400,50)
        fours = fours + 1
        print ("Number of times four has been rolled: ", fours)
    if 2.0<=n<2.5:
        circle(200,200,50)
        circle(400,200,50)
        circle(200,400,50)
        circle(400,400,50)
        circle(300,300,50)
        fives = fives + 1
        print ("Number of times five has been rolled: ", fives)
    if 2.5<=n<3.1:
        circle(200,200,50)
        circle(400,200,50)
        circle(200,400,50)
        circle(400,400,50)
        circle(200,300,50)
        circle(400,300,50)
        sixes = sixes + 1 
        print ("Number of times six has been rolled: ", sixes)
```        
        
What did we do = We added modifications to our previous dice program such as adding a counter that counts the amount of times a number pops
up in the dice and we gave it a visual representation as well. We learned how to use the 'for loop' loop structure to make our process 
simpler because we don't repeat ourselves. We also modified the position of the mouseclick() function so that the dice rolls by itself without
manual control.
What did you learn = I learned on the functionality of the 'for loop' loop structure and how to give variables function by using global to include
those variables that are not in the setup block of the program. I also learned how to create bargraphs and customize them.
What questions do I have = I have questions regarding the 'if loop' structure and in what contexts it can be used for. 
        

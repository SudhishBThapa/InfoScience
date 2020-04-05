# 1) What are some ways in which Computer Science can help the fight against Covid-19? In your opinion, should people enable access to the resources of their personal computers as tools for research? Are there any risks?#

 The behavior of Covid-19 needs to be properly observed in order to find a way to combat the virus itself. Trying to find vulnerabilities of 
the virus will then lead us to a cure. However, the issue currently is that techniques such as X-ray crystallography and cryo-electron microscopy
have not allowed us to observe the virus' behavior. So 3D simulations are the next option to observe the virus. This is where computer science and
computing itself is important to fight against Covid-19. In my opinion people should enable access to their PCs as tools for research because of the situation we are in. At this point, I feel like any measures should be taken given how desperate the situation of fighting
the virus is getting. The only risk that I see happening is the people's opinions in terms of whether they want to give up their computers for research purposes. 

```.py

3) #Code for individual -
 # definition of variables
posx = 300;
posy = 300;
 
def setup():
     size (500,500)
def draw():
    global posx, posy
    background(255)
    strokeWeight(2)
    
    #create individual
    circle(posx, posy, 40)
    posx = posx + random(-10, 10)
    posy = posy + random(-10, 10)
    
    # boundaries conditions
    if posx > 500:
        posx = 500;
    if posy > 500:
        posy = 500;
    if posy < 0:
        posy = 0;
    if posx < 0:
        posx = 0;
   
    delay(100)
 ```        
     
4) #Code for Community of 10 people -
```.py
# definition of variables
x = []
y = []
 
def setup():
    size (500,500)
    for i in range (10):
        x.append(random(0,500))
        y.append(random(0,500))
     
     
def draw():
    global x, y
    background(255)
    strokeWeight(2)
    
    #create first individual
    for i in range(10):
        circle(x[i], y[i], 40)
        x[i] = x[i] + random(-10, 10)
        y[i] = y[i] + random(-10, 10)
    
    # boundaries conditions
    if x[i] > 500:
        x[i] = 500
    if y [i] > 500:
        y[i] = 500
    if y[i] < 0:
        y[i] = 0;
    if x[i] < 0:
        x[i] = 0;

delay(100)
```        

5) #What should be some behaviours (at least 3) that we will need to include in our simulation to be a realistic approximation of the current situation in the world? Explain.

= Some behaviors would be to simulate a realistic approximation is the factor that people go inside and out of different communities. Thus, it is important to show that inside a locked community, the virus doesn't spread but a person who goes out and back in has a higher chance of spreading the virus. The other behavior is to show that each individual in the community passes the virus on one by one. Whether we can include this in the program by giving an infected individual a color and showing that overtime every individual has
the color (the virus). The final behavior that I think would give a realistic approximation is also show the passing of the virus through physical interaction. The circles should interact with each other and then switch color to indicate the passing of the virus.

#What did we do?
= We tried to create a simulation of the virus and how it spreads in a community through physical shapes like circles and used lists and loop structure to automate the process.

#What did you learn?
= I learned how to use the random function to assign random values to a list from a certain range.

#What questions do I have?
= I wonder if I can create a program where one circle has the virus (indicated by a color) and upon interaction it changes color of another circle to indicate that its been passed on.

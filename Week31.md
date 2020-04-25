
# Solution for Week 31 
```.py
# definition of variables
x = []
y= []
person = ["Sick", "Healthy"] #Sick=>infected
il = 0
h = 25
rec = 0
c = 0
bar = 0
days = [30, -1]

def setup():
    size(500,500)
    for n in range (25):
        x.append(random(0, 500))
        person.append("Healthy") #All Healthy
        y.append(random(0, 500))
        days.append(30)
        barGraph()
        

        
def distance(x1, x2, y1, y2):
    a = (x1 - x2)
    b = (y1 - y2)
    c = sqrt(a**2 + b**2)
    return c


    
    
def draw():
    global x, y, il, h, c, l, days, rec
    background(255)
    strokeWeight(2)
    barGraph()
    c += 1
    if il == 25:
        c -= 1


    
    #create 1st individual
    for i in range(len(x)):
        if person[i] == "Healthy":
            fill(255) #healthy
        elif person[i] == "Recovered":
            fill(0,255,255)
        else:
            fill (0, 200, 0) #infected
                
        if person[i] == "Sick":
            days[i] -= 1
            if days[i] == 0:
                person[i] = "Recovered"

            
            
        circle(x[i], y[i], 40)
        
        x[i] = x[i] + random(-10, 10)
        y[i] = y[i] + random(-10, 10)

        
        for g in range(len(x)):
            if g == i:
                continue
            d = distance(x[i], x[g], y[i], y[g])
            if d < 40 and (person[g] == "Sick" or person[i]== "Sick"):
                if person[i] == "Healthy":
                    #infection happens
                    person[i] = "Sick"
                    days[i] = 30
                if person[g] == "Healthy":        
                    person[g] = "Sick"
                    days[g] = 30

        
        #boundaries conditions
        if x[i] > 500:
            x[i] = 500
    
        # add three more extentions
        
        if x[i] < 0:
            x[i] = 0
            
        if y[i] > 500:
            y[i] = 500
    
        if y[i] < 0:
            y[i] = 0
            
            

            
    il = 0
    h = 0
    rec = 0
    for bar in range (len(x)):
        if person[bar] == "Sick":
            il += 1
        elif person[bar] == "Healthy":
            h += 1
        elif person[bar] == "Recovered":
            rec += 1

            

            
            
    textSize(10)
    fill(0)
    text("Infected", 445, 478)
    text("Healthy", 445, 458)
    text ("Recovered", 445, 496)
    text (c, 80, 470)
    text("Iteration #:", 20, 470)

            
    

def barGraph():
    strokeWeight(1)
    stroke(0)
    fill(255, 0, 0)
    rect (440, 469, -il*2, 8)
    fill (255)
    rect (440, 450, -h*2, 8)
    fill (0, 255, 255)
    rect (440, 488, -rec*2,8)
    ```

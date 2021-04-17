# day18-project-start
## 5 challenges to use the Python library called Turtle. Using classes and objects.
- Challenge 1: Make a square
```
for _ in range(4):
    turtle.forward(100)
    turtle.right(90)
```
- Challenge 2: Draw a dashed line (50 times)
```
for _ in range(15):
    turtle.forward(10)
    turtle.penup()
    turtle.forward(10)
    turtle.pendown()

```
- Challenge 3: Draw a triangle, square, pentagon, hexagon, heptagon, octagon, nonagon, and decagon
```
# Hint: 360 deg divided by how many lines
def draw_stuff(lines):
    for _ in range(lines):
        turtle.forward(100)
        turtle.left(360 / lines)
# Give some color;
color = ["red", "blue", "green", "yellow", "dark slate gray", "medium slate blue", "peach puff"]
lines = 3
for _ in range(12):
    turtle.pencolor(random.choice(color))
    draw_stuff(lines)
    lines += 1        
```
- Challenge 4: Create a random walk
```
# Randomly go left, right, up, down

def turning_east(steps):
    turtle.forward(steps)
    turtle.setheading(0)


def turning_north(steps):
    turtle.forward(steps)
    turtle.setheading(90)


def turning_west(steps):
    turtle.forward(steps)
    turtle.setheading(180)


def turning_south(steps):
    turtle.forward(steps)
    turtle.setheading(270)

def random_color():
    r = random.randint(0, 255)
    g = random.randint(0, 255)
    b = random.randint(0, 255)
    rgb = (r, g, b)
    return rgb
    
# Part of Challenge 4 Let's speed up the turtle!
turtle.speed("fastest")

# And make the line thicker
turtle.pensize(10)

# Set the same steps for now
steps = 20

# Choose a direction randomly
direction = [turning_south, turning_west, turning_east, turning_north]

# Choose a random color
screen.colormode(255)

# Move it around
for _ in range (1000):
    rgb = random_color()
    turtle.pencolor(rgb)
    random.choice(direction)(steps)

```
- Challenge 5: Make a spirograph
```
# Challenge 5: Make a spirograph

turtle.speed("fastest")
def draw_spirograph(gaps):
    for _ in range(int(360/gaps)):
        rgb = random_color()
        turtle.pencolor(rgb)
        turtle.circle(100) # Draw a circle with radius of 100
        turtle.setheading(turtle.heading() + gaps)

draw_spirograph(5)
```

# Key Takeaways
The main lesson was: How to use a Python library. 

I struggled, searched things, and looked up Stackoverflow. 

It took another day to complete Day 18 lessons, but in the end, it was so worth it!

Slow down. Do it everyday one at a time.

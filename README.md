# WASD-to-drawl
import turtle 
import os
wn = turtle.Screen()
wn.title("Drawl")
wn.bgcolor("green")
wn.setup(width=800, height=600)
wn.tracer(0)

p_a = turtle.Turtle()
p_a.speed(0)
p_a.shape("square")
p_a.color("white")
p_a.penup()
p_a.goto(0, 0)

def p_a_up():
    y = p_a.ycor()
    y += 20
    p_a.sety(y)
    
def p_a_down():
    y = p_a.ycor()
    y -= 20
    p_a.sety(y)

def p_a_right():
    x = p_a.xcor()
    x -= 20
    p_a.setx(x)

def p_a_left():
    x = p_a.xcor()
    x += 20
    p_a.setx(x)
    if x < -280:
        x = - 280
    
wn.listen()
wn.onkeypress(p_a_up, "w")

wn.listen()
wn.onkeypress(p_a_down, "s")

wn.listen()
wn.onkeypress(p_a_right, "a")

wn.listen
wn.onkeypress(p_a_left, "d")







while True:
    wn.update()

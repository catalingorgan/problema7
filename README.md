import math

a = input("Dati lungimea primei laturi: ")
b = input("Dati lungimea primei laturi: ")
c = input("Dati lungimea primei laturi: ")

a = float(a)
b = float(b)
c = float(c)

if a < b+c and b < a+c and c < a+b:
    p = (a+b+c)/2
    aria = math.sqrt(p*(p-a)*(p-b)*(p-c))
    print("Aria triunghiului este: " + str(aria))
    var = 2*aria
    h1 = round(var/b, 2)
    h2 = round(var/c, 2)
    h3 = round(var/a, 2)
    var1 = round(c*a/b, 2)
    var2 = round(b*a/c, 2)
    var3 = round(c*b/a, 2)
    print("Cele trei inaltimi sunt: "+str(h1)+" "+str(h2)+" "+str(h3))
    if a == b == c:
        print("Trunghiul este echilateral")
    elif h1 == var1:
        if h1 == round(b/2, 2):
            print("Triunghi dreptunghic isoscel")
        else:
            print("Triunghi dreptunghic")
    elif h2 == var2:
        if h2 == round(c/2, 2):
            print("Triunghi dreptunghic isoscel")
        else:
            print("Triunghi dreptunghic")
    elif h3 == var3:
        if h3 == round(a/2, 2):
             print("Triunghi dreptunghic isoscel")
        else:
            print("Triunghi dreptunghic")
    elif a != b and a != c and b != c:
        print("Triunghi oarecare")
    elif a == b or a == c or b == c:
        print("Triunghiul este isoscel")
else:
    print("Din lungimile date nu se poate construi un triunghi")

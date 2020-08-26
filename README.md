# hackerrank-python-practice-test
#hackerrank python practice problem for finding area of rectangle and circle upto  exact two decimal places 

def Rectangle(a,b):
    area=a*b
    print("{:.2f}".format(area))
    return area;
def Circle(r):
    pi=3.14
    area=pi*(r**2)
    print("{:.2f}".format(area))
    return area;
q = int(input())
queries = []
for _ in range(q):
    args = input().split()
    shape_name, params = args[0], tuple(map(int, args[1:]))
    if shape_name == "rectangle":
        a, b = params[0], params[1]
        shape = Rectangle(a, b)
    elif shape_name == "circle":
        r = params[0]
        shape = Circle(r)
    else:
        raise ValueError("invalid shape")

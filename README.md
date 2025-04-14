# file-handling
file1=open("MonthNames.py",'r')
print(file1.read())
print(file1.read(5))
print(file1.readlines())
print(file1.readline())



file2=open("MonthNames.py",'r')
print(file2.read())
file3=open("pythonfunctions.py","w")
file3.write("c=good morning")
for line in file2:
    file3.write(line)
file3=open("pythonfunctions.py","r")
print(file3.read())


countwords=0
with open("pythonfunctions.py","r") as file2:
 for line in file2:
    words=line.split()
    countwords+=len(words)
    print(countwords)


string = "abcd"
try:
    string_int = int(string)
    print(string_int)
except ValueError:
    print('Please enter an integer')



a = list(input("Enter numbers: ").split(','))

try:
     for i in a:
         if int(i)<0:
             print('value cant be negative')
except:
    print(a)





a = list(input("Enter numbers: ").split(','))

numbers=[]
for i in a:
    try:
        numbers.append(int(i))
    except:
        print('enter valid number')
print(numbers)

b=sum(numbers)/len(numbers)
print(b)




a = input("Enter file name ")
c=input("Enter a string ")
try:
        f = open(a, 'r')
        f.read()
        l = open(a, 'w')
        l.write(c)
except:
        print('Error occurred when opening',a, 'to read')
finally:
        print('welcome')

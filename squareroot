
def convert_tobinary(n1,count1):
    n1=bin(int(n1))
    n2=list(n1)
    n3,n4=''.join(n2),''.join(n2[2:])
    con=0
    if len(n4)<count1:
        con=count1-len(n4)

    for i in range(0,con):
        n4='0'+n4

    return n3,n4
    
def validate_no(n):
    length=len(n)
    if length%2==0:
        n1=n
    else:
        n1='0'+n
    return n1
           
def convert_toint(binary): 
      
    binary1 = binary 
    decimal, i, n = 0, 0, 0
    while(binary != 0): 
        dec = int(binary) % 10
        decimal = decimal + dec * pow(2, i) 
        binary = int(binary)//10
        i = i+ 1
    return decimal         

def subtrahend(answerlist,q):
    answerlist=str(q)+answerlist
    if len(answerlist)%2!=0:
        answerlist='0'+answerlist

    print("q:",q)
    print("subtrahend:",answerlist)
    return answerlist

def process(answerlist,qarray):
    answerlist=''.join(qarray)+'01'
    return answerlist


def perfectsqroot(remainder):
    if convert_toint(remainder)!=0:
        print("The no. you entered is not a perfect square root")
    
    
print("Enter the Number:")
n=str(input())
con_n,n1=convert_tobinary(n,0)
n2=validate_no(n1)
rem=0
qarray=[]
q=1
print("The no. you entered",n)
print("The binary number of it",n1)
print("The validated from of it",n2)
lengthn2=len(n2)
answerlist=str('01')
u=0

for i in range(2,len(n2)+1,2):
    print('----iteration no:',u,'------')
    up=convert_toint(n2[0:i])
    down=convert_toint(answerlist)
    print("up:",up)
    print("down:",down)

    if up-down>=0:
        q='1'

        qarray.append('1')
        rem1,rem=convert_tobinary(up-down,i)
        print("remainder:",rem)
        answerlist=subtrahend(answerlist,q)
        n2=rem+n2[len(rem):lengthn2]
        print ("number:",n2)
        
    else:
        q='0'
        rem=up
        answerlist=subtrahend(answerlist,q)
        qarray.append('0')
        print ("number:",n2)

    remainder=rem
    answerlist=process(answerlist,qarray)
    rem=''
    u=u+1


    
print("-------------------FINAL RESULT-------------------------------")
print("qarray:",qarray)
print("final remainder:",remainder)
perfectsqroot(remainder)
print("square root of",n,"is",convert_toint("".join(qarray)))
print("---------------------------------------------------")

    





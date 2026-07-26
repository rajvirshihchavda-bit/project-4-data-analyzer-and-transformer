print("="*60)
print("WELCOME TO THE DATA ANALZER AND TRANSFORMER PROGRAM ")
print("="*60)
print('main manu:''\n'
      "1. input data." "\n"
      "2. display data summary." "\n"
      "3. calculate factorial." "\n"
      "4. filter data by threshold." "\n"
      "5. sort data." "\n"
      "6. display dataset statisitcs." "\n"
      "7. exit program." "\n",
      "-"*60
      ) 
while True:
  choice=int(input('pleas enter your choice : '))
  match choice:
    case 1:
      print('enter data for a 1D array:')
      a = []
      size = int(input("Ketli value add karvi che? : "))
      for i in range(size):
            value = int(input("Enter Number : "))
            a.append(value)
      print(*a)
    case 2:
        print('data summary:''\n',"total element:",len(a), "\n", "minimume number :",min(a),"\n","maximum number:",max(a),"\n","sum of all value:",sum(a))
        def average(a):
             '''
             jo koy 1D array ma int value hoy to teno total kari ane len thi divide kariye to average male.
             '''
             a=sum(a)/len(a)
             return a    
        print("average of element:",average(a))
    case 3:
          b=int(input("enter the no."))
          def fectorila(a):
                '''
                koy pan no. na fectorila melava mate aa function no use thay 
                '''
                fac=1
                for i in range(1,a+1):
                    fac=fac*i
                return fac
          c=fectorila(b)
          print(c)
    case 4:
          num = int(input("Enter Number : "))

          greater = filter(lambda x: x > num, a)

          for i in greater:
           print(i)

    case 5:
          print("1. ascending order","\n","2. descending order")
          select=int(input('enter the no.'))
          match select:
              case 1:
                  print('ascending order:',a.sort(),a)
              case 2:
                  print("descending order :",a.sort(reverse=True),a)
    case 6:
       print('data summary:''\n',"total element:",len(a), "\n", "minimume number :",min(a),"\n","maximum number:",max(a),"\n","sum of all value:",sum(a))
       def average(a):
             '''
             jo koy 1D array ma int value hoy to teno total kari ane len thi divide kariye to average male.
             '''
             a=sum(a)/len(a)
             return a    
       print("average of element:",average(a))
    case 7:
          print('thank you for using the data analyzer and transformer program.',"\n","Good by")
          break
    case _:
          print('envalid choice')


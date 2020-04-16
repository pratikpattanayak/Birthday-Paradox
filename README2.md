# Birthday-Paradox
This program will predict your birthday twin
import random
import datetime
birthday=[]
i=0
while(i<50):
     year=random.randint(1895,2017)
#the oldest person ever lived was 122 years old
     if (year%4==0 and year%100!=0 or year%400==0):  #if the year is a leap year or not
         leap=1
     else:
         leap=0
     month=random.randint(1,12)
     if(month==2 and leap==1):  # if the month is february and the year is a leap year
         day=random.randint(1,29)
     elif(month==2 and leap==0):
         day=random.randint(1,28)
     elif(month==7 or month==8):  #if the month is July or August
         day=random.randint(1,31)
     elif(month%2!=0 and month<7):
         day=random.randint(1,31)
     elif(month%2==0 and month>7):
        day= random.randint(1,31) 
     else:
         day=random.randint(1,30)    
     dd=datetime.date(year,month,day)
     day_of_year=dd.timetuple().tm_yday
     i=i+1
     birthday.append(day_of_year)
birthday.sort()
i=0
while(i<50) :
 print(birthday[i])
 i=i+1
 
             

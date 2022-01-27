# Python_problems

'''
##basic question set_1
#1. Write a Python program to print the following string in a specific format
# o/p -
# Twinkle, twinkle, little star,
# 	How I wonder what you are!
# 		Up above the world so high,
# 		Like a diamond in the sky.
# Twinkle, twinkle, little star,
# 	How I wonder what you are

#sol:
print('Twinkle, twinkle, little star, \n\tHow i wounder What you are!  \n\t\tUp above the world so high, \n\t\tLike a diamound in the sky.\nTwinkle, twinkle, little star, \n\tHow i wounder What u are! ')
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

#2. Write a Python program to get the Python version you are using.
#sol:
import platform
print(platform.python_version())
print(type(platform.python_version()))
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

#3. Write a Python program to display the current date and time.
#sol:
import datetime
now = datetime.datetime.now()
print('current date and time: ')
print(now.strftime('%y-%m-%d %H:%M:%S'))
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

#4. Write a Python program which accepts the radius of a circle from the user and compute the area.
#sol:
from math import pi
r =float(input('enter ur radius of circle:'))
print('The area of circle with radius is:'+str(pi*r**2))
-----------------------------------------------------------------------------------------------------------------------------------------------

#5. Write a Python program which accepts the user's first and last name and
# print them in reverse order with a space between them
#sol:
fname = input('your first name: ')
lname = input('your last name: ')
print('Hello '+lname+" "+fname)
--------------------------------------------------------------------------------------------------------------------------------------------------

#6. Write a Python program which accepts a sequence of comma-separated
# numbers from user and generate a list and a tuple with those numbers.
#sol:
values = input('enter some comma-seperated values: ')
list  = values.split(",")
tuple = tuple(list)
print('list: ',list)
print('tuple: ',tuple)
----------------------------------------------------------------------------------------------------------

#7. Write a Python program to accept a filename from the user and print the extension of that.
#Sample filename : abc.java
#Output : java
#sol:
filename = input('enter file name: ')
f = filename.split('.')
print('the extension of file is: '+repr(f[-1]))
----------------------------------------------------------------------------

#8. Write a Python program to display the first and last colors from the following list.
#color_list = ["Red","Green","White" ,"Black"]
#sol:
color_list = ["Red","Green","White" ,"Black"]
print('%s %s'%(color_list[0],color_list[-1]))
-------------------------------------------------------------------------------------------

#9. Write a Python program to display the examination schedule.
# (extract the date from exam_st_date).
#exam_st_date = (11, 12, 2014)
#Sample Output : The examination will start from : 11 / 12 / 2014
#sol:
exam_st_date = (11, 12, 2014)
print('%i / %i / %i'%exam_st_date)
----------------------------------------------------------------------------

#10. Write a Python program that accepts an integer (n) and computes the value of n+nn+nnn
#Sample value of n is 5
#Expected Result : 615
#sol:
a = int(input('enter an integer: '))
n1 = int('%s' % a)
n2 = int('%s%s' % (a,a))
n3 = int('%s%s%s' % (a,a,a))
print(n1+n2+n3)
--------------------------------------------------------------------------------------------

#11. Write a Python program to print the documents (syntax, description etc.) of Python built-in function(s).
#Sample function : abs()
#Expected Result :
# abs(number) -> number
# Return the absolute value of the argument.
#sol:
print(abs.__doc__)
-------------------------------------------------------------------------------------------------------------

#12. Write a Python program to print the calendar of a given month and year.
#Note : Use 'calendar' module.
#sol:
import calendar
y = int(input('enter year: '))
m = int(input('enter month: '))
print(calendar.month(y,m))


#13. Write a Python program to print the following 'here document'.
#Sample string:
#a string that you "don't" have to escape
#This
#is a ....... multi-line
#heredoc string --------> example

#sol:
print("""
a string that "don't" have to escape
this
is a ....... multi-line
heredoc string  -----------> example
""")

------------------------------------------------------------------------------------------------------

#14. Write a Python program to calculate number of days between two dates.
# Sample dates : (2014, 7, 2), (2014, 7, 11)
# Expected output : 9 days
#sol:
from datetime import date
dt1 = date(2014, 7, 2)
dt2 = date(2014, 7, 11)
delta = dt2 - dt1
print(delta.days)

------------------------------------------------------------------------------------------------------------


#15. Write a Python program to get the volume of a sphere with radius 6
# v = pi * d 3/6
#sol:
pi = 3.14
r = 6.0
v = 4.0/3.0*pi*r**3
print('the volume of the spher is : ',v)

----------------------------------------------------------------------------------------

#16. Write a Python program to get the difference between
# a given number and 17, if the number is greater than 17
#return double the absolute difference
#sol:
def difference(n):
    if n<=17:
        return 17-n
    else:
        return(n-14)*2
print(difference(55))
print(difference(10))

--------------------------------------------------------------------------------------------------------

#17. Write a Python program to test
# whether a number is within 100 of 1000 or 2000.
#sol:
def near_thousand(n):
    return((abs(1000-n)<=100) or (abs(2000-n)<=100))
print(near_thousand(1000))
print(near_thousand(545))
print(near_thousand(888))
print(near_thousand(220))

----------------------------------------------------------------------------------

#18. Write a Python program to calculate the sum of three given numbers,
# if the values are equal then return three times of their sum.
#sol:
def sum_three (x, y, z):
    sum = x + y + z

    if x == y == z:
        sum = sum * 3
        return sum

print(sum_three(1, 2, 3))
print(sum_three(5, 5, 5))

-----------------------------------------------------------------------------------

#19. Write a Python program to get a new string from a given string
# where "Is" has been added to the front. If the given string already
# begins with "Is" then return the string unchanged.
#sol:
def new_str(str):
    if len(str) >= 2 and str[:2] == "Is":
        return str #if in str 'Is' is present at start then dont add 'Is' just let it be and print
    return 'Is'+str #if in str 'Is' is not present the go for it add and print it

print(new_str('array'))
print(new_str('Isdude'))

-----------------------------------------------------------------------------------------------------------

#20. Write a Python program to get a string which is n (non-negative integer) copies of a given string
#sol:
def large_string(str, n):
    result = ""
    for i in range(n):
        result = result + str
    return result

print(large_string("abc", 9))
print(large_string(".py", 5))

-----------------------------------------------------------------------------------------------------------------

#21. Write a Python program to find whether a given number (accept from the user) is even or odd,
# print out an appropriate message to the user.
#sol:
num = int(input('enter number'))
m = num % 2
if m > 0:
    print('this is an odd number')
else:
    print('this is an even number')

------------------------------------------------------------------------------------------------------------

#22. Write a Python program to count the number 4 in a given list.
#sol:
def lis_count_4(nums):
    #using naive method
    #to get count of 4 in list
    count = 0
    for num in nums:
        if num == 4:
            count = count +1

    return count

print(lis_count_4([1,2,4,5,4,6,8,4,7,9,5,2,15,3,2]))

--------------------------------------------------------------------------------------------

#23. Write a Python program to get the n (non-negative integer)
# copies of the first 2 characters of a given string.
# Return the n copies of the whole string if the length is less than 2
#sol:
def substring_copies(str,n):
    flen = 2
    if flen > len(str):
        flen = len(str)
    substr = str[:flen]

    result = ""
    for i in range(n):
        result = result + substr
    return result
print(substring_copies('abcdefsh', 2))
print(substring_copies('p', 6))

-------------------------------------------------------------------------------------

#24. Write a Python program to test whether a passed letter is a vowel or not.
#sol:
def vowel (char):
    all_vowels = 'aeiou'
    return char in all_vowels
print(vowel('c'))
print(vowel('a'))

----------------------------------------------------------------------------------------

#25. Write a Python program to
# check whether a specified value is contained in a group of values.
#Test Data :
# 3 -> [1, 5, 8, 3] : True
# -1 -> [1, 5, 8, 3] : False
#sol:
def grp_data(gdata, n):
    for value in gdata:
        if n == value:
            return True
    return False
print(grp_data([1,54,6,3], 3))
print(grp_data([-2,-5,-4,-8,-11], -1))

-------------------------------------------------------------------------------------------------


'''















































































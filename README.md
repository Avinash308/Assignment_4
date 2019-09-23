# Assignment_4
# problem statement Find the area of triangle
#Write a Python Program(with class concepts) to find the area of the triangle using the below formula.
#area = (s*(s-a)*(s-b)*(s-c)) ** 0.5#

#code:

class Triangle:
 def __init__(self, side1, side2, side3):
  self.side1 = side1
  self.side2 = side2
  self.side3 = side3
  print ("Initialised Triagle super class [" +  str(side1) + "," + str(side2) + "," + str(side3) + "]")

class Triangle_Utilities(Triangle):
 
 def __init__(self, side1, side2, side3):
  print ("Initialised Utils Child class" )
  super(Triangle_Utilities, self).__init__(side1, side2, side3)

 def get_area(self):
  s = (self.side1 + self.side2 + self.side3)/2
  print (str(s))
  return (s*(s-self.side1)*(s-self.side2)*(s-self.side3))**0.5

instance = Triangle_Utilities(3,4,5)
print ("Area of triangle = " + str(instance.get_area()) )

# Problem statement 2 
# Write a function filter_long_words() that takes a list of words and an integer n and returns
# the list of words that are longer than n.

def list_of_words(n,string):
    words = []
    txt = string.split(" ")
    for x in txt:
        if len(x)>n:
            words.append(x)
    return words
    
print(list_of_words(3, "av aja amber alex"))

# problem statemnet 3
#2.1 Write a Python program using function concept that maps list of words into a list of integers
representing the lengths of the corresponding words.

ddef list_of_words(words):
    output = []
    for x in words:
        output.append(len(x))
    return output
words = ['abv', 'try me', 'test']    
print(list_of_words(words))

# problem statement 4
# Write a Python function which takes a character (i.e. a string of length 1) and returns True if
# it is a vowel, False otherwise

def is_vowel(aset):
    all_vowels = "aeiou"
    return aset in all_vowels
print(is_vowel('c'))
print(is_vowel('e'))




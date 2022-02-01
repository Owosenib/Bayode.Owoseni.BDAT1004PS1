QUESTION 1

What data type is each of the following?

5	
5.0	
5 > 1	
'5'	
5 * 2	
'5' * 2	
'5' + '2'	
5 / 2	
5% 2	
{5, 2, 1}	
5== 3	
Pi(the number)	

QUESTION 1 SOLUTION

5 = integer

5.0  = float

5 > 1 = boolean

'5' = string

5 * 2 = integer

'5' * 2 = string

'5' + '2' = string

5 / 2 = float

5% 2 integer

{5, 2, 1} = integer

5== 3 = boolean

Pi(the number) = float




QUESTION 2a, 2b , 2c

Write (and evaluate) C# expressions that answer these questions:

How many letters are there in 'Supercalifragilisticexpialidocious'?
Does 'Supercalifragilisticexpialidocious' contain 'ice' as a substring?
Which of the following words is the longest: Supercalifragilisticexpialidocious, Honorificabilitudinitatibus, or Bababadalgharaghtakamminarronnkonn?
Which composer comes first in the dictionary: 'Berlioz', 'Borodin', 'Brian', 'Bartok', 'Bellini', 'Buxtehude', 'Bernstein'. Which one comes last?

QUESTION 2a, 2b , 2c SOLUTION

using System;

namespace MyApp
{
    internal class Program
    {
        static void Main(string[] args)
        {
            var word = "Supercalifragilisticexpialidocious";                                                  
            var length = word.Length;                                                                    
            Console.WriteLine("The number of characters in Supercalifragilisticexpialidocious are " + length);
            var result = word.Contains("ice");                  
            Console.WriteLine("Does Supercalifragilisticexpialidocious contains ice:" + result);
            var word2 = "Honorificabilitudinitatibus";          
            var word3 = "Bababadalgharaghtakamminarronnkonn";   
            var length2 = word2.Length;                       
            var length3 = word3.Length;                          
            if (length > length2)                                
            {
                if (length > length3)
                {
                    Console.WriteLine(word + " is longest among " + word + " " + word2 + " " + word3);
                }
                else if (length < length3)
                {
                    Console.WriteLine(word3 + " is longest among " + word + " " + word2 + " " + word3);
                }
                else
                {
                    Console.WriteLine(word3 + " and " + word + " are longest among " + word + " " + word2 + " " + word3);
                }
            }
            else if (length < length2)
            {
                if (length2 > length3)
                {
                    Console.WriteLine(word2 + " is longest among " + word + " " + word2 + " " + word3);
                }
                else if (length2 < length3)
                {
                    Console.WriteLine(word3 + " is longest among " + word + " " + word2 + " " + word3);
                }
                else
                {
                    Console.WriteLine(word2 + " and " + word3 + " are longest among " + word + " " + word2 + " " + word3);
                }

            }
            else
            {
                if (length > length3)
                {
                    Console.WriteLine(word + " and " + word2 + " are longest among " + word + " " + word2 + " " + word3);
                }
                else if (length < length3)
                {
                    Console.WriteLine(word3 + " is longest among " + word + " " + word2 + " " + word3);
                }
                else
                {
                    Console.WriteLine("All three are equal in length");
                }
            }
            string[] composers = { "Berlioz", "Borodin", "Brian", "Bartok", "Bellini", "Buxtehude", "Bernstein" };
            Array.Sort(composers);                                                                               
            Console.WriteLine("The first composer in dictionary is " + composers[0]);                              
            Console.WriteLine("The last composer in dictionary is " + composers[composers.Length - 1]);  //                                                                                                                                                                                        composer[composers.Length-1]



        }
    }


}



QUESTION 3

Implement function triangleArea(a,b,c) that takes as input the lengths of the 3 sides of a triangle and returns the area of the triangle. By Heron's formula, the area of a triangle with side lengths a, b, and c is , where .

  s(s-a)(s-b)(s-c)
  s=(a+b+c)/2
>>> triangleArea(2,2,2)

1.7320508075688772



QUESTION 3 SOLUTION

using System;

using System.Text;

namespace AreaTriangle
{
    class program
    {
        static void Main(string[] args)
        { //program to find Area of a Triangle = (a+b+c)/2
            double a, b, c;
            double area, s;
            Console.Write("Enter the value of a ===)  ");
            a = double.Parse(Console.ReadLine());
            Console.Write("Enter the value of b ===)  ");
            b = double.Parse(Console.ReadLine());
            Console.Write("Enter the value of c ===)  ");
            c = double.Parse(Console.ReadLine());

            s = (a + b + c) / 2;
            area = Math.Sqrt(s * (s - a) * (s - b) * (s - c));
            Console.WriteLine("The Area of a triangle is " + area);
            Console.ReadLine();



        }

    }
}


QUESTION 4


Write a program in C# Sharp to separate odd and even integers in separate arrays. Go to the editor

Test Data :

Input the number of elements to be stored in the array :5

Input 5 elements in the array :

element - 0 : 25

element - 1 : 47

element - 2 : 42

element - 3 : 56

element - 4 : 32

Expected Output:

The Even elements are:

42 56 32

The Odd elements are :

25 47

QUESTION 4 SOLUTION

using System;

using System.Text;

namespace OddandEveninteger
{
    class program
    {
        static void Main(string[] args)
        { 

            int[] arr1 = new int[10];
            int[] arr2 = new int[10];
            int[] arr3 = new int[10];
            int l, m = 0, d = 0, n;


            Console.Write("\n\nSeparate odd and even integers in separate arrays:\n");
            Console.Write("------------------------------------------------------\n");

            Console.Write("Input the number of elements to be stored in the array :");
            n = Convert.ToInt32(Console.ReadLine());

            Console.Write("Input {0} elements in the array :\n", n);
            for (l = 0; l < n; l++)
            {
                Console.Write("element - {0} : ", l);
                arr1[l] = Convert.ToInt32(Console.ReadLine());
            }

            for (l = 0; l < n; l++)
            {
                if (arr1[l] % 2 == 0)
                {
                    arr2[m] = arr1[l];
                    m++;
                }
                else
                {
                    arr3[d] = arr1[l];
                    d++;
                }
            }

            Console.Write("\nThe Even elements are : \n");
            for (l = 0; l < m; l++)
            {
                Console.Write("{0} ", arr2[l]);
            }

            Console.Write("\nThe Odd elements are :\n");
            for (l = 0; l < d; l++)
            {
                Console.Write("{0} ", arr3[l]);
            }
            Console.Write("\n\n");
        }
    }


}

QUESTION 5


Write a function inside(x,y,x1,y1,x2,y2) that returns True or False depending on whether the point (x,y) lies in the rectangle with lower left corner (x1,y1) and upper right corner (x2,y2).
>>> inside(1,1,0,0,2,3)

True

>>> inside(-1,-1,0,0,2,3)

False

Use function inside() from part a. to write an expression that tests whether the point (1,1) lies in both of the following rectangles: one with lower left corner (0.3, 0.5) and upper right corner (1.1, 0.7) and the other with lower left corner (0.5, 0.2) and upper right corner (1.1, 2).

QUESTION 5 SOLUTION

using System;

using System.Text;

namespace pointintrectangle
{

    class GF
    {
        static void Main(string[] args)
        {

            // function to find if given point lies inside a given rectangle or not.
            static bool inside(int x, int y, int x1, int y1, int x2, int y2)
            {
                if (x > x1 && x < x2 && y > y1 && y < y2)
                    return true;

                return false;
            }

            
            {
                // bottom-left and top-right corners of rectangle
                int x1 = 0, y1 = 0, x2 = 2, y2 = 3;

                // given point
                int x = 1, y = 1;

                // function call
                if (inside(x, y, x1, y1, x2, y2))
                    Console.Write("True");
                else
                    Console.Write("False");
            }

        }
    }
}

QUESTION 6


You can turn a word into pig-Latin using the following two rules (simplified):

If the word starts with a consonant, move that letter to the end and append 'ay'. For example, 'happy' becomes 'appyhay' and 'pencil' becomes 'encilpay'.
If the word starts with a vowel, simply append 'way' to the end of the word. For example, 'enter' becomes 'enterway' and 'other' becomes 'otherway' . For our purposes, there are 5 vowels: a, e, i, o, u (so we count y as a consonant).
Write a function pig() that takes a word (i.e., a string) as input and returns its pig-Latin form. Your function should still work if the input word contains upper case characters. Your output should always be lower case however.

>>> pig('happy')

'appyhay'

>>> pig('Enter')

'enterway'

QUESTION 6 SOLUTION

>>> def pig(piglatin):
...     #applying lower() method so that if input contains Uppercase letter it get converted back
...     #to lower case.applying split() method so that to convert input word to list
...     CompleteWord = piglatin.lower().split(" ")
...     # declaring Vowels i.e 'a','e','i','o', 'u'
...     Vowels = ['a', 'e', 'i', 'o', 'u']
...     #empty piglatin
...     piglatin = []
...     for Word in CompleteWord:
...         # if Word[0] (i.e first word) of input is in 'aeiou' that is vowel is first
...         if Word[0] in 'aeiou':
...             piglatin.append(Word + 'way') #append method append 'way' at last
...         else:
...             for letter in Word:
...                if letter in 'aeiou':
...                   piglatin.append(Word[Word.index(letter):] + Word[:Word.index(letter)] +'ay')
...                   break
...         #here, piglatin.append(Word[Word.index(letter):] + Word[:Word.index(letter)] +'ay')
...         #can be summarised as an example i.e word 'Enter' => 'nter' + 'e' + 'ay' i.e
...         #piglatin.append(Word[Word.index(letter):]) append the letter after first word and
...         #Word[:Word.index(letter)] is first word and further 'ay' os adding at last.
...     print(" ".join(piglatin)) #join method add all the items of list
...
>>> pig('Enter')  # calling pig function
enterway
>>>

>>> def pig(piglatin):
...     #applying lower() method so that if input contains Uppercase letter it get converted back
...     #to lower case.applying split() method so that to convert input word to list
...     CompleteWord = piglatin.lower().split(" ")
...     # declaring Vowels i.e 'a','e','i','o', 'u'
...     Vowels = ['a', 'e', 'i', 'o', 'u']
...     #empty piglatin
...     piglatin = []
...     for Word in CompleteWord:
...         # if Word[0] (i.e first word) of input is in 'aeiou' that is vowel is first
...         if Word[0] in 'aeiou':
...             piglatin.append(Word + 'way') #append method append 'way' at last
...         else:
...             for letter in Word:
...                if letter in 'aeiou':
...                   piglatin.append(Word[Word.index(letter):] + Word[:Word.index(letter)] +'ay')
...                   break
...         #here, piglatin.append(Word[Word.index(letter):] + Word[:Word.index(letter)] +'ay')
...         #can be summarised as an example i.e word 'Enter' => 'nter' + 'e' + 'ay' i.e
...         #piglatin.append(Word[Word.index(letter):]) append the letter after first word and
...         #Word[:Word.index(letter)] is first word and further 'ay' os adding at last.
...     print(" ".join(piglatin)) #join method add all the items of list
...
>>> pig('happy')  # calling pig function
appyhay
>>>


QUESTION 7


File bloodtype1.txt records blood-types of patients (A, B, AB, O or OO) at a clinic. Write a function bldcount() that reads the file with name name and reports (i.e., prints) how many patients there are in each bloodtype.

>>> bldcount('bloodtype.txt')

There are 10 patients of blood type A.

There is one patient of blood type B.

There are 10 patients of blood type AB.

There are 12 patients of blood type O.

There are no patients of blood type OO.

QUESTION 7 SOLUTION


def bldcount(filetxt):
   known_blood_groups = ["A", "B", "AB", "O", "OO"]
   with open(filetxt) as f:
      file_txt = f.read()
   blood_groups_from_file = file_txt.split(" ") 
   blood_group_in_file_not_in_know = list(set(known_blood_groups) - set(blood_groups_from_file))
   for group in set(blood_groups_from_file):
      print ("There are " + str(blood_groups_from_file.count(group)) + " patients of blood type " + group)
   for group in blood_group_in_file_not_in_known:
      print ("There are no patients of blood type " + group)


QUESTION 8

Write a function curconv() that takes as input:

a currency represented using a string (e.g., 'JPY' for the Japanese Yen or 'EUR' for the Euro)
an amount
and then converts and returns the amount in US dollars.

>>> curconv('EUR', 100)

122.96544

>>> curconv('JPY', 100)

1.241401

The currency rates you will need are stored in file currencies.txt:

AUD 1.0345157 Australian Dollar

CHF 1.0237414 Swiss Franc

CNY 0.1550176 Chinese Yuan

DKK 0.1651442 Danish Krone

EUR 1.2296544 Euro

GBP 1.5550989 British Pound

HKD 0.1270207 Hong Kong Dollar

INR 0.0177643 Indian Rupee

JPY 0.01241401 Japanese Yen

MXN 0.0751848 Mexican Peso

MYR 0.3145411 Malaysian Ringgit

NOK 0.1677063 Norwegian Krone

NZD 0.8003591 New Zealand Dollar

PHP 0.0233234 Philippine Peso

SEK 0.148269 Swedish Krona

SGD 0.788871 Singapore Dollar

THB 0.0313789 Thai Bah

QUESTION 8 SOLUTION

>>> print("Please choose which currency you want to convert:")
Please choose which currency you want to convert:
>>> print("A - New Zealand Dollar to US Dollar (Exchange Rate: 0.000905)")
A - New Zealand Dollar to US Dollar (Exchange Rate: 0.000905)
>>> print("B - New Zealand Dollar to Euro (Exchange Rate: 0.000807350908)")
B - New Zealand Dollar to Euro (Exchange Rate: 0.000807350908)
>>> print("C - New Zealand Dollar to Japanese Yen (Exchange Rate: 0.0919061643)")
C - New Zealand Dollar to Japanese Yen (Exchange Rate: 0.0919061643)
>>> print("D - New Zealand Dollar to Chinese RMB (Exchange Rate: 0.00603703605)")
D - New Zealand Dollar to Chinese RMB (Exchange Rate: 0.00603703605)
>>> print("E - Quit ")
E - Quit
>>>
>>> A=0
>>> B=0
>>> C=0
>>> D=0
>>>
>>> usd = 0.000905
>>> eur = 0.000807350908
>>> yen = 0.0919061643
>>> rmb = 0.00603703605
>>>
>>> def main():
...     (option, amount) = Input()
...     Output(totalamount)
...
>>> def Input():
...     option = eval(input("Enter your option: "))
...     amount = eval(input("Enter the amoutn in New Zealand Dollar: "))
...     if option == "A":
...         totalamount = (amount * usd)
...         print (amount +"New Zealand dollar equals to "+totalamount+" USD")
...     elif option== "B":
...         totalamount = (amount * eur)
...         print (amount +"New Zealand Dollar  equals to "+totalamount+" Euro")
...     elif option== "C":
...         totalamount = (amount * yen)
...         print (amount +"New Zealand Dollar equals to "+totalamount+" Yen")
...     elif option== "D":
...         totalamount = (amount * rmb)
...         print (amount +"New Zealand Dollar equals to "+totalamount+" Chinese RMB")
...     else:
...         quit


QUESTION 9

Each of the following will cause an exception (an error). Identify what type of exception each will cause.

Trying to add incompatible variables, as in adding 6 + ‘a’	
Referring to the 12th item of a list that has only 10 items	
Using a value that is out of range for a function’s input, such as calling math.sqrt(-1.0)	
Using an undeclared variable, such as print(x) when x has not been defined	
Trying to open a file that does not exist, such as mistyping the file name or looking in the wrong directory.	

QUESTION 9 SOLUTION

(A)Trying to add incompatible variables, as in adding 6 + ‘a’	======= unsupported operand type(s) for +: 'int' and 'str'
(B)Referring to the 12th item of a list that has only 10 items ======	‘ArrayIndexOutOfBoundsException’

(C)Using a value that is out of range for a function’s input, such as calling math.sqrt(-1.0)======	 Message will be "Can't take square root of negative number”
(D)Using an undeclared variable, such as print(x) when x has not been defined =======	X is not defined
(E)Trying to open a file that does not exist, such as mistyping the file name or looking in the wrong directory. =======	“FileNotFoundException” because the file was either non-existent or mistyped.


QUESTION 10

Encryption is the process of hiding the meaning of a text by substituting letters in the message with other letters, according to some system. If the process is successful, no one but the intended recipient can understand the encrypted message. Cryptanalysis refers to attempts to undo the encryption, even if some details of the encryption are unknown (for example, if an encrypted message has been intercepted). The first step of cryptanalysis is often to build up a table of letter frequencies in the encrypted text. Assume that the string letters is already defined as 'abcdefghijklmnopqrstuvwxyz'. Write a function called frequencies() that takes a string as its only parameter, and returns a list of integers, showing the number of times each character appears in the text. Your function may ignore any characters that are not in letters.

>>> frequencies('The quick red fox got bored and went home.')

[1, 1, 1, 3, 5, 1, 1, 2, 1, 0, 1, 0, 1, 2, 4, 0, 1, 2, 0, 2, 1, 0, 1, 1, 0, 0]

>>> frequencies('apple')

QUESTION 10 SOLUTION



import string
from collections import OrderedDict
def frequencies(str1):
    dict1=dict(OrderedDict(zip(string.ascii_lowercase,[0]*26)))
  
    # iterate string to store the charcter's frequencies in dictionary.
    for i in range(0,len(str1)):
        if str1[i]=='a' or str1[i]=='A':
           dict1['a']+=1
  
        elif str1[i]=='b' or str1[i]=='B':
           dict1['b']+=1
  
        elif str1[i]=='c' or str1[i]=='c':
           dict1['c']+=1
  
        elif str1[i]=='d' or str1[i]=='D':
           dict1['d']+=1
  
        elif str1[i]=='e' or str1[i]=='E':
           dict1['e']+=1
  
        elif str1[i]=='f' or str1[i]=='F':
           dict1['f']+=1
  
        elif str1[i]=='g' or str1[i]=='G':
           dict1['g']+=1
  
        elif str1[i]=='h' or str1[i]=='H':
           dict1['h']+=1
  
        elif str1[i]=='i' or str1[i]=='I':
           dict1['i']+=1
  
        elif str1[i]=='j' or str1[i]=='J':
           dict1['j']+=1
  
        elif str1[i]=='k' or str1[i]=='K':
           dict1['k']+=1
  
        elif str1[i]=='l' or str1[i]=='L':
           dict1['l']+=1
  
        elif str1[i]=='m' or str1[i]=='M':
           dict1['m']+=1
  
        elif str1[i]=='n' or str1[i]=='N':
           dict1['n']+=1
  
        elif str1[i]=='o' or str1[i]=='O':
           dict1['o']+=1
  
        elif str1[i]=='p' or str1[i]=='P':
           dict1['p']+=1
  
        elif str1[i]=='q' or str1[i]=='Q':
           dict1['q']+=1
  
        elif str1[i]=='r' or str1[i]=='R':
           dict1['r']+=1
  
        elif str1[i]=='s' or str1[i]=='S':
           dict1['s']+=1
  
        elif str1[i]=='t' or str1[i]=='T':
           dict1['t']+=1
  
        elif str1[i]=='u' or str1[i]=='U':
           dict1['u']+=1
  
        elif str1[i]=='v' or str1[i]=='V':
           dict1['v']+=1
  
        elif str1[i]=='w' or str1[i]=='W':
           dict1['w']+=1
  
        elif str1[i]=='x' or str1[i]=='X':
           dict1['x']+=1
  
        elif str1[i]=='y' or str1[i]=='Y':
           dict1['y']+=1
  
        elif str1[i]=='z' or str1[i]=='Z':
           dict1['z']+=1
  
    # Return dictionary
    return dict1

def main():
  str1=input("The quick red fox got bored and went home : ")
  dict1=frequencies(str1)
  print("Resultant Dictionary : ")
  print(dict1)


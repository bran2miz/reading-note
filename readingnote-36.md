# Reading 8 - Game of Greed 3

## List Comprehension

### Why use list comprehension?

List comprehension:
1.Another great way to form and handle lists
2.Compartmentalize lists
3.Faster than other methods.

### Examples of List Comprehension

**range()**- generate list (string or numbers)
-loop through each item in that range
-stores a copy of item in new list.

  ex: digits = [x for x in range(10)]


  ex: squares = []

    for x in range(10):
      # raise x to the power of 2
      squares.append(x**2)

    print(squares)

#### String List Comprehension

  ex. authors = ["Ernest Hemingway","Langston
    Hughes","Frank Herbert","Toni Morrison",
    "Emily Dickson","Stephen King"]

    # create an acronym from the first letter of the author's names
    letters = [ name[0] for name in authors ]
      **"authors"** is the name of list to iterate through
      **name** is the item that we are trying to retrieve and save in our new list
      **[0]** is the letter position 
    print(letters)
  expected output: ['E', 'L', 'F', 'T', 'E', 'S']

  ex. separating characters in a string
  
  letters = [ letter for letter in "20,000 Leagues Under The Sea"]

  print(letters)
  expected output: print out all the letters individually as a string
  ['2', '0', ',', '0', '0', '0', ' ', 'L', 'e', 'a', 'g', 'u', 'e', 's', ' ', 'U', 'n', 'd', 'e', 'r', ' ', 'T', 'h', 'e', ' ', 'S', 'e', 'a']

#### Lower/Upper case converter using Python

**lower()**- transforms letters to lowercase
**upper()**- transforms letters to uppercase

#### Print numbers from String

**isdigit**- extract number data from a string

  ex. user_data = "Elvis Presley 987-654-3210"
        phone_number = [ x for x in user_data if x.isdigit()]

      print(phone_number)
  output: extract the numbers in user_data if it is a number. Iterate through the string to find number.
  ['9', '8', '7', '6', '5', '4', '3', '2', '1', '0']

#### Parsing a file using list comprehension

  ex. file = open("dreams.txt", 'r')
      poem = [ line for line in file ]

      for line in poem:
        print(line)
  output: will open the text file to read and iterate through the file to print out each line of the poem
  Hold fast to dreams

  For if dreams die

  Life is a broken-winged bird

  That cannot fly.

  -Langston Hughs

#### Functions in list comprehension

Create a separate function first, then iterate through desired range with that function to get expected output.
  ex. def double(x):
        return x*2

      nums = [double(x) for x in range(1,10)]
      print(nums)

  output: implement the function to iterate through the targeted range (from the number one to the number ten) to print out numbers that are multiples of 2.
  [2, 4, 6, 8, 10, 12, 14, 16, 18]

[<==BACK](README.md)

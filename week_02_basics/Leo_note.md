Week2
Ch3. Varaible
1. name = object # get the name to the object
2. type(name) # show the type of name
3. There are 35 Keyword can not use for name
4. del name # delete the 'name' and the connection between 'name' and object
5. function input()
    english_name = input()
    Leo 
    print(english_name, type(chinese_name)) # it gives you (Leo, str)
6. You do not need to announce the type of name
    english_name: str = 'Leo'
    or 
    def add(a: int, b: int) -> int:
        return a + b

Ch5. Numbers and Words(String)
1. Numbers have int and float two types
2. round() 四捨六入五成雙
    round(0.5) gives 0
    round(1.5) gives 2
3. math package https://docs.python.org/3/library/math.html
4. 科學記號 1.234e3 = 1234 . 0
5. bin(number) gives a string '0b + number' in binary
    bin(10) gives 0b1010
6. int(str, 2) change str into decimal (十進制)
    int('1000', 2) = 8
7. float('nan'), float('inf'), float('-inf'), all these three satisfy math calculation
    nan mean not a number
    nn = float('nan')
    print(nn == 123)  # False
    print(nn == nn)   # False
    use math.isnan(float)
    use math.isinf(float)
8. /n gives the next line, /t gives a tab space
    print('I am Leo./n I am a male.')
    I am Leo.
    I am a male.
9. string can multiple to number
    s = 'a'
    s * 5 gives 'aaaaa'
10. put variable in to string 
    a. %s to put variable into string
        age = 18
        name = "Kitty"
        print("我的名字是 %s，我今年 %s 歲" % (name, age))
    b. .format() to put variable into string
        age = 18
        name = "Kitty"
        print("我的名字是 {}，我今年 {} 歲".format(name, age))
        
    c. F字串
        print(f"我的名字是 {name}，我今年 {age} 歲")
11. F字串
12. string index
    message = 'python'
    message[0] gives p
    message[-1] gives n
    message[10] gives error
13. string slice
    message = 'python'
    message[start index: end index: step], # include start, exclude end
    start can be empty or larger then lenght of string
    end can be empty or larger then lenght of string
    step can be empty, default is 1
14. string function
    s.split(string, int)  #split s with string it gives a list with split out how mane elements and less string
    s.join()
    s.lower()
    s.upper()
    s.isalpha()
    s.isalnum()
    s.swapcase()
    s.capitalize()
    s.replace(str, str, int)
    s.startswith(string)
    s.endswith(string)
    s.isupper()
    s.islower()
    s.isnumeric()
    s.index()
    s.rindex()
    s.find()
    s.rfind()
    s.strip() # remove the space at the begin and last, also can remove string 

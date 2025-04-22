Week3
Ch5. Boolean
1. True and False is Boolean
2. Boolean is int type
3. or, and, not logic
    x and y “and”-如果x為False，x和y返回False，否則它返回y的計算值。
    x or y “or”-如果x是True，它返回x的值，否則它返回y的計算值。
    not x -如果x為True，返回False。如果x為False，它返回True。
    優先級 not > and > or
4. if statement logic
    if (condition):
        (statements) or pass to do nothing
    elif (condition):
        (statements)
    else:
        (statements)
5. if statement
    message = 'a' if condition else 'b'

Ch6. Loop
1. for variable in (string, list, dcitionary):
    statements
2. for idx, num in enumerate(list):
    idx gives index
    num gives the object in list
3. 'break' will stop the loop and jump out the loop
4. for - else statement
    for i in range(10):
        if i > 5:
            break
    else:
        print(there are no number bigger than five)
5. while condition:
    statements
    

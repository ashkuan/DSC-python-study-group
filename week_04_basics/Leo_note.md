Week4 
Ch.7 List
1. List can have many elements with different types
2. List index from zero
3. Use ele in list, list.index(ele), find(ele) to find element is in the list
4. list.count(ele) to count how frequent element exist in the list
5. list.append(ele) put element at the last, list.insert(index, element) put element at the index
6. list.extend(b-list) put b-list at the last
7. list.pop(index) remove the index element, default the last one element
8. list.remove(element) remove the first(left) element in the list
9. list.clear() remove all the elements in the list
10. copy() and deepcopy() can build the other different list, also slice can have the same result

Ch. 8 Dictionary
1. dictioanry = dict(key: value) build a dictionary
2. dict.get(key, default) get the key value
3. dict.setdefault(key, value) if there are no key than build the key with value
4. dictionary do not have index use key to call the value
5. dict.update(b-dict) use b-dict key and value to change the initial dictionary
6. key in dict, or dict.__contains__() to check the key is in dictionary
7. key have limit, only immutable type can be used, ex. int, tuple, string
8. del dict[key] delete the key in the dictionary
9. dict.pop(key) pop the key value 
10. dict.popitem(key, default) pop the key and value
11. c-dict = a-dict | b-dict combine two dictionaries into one
12. print all keys or values with three functions
    a. dict.items() gives keys and values
    b. dict.keys() gives keys
    c. dict.values() gives values

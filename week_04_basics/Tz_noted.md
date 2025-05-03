## 📘 書籍資訊

本讀書會共筆內容是依據 **《為你自己學 Python（第二版）》** 所整理。  
作者：高見龍老師（[@kaochenlong](https://github.com/kaochenlong)）  
出版：旗標出版社，ISBN：9789863125641  
📖 書籍介紹頁面：[https://pythonbook.cc/](https://pythonbook.cc/)
讀書會排程: [study_plan.md](./study_plan.md)
> 本共筆為讀書會學習交流用途，內容皆為成員學習心得與練習，尊重原書著作權 🙏  
> 感謝一起學習的讀書會夥伴們
---

## 📚 Tz_notes

### 關於串列（List）
1. 符號是[]
2.  一塊連續的記憶體位置，記憶體內的物件為元素  
3. 內容物不限制需相同型別，放串列亦可  
4. .copy():複製串列，不影響原串列，只會複製第一層  
     (1)或list()建立一個新串列  
     (2)deepcopy():可連串列內的串列也複製  
5. 可變的  

### 關於索引值（Index）
1.  由左至右的話開始算是0，從右往左開始算則是-1  
2.  len(): 可得知元素數量
3.  使用超過範圍的索引值會得到:IndexError: list index out of range  
4.  in: 知道某個元素是不是有在這個串列  
5.  .index(): 取得指定元素  
6.  .count(): 元素在串列裡出現的次數，如果不包含=0
7.  .append(): 將元素加入串列的最後  
    (1)【補充】因為資料結構屬於堆疊(Stack)類型(單向開口)，所以加入資料時會在最後，移除資料時則是last in first out  
8. .insert(): 將元素插入到指定位置,原本的值會往後挪  
    (1)【補充】如果插入的索引值是負數的話，插入的值會在索引值的左一位。例如:number = [1,2,5,4] numbers.insert(-2, 99) output = [1, 2, 99, 5, 4]  
9. .pop():搭配索引值移除指定元素  
    (1) 如果沒有給索引值的話，會把串最的最後一個元素拿出來  
    (2) 如果已經沒有元素可以移除的話: IndexError: pop from empty list  
10. .remove():移除指定元素  
    (1)如果元素在串列中有複數個，只會移除第1個  
11. .sort():可將串列中元素排序，且會改變原串列  
12. sorted():排序，不改變原串列  
13. .reverse():反向排序，且會改變原本串列  
     (1)如sort() /  sorted()要反向排序，將reverse參數 = False  

### 關於迭代（Iteration）
1. 一個一個讀取物件裡面的元素的行為  
2. 可迭代（Iterable）:可以被一個一個讀取物件裡面的元素的物件  

### 關於開箱(Unpacking)
1. 數量跟索引值不同的話會開不起來 :ValueError: too many values to unpack / ValueError: not enough values to unpack  
2. *(Extended Unpacking):不管最後收到的元素有幾個，最終的結果都會是一個串列  
3. Python內能交換變數即是依照開箱的邏輯執行  

### 關於字典（Dictionary）
1. 符號是{}  
2. 由鍵（Key）與值（Value）組成  
3. 字典本身並沒有順序，使用 Key 來存取資料  
     (1)不可變的資料才能作為Key: 數字、字串、布林值、元組  
4. .clear():清除所有內容  
5. del:只刪除其中一組Key+Value  
     (1)不是函數，使用的時候不需要加小括號  
6. .pop():指定Key後取出Value  
    (1) .keys()取出字典中所有Key  
    (2) .values()取出字典中所有Value  
    (3) .items()取出字典中所有Key+Value  
7. .popitem():取出Key+Value  
8. **:開箱運算子（Unpacking Operator） 
9. .copy():複製字典，不影響原字典，只會複製第一層  

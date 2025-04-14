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
### 關於變數(Variable)
1.  標籤資料讓電腦方便取用
2.  宣告(Declaration):標籤或指定資料/數值名稱的行為
3.  Python在宣告的時候不特別指定型別就能使用
4.  _ :可以用來跳過不需要命名的變數  
  (1)名稱是匿名變數（Anonymous Variable）/虛擬變數（Dummy Variable)  
  (2)是Python內的合法變數名稱，所以可被使用  
  (3)在REPL環境下，可以用於表示上一次的結果  
5.  變數需要先宣告才能被使用，例如:print(girl_friend)就會找不到
6.  練習存放位置:VS Code:PRA_0412.py
7.  del:這邊的刪除是中斷變數與變數內容的連結後，刪除變數
8.  Python會回收掉沒有參照變數的字串

### 關於常數(Constant)
1. 在Python沒有
2. 慣例會以全大寫方式命名，但沒辦法讓人無法修改，只是比較醒目

### 關於命名(Naming)
1. 規則:  
   (1)任何語言的一般文字  
   (2)開頭:_可以；數字不行  
   (3)大小寫不一樣  
   (4)保留字(Reserved Keyword)會造成語法錯誤（SyntaxError）不可以用來命名:在終端機REPL環境下輸入keyword.kwlist，可以找到當前版本包含哪些保留字  
   (5)內建函數像是print()也會卡住
2. 慣例:  
   (1)駝峰式（CamelCase）:開頭小寫中間大寫；Pascal 命名法（Pascal Case）:一開始就大寫的駝峰  
   (2)蛇式命名法（snake_case）:中間用_區隔，常用於變數與函數名稱  
   (3)烤肉串命名法（Kebab-Case）:中間用-區隔，常用於類別名稱  
3.有規律的命名程式的可讀性會比較好  

### 關於元組(Tuple)
1.  是Python能一次處理多個變數的背後邏輯
2.  讀音可以是吐波或塔波，字尾的ple在拉丁文中表示plus/more
3.  數學上表示**有限的有序數列**
4.  設計上跟字串接近，但建立後就不可變:不能新增/修改/刪除包含的元素
5.  Tuple 的小括號可以省略，但逗號卻不行，不過考量到可讀性還是加上小括號比較好
6.  分別建立的 Tuple 就是不同的東西(每日一題出現過)
  (1)Tuple有值的話，T1 == T2會成立但T1 is T2 就會False了
  (2)Tuple為空的話 T1 == T2和T1 is T2都為Ture
7. 使用建議:  
   (1)要裝的資料是不會變動的，選 Tuple，有可能需要變動的，選串列=>附加的好處是從資料型態本身也能知道這個容器裡裝的是不會變動的資料，比較不會發生意外  
   (2)異質性資料選Tuple；同質性資料選串列  

### 關於使用者輸入(Input)
1.  在網頁中通常是透過表單(Form)
2.  一般程式通常透過文字介面(Command-Line Interface，簡稱 CLI)
3.  Python中可以透過input()取得使用者輸入內容

### 關於型別(Type)
1. 動態型別(Dynamic Typing):**Python特性之一**，可隨時變更變數所指向的資料的型別  
2. 型別註記（Type Annotation）:宣告變數時可同時標註指向資料的型別，**註記沒有強制力只是註記**  
3. 可以是任何合法的表達式（Expression），但意義不明且影響可讀性  

### 關於索引(Index)
1. []:表示字串中字元所在的位置  
2. 從0開始，-的話表示從尾巴開始算，值超過範圍就會變**索引超出範圍(IndexError)**  
3. 一旦建立之後就不能再改變裡面的內容(Tuple也有同樣特質)  
4. 不過可以重新指定（Reassign）取代變數內容  

### 關於切片(Slice)
1. [::]:分別表示起始位置、停止位置、移動距離  
  (1)[2:8:2]表示從2之後到8(本身不算)，每次移動2索引值  
2. [x:y:z]3個欄位都可視情況省略，會帶入預設值None  
  (1)省略(或預設)x或y，則x或y會是邊界值（end value） 
  (2)如z為正數，則x 會是左邊界，y 會是右邊界；z為負數的話就反過來  
3. [x:y]2個欄位中有省略的情況  
  (1)省略(或預設)x的話，起始位置會設為0  
  (2)省略(或預設)y的話，停止位置為leg()的值  
4. 邊界值不是0也不是len()的數字，而是字串最邊邊那個字  

### 關於常用字串方法
1. V.upper():全部轉大寫  
2. V.lower():全部轉小寫    
3. V.capitalize():首字轉大寫  
   (1)如果首字轉小寫:沒有內建，可以用lowercased_V = V[0].lower() + V[1:]方式處理  
4. V.message.swapcase():大小寫交換
5. 判斷開頭/結尾用with，字元字串都適用，大小寫會識別為不同東西  
   (1)V.startswith("H") / V.startswith("Hello")  
   (2)V.endswith("y") / V.endswith("kitty")  
6. 判斷是否為用is  
   (1)V.isupper():是否全大寫  
   (2)V.islower():是否全小寫  
   (3)V.isnumeric():是否全數字  
7. 搜尋:如果有多個符合的字元，只會找到第一個；如果一個符合的字元都沒有，會變錯誤(ValueError: substring not found)  
   (1)V.index():從頭開始
   (2)V.rindex():從尾開始  
   (3)V.find():也從尾開始，但找不到是回傳-1，通常用在判斷字元或字串是否存在
8. V.replace():取代，實際上是得到一組新的字串
9. V.strip():清除字串中多餘的空白字元
10. 拆解:把字串逐個拆回字元  
   (1)V.split():無拆解字元  
   (2)V.split("-"):以-為拆解字元  
   (3)V.split(",", 2):以,為拆解字元且只拆2個出來(會拆出前兩個)  
   (4)V.split("c"):以c為拆解字元(c會成為那條分隔線，不會帶到c)  
11.合併:把字元併在一起  
   (1)"-".join("abcdefg") / "/".join("abcdefg"):用符號串起來
   (2)"".join("abcdefg"):用空字串串起來

### 關於Unicode跟位元組
1. 美國標準資訊交換碼ASCII(American Standard Code for Information)，讀音是阿斯KI，用來表示文字的編碼方式，主要用於英文(7位元->8位元)  
2. 萬國碼Unicode(The Unicode Standard)，字元集合，可支援的字元比ASCII多很多(16位元->21位元)，包含表情符號:)  
3. UTF（Unicode Transformation Format），一種編碼方式，以不同位元分為utf-8(最常見)、utf-16 及 utf-32


---

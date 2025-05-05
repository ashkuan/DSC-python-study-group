## 📘 書籍資訊

本讀書會共筆內容是依據 **《為你自己學 Python（第二版）》** 所整理。  
作者：高見龍老師（[@kaochenlong](https://github.com/kaochenlong)）  
出版：旗標出版社，ISBN：9789863125641  
📖 書籍介紹頁面：[https://pythonbook.cc/](https://pythonbook.cc/)
讀書會排程: [study_plan.md](./study_plan.md)
> 本共筆為讀書會學習交流用途，內容皆為成員學習心得與練習，尊重原書著作權 🙏  
> 感謝一起學習的讀書會夥伴們
---

## 📚 Ash_note
# Python 串列、字典與雜湊筆記 (對應書籍中第7章 及 第8章)

## 1. 串列 (List)

### 定義與特點
- **有序**、**可變**的資料結構，用於儲存多個元素。
- 元素可為任何型態（數字、字串、其他串列等）。
- 使用方括號 `[ ]` 定義，元素以逗號分隔。
- 支援**索引**（從 0 開始）與**負數索引**（從 -1 倒數）。

### 建立串列
```python
# 空串列
my_list = []
# 含元素串列
numbers = [1, 2, 3, 4]
mixed = [1, "hello", 3.14]
```

### 常用操作

**訪問元素：**
```python
print(numbers[0])   # 輸出: 1
print(numbers[-1])  # 輸出: 4
```

**修改元素：**
```python
numbers[1] = 10
print(numbers)      # 輸出: [1, 10, 3, 4]
```

**新增元素：**
- `append()`：末尾新增單一元素。
- `extend()`：合併另一串列。
- `insert()`：指定位置插入。
```python
numbers.append(5)        # [1, 10, 3, 4, 5]
numbers.extend([6, 7])   # [1, 10, 3, 4, 5, 6, 7]
numbers.insert(1, 99)    # [1, 99, 10, 3, 4, 5, 6, 7]
```

**刪除元素：**
- `remove()`：移除第一個匹配元素。
- `pop()`：移除並返回指定索引元素（預設最後一個）。
- `clear()`：清空串列。
```python
numbers.remove(99)       # [1, 10, 3, 4, 5, 6, 7]
numbers.pop()            # [1, 10, 3, 4, 5, 6]
numbers.clear()          # []
```

**切片 (Slicing)：**
```python
numbers = [1, 2, 3, 4, 5]
print(numbers[1:4])      # [2, 3, 4]
print(numbers[:3])       # [1, 2, 3]
print(numbers[::2])      # [1, 3, 5]
```

**其他方法：**
```python
numbers.sort()           # [1, 2, 3, 4, 5]
numbers.reverse()        # [5, 4, 3, 2, 1]
print(numbers.count(3))  # 1
print(numbers.index(4))  # 3
```

### 串列解析 (List Comprehension)
```python
squares = [x**2 for x in range(5)]  # [0, 1, 4, 9, 16]
evens = [x for x in range(10) if x % 2 == 0]  # [0, 2, 4, 6, 8]
```

## 2. 字典 (Dictionary)

### 定義與特點
- 無序、可變的鍵值對集合，儲存鍵 (key) 與值 (value) 的對應。
- 使用大括號 `{ }` 定義，鍵值對以 key: value 表示。
- 鍵必須為不可變物件，值可為任何型態。
- Python 3.7+ 起，字典保持插入順序。
- 底層使用雜湊表實現，確保快速查找。

### 建立字典
```python
my_dict = {}
person = {"name": "Alice", "age": 25, "city": "Taipei"}
```

### 常用操作

**訪問值：**
```python
print(person["name"])      # 輸出: Alice
print(person.get("age"))   # 輸出: 25
```

**新增/修改鍵值對：**
```python
person["email"] = "alice@example.com"
person["age"] = 26
print(person)
```

**刪除鍵值對：**
```python
person.pop("city")
person.popitem()
person.clear()
```

**遍歷字典：**
```python
for key in person:
    print(key)

for value in person.values():
    print(value)

for key, value in person.items():
    print(f"{key}: {value}")
```

**其他方法：**
```python
person.update({"job": "Engineer"})
```

### 字典解析 (Dictionary Comprehension)
```python
squares = {x: x**2 for x in range(5)}
filtered = {k: v for k, v in person.items() if v != "Taipei"}
```

## 3. 雜湊 (Hash) 與字典的關係

### 定義與特點
- 雜湊表是字典的底層實現。
- 雜湊函數將鍵轉為數字雜湊值，用於快速定位。
- 鍵需為不可變、可雜湊的物件。
- 平均時間複雜度為 O(1)。

### 雜湊函數範例
```python
print(hash("name"))
print(hash(42))
print(hash((1, 2)))
# print(hash([1, 2]))  # 錯誤，列表不可雜湊
```

### 為何鍵必須可雜湊？
```python
my_dict = {("a", 1): "value"}
print(my_dict[("a", 1)])
# my_dict[[1, 2]] = "value"  # 錯誤
```

### 雜湊衝突
- 雜湊值相同的鍵由 Python 內部處理，不影響使用。

### 應用場景
- 快速檢索資料
- 計數問題
- 資料索引

## 4. 串列 vs 字典 vs 雜湊表 比較

| 特性 | 串列 (List) | 字典 (Dictionary) | 雜湊表 (Hash Table) |
|------|-------------|--------------------|----------------------|
| 結構 | 有序，索引存取 | 鍵值對，保持插入順序 | 鍵值對，雜湊實現 |
| 定義方式 | `[1, 2, 3]` | `{"key": "value"}` | 內部實現 |
| 存取方式 | `list[0]` | `dict["key"]` | 雜湊鍵定位 |
| 時間複雜度 | 查找 O(n) | 查找/插入 O(1) | 查找/插入 O(1) |
| 使用場景 | 有序資料 | 鍵值對儲存 | 字典實現 |

## 5. 實用範例

### 5.1 串列應用：計算成績平均
```python
scores = [85, 90, 78, 92]
average = sum(scores) / len(scores)
print(f"平均分數: {average}")
```

### 5.2 字典應用：管理學生資訊
```python
student = {"name": "Bob", "scores": [85, 90, 78]}
student["average"] = sum(student["scores"]) / len(student["scores"])
print(student)
```

### 5.3 雜湊應用：計數字詞出現次數
```python
words = ["apple", "banana", "apple", "cherry"]
word_count = {}
for word in words:
    word_count[word] = word_count.get(word, 0) + 1
print(word_count)
```

### 範例解釋
- 使用 `get()` 取得現有值或預設值。
- 雜湊表實現使查找快速 (O(1))。
- 使用字串作為鍵因為其可雜湊。

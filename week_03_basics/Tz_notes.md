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
### 關於布林值（Boolean）
1.  本質上是數字，分為    
    (1)真的(Ture):1  
    (2)假的(False):0  
2.  可以用bool()轉換型別  
    (1)結果為False是少數，包含:False(本身)、None、0(數字)、" "(空字串)、[ ] ( ) { }(空容器)  
3.  比較:  
    (1)指定: =  
    (2)比較: ==  
    (3)不適用: === (JS可以(用於嚴格相等，會先判定型別再判定值)  
4.  運算規則:  
    (1)And:都，處理次序2(如位元運算用&)  
    (2)Or:或，處理次序3(如位元運算用|)  
    (3)Not:顛倒，處理次序1
5.  會有邏輯短路（Short-circuit）的情況*詳見黑貓貓補充知識段落  

### 關於流程控制及迴圈
1. 本周Code in Place剛好也有這個段落，從新手的角度整理了簡易判斷方式:  
    (1)要執行的動作是重複的嗎? Y: For / While；N: if/ if...else/if...elif...else  
    (2)如需重複，重複的次數有限/已知嗎? Y: For；N: While    
    (3)如不需重複，是否只有符合單一條件的情況需執行動作? Y:if；N:if...else/if...elif...else  
    (4)是否只依單一條件的真偽執行動作? Y:if...else；N:if...elif...else  
2. 三元運算子（Ternary Operator）:使用?、:、=符號簡單取代if...else的功能  
3. Match:if...else的替代品，正式名稱是結構化模式比對（Structural Pattern Matching） 
4. Python由縮排判斷結構，需注意縮排，可先放pass卡位，官方建議使用四個空白  

### 關於is和=
1. Python內建函數id()  
2. is 判定的是Python內建的id()  
3. = 是指派變數值  

### 關於邏輯短路
1. And的情況下，只要第一個值為False，則結果為False  
2. Or的情況下，只要第一個值為True，則結果為True  
3. 【補充】And的運算邏輯是相乘，Or的運算邏輯為相加  
4. 【補充】套用邏輯閘的說明可以配合真值表來理解(高中提過有P、Q、1、0的那張表)  
5. 【補充】一些後面會遇到的名詞:  
    (1)遞迴(Recursion):Call自己解決問題的方式  
    (2)演算法(Algorithm):為了解決問題的方法
    (3)參數(Parameter)  
    (4)函式(Function)  
    (5)階乘(N!,Factorial)，舉例來說:  
       def fac(X): #這邊的X是input  
           if x == 1: #這邊是終止條件，忘記寫就會一路算不停  
              return 1
           else:  
              return fac(x-1)*x  

### 關於導讀
1. 說明可以更簡要一點，比較容易引起討論情境  

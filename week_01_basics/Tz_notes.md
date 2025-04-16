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
### 關於Python
1.1991 年上市，名稱來源於英國表演團體《Monty Python》，拍森跟拍桑都有人讀  
2.TIOBE NO.1的語言  
3.2.X和3.X語法不相容 *>3.X全面翻新取代2.X*  
4.用 C 語言所設計出來的，沒特別聲明的話通常指CPython  
5.常見用途:  
  (1)自動化程式  
  (2)爬蟲抓取資料*  
  (3)資料整理分析  
  (4)網站應用程式開發  
  (5)機器學習  
  (6)人工智慧  
*6.透過高階語法、動態型別、記憶體自動化管理，解決問題:易讀性、結構清楚、腳本及自動化工具開發*  
*7.原則是簡單、明確、美感*  
*爬蟲(Web crawler)

### 關於本書
1.無基礎新手適用  
2.章節安排依照新手的學習路徑，跳著讀也可以  
3.$表示系統指令，輸入的時候不要一起輸  
4.>>>可進入Shell 環境(REPL,Read-Eval-Print Loop*)  
5.Python表示語言；python表示終端機指令或程式碼執行檔  
6.有問題可以加入線上或實體社群  
  *REPL:讀取（Read）、評估（Eval）、印（Print）、迴圈（Loop）， *可用於快速驗證*  

### 關於學習方式
1.看一段落理解後再自行輸出，重點表述或練習題  
2.挑選可信來源(官方文件或原始碼)建立SSOT(Single Source of True)，對新手而言是困難但重要的過程

### 關於程式語言
1.電腦程式的運行本質為1和0，不同的程式語言即使用不同語法讓電腦執行功能，每種語言的用途跟要解決的問題各有差異  
2.指令:會執行的動作，書中以$標示  
3.註解(Comment):Python的話是用#標示  

### 關於安裝
1.程式本人:Python  
2.環境管理工具:pyenv  
  (1)pyenv權限錯誤，提示訊息:'files name' is denied~~pyenv-win is successfully installed. You may need to close and reopen your terminal before use it.  
  **這個狀態是沒裝成功的**  
  (2)Solution: Open Power Shell(以系統管理員身分執行) ->  
  Invoke-WebRequest -Uri "https://raw.githubusercontent.com/pyenv-win/pyenv-win/master/pyenv-win/install-pyenv-win.ps1" -OutFile "$HOME\install-pyenv-win.ps1"->  
  Install-Module Microsoft.PowerShell.Archive -Force -Scope CurrentUser ->& "$HOME\install-pyenv-win.ps1" ->reopen  
  **貼上pyenv --version有顯示版次就成功了  謝謝Ash救我** 

3.整合開發工具(Integrated Development Environment, IDE):PyCharm(常見),VS Code(新手推薦)  
  (1)VS擴充:Python,Pylance,Black Formatter  
4.套件庫:PyPI  
5.通常附檔名是.py,但另存成其他也不影響運行 >附檔名只是讓你的作業系統知道當你用滑鼠點兩下之後應該用什麼程式來開啟
  (1)【補充】W2討論中提到，新手附檔名建議使用.ipynb

### 關於虛擬環境
*1.讓不相容的語言可以各自在環境內運行*  
*2.這個環境不要了砍掉資料夾即可*  
*3.Poetry用於建置虛擬環境與專案管理*


---

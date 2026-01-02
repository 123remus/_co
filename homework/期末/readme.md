我是複製 https://github.com/havivha/Nand2Tetris
##  第二部分：軟體堆疊 (Ch 6 - 12)

這個階段我們將開發一個完整的編譯器鏈，將高階語言轉化為前述硬體能執行的二進制碼。

### Ch 6: 組譯器 (Assembler)

* **核心**：將文字符號轉為 `0101`。
* **任務**：寫一個 Python 程式，將 `.asm` 轉為 `.hack`。
* **挑戰**：處理「符號表」（Symbol Table），例如跳躍標籤 `(LOOP)` 或變數名，需要兩次掃描（Two-pass）來確定位址。

### Ch 7 & 8: 虛擬機 (Virtual Machine)

* **核心**：中間語言（Intermediate Language）。
* **任務**：實作一個基於「堆疊」（Stack）的運算體系。
* **關鍵觀念**：
* **Ch 7**：算術運算與記憶體存取（push/pop 到不同段落如 local, argument, static）。
* **Ch 8**：程式流控制。最難的是 **Function Call**，需要精準地管理傳回位址（Return Address）與呼叫者的狀態。



### Ch 9: Jack 語言 (Jack Language)

* **核心**：撰寫你的第一個程式。
* **任務**：使用一種類似 Java 的物件導向語言 **Jack** 寫遊戲。
* **目標**：讓學生熟悉接下來要編譯的對象。

### Ch 10 & 11: 編譯器 (Compiler)

* **核心**：從高階結構到機器邏輯。
* **任務 10 (Syntax Analysis)**：使用遞迴下降解析法（Recursive Descent Parsing）將代碼轉為 XML/語法樹。
* **任務 11 (Code Generation)**：將語法結構轉化為第 7-8 章的 VM 指令。處理物件（Object）在 Heap 中的布局。

### Ch 12: 作業系統 (Operating System)

* **核心**：基礎服務庫。
* **任務**：用 Jack 語言手寫 OS 核心功能。
* **關鍵模組**：
* `Math`: 透過位移實作乘除法（因為硬體 ALU 只會加法）。
* `Memory`: 實作 `alloc` 和 `dealloc`（記憶體碎片管理）。
* `Screen` & `Output`: 處理像素繪圖與字型渲染。


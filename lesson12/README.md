
## Python function 教學範例

### 1) 最基本：定義與呼叫 function

```python
def say_hello():
	print("Hello, Python!")

say_hello()
```

重點：
- 使用 `def` 建立函式
- 函式名稱後面一定要有括號 `()`
- 縮排是 Python 語法的一部分

### 2) 帶參數的 function

```python
def greet(name):
	print(f"你好, {name}")

greet("Sean")
greet("Amy")
```

重點：
- `name` 是參數
- 呼叫時放進去的值叫做引數
- 同一個 function 可重複使用不同資料

### 3) 有回傳值 `return`

```python
def add(a, b):
	result = a + b
	return result

total = add(10, 20)
print(total)
```

重點：
- `return` 會把結果傳回去
- `print` 是顯示結果，`return` 是回傳資料
- 有回傳值的函式通常更容易重複使用

### 4) 預設參數

```python
def power(base, exp=2):
	return base ** exp

print(power(3))
print(power(3, 3))
```

重點：
- `exp=2` 是預設值
- 沒有傳入 `exp` 時就使用預設值

### 5) 關鍵字參數

```python
def introduce(name, age, city):
	print(f"我是{name}, {age}歲, 住在{city}")

introduce(name="王小明", age=15, city="台北")
introduce(city="台中", name="小美", age=16)
```

重點：
- 使用關鍵字參數時，參數順序可調整
- 可讀性更高

### 6) 多個回傳值

```python
def calc(a, b):
	s = a + b
	d = a - b
	return s, d

x, y = calc(8, 3)
print("加法:", x)
print("減法:", y)
```

重點：
- Python 支援一次回傳多個值
- 可用多個變數接收

### 7) function 裡呼叫 function

```python
def square(n):
	return n * n

def sum_of_squares(a, b):
	return square(a) + square(b)

print(sum_of_squares(2, 3))
```

重點：
- 函式可以互相組合
- 有助於建立模組化思維

### 8) 常見錯誤示範

```python
def area(width, height):
	return width * height

# print(area(5))  # 會錯：少一個參數
print(area(5, 10))
```

重點：
- 常見錯誤為參數數量不正確
- 讀取錯誤訊息可快速定位問題

---

## 課堂小練習

1. 寫一個 function，輸入攝氏溫度，回傳華氏溫度。
2. 寫一個 function，輸入半徑，回傳圓面積。
3. 寫一個 function，輸入成績，回傳 A、B、C 或不及格。
4. 寫一個 function，輸入三個數字，回傳最大值。

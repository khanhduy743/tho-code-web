# Hướng dẫn học JS chắc là trong một ngày

Chà học được đống này trong một ngày cũng đúng, tức là trong 24h đấy.

### Cách sử dụng JS trong HTML

Thêm `<script>{Chỗ này chính là để Code}</script>` vào trong `<head>` hoặc `<body>` đều được:

```html
<html>
  <head>
    <!--Thêm như này cũng được-->
    <script type="text/javascript">
        function sayHello() {
          alert("Hello World")
        }
    </script>
  </head>
  <body>
    <input type="button" onclick="sayHello()" value="Hello!" />
    <!--Thêm như này cũng oke-->
    <script type="text/javascript">
        function sayHello() {
          alert("Hello World")
        }
    </script>
    <!--Nếu muốn viết ra một tệp JS khác thì làm như này, giả sử mình viết ra một tệp mới là `vi_du.js` thì-->
    <script type="text/javascript" src="vi_du.js" ></script>
  </body>
</html>
```

### Khai báo biến

```js
// Cái này không thay đổi được
const username = 'giá trị';
// Cái này thì được
let mon_ngon_ha_noi = 'bún chả';
// Có thể tôi sẽ thích phở hơn
mon_ngon_ha_noi = 'phở bò';
```
### Comments

```js
// Học JS xong trong một ngày
// Đây là một "bình luận" cái code của bạn, nó sẽ không được tính là Code
```

### Một số hàm built-in  - Built-in functions

> Nguồn từ [bài viết này](https://www.truongcongly.com/2023/11/javascript-built-in-functions-nhung-ham-tich-hop-doc-dao-va-huu-ich.html)

1.  **[String Functions (Hàm Chuỗi) (!)](https://www.truongcongly.com/2023/11/ham-xu-ly-chuoi-trong-javascript-string-function-javascript.html) :**
    -   `charAt(index)`: Trả về ký tự tại vị trí chỉ định trong chuỗi.
    -   `concat(string1, string2)`: Ghép nối các chuỗi.
    -   `indexOf(substring)`: Trả về vị trí đầu tiên của chuỗi con trong chuỗi.
    -   `toLowerCase()`, `toUpperCase()`: Chuyển đổi chuỗi thành chữ hoa hoặc chữ thường.
    -   `charCodeAt(index)`: Trả về mã Unicode của ký tự ở vị trí chỉ định trong chuỗi.
    -   `lastIndexOf(substring)`: Trả về vị trí cuối cùng của một chuỗi con trong chuỗi gốc. Nếu không tìm thấy, trả về -1.
    -   `slice(start, end)`: Trích xuất một phần của chuỗi từ vị trí bắt đầu đến vị trí kết thúc (không bao gồm).
    -   `substring(start, end)`: Tương tự như slice, nhưng không hỗ trợ các giá trị âm.
    -   `substr(start, length)`: Trích xuất một phần của chuỗi từ vị trí bắt đầu với chiều dài xác định.
    -   `replace(search, replacement)`: Thay thế chuỗi con đầu tiên được tìm thấy bằng chuỗi thay thế.
2.  **[Array Functions (Hàm Mảng) (!)](https://www.truongcongly.com/2023/11/tong-hop-cac-ham-mang-trong-javascript-array-functions.html):**
    -   `push(element)`: Thêm phần tử vào cuối mảng.
    -   `pop()`: Loại bỏ phần tử cuối cùng của mảng.
    -   `shift()`, `unshift()`: Loại bỏ hoặc thêm phần tử ở đầu mảng.
    -   `splice(start, count, element1, ..., elementN)`: Thay đổi nội dung của mảng bằng cách loại bỏ hoặc thêm các phần tử.
    -   `concat(array1, array2, ..., arrayN)`: Tạo một mảng mới bằng cách kết hợp nhiều mảng hoặc giá trị vào một mảng.
    -   `slice(start, end)`: Trả về một phần của mảng từ vị trí start đến end (không bao gồm end).
    -   `indexOf(element, fromIndex)`: Trả về vị trí đầu tiên của phần tử trong mảng. Nếu không tìm thấy, trả về -1.
    -   `lastIndexOf(element, fromIndex)`: Tìm vị trí cuối cùng của phần tử trong mảng. Nếu không tìm thấy, trả về -1.
    -   `reverse()`: Đảo ngược thứ tự các phần tử trong mảng.
    -   `join(separator)`: Chuyển đổi mảng thành một chuỗi bằng cách nối các phần tử với một chuỗi phân tách.
    -   `forEach(callback(currentValue, index, array))`: Thực hiện một hàm callback cho mỗi phần tử trong mảng.
    -   `map(callback(currentValue, index, array))`: Tạo một mảng mới bằng cách ánh xạ mỗi phần tử của mảng qua một hàm callback.
    -   `filter(callback(element, index, array))`: Tạo một mảng mới chứa các phần tử của mảng gốc mà thỏa mãn một điều kiện được xác định bởi hàm callback.
    -   `reduce(callback(accumulator, currentValue, index, array), initialValue)`: Thực hiện một hàm callback trên từng phần tử của mảng để giảm mảng thành một giá trị duy nhất.
    -   `every(callback(element, index, array))`: Kiểm tra xem tất cả các phần tử của mảng có thỏa mãn một điều kiện nào đó hay không.
    -   `some(callback(element, index, array))`: Kiểm tra xem có ít nhất một phần tử của mảng thỏa mãn một điều kiện nào đó hay không.
    -   `sort(compareFunction)`: Sắp xếp các phần tử của mảng dựa trên hàm so sánh.
3.  **[Math Functions (Hàm Toán Học) (!)](https://www.truongcongly.com/2023/11/ham-toan-hoc-trong-javascript.html):**
    -   `Math.abs(x):` Trả về giá trị tuyệt đối của x.
    -   `Math.ceil(x):` Làm tròn số lên đến số nguyên gần nhất.
    -   `Math.floor(x):` Làm tròn số xuống đến số nguyên gần nhất.
    -   `Math.round(x):` Làm tròn số tới số nguyên gần nhất.
    -   `Math.max(x1, x2, ...):` Trả về giá trị lớn nhất từ danh sách các tham số.
    -   `Math.min(x1, x2, ...):` Trả về giá trị nhỏ nhất từ danh sách các tham số.
    -   `Math.pow(x, y):` Trả về x mũ y.
    -   `Math.sqrt(x):` Trả về căn bậc hai của x.
    -   `Math.random():` Trả về một số ngẫu nhiên từ 0 đến 1.
    -   `Math.sin(x), Math.cos(x), Math.tan(x):` Trả về sin, cos, và tan của x (x được đo theo radian).
    -   `Math.asin(x), Math.acos(x), Math.atan(x):` Trả về arcsin, arccos, và arctan của x (kết quả được đo theo radian).
    -   `Math.log(x):` Trả về logarithm tự nhiên của x.
    -   `Math.exp(x):` Trả về e mũ x.
4.  **[Date Functions (Hàm Ngày Tháng)(!)](https://www.truongcongly.com/2023/11/ham-ngay-thang-trong-javascript.html):**
    -   `new Date():` Tạo một đối tượng `Date` mới đại diện cho thời điểm hiện tại.
    -   `new Date(milliseconds):` Tạo một đối tượng `Date` từ số mili giây kể từ 1 tháng 1 năm 1970 (Epoch time).
    -   `new Date(dateString):` Tạo một đối tượng `Date` từ một chuỗi ngày tháng.
    -   `new Date(year, month, day, hours, minutes, seconds, milliseconds):` Tạo một đối tượng `Date` từ các thành phần ngày tháng cụ thể.
    -   `Date.now():` Trả về số mili giây kể từ 1 tháng 1 năm 1970 cho thời điểm hiện tại.
    -   `getFullYear():` Trả về năm.
    -   `getMonth():` Trả về tháng (từ 0 đến 11).
    -   `getDate():` Trả về ngày trong tháng.
    -   `getDay():` Trả về ngày trong tuần (từ 0 đến 6, 0 là Chủ nhật).
    -   `getHours():` Trả về giờ.
    -   `getMinutes():` Trả về phút.
    -   `getSeconds():` Trả về giây.
    -   `getMilliseconds():` Trả về mili giây.
    -   `getTime():` Trả về số mili giây kể từ 1 tháng 1 năm 1970.
    -   `setFullYear(year):` Đặt giá trị năm.
    -   `setMonth(month):` Đặt giá trị tháng (từ 0 đến 11).
    -   `setDate(day):` Đặt giá trị ngày trong tháng.
    -   `setHours(hours):` Đặt giá trị giờ.
    -   `setMinutes(minutes):` Đặt giá trị phút.
    -   `setSeconds(seconds):` Đặt giá trị giây.
    -   `setMilliseconds(milliseconds):` Đặt giá trị mili giây.
    -   `toString():` Chuyển đối tượng `Date` thành một chuỗi.
5.  **[JSON Functions (Hàm JSON) (!):](https://www.truongcongly.com/2023/11/lam-viec-voi-json-trong-javascript.html)**
    -   `JSON.stringify(obj)`: Chuyển đối tượng JavaScript thành chuỗi JSON.
    -   `JSON.parse(json)`: Chuyển chuỗi JSON thành đối tượng JavaScript.
6.  **[DOM Manipulation Functions (Hàm Thao Tác DOM) (!):](https://www.truongcongly.com/2023/11/ham-ham-thao-tac-voi-dom-trong.html)**
    -   `document.getElementById(id)`: Lấy phần tử theo id.
    -   `document.querySelector(selector)`: Lấy phần tử đầu tiên phù hợp với selector.
    -   `document.querySelectorAll(selector)`: Lấy tất cả các phần tử khớp với một CSS selector.
    -   `document.getElementsByClassName(className)`: Lấy tất cả các phần tử DOM có cùng class.
    -   `document.getElementsByTagName(tagName)`: Lấy tất cả các phần tử DOM có cùng thẻ HTML.
    -   `document.createElement(tagName)`: Tạo một phần tử DOM mới.
    -   `parentElement.appendChild(node)`: Thêm một nút con vào một phần tử.
    -   `parentElement.removeChild(node)`: Xóa một nút con khỏi một phần tử.
    -   `element.setAttribute(name, value)`: Đặt giá trị cho thuộc tính của một phần tử.
    -   `element.getAttribute(name)`: Lấy giá trị của một thuộc tính của phần tử.
    -   `element.innerHTML`: Lấy hoặc gán nội dung HTML của phần tử.
    -   `element.innerText`: Lấy hoặc đặt nội dung văn bản của một phần tử.
    -   `element.classList`: Cho phép thêm, xóa, hoặc kiểm tra sự tồn tại của các lớp CSS trên phần tử.
    -   `element.style`: Cho phép thao tác với các thuộc tính kiểu dáng của phần tử.
7.  **[Event Handling Functions (Hàm Xử lý Sự kiện) (!):](https://www.truongcongly.com/2023/11/tong-hop-ham-xu-ly-su-kien-trong-javascript.html)**
    -   `addEventListener(event, function)`: Gắn một hàm xử lý sự kiện cho một phần tử.
    -   `removeEventListener(event, function)`: Loại bỏ hàm xử lý sự kiện khỏi một phần tử.
8.  **[Number Functions (Hàm Số) (!):](https://www.truongcongly.com/2023/11/ham-number-trong-javascript.html)**
    -   `parseInt(string, radix)`: Chuyển đổi chuỗi thành số nguyên theo cơ số (radix) chỉ định.
    -   `parseFloat(string)`: Chuyển đổi chuỗi thành số thực.
    -   `isNaN(value)`: Kiểm tra xem giá trị có phải là NaN (Not a Number) hay không.
    -   `isFinite(value)`: Kiểm tra xem giá trị có phải là số hữu hạn hay không.
9.  **[RegExp Functions (Hàm Biểu thức Chính quy) (!):](https://www.truongcongly.com/2023/11/ham-bieu-thuc-chinh-quy-trong-javascript.html)**
    -   `test(string)`: Kiểm tra xem một chuỗi có khớp với biểu thức chính quy hay không.
    -   `exec(string)`: Tìm kiếm một chuỗi cho biểu thức chính quy và trả về kết quả.
10. **[Global Functions (Hàm Toàn cục) (!):](https://www.truongcongly.com/2023/11/mot-so-ham-toan-cuc-trong-javascript.html)**
    -   `setTimeout(function, delay)`: Thiết lập một hàm để chạy sau một khoảng thời gian xác định.
    -   `setInterval(function, delay)`: Thiết lập một hàm để chạy lặp lại sau mỗi khoảng thời gian xác định.
    -   `clearTimeout(timeoutID)`, `clearInterval(intervalID)`: Hủy bỏ việc chạy một hàm đã được lên lịch trước đó.
11. **[Console Functions (Hàm Console) (!):](https://www.truongcongly.com/2023/11/ham-console-trong-javascript-javascript.html)**
    -   `console.log(message)`: In ra thông điệp vào console.
    -   `console.error(message)`: In ra thông điệp lỗi vào console.
    -   `console.warn(message)`: In ra thông điệp cảnh báo vào console.
12. **[Promise Functions (Hàm Promise) (!):](https://www.truongcongly.com/2023/11/ham-promise-trong-javascript.html)**
    -   `Promise(resolve, reject)`: Tạo một đối tượng promise với các hàm resolve và reject.
    -   `then(onFulfilled, onRejected)`: Xử lý kết quả hoặc lý do thất bại của một promise.
13. **[Object Methods (Phương thức Đối tượng) (!):](https://www.truongcongly.com/2023/11/cac-phuong-thuc-object-trong-javascript.html)**
    -   `Object.keys(obj)`: Trả về một mảng chứa tất cả các khóa của đối tượng.
    -   `Object.values(obj)`: Trả về một mảng chứa tất cả các giá trị của đối tượng.
    -   `Object.entries(obj)`: Trả về một mảng chứa các cặp [khóa, giá trị] của đối tượng.


### Toán tử trong JS
> Nguồn bài viết [200lab.io](https://200lab.io/blog/toan-tu-trong-javascript)

Trong JavaScript có các loại toán tử cơ bản cần phải ghi nhớ gồm:

-   Toán tử số học - Arithmetic Operators
-   Toán tử so sánh - Comparison Operators
-   Toán tử logic - Logical Operators
-   Toán tử gán - Assignment Operators
-   Toán tử ba ngôi - Conditional Operators

### Toán tử số học - Arithmectic Operators

| Toán tử - Mô tả |
| + - Cộng |
| - - Trừ |
| * - Nhân |
| ** - Lũy thừa (**ES6**) |
| / - Phép chia |
| % - Phép chia lấy phần dư |
| ++ - Tăng một giá trị |
| -- - Giảm một giá trị |

Cùng đi vào ví dụ cho dễ hiểu nhé 😁, phép `+` , `-`, `*` thì quá quen thuộc rồi nên mình không đề cập đến nó nhé 😆

Giải thích một chút nhé 😁, `c++` bằng `1` là vì ta log `c` rồi mới tăng lên một, đó là ý nghĩa khi đặt toán tử `++` sau một biến, còn đối với `++d` là tăng `d` lên `1` rồi mới log `d` do đó `d = 2`. Đây là ý nghĩa của việc đặt toán tử `++` trước một biến, tương tự với toán tử -- nhé 😉.

`f = 5` mà `f` chia lấy dư cho `2` mà cho kết quả bằng `1` là do trong JavaScript tự động làm tròn số lên đó nha 😁.

### Toán tử so sánh - Comparison Operators

| Toán tử - Mô tả |
| == - So sánh bằng theo giá trị |
| === - So sánh bằng theo cả kiểu dữ liệu và giá trị |
| != - So sánh không bằng theo giá trị |
| !== - So sánh không bằng theo cả kiểu dữ liệu và giá trị |
| > - So sánh lớn hơn |
| < - So sánh bé hơn |
| >= - So sánh lớn hơn hoặc bằng |
| <= - So sánh bé hơn hoặc bằng |
| ? - Toán tử ba ngôi |

Giải thích nè 😁, `a == b` trả về `true` là vì về mặt giá trị `a` và `b` đều bằng `1` nên `a !=b` trả về `false` luôn nè, tuy nhiên về mặt kiểu dữ liệu lại khác nhau (một thằng kiểu `number` một thằng kiểu `string`) do đó `a === b` trả về `false` và `a !== b` là `true`.

### Toán tử logic - Logical Operators

| Toán tử - Mô tả |
| && - Toán tử và (còn được gọi là toán tử **AND**) |
| || - Toán tử hoặc (còn được gọi là toán tử **OR**) |
| ! - Toán tử phủ định |

Đối với toán tử `&&` thì nếu toán hạn cả hai vế đều khác 0 thì sẽ trả về `true` còn ngược lại thì nó sẽ trả về `false`. Toán tử `||` thì khác, nếu một trong hai toán hạng khác `0` thì sẽ trả về `true`. Với toán tử `!` là toán tử phủ định, `(a < b)` là đúng sẽ trả về `true` nhưng gặp toán tử `!` thì phủ định của `true` là `false` 😉.

### Toán tử gán - Assignment Operators

| Toán tử - ví dụ - Tương đương |
| = - a = b - a = b |
| += - a += b - a = a + b |
| -= - a -= b - a = a - b |
| *= - a *= b - a = a * b |
| /= - a /= b - a = a / b |
| %= - a %= b - a = a % b |
| **= - a **= b - a = a**b |

### Toán tử ba ngôi - Conditional Operators

Toán tử 3 ngôi là một toán tử vô cùng hữu ích trong JavaScript, toán tử này giống  như là bản rút gọn của câu lệnh `if-else`

| Toán tử - Mô tả |
| ?: - Điều kiện ? giá trị 1 : giá trị 2 |

Đơn giản thôi, nếu điều kiện trước dấu `?` trả về `true` thì sẽ trả về `giá trị 1` còn `false` thì sẽ trả về `giá trị 2`

### Toán tử chuỗi (String Operator) - khi nào sử dụng toán tử chỗi

> Nguồn bài viết [Bài này](https://truonghoclaptrinh.com/khoa-hoc/javascript/toan-tu-javascript-javascript-operators-99.html)

**So sánh chuỗi**: Tất cả các toán tử so sánh ở trên (trong bài viết gốc) cũng có thể được sử dụng trên chuỗi:

```js
let text1 = "A";
let text2 = "B";

let result = text1 < text2;
```

Lưu ý rằng các chuỗi được so sánh theo thứ tự bảng chữ cái:

```js
let text1 = "20";
let text2 = "5";
let result = text1 < text2;
```

Dấu `+` cũng có thể được sử dụng để cộng (nối) chuỗi:

```js
let text1 = "John";
let text2 = "Doe";
let text3 = text1 + " " + text2;  // John Doe
```

Toán tử gán `+=` cũng có thể được sử dụng để thêm (nối) chuỗi:

```js
let text1 = "What a very ";
text1 += "nice day";  // What a very nice day
```

**Cộng số và chuỗi**: Cộng hai số sẽ trả về tổng, nhưng cộng một số và một chuỗi sẽ trả về một chuỗi:

```
let x = 5 + 5;  // 10
let y = "5" + 5;  // 55
let z = "Hello" + 5;  // Hello5
```

### Kiểu dữ liệu Boolean 

### Tất tần tật về câu điều kiện `if-else` trong JS

> Nguồn [homiedev.com](https://homiedev.com/cau-lenh-if-else-trong-javascript/)

Trong lập trình, có thể nảy sinh các tình huống mà bạn muốn làm một việc nào đó **tùy theo từng trường hợp** cụ thể. Ví dụ, đặt điểm A, B hoặc C dựa theo điểm trung bình của một học sinh.

Trong những tình huống như vậy, bạn có thể sử dụng câu lệnh `if...else` của JavaScript.

Trong JavaScript, có ba dạng của câu lệnh `if...else`.

1.  if statement
2.  if...else statement
3.  if...else if...else statement

**Cú pháp của câu lệnh if** là:

```
if (condition) {
    // Phần thân của câu lệnh if
}
```

Với câu lệnh if, bên trong dấu ngoặc đơn (parenthesis) `()` ta sẽ truyền điều kiện - condition vào trong đó.

1.  Nếu điều kiện có kết quả là *true*, code trong phần thân của if sẽ được thực thi (execute).
2.  Nếu điều kiện có kết quả là *false*, code trong phần thân của if sẽ được bỏ qua (Không chạy vào phần thân).

Ví dụ:

```
// Kiểm tra số dương

const number = 3;

// Nếu number lớn hơn 0 sẽ chạy code trong {}
if (number > 0) {
 // Phần thân của câu lệnh if
  console.log("Đây là một số dương");
}

console.log("Chương trình của bạn đã chạy đến dòng này 🤗");
```

Ở ví dụ trên nếu `number` là một số dương thì `number > 0` là *true* thì code trong phần thân của câu lệnh if hay code trong `{}` sẽ được thực thi. Sau khi thực thi code trong phần thân của `if`, chương trình tiếp tục chạy từ trên xuống như bình thường 😄.

Kết quả sẽ như sau:

```
Đây là một số dương
Chương trình của bạn đã chạy đến dòng này 🤗
```

Đoạn code trên, Javascript đã chạy lần lượt từ trên xuống. Nếu gặp điều kiện `if` nó sẽ kiểm tra giá trị mà bạn truyền vào trong `()` và nếu kết quả là *true* thì code trong `{}` sẽ được thực thi. Ngược lại nếu là *false* thì Javascript sẽ bỏ qua đoạn code trong phần thân của `if`.

Giả sử chúng ta nhập một số âm:

```
const number = -3;

// Kiểm tra -3 < 0 nên không chạy code trong phần thân của if
if (number > 0) {
  // -3 < 0 nên không chạy vào đây 🤪
  console.log("Đây là một số dương"); // Không chạy ở đây luôn 🥱
  // Không chạy ở đây nữa 😆
}

console.log("Chương trình của bạn đã chạy đến dòng này 🤗");
```

Kết quả sẽ như sau:

```
Chương trình của bạn đã chạy đến dòng này 🤗
```

Do dòng `console.log("Chương trình của bạn đã chạy đến dòng này 🤗");` nằm ngoài phần thân của câu lệnh if, nên nó luôn được thực thi.

Các toán tử so sánh và logic sẽ được sử dụng trong các điều kiện. Để tìm hiểu thêm về các toán tử so sánh và logic, bạn có thể xem lại bài viết trước để tìm hiểu thêm nhé ^^.

**if...else statement**: Một câu lệnh if còn có thể kết hợp với `else`. Cú pháp của câu lệnh `if...else` là:

```
if (viết điều kiện ở đây) {
    // Nếu điều kiện là *true* thì chạy vào đây 🎉
} else {
   // Nếu điều kiện là *false* thì chạy vào đây 🥱
}
```

Có đúng thì sẽ có sai, nếu bộ đồ này đẹp mà giá cả ok thì mình mua, còn không thì mình mua chỗ khác 😂. Câu lệnh `if...else` cũng hoạt động y như vậy.

Nếu điều kiện trả kết quả là *true*:

1.  code trong phần thân của **if** được thực thi
2.  code trong phần thân của **else** bị bỏ qua khỏi quá trình thực thi (Vì đã thực thi tại if)

Nếu điều kiện trả kết quả là *false*:

1.  code trong phần thân của **else** được thực thi
2.  code trong phần thân của **if** bị bỏ qua khỏi quá trình thực thi (Vì đã thực thi tại else)

Ví dụ:

```
// Kiểm tra số truyền vào là dương hay âm hoặc 0

const number = 3;

// kiểm tra nếu number > 0 thì chạy vào trong if và bỏ qua else
if (number > 0) {
  console.log("Bạn vừa nhập số dương");
}
// nếu số truyền vào <= 0, chạy vào else
else {
  console.log("Số vừa nhập có thể là số âm hoặc 0");
}

console.log("Chương trình chạy đến đây rồi nè 🤗");
```

Kết quả chương trình trên sẽ là:

```
Bạn vừa nhập số dương
Chương trình chạy đến đây rồi nè 🤗
```

Bạn thấy nếu nhập số dương thì chương trình sẽ chạy vào phần thân `if` và phần thân `else` sẽ bị bỏ qua. Nếu ta nhập số < 0 thì chương trình sẽ chạy vào phần thân `else` và bỏ qua mọi thứ trong `if`.

Kết quả khi nhập số âm sẽ là:

```
Số vừa nhập có thể là số âm hoặc 0
Chương trình chạy đến đây rồi nè 🤗
```

Chương trình sẽ vẫn chạy từ trên xuống dưới 😊.

**if...else if statement**: Câu lệnh `if...else` được sử dụng để thực thi một khối code trong số hai lựa chọn (Không được cái này thì được cái kia). Tuy nhiên, nếu bạn muốn có nhiều hơn hai lựa chọn (Không được cái này thì được cái kia, hoặc được cái kia), thì chúng ta có thể dùng `if ... else if ... else`.

Cú pháp của câu lệnh if ... else if ... else là:

```
if (condition1) {
    // code block 1
} else if (condition2){
    // code block 2
} else {
    // code block 3
}
```

1.  Nếu *condition1* kết quả là *true*, khối code 1 được thực thi.
2.  Nếu *condition1* kết quả là *false*, thì kiểm tra *condition2*.
3.  Nếu *condition2* kết quả là *true*, khối code 2 được thực thi.
4.  Nếu *condition2* kết quả là *false*, chạy vào khối code 3 😋.

Ví dụ:

```js
// Kiểm tra số truyền vào là dương, âm hoặc 0

const number = 0;

// kiểm tra nếu number > 0 thì chạy vào trong if và bỏ qua mấy câu lệnh dưới luôn
if (number > 0) {
  console.log("Bạn vừa nhập số dương");
}
// nếu số truyền vào < 0, chạy vào else if
else if (number < 0) {
  console.log("Này là số âm chứ còn gì nữa 🤩");
}
// Không phải số dương 😶, cũng không phải số âm 😥, chạy vào else thôi 🥱
else {
  console.log("Số vừa nhập là số 0");
}
```

Kết quả đoạn chương trình trên:

Giả sử bạn đã nhập `-3`, khi đó điều kiện kiểm tra đầu tiên > 0 sẽ trả kết quả là *false* (không chạy vào if). Sau đó, kiểm tra điều kiện thứ hai < 0, kết quả là true (-3 < 0) thì chương trình sẽ chạy vào khối trong điều kiện thứ hai và kết quả là: `Này là số âm chứ còn gì nữa 🤩`.

Tương tự nếu nhập số `0` thì 2 điều kiện trên không thỏa mãn điều kiện, do đó nó sẽ chạy vào khối code của `else`.

**Nested if...else**: Sau khi đã tìm hiểu về các câu lệnh trên, chúng ta có thể kết hợp chúng lại với nhau. Các câu lệnh có thể lồng nhau (nested) để thực hiện các đoạn mã theo từng trường hợp ^^.

```js
// Kiểm tra số truyền vào là dương, âm hoặc 0
const number = 3;

if (number >= 0) {
    if (number == 0) {
        console.log("Bạn vừa nhập số 0");
    } else {
        console.log("Bạn vừa nhập số dương");
    }
} else {
    console.log("Đây là số âm");
}
```

Giả sử ta nhập `3`. Trong trường hợp này, `number >= 0` là *true*, nên nó sẽ đi vào bên trong câu lệnh if.

Trong câu lệnh if, tiếp tục lại có các câu lệnh khác, `3 == 0` là *false* nên nó không chạy vào `if` mà chạy vào `else`. Kết quả sẽ là `Bạn vừa nhập số dương`.

> Nếu phần thân của if ... else **chỉ có một** câu lệnh, chúng ta có thể bỏ qua `{}` trong chương trình của mình.

Ví dụ, bạn có thể viết code ngắn lại như sau:

```js
if (number >= 0) {
    if (number == 0) console.log("Bạn vừa nhập số 0");
    else console.log("Bạn vừa nhập số dương");
} else {
  console.log("Đây là số âm");
  console.log("Bạn vừa nhập số " + number);
}
```

## Các kiểu dữ liệu JS
Bài viết này sẽ dài phết, mà siêu đỉnh

> Nguồn [Kiểu dữ liệu trong JavaScript](https://viblo.asia/p/kieu-du-lieu-trong-javascript-L4x5xLXg5BM) trên Viblo

Bài viết này là một phần của series [JavaScript dành cho người không mới](https://viblo.asia/s/javascript-danh-cho-nguoi-khong-moi-yEZkg8LgZQ0), giúp các bạn đã có kinh nghiệm code trong các ngôn ngữ khác nhanh chóng làm quen với JS.

Nếu được rất mong nhận được sự ủng hộ và đóng góp ý kiến của mọi người để hoàn thiện series.

## A. Data types

Trong JS có 6 kiểu dữ liệu cơ bản:

- Number
- Boolean
- String
- Null
- Undefined
- Object

![](https://images.viblo.asia/full/3b500a63-bb8b-4ee5-b0bb-619419a7e177.png)

Mặc dù JS là ngôn ngữ weak type, không có nghĩa là nó không có khái niệm kiểu dữ liệu. JS chỉ không phải chỉ định rõ ràng kiểu và có khả năng ép kiểu linh hoạt, nên nó được gọi là weak typing (kiểu yếu).

**Primitive types**

Trong 6 kiểu trên, 5 kiểu đầu còn được gọi là primitive types (kiểu nguyên thủy), và kiểu object là non-primitive. Kiểu nguyên thủy chỉ thuần chứa dữ liệu, ví dụ.

```
let x = 10;
let s = "Hello";
let z = true;

```

Và các kiểu primitive cũng có thể có method và property như object, nhưng thực sự không phải. Đó là trick của JS, khi chúng ta dùng tới bất kì property hoặc method nào, JS sẽ biến đối tượng primitive thành một wrapper. Wrapper là kiểu primitive, được gói thành một object và sử dụng như object, do đó nó có thuộc tính và phương thức.

```
let x = new Number(10);
let s = new String("Hello");
let z = new Boolean(true);

```

Tuy nhiên, không nên sử dụng dạng như trên. Nó vừa gây rối code, vừa dài dòng không cần thiết, lại vừa sinh ra một số vấn đề khác. Ví dụ như phép so sánh hai kiểu wrapper sẽ luôn trả về false, vì JS không so sánh value chứa bên trong. Nếu bạn không hiểu rõ, bạn sẽ gặp lỗi. Do đó, primitive thì cứ dùng như bình thường thôi.

Và đối với wrapper, có thể dùng method `valueOf()` để lấy ra nội dung primitive được gói bên trong.

**Object types**

Kiểu dữ liệu còn lại là object, có thể chứa thuộc tính (property) và phương thức (method). Object phải được khởi tạo bằng từ khóa new và Object constructor.

```
let obj = new Object();
...

```

Các phiên bản JS mới hơn cho phép sử dụng cú pháp dấu ngoặc {} để tạo object gọn gàng hơn.

```
let obj = {
    ...
}

```

Từ kiểu object, có thể phát sinh thêm nhiều kiểu object khác, như mảng (array) cũng là object, function cũng là object (mặc dù tên kiểu là function), Date cũng là object,...

## B. Number

### 1\. Overview

Number trong JavaScript dùng cho cả số nguyên (integer) và số thực (float), và luôn là số có dấu (signed). Kiểu dữ liệu được xác định trên giá trị gán cho nó (value) chứ không cần chỉ định rõ ràng.

```
let a = 5, b = 2.5;  // Khai báo nhiều biến trên cùng dòng
let c = 12e-3;  // Số thực dạng khoa học
let d = .25;  // Rút gọn cho 0.25
let e =
    10;  // Viết trên nhiều dòng

```

Vì không phân biệt số nguyên và số thực, nên có thể viết số nguyên dạng có chấm hoặc không chấm như nhau.

Số thực có thể viết dạng thập phân hoặc khoa học, số dạng `0.abc` được viết gọn lại thành `.abc`.

```
let x = 0xff;
let y = 017;

```

Có thể viết số dạng hexa (hệ 16) với tiền tố `0x` ở đầu, hoặc một số phiên bản JS cho phép số hệ octal (hệ 8) bằng cách viết chữ số đầu tiên là 0. Do đó, không nên viết số với chữ số 0 ở đầu, trừ khi bạn hiểu rõ bạn đang làm gì.

### 2\. Operators

Các toán tử trong JS tương tự trong các ngôn ngữ khác. Từ ES6 trở đi có thêm toán tử \*\* để tính lũy thừa.

Phép cộng trong JS có điểm đặc biệt, là khi cộng một number với một string sẽ cho kết quả là string (phép nối chuỗi).

```
let x = 5;
let y = "Hi " + x;  // y = "Hi 5"

```

Đối với phép tính khác như nhân chia,... giữa hai string có nội dung số, JS sẽ cố gắng chuyển đổi thành số và thực hiện tính. Ví dụ.

```
let s1 = "2000";
let s2 = "10";
let result = s1 / s2;  // result = 200

```

### 3\. Special values

Hai value number đặc biệt trong JS là NaN (not a number) và Infinity. Hai giá trị đặc biệt này thuộc kiểu number, khi dùng typeof cho ra kết quả number.

```
let x = NaN;
let y = Infinity;
typeof x;  // number
typeof(y);  // number

```

**NaN value**

Giá trị NaN được trả về khi thực hiện phép tính không hợp lệ, chẳng hạn chia một chuỗi cho một số (chuỗi không có nội dung là số). Khi đó kết quả phép tính là NaN.

```
let x = 100 / "Apple";
isNaN(x);  // true

```

Sử dụng hàm `isNaN()` để kiểm tra xem một số có mang giá trị NaN hay không.

Trong những biểu thức có chứa NaN, thì kết quả cuối cùng là NaN. Nếu kết quả dạng chuỗi, JS sẽ chuyển đổi NaN thành chuỗi "NaN" và ghép lại cho phù hợp.

**Infinity value**

Số vô cực dương (Infinity) và vô cực âm (-Infinity) được trả về khi kết quả biểu thức quá lớn so với giới hạn của JS. Infinity cũng được trả về nhờ phép chia một số cho 0, hoặc tính toán biểu thức có Infinity.

```
let x = 5;
let y = 5 / 0;
isFinite(x);  // true
isFinite(y);  // false

```

Dùng hàm `isFinite()` để kiểm tra số có hữu hạn hay không, nếu là số vô hạn (Infinity và -Infinity) sẽ trả về false. NaN cũng trả về false.

### 4\. Number methods

Mặc dù number là kiểu primitive (nguyên thủy), nhưng JS thực hiện một số trick để làm number hoạt động tương tự object, nghĩa là có các thuộc tính (property) và phương thức (method).

Các property và method bên dưới không nhất thiết phải gọi từ biến number, có thể gọi từ value, const hoặc biểu thức tính ra number. Ví dụ.

```
let x = 123;
x.toString();
123.toString();
(100 + 23).toString();

```

### 5\. Number properties

Các thuộc tính bên dưới chỉ được truy cập qua Number, không phải qua biến, hằng hoặc biểu thức như method bên trên. Nếu cố tình vi phạm, thì kết quả trả về là undefined.

```
Number.MAX_VALUE;  // Ok
123.MAX_VALUE;  // Sai

```

Bên dưới là danh sách các thuộc tính. Có lẽ không cần nói nhiều nữa, chỉ cần đọc qua tên thôi các bạn cũng có thể hiểu được rồi.

```
Number.MAX_VALUE;
Number.MIN_VALUE;
Number.MAX_SAFE_INTEGER;
Number.MIN_SAFE_INTEGER;
Number.POSITIVE_INFINITY;
Number.NEGATIVE_INFINITY;
Number.NaN;
Number.EPSILON;

```

## C. Boolean

### 1\. Overview

Boolean lưu trữ hai giá trị đúng (true) và sai (false). Biến kiểu boolean có thể được dùng thay cho điều kiện trong các câu lệnh khác.

```
let b = false;
if (b) ...

```

Các biểu thức so sánh (comparison) và logic đều trả về một giá trị boolean.

### 2\. Truthy & falsy

Trong JS, mọi thứ đều có thể được xem như một kiểu boolean, và có hai giá trị là truthy và falsy:

- Falsy: chứa giá trị rỗng, ví dụ như 0, false, "", null, undefined và NaN
- Truthy: ngược lại các trường hợp trên, và thêm Infinity và -Infinity nữa.

Sử dụng toán tử `!!` phía trước một đối tượng sẽ biến nó thành Boolean, như ví dụ sau đây.

```
let x = 10, y = 0;
!!x;  // true
!!y;  // false

```

### 3\. Properties & methods

Boolean không có nhiều property và method, chủ yếu là hai method `toString()` (chuyển thành string) và `valueOf()` (lấy giá trị primitive - trong trường hợp này không có nhiều ý nghĩa).

### 4\. Boolean tricks

Một số trick liên quan tới boolean, giúp viết code nhanh hơn.

**Shorthand evaluate**

Thay vì viết.

```
if (<condition>)
    <statement>;

```

Thì có thể viết nhanh thành

```
<condition> && <statement>;

```

Trick này được thực hiện nhờ JS tối ưu hóa phép so sánh AND. Nếu vế trái `condition` là false, thì không thực hiện vế phải (tối ưu hơn), ngược lại `condition` là true thì phải xét tiếp vế phải `statement` nữa. Kết quả là `statement` chỉ được thực thi khi `condition` là true.

**Default value**

Đôi khi chúng ta muốn kiểm tra dữ liệu nhập vào, thường là kiểm tra dữ liệu có tồn tại hay không. Nếu có thì ok, nếu không có cần cho nó một giá trị mặc định (default value) thay thế. Do đó, chúng ta thường viết code như sau.

```
function saveFile(fileName) {
    if (fileName === "")
        fileName = "Noname.txt";
    ...
}

```

Với boolean trong JS, có thể rút gọn code trên thành thế này.

```
function saveFile(fileName) {
    fileName = fileName || "Noname.txt";
    ...
}

```

Giải thích là trong các phép so sánh logic, thì JS chuyển các phần thành boolean hết. Vế trái được kiểm tra có dữ liệu hay không, nghĩa là biến thành boolean. Nếu là true, thì không cần so sánh vế phải, toàn bộ phép OR trả về vế trái. Ngược lại nếu vế trái là false, nghĩa là không có dữ liệu, thì xét vế phải. Vế phải phép OR luôn là true (do là string có dữ liệu), nên lúc này giá trị trả về là vế phải.

Trong code nên, phép so sánh OR bắt JS lựa chọn: Nếu `fileName` có dữ liệu thì chọn nó, nếu không có dữ liệu thì chọn vế phải biểu thức là chuỗi `Noname.txt`.

**Number tricks**

Hai phép and và or cũng dùng đượ với các số, như sau.

```
// a && b: nếu a là truthy thì trả về b, nếu a là falsy thì trả về a
10 && 20 = 20;
0 && 20 = 0;

// a || b: nếu a là truthy thì trả về a, nếu a là falsy thì trả về b
10 || 20 = 10;
0 || 20 = 20;

```

## D. String

### 1\. Overview

String (chuỗi) dùng lưu dữ liệu dạng text. Nội dung của string được bao lại trong cặp nháy kép hoặc nháy đơn tùy trường hợp. Nếu nội dung chứa nháy kép, thì dùng nháy đơn, và ngược lại. Một số trường hợp code JS trong HTML event, thì phải bắt buộc dùng nháy đơn do nháy kép bị HTML attribute lấy rồi.

```
let s1 = "I'm Vu";  // Dùng nháy kép, vì bên trong có nháy đơn
let s2 = 'He said "ABC" yesterday';
    // Dùng nháy đơn, vì bên trong có nháy kép

```

Khác với các ngôn ngữ khác, việc truy cập ngoài phạm vi mảng hoặc chuỗi không xảy ra lỗi. Khi đó giá trị bên ngoài phạm vi có value là undefined.

Chuỗi về cơ bản là một mảng các kí tự, có index đếm từ 0.

**Escape character**

String không thể trực tiếp chứa một số kí tự, do không gõ được trên bàn phím hoặc gây nhầm lẫn (như trường hợp trên). Do đó cần thoát nó bằng cách chèn dấu \ (backslash) trước kí tự đặc biệt trên. Ví dụ.

```
let hello1 = "He said "ABC" yesterday";  // Sai
let hello2 = "He said \"ABC\" yesterday";  // Ok

```

Kí tự `"` trong chuỗi phải ghi thành `\"` gọi là escape character (escape sequense)

Ngoài ra các kí tự khác như tab ( `\t`), new line ( `\n`),... cũng được viết như trên, tương tự các ngôn ngữ khác.

**Line breaking**

Khi viết code không nên dài quá 80 kí tự một dòng, khi đó nên ngắt xuống dòng mới ngay tại toán tử, không ngắt giữa string như sau là sai.

```
let s1 =
    "Hello world";  // Ok
let s2 = "Hello
    world";  // Sai

```

Trong trường hợp nếu muốn ngắt ngay giữa string, nghĩa là chia chuỗi thành 2 dòng, thì phải viết như sau với dấu \ ở cuối dòng.

```
let s = "Hello \
    world";

```

ES6 có template string nhưng tạm thời không nói tới ở đây.

### 2\. Properties & methods

Vì phần property của string chỉ có mỗi cái length, nên mình gộp chung vào đây luôn.

**Length property**

Thuộc tính length trả về độ dài chuỗi, chú ý length là thuộc tính nên không có ngoặc () tham số.

```
let s = "ABC";
s.length;  // 3
s.length();  // Sai

```

**Access character**

Dùng hai method `charAt()` và `charCodeAt()` để lấy kí tự và mã tại một vị trí (index) nào đó.

```
let s = "ABC";
s[0];  // A
s.charAt(1);  // B
s.charCodeAt(2);  // 67 (mã của kí tự C là 67)

```

Chú ý chuỗi mã hóa UTF-16, nên có thể chứa tiếng Việt và có mã trong khoảng 0 - 65535.

ES5 giới thiệu cách dùng \[\] để truy xuất kí tự trong chuỗi, tương tự như mảng. Khi không tìm thấy kí tự, \[\] trả về undefined trong khi `charAt()` trả về rỗng.

Ngoài ra không thể thay đổi nội dung của string, vì JS string là immutable (bất biến). Mọi thay đổi vào string phải tạo chuỗi mới, do đó các method tiếp theo sẽ trả về chuỗi mới thay vì thay đổi trực tiếp lên chuỗi cũ.

Nếu cố tình thay đổi chuỗi, thì không có lỗi nhưng không có gì xảy ra cả.

**String concat**

Có nhiều cách nối chuỗi, gồm dùng phép +, dùng method `concat()` hoặc gom thành mảng rồi `join()`. Phần này chỉ nó về method `concat()`.

```
let s1 = "Hello";
let s2 = "world";
let s3 = s1 + " " + s2;  // Dùng phép cộng
let s4 = s1.concat(" ", s2;  // Dùng method concat
let s5 = [s1, s2].join(" ");  // Gom thành mảng rồi join thành chuỗi

```

**Trim method**

Dùng method này để loại bỏ các khoảng trắng (space) ở đầu và cuối chuỗi.

```
let s = "   This string has 3 spaces before and 2 spaces after  ";
s.trim();  // s = "This string ... after"

```

**Uppercase, lowercase**

Dùng hai method `toUpperCase()` và `toLowerCase()` để chuyển chuỗi thành hoa/thường toàn bộ.

```
let s = "Hello World";
s.toUpperCase();
s.toLowerCase();

```

**Find substring position**

Để tìm vị trí chuỗi con (substring) trong chuỗi đã cho thì có 3 method như sau. Các method này trả về index (vị trí) tìm thấy, nếu không có trả về -1.

```
let s = "Anh yeu anh";
s.indexOf("nh");  // Tìm thuận
s.lastIndexOf("nh");  // Tìm ngược
s.search("anh");  // Tìm bằng chuỗi
s.search(/anh/i);  // Tìm khớp regex

```

Đúng, đó là 3 method `indexOf()`, `lastIndexOf()` và `search()`. Khác biệt như sau:

- `indexOf()`, `lastIndexOf()` tìm chính xác chuỗi đã cho. `indexOf()` tìm từ trái sang phải, trong khi `lastIndexOf()` tìm ngược lại.
- `search()` hỗ trợ tìm chuỗi chính xác và cả regex, như ví dụ trên chuỗi `/anh/i` là một regex trong JS.

Ngoài ra `search()` không có param (tham số) thứ 2 là vị trí bắt đầu tìm, trong khi hai method còn lại có. Vị trí này chỉ định tìm từ index trở đi, không phải tìm từ đầu, giúp tối ưu hơn trong một số bài toán.

**Extract substring**

Dùng 3 method sau để trích xuất (extract) một phần chuỗi và trả về chuỗi mới.

```
let s = "Anh yeu anh";
s.substring(0, 3);  // Từ đầu - kết thúc tại index 3 (space)
s.substr(4, 3);  // Từ index 4 - và độ dài 3
s.slice(-3);  // Từ index -3 tới hết chuỗi

```

Method `substring()` không cho phép chỉ số là số âm, trong khi hai method còn lại cho phép. Method này cắt chuỗi từ start index và kết thúc tại end index (kí tự end không được lấy).

Method `substr()` bắt đầu tìm tại index và lấy ra chuỗi con có độ dài yêu cầu.

Method `slice()` khá giống `substring()`, nhưng chấp nhận chỉ số index âm (chỉ số âm sẽ đếm ngược từ cuối chuỗi lên đầu, -1, -2,....).

**Replace method**

Method `replace()` dùng để thay thế một phần của chuỗi bằng một chuỗi mới.

```
let s = "Anh yeu em cua anh";
s.replace("anh", "em");  // "Anh yeu em cua em"
s.replace(/anh/gi, "em");  // "em yeu em cua em"

```

Tham số 1 là chuỗi cũ, tham số 2 là chuỗi cần thay thế. `replace()` chấp nhận tham số 1 là chuỗi regex.

**Split method**

Dùng tách chuỗi thành một mảng các chuỗi con, dựa trên chuỗi phân tách (separator).

```
let s = "Viet Nam vo dich";
s.split("");  // Param chuỗi rỗng, tách từng kí tự
s.split(" ");  // Dấu phân cách là space, tách từng từ

```

Khi tách theo dấu phân cách như trên, sẽ gặp trường hợp nhiều dấu phân cách liền nhau. Khi đó split sẽ không hoạt động như mong đợi, ví dụ.

```
let s = "Viet   Nam";
s.split(" ");  // ["Viet", " ", "Nam"]

```

Để xử lý trường hợp nhiều dấu phân tách liền kề nhau, chúng ta sử dụng regex.

```
s.split(/ {1,}/);

```

Chuỗi regex trên đại diện cho 1 hoặc nhiều kí tự space liền kề, do đó regex có thể làm dấu phân tách chuỗi, kết quả cho ra sẽ đúng với những gì bạn nghĩ.

**ES6 new methods**

ES6 bổ sung thêm một số method xử lý string mới.

```
let s = "Hello world";
s.startsWith("Hello");  // true
s.endsWith(".");  // false
s.includes("o");  // true

```

Mặc dù các method này có thể được thay thế bằng cách so sánh `indexOf()`, nhưng dùng những method mới sẽ rõ ràng hơn.

## E. Array 1

### 1\. Overview

Array (mảng) cho phép lưu trữ nhiều giá trị trong một biến duy nhất (biến mảng). Các phần tử (element) trong array được truy cập theo chỉ số (index) tính từ 0.

Khác với nhiều ngôn ngữ khác, array trong JS cho phép chứa nhiều kiểu dữ liệu khác nhau. Và array không bị giới hạn số phần tử như một số ngôn ngữ strong type.

**Array declaration**

```
let primes = [2, 3, 5, 7];
let names = ["Vu", "John"];
let points = ["Vu", 10, "John", 9.5];
let empty = [];

```

Khai báo mảng gồm tên mảng và danh sách các value trong cặp \[\], cách nhau bởi dấu phẩy.

**Access array element**

Sử dụng chỉ số (index) để truy cập phần tử. Chỉ số được tính từ 0.

```
let third_prime = primes[2];

```

Nếu vượt quá phạm vi mảng, thì không có lỗi mà giá trị nhận được là undefined.

### 2\. Array and object?

**Array is an object**

Array thực sự là một object, nếu dùng typeof cho một mảng thì kết quả trả về là object.

Mảng trong JS dùng index truy cập các phần tử, đây là cách tốt nhất. Tuy nhiên tương tự các object khác, những phần tử có thể được truy cập thông qua tên thuộc tính.

**Creating array as an object**

Array thay vì được khai báo bằng cách gán giá trị thông thường, còn có thể được khai báo bởi từ khóa new và Array constructor.

```
let primes = new Array(2, 3, 5, 7);

```

Array constructor nhận vào danh sách các đối số làm giá trị khởi tạo cho mảng. Tuy nhiên, không nên dùng cách này vì rối rắm và gây lỗi. Ví dụ.

```
let a = new Array(10);

```

Nghĩa là gì, tạo mảng a có một giá trị 10, hay mảng a có 10 giá trị ban đầu??? Do đó, nên khai báo array với \[\] như bình thường thôi.

**Associative array**

Như đã nói, thì array trong JS thực sự là một object, nó sẽ có tên thuộc tính và value của thuộc tính đó. Thay vì truy cập value qua index, thì dạng object sẽ sử dụng tên thuộc tính để truy cập.

Do đó, array dạng này gọi là associative array, có index được đặt tên (named index).

Khi khai báo với \[\] thì chỉ tạo value và index. Để thực sự có tên thuộc tính, cần phải gán thêm giá trị cho mảng.

```
let age = [];
age["John"] = 19;
age["Josie"] = 20;

```

Lúc này, chúng ta có thể gọi `a["John"]` thay vì `a[i]` để truy cập value. Index là số, trong trường hợp này đã được đặt tên là "John".

Chú ý, lúc này một số method, property sẽ cho giá trị không đúng. Và nên hạn chế dùng array dạng này, nếu muốn có tên thuộc tính thì dùng object thay thế.

**Compare array**

Vì array là object, nên việc so sánh hai array thực chất là so sánh hai object. Mà so sánh hai object dù bằng cách nào đi nữa, bằng toán tử `==` hay `===` hoặc cả `Object.is()` thì đều là so sánh địa chỉ của chúng.

Hai object khác nhau sẽ có địa chỉ khác nhau, array cũng thế, nên các phép so sánh trên luôn trả về false.

Để so sánh nội dung hai array có giống nhau hay không, phải sử dụng các phép lặp kiểm tra từng phần tử và kèm thêm so sánh độ dài.

### 3\. Properties & methods 1

**Length property**

Trả về độ dài mảng. Chú ý `length` là thuộc tính, không phải method, nên viết như sau là sai.

```
primes.length;  // Ok
primes.length();  // Sai

```

`length` có một số hành vi kì lạ, cụ thể giá trị của length là giá trị index cao nhất có value + 1. Ví dụ mảng `[1, 2, 3, 4]` có chỉ số cao nhất là 3, nên `length` được tính là 3 + 1 = 4.

Điều này dẫn tới một vấn đề sau đây.

```
let a = [0, 1, 2, 3];
a[6] = 6;

```

Bạn nghĩ `a.length` sẽ có giá trị bao nhiêu? Nếu là 5 thì bạn sai rồi đó, bây giờ length là 7 (index cao nhất 6 + 1 = 7). Rõ ràng nó không đúng với logic suy nghĩ của mình, khi mảng chỉ có 5 phần tử mà length lại là 7.

Thực ra, cấu trúc mảng a bây giờ như sau.

```
[0, 1, 2, 3, empty, empty, 6]

```

Xuất hiện những khoảng empty (chưa có value) bên trong mảng, và nó làm thuộc tính `length` bị tính sai.

Do đó, thay vì gán trực tiếp như trên, nên sử dụng các method được trình bày tiếp theo đây để thêm phần tử vào mảng một cách an toàn.

**Unshift & push method**

```
let primes = [5];
primes.push(7);  // Thêm 7 vào cuối
primes.unshift(2, 3);  // Thêm 2, 3 vào đầu
    // Primes = [2, 3, 5, 7]

```

Hai method này thêm element vào mảng và trả về độ dài mảng mới. `push()` thêm vào cuối còn `unshift()` thêm vào đầu mảng (các phần tử khác bị đẩy về sau).

**Shift & pop method**

```
primes.pop();  // 7
primes.shift();  // 2
    // Primes = [3, 5]

```

Hai method này xóa element ra khỏi mảng, và return giá trị vừa xóa. `pop()` xóa ở cuối còn `shift()` xóa ở đầu (các phần tử khác bị dời về trước 1 đơn vị).

**Delete element**

```
delete primes[2];  // Xóa phần tử thứ 3

```

Xóa element của array nhưng không dời chỗ các element khác. Xem lại ví dụ vấn đề của length, thì có thể dùng lệnh này để xóa đi một phần tử, xem như nó chưa từng có value.

**Xóa toàn bộ mảng**

Có hai cách, gán cho nó mảng rỗng \[\] hoặc đặt `length` thành 0.

## F. Array 2

### 1\. Methods 2

**Array concat**

Dùng method `concat()` để gộp hai mảng thành 1, method trả về một mảng mới.

```
let a = ["Mike", "John"];
let b = ["Josie"];
let d = [];
let d = a.concat(b, c);  // d = ["Mike", "John", "Josie"]

```

Ngoài ra còn cách khác là dùng spread operator (ES6) để nối nhanh hơn, nhưng không bàn tới ở đây.

**Splice method**

Method này vừa xóa các phần tử đã có, vừa thêm các phần tử mới vào.

```
let primes = [2, 3, 4, 11];
primes.splice(2, 1, 5, 7);
    // Tại index 2, xóa 1 số (số 4), sau đó chèn thêm 2 số (5 và 7) vào
    // primes = [2, 3, 5, 7, 11]

```

Ngoài ra, `splice()` còn có thể dùng chỉ để xóa hoặc chèn thêm.

**Slice method**

Giống với string, method `slice()` dùng cắt một phần mảng và trả về mảng mới.

```
let primes = [2, 3, 5, 7, 11, 13];
let primes_smaller_than_10 = primes.slice(0, 4);  // Start 0, end 4
let primes_greater_than_10 = primes.slice(4);  // từ index 4 tới hết

```

`slice()` có thể có 1 hoặc 2 tham số, nếu tham số 2 không có thì nó sẽ cắt tới hết mảng. Nếu có đối số thứ 2 thì đó là vị trí dừng, phần tử ở vị trí end không được lấy.

Chú ý tên method là `slice()`, khác với `splice()` ở trên.

**Join & toString method**

Hai method này dùng chuyển mảng thành một chuỗi duy nhất.

```
let primes = [2, 3, 5, 7];
primes.toString();  // 2,3,5,7

```

`toString()` chuyển thành chuỗi, phân tách các phần tử bởi dấu phẩy và viết sát nhau. Phần tử cuối không có phẩy (no trailing comma).

Trong khi đó `join()` thì nâng cao hơn một chút. Method này nhận vào một chuỗi làm dấu phân tách tùy chỉnh, ví dụ muốn đẹp hơn thì dùng `join()`.

```
primes.join(", ");  // 2, 3, 5, 7

```

Nếu `join()` không có tham số thì giống như `toString()`.

**IndexOf, lastIndexOf method**

Dùng tìm vị trí một value trong mảng, tương tự như của string. Kết quả trả về là -1 nếu không tìm thấy, là vị trí nếu tìm thấy element.

Hai method trên nhận vào một tham số thứ 2, là vị trí bắt đầu tìm.

**Includes method**

Method trả về boolean, cho biết một value có tồn tại trong mảng hay không.

```
let a = [1, 2, 3];
a.includes(2);  // true
a.includes(4);  // false

```

Mặc dù có thể sử dụng phép so sánh `a.indexOf(2) !== -1` nhưng nên dùng `include()` vì làm code rõ ràng hơn.

**Fill method**

Method dùng để điền (fill) một phần tử vào một đoạn liên tục của mảng. Method nhận vào ba đối số:

- Đối 1 là value cần điền
- Đối 2 là vị trí bắt đầu (vị trí này được điền)
- Đối 3 là vị trí kết thúc (vị trí này không được điền)

Kết quả trả về là chính mảng đó.

```
let a = [0, 1, 2, 3, 4, 5];
a.fill(9, 2, 4);  // a = [0, 1, 9, 9, 4, 5]

```

Hai đối số sau có thể bỏ qua, nếu đối 3 bỏ qua thì điền từ vị trí bắt đầu cho tới hết, nếu hai đối sau bị bỏ qua thì điền toàn bộ mảng.

```
a.fill(9, 2);  // a = [0, 1, 9, 9, 9, 9]
a.fill(9);  // a = [9, 9, 9, 9, 9, 9]

```

### 2\. Array constructor methods

Những method với array bên trên như `concat()`, `join()` đều dùng thông qua biến array. Bên cạnh đó JS còn hỗ trợ thêm một số method trong `Array` constructor, có dạng `Array.method(var)` để xử lý một số thao tác trên mảng.

**Array.isArray method**

Dùng kiểm tra một đối tượng có phải array hay không.

```
let primes = [2, 3, 5, 7];
Array.isArray(primes);  // true

```

Vì array là object, nên chúng ta có cách thứ 2 là dùng toán tử `instanceof` như sau.

```
primes instanceof Array;  // true

```

Ngoài ra còn có một cách là tìm chữ "Array" trong code constructor (thuộc tính constructor) của biến đó. Nhưng chúng ta không dùng cách này vì hơi nhảm và chậm.

**Array.of method**

Method `Array.from()` nhận vào một số lượng đối số bất kì và trả về một mảng mới. Ví dụ hai lệnh sau là tương đương.

```
let a1 = [1, 2, 3];
let a2 = Array.of(1, 2, 3);

```

**Array.from method**

Method `Array.from()` lấy các phần tử trong một thứ giống mảng và trả về một mảng mới. Nói nôm nay là method này biến một danh sách giống mảng thành một mảng. Ví dụ như bên dưới, `document.getElementsByTagName()` trả về một HTMLcollection, và dùng `Array.from()` để tạo một mảng từ nó.

```
let a = document.getElementsByTagName('img');
let b = Array.from(a);

```

Cách thứ hai là nó cũng hoạt động như method `map()`, dùng để map phần tử từ mảng sang mảng nhưng với giá trị được tính toán khác đi (ví dụ mỗi phần tử nhân đôi). Phần method `map()` phần sau sẽ được bàn tới.

```
let a = [1, 2, 3];
let b = Array.from(a, function (value) {
    return value * 2;
});

```

### 3\. Sorting

**String sort**

Array có hai method để sắp xếp và đảo ngược mảng là `sort()` và `reverse()`.

```
let primes = [5, 3, 7, 2];
primes.sort();   // [2, 3, 5, 7]
primes.reverse();  // [7, 5, 3, 2]

```

`sort()` sắp xếp tăng dần, nếu muốn giảm dần thì dùng thêm `reverse()` để đảo lại.

Nhưng có vấn đề, `sort()` mặc định sẽ sắp xếp chuỗi (string sort), nên các số bị xếp sai (ví dụ 11 nhỏ hơn 2). Do đó, để sắp xếp các mảng số thì cần dùng numberic sort như bên dưới.

**Numberic sort**

Ở đây chúng ta cũng dùng method `sort()` với 1 tham số là hàm callback tùy chỉnh cách so sánh, gọi là compare function. Function này nhận vào hai số, và kết quả trả về sẽ quyết định cách sort.

```
primes.sort(function(a, b) { return a - b; });

```

Kết quả trên cho mảng sắp xếp tăng dần. Để xếp giảm dần, không cần dùng `reverse()` trong trường hợp này, chỉ cần sửa `return a - b` thành `return b - a` trong code trên là được.

### 4\. Find max, min

Tìm max, min trong mảng nhanh chóng thì dùng method `Math.max()` và `Math.min()`. Chú ý không gọi như cách bình thường được, vì các method trên không nhận mảng, do đó cần gọi với `apply()` như sau.

```
Math.max.apply(null, primes);
Math.min.apply(null, primes);

```

Tham số null không cần quan tâm, vì chúng ta không truyền object gì vào cho `apply()` cả.

* * *

## G. Array iteration methods

### 1\. Overview

ES5 có thêm một số iteration methods, là những method dùng để lặp, duyệt qua tất cả phần tử của iterable object, hiểu đơn giản là những đối tượng có thể lặp qua (iterable). Trong phần này chỉ xét tới array.

Các iteration method đều yêu cầu truyền 1 param dạng callback function. Function này có dạng như sau.

```
function(value) {}  // Dạng rút gọn
function(value, index, array) {}  // Dạng đủ

```

Qua mỗi lần duyệt một phần tử, thì thông tin sẽ được cập nhật và hàm callback trên được gọi một lần, với thông tin mới. Do đó, chúng ta đặt các xử lý bên trong chúng, và return về một giá trị phù hợp với chức năng từng method.

Nếu vẫn chưa hiểu, không sao cả, hãy đi vào ví dụ bên dưới.

Không nhất thiết các method này duyệt hết mảng, một số method chỉ duyệt đủ điều kiện là dừng ngay, như `some()` hoặc `every()`.

### 2\. Iteration methods

**Array looping**

Để lặp qua các phần tử của mảng thì chúng ta có thể dùng vòng lặp for như bình thường, lặp qua các index và truy cập phần tử qua index.

Hoặc ES5 có thêm vòng lặp for of như sau.

```
let a = [1, 2, 3];
for (let e of a)
    ...

```

Trong mỗi lần lặp như vậy e sẽ lần lượt mang từng giá trị của phần tử trong mảng. Nhược điểm cách này là không biết được index cua phần tử là bao nhiêu, muốn biết cần thêm vài dòng code rườm rà nữa.

Do đó, method `forEach()` ra đời như một cách thức nâng cao hơn để lặp mảng.

```
a.forEach(function(value, index, array) {
    ...
});

```

Chú ý tới function ẩn danh (không có tên) có chứa 3 tham số `value, index, array`. Các bạn sẽ gặp lại nó trong suốt phần này.

Hàm callback trên có 3 tham số, nhưng có thể bỏ đi hai tham số sau nếu không cần thiết, chỉ cần giữ lại value. Với method `forEach()` có tới 3 tham số như trên, chúng ta có thể vừa biết value, vừa biết được index đang ở vị trí nào, vừa có thể truy cập array. Quá tiện phải không, nhưng bù lại thì tốc độ sẽ chậm hơn.

**Map method**

Tạo mảng mới có độ dài giống mảng ban đầu, nhưng các phần tử có giá trị được tính toán, biến đổi mới lại theo một cách nào đó.

```
let a = [1, 2, 3, 4];
let b = a.map(function(value) {  // Đã rút gọn callback
    return value * 2;
});
// b = [2, 4, 6, 8]

```

Method `map()` tạo array mới, với từng phần tử trong array cũ sẽ được áp dụng một số phép biến đổi (trong code là nhân 2) để thành phần tử mới. Thao tác này gọi là map.

Chú ý return trong callback là return từng giá trị mới cho mảng mới được tổng hợp.

**Filter method**

Trả về mảng mới, gồm các phần tử nào trong mảng cũ khớp với điều kiện gì đó.

```
let primes = [2, 3, 5, 7, 11, 13];
let primes_smaller_than_10 = primes.filter(function(value) {
    return value < 10;
});
// b = [2, 3, 5, 7]

```

Method `filter()` duyệt từng phần tử, với mỗi phần tử xét xem nó có được thêm vào mảng mới hay không.

Return của filter là return boolean, true thì phần tử được nhận, false thì phần tử bị bỏ qua.

**Every, some method**

Toàn bộ method trả về boolean, `every()` kiểm tra mảng có tất cả phần tử hợp điều kiện, trong khi `some()` chỉ cần một phần tử khớp điều kiện cho là ok.

```
let primes = [2, 3, 5, 7, 11];
let is_odd_all = primes.every(function(value) {
    return value % 2 === 1;
});  // false
let any_bigger_than_10 = primes.some(function(value) {
    return value > 10;
});  // true

```

Cả hai method duyệt từng element, `every()` tất cả element phải return true thì every mới true, còn `some()` chỉ cần một element true là true ngay.

**Find, findIndex method**

Dùng trả về vị trí một value trong mảng. `find()` trả về value, trong khi `findIndex()` trả về index của value tìm thấy (phần tử đầu tiên). Nếu không có, `find()` trả về undefined và `findIndex()` trả về -1.

Lưu ý "find" ở đây không chỉ đơn thuần là tìm một giá trị trong mảng, mà chính xác hơn nó tìm phần tử đầu tiên khớp với một điều kiện nào đó.

```
let a = [3, 5, 2, 13, 4];
let pos = a.findIndex(function(value) {
    return value > 10;
});
// pos = 3

```

Bên trong callback, chúng ta return một boolean mô tả điều kiện tìm thấy, ví dụ như bằng 5 (tìm số 5 trong mảng), nhỏ hơn 5 (tìm số đầu tiên nhỏ hơn 5),...)

Nếu đang tìm giữa chừng mà tìm thấy value khớp điều kiện, thì dừng lại luôn không xét nữa.

**Reduce, reduceRight**

Reduce là thao tác từ một array nhiều phần tử "giảm" (reduce) xuống còn một giá trị duy nhất. Thường dùng cho tính tổng tất cả phần tử trong mảng, ta gọi là "giảm dần mảng thành một tổng" thay vì "tính tổng của toàn bộ mảng".

`reduce()` và `reduceRight()` hơi khác với các iteration method khác, là callback của nó có thêm một tham số `prevValue` đầu tiên.

```
let a = [1, 2, 3, 4, 5];
let sum = a.reduce(function(prevValue, value, index, array) {
    return prevValue + value;
});
// sum = 15

```

Giá trị `prevValue` là giá trị được "gom" lại trước đó. Trong đoạn code trên thì giá trị trước đó được cộng thêm value vào, và return thành giá trị mới. Giá trị này trong vòng lặp tiếp theo sẽ trở thành `prevValue`.

Tóm lại, sau khi lặp hết mọi phần tử, `prevValue` từ 0 được cộng dần lên, và cuối cùng thành tổng của mảng. Tổng này được trả về cho method `reduce()` hoặc `reduceRight()`.

Hai method trên còn nhận vào param 2 phía sau hàm callback, là khởi tạo giá trị ban đầu cho `prevValue`. Và đặc biệt, JS rất thông minh khi dùng phép cộng (tính tổng) thì mặc định giá trị ban đầu là 0, nhưng khi dùng phép nhân (tính tích) thì giá trị ban đầu lại là 1. Thông minh chưa ![😐](https://twemoji.maxcdn.com/v/14.0.2/72x72/1f610.png).

`reduceRight()` tương tự `reduce()`, nhưng được chạy từ cuối mảng lên đầu, vậy thôi.

### 3\. Arrow function

Thường thì người ta sẽ dùng arrow function (ES6) trong trường hợp này để viết code ngắn hơn. Ví dụ thay vì.

```
let b = a.map(function(value, index, array) {
    ...
});

```

thì sẽ viết với arrow function là

```
let b = a.map((value, index, array) => { ... });

```

hoặc

```
let b = a.map(value => { ... });

```

Nếu bạn chưa biết arrow function thì đừng lo, các bài sau sẽ có nói tới. Trong các code phía trên mình viết function callback dạng thường cho dễ hiểu.

## H. Date

### 1\. Date object

Để thực hiện các thao tác với thời gian, chúng ta sử dụng đối tượng Date. Chú ý thời gian ở đây gồm ngày tháng (date) và thời gian (time).

Có 4 cách để tạo date object, bằng các tham số khác nhau được truyền cho Date constructor.

**Current datetime**

```
let current = new Date();

```

`Date()` constructor không có param sẽ lấy thời gain hiện tại lưu vào biến. Chú ý thời gian lưu vào là cố định, không tự động thay đổi trừ khi bạn cập nhật lại cho nó.

**Custom datetime**

```
let birthday = new Date(2001, 7, 27, 6, 30, 0, 0);

```

Nhận 7 tham số lần lượt là năm (year), tháng (month), ngày (day), giờ (hour), phút (minute), giây (second) và mili giây (milisecond - msec).

Có hai chú ý sau:

- Năm nếu có 1 hoặc 2 chữ số, thì hiểu là năm 19AB.
- Tháng trong JS đếm từ 0, do đó số 7 sẽ là tháng 8.

**Miliseconds**

JS thực sự lưu trữ thời gian dưới dạng số nguyên cực lớn, là số mili giây trôi qua từ thời điểm gốc.

Thời điểm được chọn làm mốc của JS là 1/1/1970, 00:00:00.

```
let root = new Date(0);

```

Số miliseconds có thể là số âm, như vậy thì thời điểm sẽ được lùi về quá khứ.

**String datetime**

JS cũng cho phép nhận chuỗi ngày tháng và tự động phân tích ra thời gian phù hợp. Chuỗi datetime này phải tuân theo một số chuẩn nhất định để JS nhận diện chính xác, đọc thêm phần tiếp theo.

```
let birthday = new Date("August 27, 2001 06:30:00");

```

### 2\. Date format

JS cho phép nhận diện chuỗi ngày tháng theo một quy tắc nhất định, gồm ngày chuẩn ISO, ngày dài (long date) hoặc ngày ngắn (short date) được chấp nhận.

**ISO date**

```
2001-08-27
2001-08
2001

```

Bên trên là một số ví dụ chuỗi ISO date được chấp nhận.

```
2001-08-27T06:30:00Z

```

Thời gian trên có chữ "T" phân tách ngày tháng và thời gian. Chữ "Z" ở cuối cho biết đây là thời gian UTC, múi giờ GMT (0). Hoặc có thể bỏ Z đi và chỉ định độ lệch múi giờ như sau.

```
2001-08-27T06:30:00+07:30

```

Thay chữ "Z" bằng `+hh:mm` hoặc `-hh:mm` đều được.

**Long date**

Long date trong JS có dạng `MMM DD yyyy`, trong đó dùng dấu space để tách ra. Năm luôn ở cuối cùng và tháng và ngày có thể đổi chỗ cho nhau.

```
let d1 = new Date("August 27 2001");
let d2 = new Date("27 Aug 2001");

```

Tháng có thể viết tắt hoặc đầy đủ đều được, và không phân biệt hoa thường.

**Short date**

Cú pháp chuỗi short date trong JS chấp nhận có dạng `MM/dd/yyyy`.

### 3\. Date get, set methods

Date object có một số method dạng `get_()` và `set_()`, dùng để đọc (get) hoặc thay đổi (change) các thành phần của thời gian.

**Get methods**

```
let d = new Date("2001-08-27");
d.getTime();  // Số miligiây
d.getFullYear();  // 2001
d.getMonth();  // 7, vì tháng 8 là index 7
d.getDate();  // 1-31, date là ngày trong tháng
d.getDay()  // 0-6, day là ngày trong tuần, Chủ nhật là 0

```

Chú ý các method lấy thời gian cần có `s`.

```
d.getHours();
d.getMinutes();
d.getSeconds();
d.getMiliseconds();

```

Ngoài ra còn có các method dạng `getUTC_()` tương tự để lấy thời gian tại mốc GMT.

**Set methods**

Tương tự như `get_()`, nhưng nhận vào các tham số là giá trị mới để gán, thay vì để trống. Ví dụ

```
let d = new Date();
d.getMonth();  // return 7
d.setMonth(7);  // no return

```

### 4\. Date actions

**Display date**

Method `toString()` chuyển date object thành một chuỗi mô tả thời gian, gồm thứ, tháng ngày, năm, giờ, phút, giây, (không có miligiây), múi giờ và tên múi giờ.

Bên cạnh đó ocnf có method `toUTCString()` để lấy chuỗi thời gian tại GMT.

**Get miliseconds**

Nếu chri muốn lấy số miligiây của một chuỗi ngày cụ thể mà không cần tạo date object, có thể dùng method `Date.parse()` để parse chuỗi và lấy ra số miliseconds.

```
let msec = Date.parse("August 27, 2001");
let d = new Date(msec);

```

**So sánh**

Vì các date object lưu trữ số mili giây, nên có thể xác định thời điểm nào trướ thời điểm nào bằng cách so sánh.

**Current time**

Khi bạn muốn cập nhật lại thời gian hiện tại cho date object, sử dụng method `Date.now()` và method `setTime()` của đối tượng cần update như sau.

```
let d = new Date("2001");
d.setTime(Date.now());

```

`Date.now()` trả về số mili giây hiện tại, do đó để gán giá trị miligiây cần dùng `setTime()`.

**Cộng trừ thêm ngày**

Dùng kết hợp method `getDate()` và `setDate()` để cộng trừ một số ngày nhất định.

```
let today = new Date();
let tomorrow = new Date();
tomorrow.setDate(today.getDate() + 1);

```

**Tính số ngày giữa hai ngày**

Thực sự không có hàm, method nào hỗ trợ việc này cả. Có một giải pháp là tìm hiệu số miligiây, rồi chia cho số miligiây của một ngày như sau.

```
let d1 = new Date("2001-07-27");
let d2 = new Date();
let days_between = (d2.getTime() - d1.getTime()) /
    (1000 * 3600 * 24);

```

Chú ý công thức này chỉ là gần đúng, nhưng có thể chấp nhận được nếu không yêu cầu độ chính xác cao.


## Chuỗi - JavaScript String

**Chuỗi (String) trong JavaScript** là một đối tượng đại diện cho một chuỗi ký tự. Có 2 cách để tạo chuỗi trong JavaScript:

1. Theo chuỗi chữ.
2. Theo đối tượng String (sử dụng từ khóa new).

### 1\. Theo chuỗi chữ

Chuỗi chữ được tạo ra bằng cách sử dụng dấu ngoặc kép. Cú pháp tạo chuỗi bằng cách sử dụng chuỗi ký tự được đưa ra dưới đây:

```
var stringName="string value";

```

Ví dụ đơn giản về việc tạo chuỗi ký tự.

```
<script>
    var str = "Day la mot chuoi JavaScript";
    document.write(str);
</script>

```

Kết quả:

```
Day la mot chuoi JavaScript

```

* * *

### 2\. Theo đối tượng String (sử dụng từ khóa new)

Cú pháp tạo đối tượng String sử dụng từ khóa mới được đưa ra dưới đây:

```
var stringName = new String("string value");

```

Ở đây, từ khóa **new** được sử dụng để tạo thể hiện của đối tượng String.

Hãy xem ví dụ tạo chuỗi trong JavaScript bằng từ khóa new.

```
<script>
    var stringname = new String("Hello javascript string");
    document.write(stringname);
</script>

```

Kết quả:

* * *

### Các phương thức xử lý chuỗi trong JavaScript

Dưới đây là danh sách các phương thức xử lý chuỗi JavaScript:

- charAt(index)
- concat(str)
- indexOf(str)
- lastIndexOf(str)
- toLowerCase()
- toUpperCase()
- slice(beginIndex, endIndex)
- trim(str)

### 1\. Phương thức charAt(index) trong JavaScript

Phương thức String String charAt () trả về ký tự ở chỉ mục đã cho. Ví dụ:

```
<script>
    var str = "javascript";
    document.write(str.charAt(2));
</script>

```

Kết quả:

### 2\. Phương thức concat(str) trong JavaScript

Phương thức concat(str) trong JavaScript được sử dụng để nối 2 chuỗi. Ví dụ:

```
<script>
    var s1 = "javascript ";
    var s2 = "concat example";
    var s3 = s1.concat(s2);
    document.write(s3);
</script>

```

Kết quả:

```
javascript concat example

```

### 3\. Phương thức indexOf(str) trong JavaScript

Phương thức indexOf(str) trong JavaScript trả về vị trí chỉ mục của chuỗi đã cho. Ví dụ:

```
<script>
    var s1 = "javascript from viettuts indexof";
    var n = s1.indexOf("from");
    document.write(n);
</script>

```

Kết quả:

### 4\. Phương thức lastIndexOf(str) trong JavaScript

Phương thức lastIndexOf(str) trong JavaScript trả về vị trí chỉ mục cuối cùng của chuỗi đã cho. Ví dụ:

```
<script>
    var s1 = "javascript from java...";
    var n = s1.lastIndexOf("java");
    document.write(n);
</script>

```

Kết quả:

### 5\. Phương thức toLowerCase() trong JavaScript

Phương thức toLowerCase() trong JavaScript trả về chuỗi đã cho bằng chữ thường. Ví dụ:

```
<script>
    var s1 = "JavaScript toLowerCase Example";
    var s2 = s1.toLowerCase();
    document.write(s2);
</script>

```

Kết quả:

```
javascript tolowercase example

```

### 6\. Phương thức toUpperCase() trong JavaScript

Phương thức toLowerCase() trong JavaScript trả về chuỗi đã cho bằng chữ hoa. Ví dụ:

```
<script>
    var s1 = "JavaScript toLowerCase Example";
    var s2 = s1.toLowerCase();
    document.write(s2);
</script>

```

Kết quả:

```
JAVASCRIPT TOUPPERCASE EXAMPLE

```

### 7\. Phương thức slice(beginIndex, endIndex) trong JavaScript

Phương thức slice(beginIndex, endIndex) trong JavaScript trả về chuỗi con của chuỗi đã cho từ beginIndex cho đến endIndex. Trong phương thức slice(), beginIndex được bao gồm và endIndex là không được bao gồm. Ví dụ:

```
<script>
    var s1 = "abcdefgh";
    var s2 = s1.slice(2, 5);
    document.write(s2);
</script>

```

Kết quả:

```
cde
```

### 8\. Phương thức trim(str) trong JavaScript

Phương thức trim(str) trong JavaScript

```
<script>
    var s1 = "     javascript trim    ";
    var s2 = s1.trim();
    document.write(s2);
</script>

```

Kết quả:

* * *
javascript trim
* * *







### Số và làm việc với kiểu số - JavaScript number methods

### Hàm - JavaScript function

### Tham số trong hàm - JavaScript function

### Return trong hàm JS - JavaScript function

### Polyfill là gì? - Khái niệm polyfill 

### Câu lệnh rẽ nhánh Switch 

## Tất tần tật về Loop trong JS

> Nguồn bài viết: [ Các loại vòng lặp trong Javascript ](https://viblo.asia/p/cac-loai-vong-lap-trong-javascript-07LKXp82KV4)

Các loại vòng lặp trong Javascript
========================================

Vòng lặp là một thành phân vô cùng quan trọng của các ngôn ngữ lập trình và thường sẽ là một trong những thứ được lập trình viên tiếp cận đầu tiên. Hẳn lập trình viên nào cũng quen với các loop phổ biến như **for**, **while** . Javascript thì cũng tương tự như vậy, tuy nhiên nó còn thêm một đống thứ kéo theo và đôi lúc không biết nó giúp ích cho dev hay lại chính là nguyên nhân tạo thêm bug. Trong bài viết mở đầu cho series **Loop**, mình sẽ giới thiệu về các loại vòng lặp trong Javascript

![](https://images.viblo.asia/full/f07ee891-403b-44db-bd0a-05f25a8562b9.png)

## For loop

* * *

Đầu tiên hẳn sẽ là loop phổ biến nhất và có phần lớn trong các ngôn ngữ lập trình : **for**

Với vòng lặp **for** ta sẽ khởi tạo biến đếm, kiểm tra điều kiện và tăng hoặc giảm biến được thực hiện trên cùng một dòng, do đó khá dễ dàng cho những người mới tiếp cận để debug và cũng giảm khả năng sinh ra lỗi

### Cú pháp

```
for ([initialization];[condition];[final-expression]){
   Block of code
}

```

### Ví dụ

```
for(var i = 0; i < 10; i++) {
    console.log(i)
}

```

### Kết quả

```
0
1
2
...
9

```

## While loop

* * *

Bên cạnh **for** thì **while** cũng là một trong những vòng lặp tương đối basic. Câu lệnh while tạo ra một vòng lặp thực thi một khối lệnh (block of code) cho đến khi điều kiện vẫn đúng.

### Cú pháp

```
while (condition) {
  Block of code
}

```

### Ví dụ

```
var i = 0;
while(i < 10) {
    console.log(i);
    i++;
}

```

### Kết quả

```
0
1
2
...
9

```

## Do ... While

* * *

\*\*do-while\*\* về cơ bản khá giống với \*\*while\*\*, chúng chỉ khác nhau duy nhất. Đối với \*\*Do While\*\* dù điều kiện lặp như thế nào thì đoạn code vẫn được chạy ít nhất 1 lần còn nếu điều kiện thỏa mãn thì sẽ tương tự như \*\*While\*\* : tạo ra thêm vòng lặp

### Cú pháp

```
do {
    Block of code
 }
while (condition);

```

### Ví dụ

```
var i = 10;
do {
    console.log(i);
    i++;
}
while ( i > 10 && i < 12)

```

### Kết quả

```
10
11

```

## forEach()

* * *

Hàm này thì có vẻ đã không quá còn basic như những hàm phía trên nữa. **forEach** sẽ lặp lại từng phần tử trong mảng theo thứ tự index và thực thi **function** được truyền vào. Lưu ý rằng **forEach** sẽ không thực thi **function** đầu vào cho các phần tử không có giá trị

### Cú pháp

```
arrayName.forEach(function(currentValue, index, array){
    function body
})

```

Hàm được truyền vào **forEach** sẽ nhận tối đa 3 đối số đầu vào:

- currentValue: Giá trị đang được vòng lặp xử lý
- index: Chí số của giá trị ( **currentValue**) trong mảng
- array: toàn bộ array đang gọi đến **forEach**

### Ví dụ

```
var arr=[10, 20, "hi", ,{}];

arr.forEach(function(item, index){
    console.log(' arr['+index+'] is '+ item);
});

```

### Kết quả

```
arr[0] is 10
arr[1] is 20
arr[2] is hi
arr[4] is [object Object]

```

Lưu ý rằng bạn không nhất thiết phải truyền toàn bộ 3 đối số vào, chỉ truyền vào những đối số cần thiết.

Nhìn qua thì thấy **forEach** khá là đem lại nhiều điều đơn giản cho lập trình viên, không cần quan tâm đến khởi tạo biến đếm, điều kiện dừng .... Tuy nhiên trong đó cũng tiềm tàng khá nhiều điều hay ho mà mình sẽ trình bày trong phần tiếp theo của series

## Map

* * *

Tiếp tục là một hàm sẽ giúp bạn loop các phần tử của một Array. Tuy nhiên \*\*map\*\* sẽ tạo ra một mảng mới chứ không phải thực thi với mảng gọi đến nó như \*\*forEach\*\*.

### Cú pháp

```
var newArray= oldArray.map(function (currentValue, index, array){
    //Return element for the newArray
});

```

Tương tự như **forEach**, **map** cũng lấy 3 tham số đầu vào

- currentValue: Giá trị đang được vòng lặp xử lý
- index: Chí số của giá trị ( **currentValue**) trong mảng
- array: toàn bộ array đang gọi đến **forEach**

### Ví dụ

```
var num = [1, 5, 10, 15];
var doubles = num.map(function(x) {
   return x * 2;
});

```

### Kết quả

```
(4) [2, 10, 20, 30]

```

Có thể thấy thì hàm này thường để dùng khi muốn thay đối giá trị toàn bộ mảng tạo ra một thực thể mới chứ không đơn thuần dùng để truy xuất.

## For...in

* * *

Vòng lặp này có đôi chút khác biệt với các hàm phía trên, **For ... in** mục đích chủ yếu được dùng để loop trong một **object** chứ không phải **array** . Số lượng vòng lặp sẽ tương ứng với số lượng thuộc tính của **object**

Mỗi **array** cũng là một object đặc biệt, do đó ta vẫn có thể sử đụng **for...in** cho **array**, tuy nhiên key sẽ tương ứng với giá trị **index** của từng phần tử

### Cú pháp

```
for (variableName in object) {
    Block of code
}

```

### Ví dụ

```
var obj = {a: 1, b: 2, c: 3};
for (var prop in obj) {
   console.log('obj.'+prop+'='+obj[prop]);
};

```

### Kết quả

```
obj.a=1
obj.b=2
obj.c=3

```

**for...in** không được khuyến khích sử dụng với những mảng mà thứ tự index của nó quan trọng.

Thêm một ví dụ:

```
var arr = [];
arr[2] = 2;
arr[3] = 3;
arr[0] = 0;
arr[1] = 1;

```

Với ví dụ trên được loop bởi **forEach** thì kết quả sẽ theo thứ tự là 0, 1, 2, 3 còn với **for...in** thì sẽ không đảm bảo như vậy.

Thêm một điều nữa, với **for...in**, nó sẽ duyệt qua cả những thuộc tính kế thừa của object . Do đó nếu muốn chỉ duyệt qua thuộc tính riêng của object thì cú pháp cần thay đổi một chút

```
for(var prop in obj){
   if(obj.hasOwnProperty(prop)){
       Code block here
   }
}

```

## for...of

* * *

Vòng lắp được ra mắt trong phiên bản ES6. Hàm này có thể sử dụng để duyệt phần lớn các đối tượng từ Array, String, Map, WeakMap, Set ,...

### Cú pháp

```
for (variable of iterable) {
  Block of code
}

```

### Ví dụ

```
var str= 'paul';
for (var value of str) {
console.log(value);
}

```

### Kết quả

```
"p"
"a"
"u"
"l"

```

### Một ví dụ khác

```
let itobj = new Map([['x', 0], ['y', 1], ['z', 2]]);

for (let kv of itobj) {
  console.log(kv);
}
// ['x', 0]
// ['y', 1]
// ['z', 2]

for (let [key, value] of itobj) {
  console.log(value);
}

//0
//1
//2

```

Bài viết được tham khảo trực tiếp và có chính sửa tại bài viết [All type of loops in JavaScript, a brief explanation](http://voidcanvas.com/all-type-of-loops-in-javascript-a-brief-explanation/)



### Phương thức reduce khi làm việc với array - JavaScript array reduce() method

### Phương thức reduce khi làm việc với array - phần 2 - JavaScript array reduce() method

### Phương thức includes - JavaScript String/Array includes() method

### Đối tượng math - JavaScript math object

### Callback Functions trong JS

### Xây dựng phương thức filter - JavaScript Array filter() method

### Xây dựng phương thức some - JavaScript Array some() method

### Xây dựng phương thức every - JavaScript Array every() method

### Đệ quy là gì? Học về đệ quy - Recursive Function

### HTML DOM là gì? - JavaScript HTML DOM

### HTML DOM và DOM API là gì? - JavaScript HTML DOM

### DOM Document Object - HTML DOM

### Lấy element trong DOM

### Attribute node và Text node trong HTML DOM

### DOM attribute - Thêm sửa xóa attribute

### InnerText & textContent Property - Text node in Dom

### Thêm element vào element trong DOM - InnerHTML property - OuterHTML property

### Node properties - HTML DOM

### Đối tượng DOM style trong Element node - DOM CSS

### ClassList Property

### DOM events

### DOM events example - JavaScript HTML DOM Events

### PreventDefault & StopPropagation - DOM events

### Event listener - add & removeEventListener

### JSON là gì? JSON được sử dụng như thế nào ?

### Promise (sync async) - Khái niệm promise

### Promise chain - Cách hoạt động của Promise - JavaScript Promise

### Promise methods (resolve, reject, all) - JavaScript Promise

### Arrow function  ES6 - Khái niệm arrow function

### Template literals (Template string)  ES6

### Classes  ES6

### Enhanced object literals  ES6

### Default parameter values  ES6

### Destructuring  ES6

### Spread  ES6

### Khái niệm tagged template literals

### Module  ES6

### Khái niệm Optional chaining - ECMAScript 6+

### Promise example - Ví dụ sử dụng Promise 

### Fetch - Khái niệm Fetch 

### Phương thức reduce có logic như thế nào? - JavaScript reduce

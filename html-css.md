# Tất tần tật về HTML/CSS cơ bản trong một trang

Nội dung trong trang được lấy từ (~~ăn cắp~~) từ rất nhiều trang khác nhau. Mình sẽ để nguồn ở đầu bài để mọi người truy cập các bài gốc và đọc thêm. Nếu tác giả của bài bất kì muốn bài được gỡ thì nhắc mình trong Repo của trang này trên Github luôn nha


### Cài đặt công cụ + sử dụng Dev Tools

## Cấu trúc tệp HTML

> Nguồn: [bài này](https://hocwebchuan.com/tutorial/tut_html_basic.php)

Cấu trúc cơ bản của trang HTML có dạng như sau, thường gồm 3 phần:

-   `<!Doctype>`: Phần khai báo chuẩn của html hay xhtml.
-   `<head></head>`: Phần khai báo ban đầu, khai báo về `meta`, `title`, CSS, JS...
-   `<body></body>`: Phần chứa nội dung của trang web, nơi hiển thị nội dung.


```html
<!--Cấu trúc cơ bản sẽ trông như thế này. Đây được gọi là một comment-->
<!DOCTYPE html>
<html>
<head>
<title>Tiêu đề trang web</title>
</head>

<body>
...Phần thân viết ở đây...
</body>
</html>
```

Mỗi trang web đều có cách thể hiện cấu trúc khác nhau, có trang 1 cột, có trang 2 và cũng có trang chứa nhiều cột, bên dưới đây chúng ta tham khảo một trang đơn giản sử dụng 2 cột để layout.

-   **Phần đầu:** header, có thể chứa logo, câu slogan, các liên kết, các banner liên kết, các button, đoạn flash, hoặc các form ngắn như form tìm kiếm,...
-   **Phần liên kết toàn cục:** global navigation, dùng để chứa các liên kết đến những trang quan trọng trong toàn bộ trang, trong phần này có thể chứa thêm các liên kết con (sub navigation).
-   **Phần thân của trang:** page body, phần này chứa phần nội dung chính (content) và phần nội dung phụ (sidebar).
-   **Phần nội dung chính:** content, phần này chứa nội dung chính cần thể hiện cho người dùng xem.
-   **Phần nội dung phụ:** sidebar, phần này có thể chứa liên kết phụ của từng trang (local navigation), hoặc các banner chứa liên kết liên quan, hoặc có thể dùng để chứa các liên kết quảng cáo,...
-   **Phần cuối trang web:** footer, phần này thường chứa phần liên hệ như: tên công ty, địa chỉ, số điện thoại, mail liên hệ,... và đặc biệt là copyright, hoặc có thể chứa các liên kết toàn trang, các banner liên kết,...

![alt text](image.png)

## Comments trong HTML

```html
<!-- Đây là một comment -->

<!-- Đây là một comment. Các comment không được hiển thị trên trình duyệt-->
<p>Đây là một đoạn văn.</p>
```
> Kết quả: Đây là một đoạn văn.

## Những thẻ HTML thông dụng

> Nguồn: [bài viết này](https://blog.haposoft.com/gioi-thieu-ve-html-css-va-tong-quan-ve-cau-truc-web/)

### Heading

Trong HTML, các thẻ heading sẽ được định nghĩa bằng cặp thẻ <h**n**>, trong đó **n** là số tự nhiên từ 1 đến 6 tương ứng với từng cấp độ, số càng nhỏ thì cấp độ càng lớn. Để dễ hiểu hơn, hãy thử soạn thảo một tài liệu HTML như dưới đây.

```
<h1>Heading 1</h1>
<h2>Heading 2</h2>
<h3>Heading 3</h3>
<h4>Heading 4</h4>
<h5>Heading 5</h5>
<h6>Heading 6</h6>

```

![Heading tags](https://blog.haposoft.com/content/images/2021/07/h_tag-1.png)

### Thẻ văn bản

Đoạn văn bản thì sẽ được khai báo bằng cặp thẻ `<p></p>` Các văn bản nằm trong cặp thẻ này sẽ được hiểu là một đoạn văn bản, mỗi đoạn văn bản sẽ được xuống dòng và cách nhau với tỷ lệ nhất định.

```html
<p>My first paragraph</p>
```

![](https://blog.haposoft.com/content/images/2021/07/p.png)

Với HTML, cách hiển thị không thể thay đổi bằng cách thêm khoảng trắng hoặc dòng trắng trong đoạn văn bản của mình. Trình duyệt sẽ tự động loại bỏ bất kỳ khoảng trắng và dòng thừa nào khi trang được hiển thị.

![](https://blog.haposoft.com/content/images/2021/07/p_2.png)

Nếu muốn viết một đoạn văn đã được định dạng sẵn thì có thể sử dụng thẻ `<pre>`. Lúc này đoạn văn được hiển thị sẽ giống như đoạn văn được viết ở trình soạn thảo.

![](https://blog.haposoft.com/content/images/2021/07/pre.png)

### List

Có 2 thẻ để định dạng một danh sách trong HTML đó là thẻ `<ul>` và `<ol>`. Mỗi mục trong danh sách này được bắt đầu bằng thẻ `<li>`. Điểm khác biệt giữa 2 thẻ này là gì ?

Thẻ `<ol>` khai báo một danh sách có thứ tự.

![](https://blog.haposoft.com/content/images/2021/07/ol.png)

Trong `<ol>` có các kiểu định dạng số thứ tự như sau:

-   `type="A"` or `type="a"`: hiển thị số thứ tự từ `a->z` bằng ký tự in hoa hoặc in thường.
-   `type="I"` or `type="i"`:hiển thị số thứ tự bằng ký tự số la mã in hoa hoặc in thường.

Nếu không khai báo thuộc tính `type` thì số thứ tự sẽ được mặc định đánh số từ `1->n`.

![](https://blog.haposoft.com/content/images/2021/07/ol_ex.png)

Thẻ `<ul>` danh sách không có thứ tự

![](https://blog.haposoft.com/content/images/2021/07/ul.png)

### Table


Thẻ `<table>` khởi tạo một bảng trong HTMl

-   Mỗi hàng trong bảng được xác định bằng thẻ `<tr>`
-   Mỗi tiêu đề bảng được xác định bằng thẻ `<th>`
-   Mỗi ô dữ liệu của bảng được xác định bằng thẻ `<td>`

![](https://blog.haposoft.com/content/images/2021/07/table.png)

Để tạo một ô kéo dài nhiều hơn một cột, hãy sử dụng thuộc tính `colspan`.

![](https://blog.haposoft.com/content/images/2021/07/colspan.png)

Để tạo một ô kéo dài nhiều hơn một hàng, hãy sử dụng thuộc tính `rowspan`.

![](https://blog.haposoft.com/content/images/2021/07/rowspan.png)

Để thêm chú thích cho bảng, hãy sử dụng `<caption>`

![](https://blog.haposoft.com/content/images/2021/07/caption.png)

### Links

Thẻ `<a>` dùng để tạo một một liên kết. Khi người dùng bấm vào thì sẽ được chuyển đến liên kết đó.

Cấu trúc:

```html
<a href="url">link text</a>
```

Thuộc tính quan trọng nhất của thẻ `<a>` là thuộc tính `href`, nó chỉ ra đường dẫn tới liên kết đó. Khi nhấp vào, nó sẽ đưa người dùng đến địa chỉ URL được chỉ định.

Ví dụ:

```html
<a href="https://haposoft.com/vi">Haposoft</a>
```

Các thuộc tính có trong thẻ `<a>`:

-   `href`: Xác định đường dẫn đến tài nguyên mà bạn muốn chuyển tới.
-   `download`: khi người dùng bấm vào liên kết thì tài nguyên của liên kết đó sẽ tự động được tải về.
-   `target` thuộc tính được chỉ định nơi để mở liên kết. Một số target và cách dùng như sau:
    -   `_self` (default): Mở liên kết trong cùng một cửa sổ/tab.
    -   `_blank:` Mở liên kết trong cửa sổ hoặc tab mới.
    -   `_parent:` Mở liên kết dưới dạng popup
    -   `_top:` Mở liên kết dưới dạng popup toàn màn hình

```html
<a href="https://haposoft.com/" target="_blank">Haposoft!</a>
```

Khi click vào địa chỉ này, người dùng sẽ được chuyển sang một tab mới.

Ngoài ra còn một số trò hay ho có thể dùng với thẻ `<a>` như:

-   Liên kết đến một địa chỉ email:

```html
<a href="mailto:someone@example.com">Send email</a>

```

-   Thực hiện một cuộc gọi:

```html
<a href="tel:0911111xxx">Call 0911111xxx </a>

```

### Thẻ Div


Thẻ `<div>` xác định 1 phần trong HTML.

Thẻ `<div>` thường được sử dụng để chứa các element khác. Bất kì nội dung nào cũng có thể đặt trong thẻ `<div>`. Ví dụ như:

```html
<div>
    <h1>H1 Title</h1>
    <a href="https://haposoft.com/" target="_blank">Haposoft!</a>
</div>

```

trong thẻ `<div>` đã chứa thẻ `<h1>` và `<a>`.

*Lưu ý:* Mặc định thì các trình duyệt sẽ hiển thị nội dung của thẻ `<div>` xuống dòng.

### Thẻ Span

Thẻ `<span>` là thẻ khá đặc biệt trong HTML, theo mặc định đoạn văn bản trong cặp thẻ span không bị thay đổi bất cứ điều gì -- do vậy nó còn được gọi là thẻ trung tính. Sự thay đổi chỉ xảy đến khi bạn tác động đến thẻ span thông qua CSS. Ngoài ra thẻ này nằm trong nhóm inline.

Ví dụ, ta có đoạn code sau:

```html
<p><span style="color: red;">Màu đỏ</span>, <span style="color: yellow;">màu vàng</span>, <span style="color: blue;">màu xanh</span> là 3 màu của đèn tín hiệu giao thông.</p>
```

Kết quả hiển thị sẽ là:

<p><span style="color: red;">Màu đỏ</span>, <span style="color: yellow;">màu vàng</span>, <span style="color: blue;">màu xanh</span> là 3 màu của đèn tín hiệu giao thông.</p>

Lúc này ta thấy được các text trong thẻ span được đổi màu do tác động từ css.

### Image

Hình ảnh làm trang web sống động hơn, đẹp. Để sử dụng hình ảnh mình sử dụng như sau:

```html
<img src="pic_trulli.jpg" alt="Italian Trulli">

```

Trong HTML, dùng thẻ `<img>` để nhúng ảnh vào web của mình.

Thẻ `<img>` yêu cầu bắt buộc 2 attributes:

-   `src` - Thuộc tính khai báo đường dẫn của ảnh hoặc dữ liệu dạng base64 của ảnh.
-   `alt` - Thuộc tính sẽ hiển thị cho trường hợp bạn truyền URL image bị sai. Tức là nó sẽ hiển thị đoạn text này thay vì hình ảnh nếu URL bạn truyền vào bị sai.

### Forms

Một `form` được sử dụng để nhận thông tin `input` của người dùng. Input của người dùng thường được gửi đến server để xử lý.

`<form>` được sử dụng để tạo một biểu mẫu HTML cho đầu vào của người dùng.

Thẻ `<form>` là vùng chứa cho các loại `input` khách nhau như: text fields, checkboxes, radio buttons, submit buttons, ...

`<input>` có thể được hiển thị theo nhiều cách, tùy thuộc vào thuộc tính `type`.

### Text Fields

`<input type="text">` xác định một trường nhập để nhập văn bản.

![](https://blog.haposoft.com/content/images/2021/07/Text.png)

Lưu ý việc sử dụng `<label>` cho ví dụ bên trên:

-   Thẻ `<label>` rất hữu dụng cho người dùng vì người dùng thường đọc các nhãn này để xác định xem họ đang chỉnh sửa cho `input` nào. Nó cũng giúp người dùng có thể chọn phần `input` một cách dễ dàng hơn bằng cách click vào thẻ này.

-   Thuộc tính `for` của thẻ phải bằng với `id` của thẻ `input` để liên kết chúng lại với nhau.

### Radio button

`<input type="radio">` khai báo một nút radio, cho phép người dùng lựa chọn chỉ một trong các giá trị.

![](https://blog.haposoft.com/content/images/2021/07/radio.png)

### Checkbox

Khác với radio button chỉ cho phép người dùng chọn một giá trị duy nhất. Thì `<input type="checkbox">` khai báo một ô checkbox, cho phép người dùng chọn KHÔNG hoặc NHIỀU giá trị.

![](https://blog.haposoft.com/content/images/2021/07/checkbox.png)

### Submit button

`<input type="submit">` tạo một nút để người dùng gửi dữ liệu nhập vào đến trình xử lý. Trình xử lý này thường được thực hiện ở phía server bằng một script.

Nơi dữ liệu được xử lý sẽ được chỉ định bởi thuộc tính `action` của `form`.

Chú ý: mỗi `input` phải có một thuộc tính `name` để được gửi đi. Nếu không có `name` giá trị nhận được từ `input` này sẽ bị bỏ qua.


## Attributes trong HTML - Thêm thuộc tính (Attributes) vào thẻ

> Nguồn bài viết: [Bài này](https://cafedev.vn/tu-hoc-html-thuoc-tinhattributes-trong-html/)

### 1. Thuộc tính HTML

-   Tất cả các phần tử HTML có thể có các thuộc tính
-   Các thuộc tính cung cấp thêm thông tin cho các yếu tố
-   Các thuộc tính luôn được chỉ định trong thẻ bắt đầu
-   Các thuộc tính thường có các cặp tên / giá trị như: name = "value"

### 2. Thuộc tính `href`


Thẻ <a> định nghĩa một liên kết. Thuộc tính href chỉ định URL của trang mà liên kết đến:

```
<a href="https://example.com">Example</a>
```


### 3. Thuộc tính `src`

Thẻ <img> được sử dụng để nhúng hình ảnh vào trang HTML. Thuộc tính src chỉ định đường dẫn đến hình ảnh sẽ được hiển thị:

```
<img src="example.jpg">
```

### 4. Các thuộc tính chiều rộng và chiều cao


Thẻ `<img>` cũng phải chứa các thuộc tính `width` và `height`, chỉ định chiều rộng và chiều cao của hình ảnh (tính bằng pixel):

```
<img src="img_example.jpg" width="500" height="600">
```

### 5. Thuộc tính `alt`


Thuộc tính `alt` được yêu cầu cho thẻ `<img>` chỉ định văn bản thay thế cho hình ảnh, nếu hình ảnh vì lý do nào đó không thể được hiển thị. Điều này có thể là do kết nối chậm hoặc lỗi trong thuộc tính `src` hoặc nếu người dùng sử dụng trình đọc màn hình.

Ví dụ:

```
 <img src="void.jpg" alt="Emptiness">
```


### 6. Thuộc tính `style`


Thuộc tính `style` được sử dụng để thêm kiểu vào một phần tử, chẳng hạn như màu sắc, phông chữ, kích thước và hơn thế nữa.

```
 <p style="color:red;">This is a red paragraph.</p>
```


### 7. Thuộc tính `lang`
-------------------

Bạn phải luôn bao gồm thuộc tính `lang` bên trong thẻ `<html>` để khai báo ngôn ngữ của trang Web. Điều này có nghĩa là để hỗ trợ công cụ tìm kiếm và trình duyệt.

Ví dụ sau chỉ định Tiếng Việt là ngôn ngữ:

```html
<!DOCTYPE html>
<html lang="vi">
<body>
...
</body>
</html>
```

Mã quốc gia cũng có thể được thêm vào Code ngôn ngữ trong thuộc tính `lang`. Vì vậy, hai ký tự đầu tiên xác định ngôn ngữ của trang HTML và hai ký tự cuối xác định quốc gia.

Ví dụ sau chỉ định tiếng Anh là ngôn ngữ và Hoa Kỳ là quốc gia:

```
<!DOCTYPE html>
<html lang="en-US">
<body>
...
</body>
</html>
```

### 8. Thuộc tính `title`


Thuộc tính `title` định nghĩa một số thông tin bổ sung cho một phần tử.

Giá trị của thuộc tính `title` sẽ được hiển thị dưới dạng chú giải khi bạn di chuột qua phần tử:

```
<p title="I'm a tooltip">This is a paragraph.</p>
```


### 9. Một số kinh nghiệm

-   Luôn sử dụng các thuộc tính bằng chữ thường: Không nên ghi là TITLE hay ghi là title
-   Luôn trích dẫn giá trị thuộc tính (Tức là đóng ngoặc kép á)

```html
<!--Được này-->
<a href="https://example.vn"></a>
<!--Cái này bất ổn-->
<a href=https://example.vn></a>

```

### 10. Nên dùng dầu nhấy đơn hay đôi?


Dấu ngoặc kép xung quanh các giá trị thuộc tính là phổ biến nhất trong HTML, nhưng cũng có thể sử dụng dấu ngoặc đơn. Trong một số trường hợp, khi chính giá trị thuộc tính chứa dấu ngoặc kép, cần sử dụng dấu ngoặc đơn:

```html
<p title='John "ShotGun" Nelson'>
<p title="John 'ShotGun' Nelson">
```

### 11. Tóm tắt


-   Tất cả các yếu tố HTML có thể có các thuộc tính
-   Thuộc tính `href` của `<a>` chỉ định URL của trang mà liên kết đi đến
-   Thuộc tính `src` của `<img>` chỉ định đường dẫn đến hình ảnh sẽ được hiển thị
-   Các thuộc tính `width` và `height` của `<img>` cung cấp thông tin kích thước cho hình ảnh
-   Thuộc tính `alt` của `<img>` cung cấp văn bản thay thế cho hình ảnh
-   Thuộc tính `style` được sử dụng để thêm kiểu vào một thành phần, chẳng hạn như màu sắc, phông chữ, kích thước và hơn thế nữa
-   Thuộc tính `lang` của thẻ `<html>` khai báo ngôn ngữ của trang Web
-   Thuộc tính `title` định nghĩa một số thông tin bổ sung về một yếu tố


## Cách sử dụng CSS trong HTML

> Nguồn bài viết: [Bài này](https://naototnhat.com/cach-lien-ket-css-voi-html.html)

### 1. Sử dụng thuộc tính "style"

Phương pháp đầu tiên là sử dụng thuộc tính "style" trực tiếp trong thẻ HTML. Bằng cách này, bạn có thể áp dụng các quy tắc CSS trực tiếp cho các phần tử HTML.

Ví dụ, để thay đổi màu chữ của một đoạn văn bản, bạn có thể sử dụng thuộc tính "style" như sau:

```html
<p style="color: red;">Đây là một đoạn văn bản có màu chữ đỏ.</p>
```

Tuy nhiên, phương pháp này thích hợp cho việc chỉnh sửa nhanh chóng và áp dụng CSS cho một số phần tử nhỏ. Đối với những trang web lớn hơn, nên sử dụng phương pháp khác để tách biệt CSS và HTML một cách rõ ràng hơn.

### 2. Sử dụng thẻ "style"

Phương pháp thứ hai là sử dụng thẻ "style" trong phần tử "head" của tài liệu HTML. Bằng cách này, bạn có thể định nghĩa các quy tắc CSS cho toàn bộ trang web.

Ví dụ, để định nghĩa một quy tắc CSS để thay đổi màu nền của trang web, bạn có thể sử dụng thẻ "style" như sau:

```html
<!DOCTYPE html>
<html>
<head>
  <style>
    body {
      background-color: lightblue;
    }
  </style>
</head>
<body>
  <!-- Nội dung trang web -->
</body>
</html>
```

Sử dụng thẻ "style" cho phép bạn tạo ra các kiểu dáng phức tạp hơn và áp dụng chúng cho toàn bộ trang web. Tuy nhiên, nếu bạn muốn sử dụng CSS một cách linh hoạt hơn và không muốn lồng ghép CSS trong tài liệu HTML, phương pháp tiếp theo sẽ là lựa chọn tốt nhất.

### 3. Sử dụng thẻ "link"

Phương pháp cuối cùng, và cũng là phương pháp được khuyến nghị cho việc liên kết CSS với HTML, là sử dụng thẻ "link". Bằng cách này, bạn có thể liên kết một file CSS riêng biệt với tài liệu HTML.

Đầu tiên, bạn cần tạo một file CSS với phần mở rộng ".css". Ví dụ, bạn có thể tạo file "style.css" để chứa các quy tắc CSS của bạn.

Sau đó, bạn cần thêm thẻ "link" trong phần tử "head" của tài liệu HTML để liên kết file CSS:

```html
<!DOCTYPE html>
<html>
<head>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <!-- Nội dung trang web -->
</body>
</html>
```

Trong ví dụ trên, "style.css" là đường dẫn tương đối đến file CSS của bạn. Bạn cũng có thể sử dụng đường dẫn tuyệt đối nếu cần thiết.

## ID và Class trong CSS selectors

**Thuộc tính ID**
-----------------

ID Selector dùng để khai báo cho một phần tử HTML duy nhất và không sử dụng lần nào nữa trên website. Chẳng hạn như một trang web chỉ có một Header, một Footer. Lúc này chúng ta sẽ sử dụng ID cho chúng.

Khi viết trong CSS sẽ đặt dấu "#" ở phía trước.

Ví dụ:

<!DOCTYPE html>
<html>
<head>
#header {
max-height: 100px;
}
#footer {
background: #ddd;
}
</head>
<body>
<div id="header">Phần Header</div>
<div id="main">Phần nội dung</div>
<div id="footer">Phần Footer</div>
</body>
</html>

**Thuộc tính CLASS**
--------------------

CLASS Selector dùng để khai báo cho nhiều phần tử có thể dùng chung một class. Có nghĩa là bạn có thể dùng một class nhiều lần trên website.

Khi dùng class bạn sẽ dùng dấu "." ở phía trước

<!DOCTYPE html>
<html>
<head>
.content {
font-size: 15px;
font-family: Arial, san-serif;
}
</head>
<body>
<div class="content">Phần Header</div>
<div class="content">Phần nội dung</div>
<div class="content">Phần Footer</div>
</body>
</html>

Kết luận: Thẻ ID và CLASS trong HTML và CSS rất quan trọng. Hiểu một cách đơn giản là ID dùng cho một phần tử duy nhất, còn với CLASS thì có thể sử dụng cho nhiều phần tử khác nhau. Trên đây SONGMAWEB đã giải thích khá rõ ràng sự khác biệt về 2 thuộc tính này. Chúc bạn học thiết kế web nhanh chóng!
https://songmaweb.com/su-khac-nhau-giua-class-va-id-trong-css/

### Mức độ ưu tiên trong CSS
[viblo.asia](https://viblo.asia/p/css-priority-rankings-djeZ1pxGKWz)

CSS Priority Rankings
=====================

looj

4--5 minutes

* * * * *

[![Avatar](https://images.viblo.asia/avatar/b775c582-a40b-4b6e-ac23-8ddae555af6b.jpeg)](https://viblo.asia/u/quocanh253)

Đã đăng vào thg 10 21, 2019 3:50 CH 4 phút đọc

Xin chào mọi người, trong bài viết này mình sẽ tập trung nói về vấn đề CSS Priority Rankings. Mình nghĩ đây là một kiến thức căn bản mà một Coder Front-end nên biết. Biết nó các bạn sẽ dễ dàng control CSS của mình khi sử dụng các CSS Framework trong quá trình đi xây dựng giao diện cho dự án.

![](https://images.viblo.asia/f175ff5e-4348-4d0c-9bfe-5dcb94edd4f0.png)

1
. CSS Priority Rankings là gì?
--------------------------------

CSS Priority Rankings là thứ tự ưu tiên các CSS được browser quy định, thông qua đó các bạn có thể biết đâu sẽ là thuộc tính được hiển thị trong trường hợp có sự xung đột CSS trên cùng một phần tử HTML.

Dưới dây là danh sách liệt kê thứ tự ưu tiên của thuộc tính CSS:

![](https://images.viblo.asia/7e0d4ab2-327c-4f1a-9d0a-97f3a6a3785b.png)

2
. Important
-------------

Là thuộc tính có thứ tự ưu tiên cao nhất trong CSS. Nó sẽ luôn luôn overwrite tất cả các thuộc tính CSS còn lại. Có thể nói đây là ông trùm của những ông trùm.

```
<style>
  .red {
      color: red;
  }
  .blue {
      color: blue!important;
  }
</style>

<p class="red blue">Thuộc tính "important"</p>

```

-   Theo quy định trên thì kết quả của đoạn text trên sẽ là màu `blue` vì ở đây chúng ta có thuộc tính **!important** được khai báo trong class `.blue`

3
. Inline CSS
--------------

Inline CSS thường được dùng cho một phần tử HTML xác định. <style> attribute được dùng để style mỗi HTML tag.

Chúng ta có đoạn code sau đây:

```
<style>
  .red {
      color: red;
  }
  .black {
      color: black!important;
  }
</style>

<h3 class="red" style="color: blue;">Inline CSS</h3>
<h4  class="red black" style="color: blue;">Inline CSS và Important</h4>

```

-   Ở đây đoạn text trong tag h3 sẽ có kết quả là màu `blue` vì độ ưu tiên của Inline CSS cao hơn với việc style CSS bằng class, nhưng đoạn text trong tag h4 sẽ có màu `black` vì độ ưu tiên của thuộc tính Important cao hơn.

Media Query là một trong những tính năng mới được thêm vào trong CSS3, bằng việc sử dụng những cú pháp query để chúng ta có thể đáp ứng được nhiều kích cỡ màn hình khác nhau cho riêng mỗi thiết bị: desktop, mobile, tablet.

Chúng ta có đoạn code như sau:

```
<style>
  .red {
      color: red;
  }

  @media screen (mix-width: 320px) {
      .blue {
          color: blue;
      }
  }
</style>

<h1 class="red blue">Media Query</h1>

```

-   Ở đây kết quả của đoạn text trong tag h1 sẽ màu blue ở kích cỡ màn hình lớn hơn 320px vì ở đây mình dùng Media Query để overwrite CSS và nếu màn hình nhỏ hơn 320px nó sẽ màu red.

5
. Selector Specificity
------------------------

Selector Specificity là việc dùng các thẻ ID hoặc Class để khai báo CSS, trong phần này nó có thêm một số thứ phức tạp khác như việc sử dụng Pseudo Class để khai báo CSS nhưng mình không có quá đi sâu vào cái này.

Chúng ta sẽ làm rõ phần này bằng đoạn code nhỏ như sau:

```
<style>
  #red {
      color: red;
  }

  .blue {
      color: blue;
  }

  h2 {
      color: yellow;
  }
</style>

<h1 class="blue" id="red">Selector Specificity</h1>
<h2 class="blue">Selector Specificity</h2>
<h2 id="red">Selector Specificity</h2>

```

-   Theo thứ tự xếp độ ưu tiên thì Select phần tử HTML bằng ID > CLASS > Default tag HTML. Do đó thẻ h1 đầu tiên sẽ là `red`, thẻ h2 tiếp theo sẽ là `blue` và thẻ h2 cuối cùng sẽ là màu `red`.

6
. Rule Order
--------------

Vì code của chúng ta luôn được trình duyệt đọc theo thứ tự từ trên xuống nên các CSS đặt sau cùng sẽ luôn luôn overwrite các CSS ở trên cùng.

Chúng ta sẽ làm rõ vấn đề này bằng việc khai báo hai CSS cùng dùng thuộc tính !important ở ví dụ sau:

```
<style>
  .red {
      color: red!important;;
  }

  .blue {
      color: blue!important;;
  }
</style>

<h1 class="blue red">Rule Order</h1>

```

-   Ở đây kết quả sẽ là màu `red` vì CSS của classs .red đứng sau CSS của class .blue

7
. Browser Default
-------------------

Browser Default là những CSS mặc định mà các trình duyệt quy định vì mỗi tag HTML sẽ được browser hiển thị theo từng các khác nhau và nó cũng là những CSS có cấp độ ưu tiên thấp nhất.

8
. Tổng kết
------------

-   Trên đây là thứ tự độ ưu tiên khi làm việc với CSS, rất hữu ích cho các bạn Front-end mới tập tãnh vào nghề, h vọng bài viết sẽ giúp ích cho các bạn. Cám ơn các bạn đã theo dõi!
-   Nguồn: [thebookdesigner](https://www.thebookdesigner.com/2017/02/styling-priorities-css-for-ebooks-3/)

All rights reserved
https://viblo.asia/p/css-priority-rankings-djeZ1pxGKWz

### CSS Variable là gì? - Cách đặt biến trong CSS

[viblo.asia](https://viblo.asia/p/cach-su-dung-co-ban-css-variables-gGJ59kXGZX2)

Cách sử dụng cơ bản CSS Variables
=================================

Trịnh Văn Thắng

4--5 minutes

* * * * *

[![Avatar](https://viblo.asia/images/mm.png)](https://viblo.asia/u/TrinhThangFG)

Đã đăng vào thg 12 17, 2018 10:17 SA 3 phút đọc

Giới thiệu
----------

Biến (variables) là một trong những khái niệm cơ bản trong lập trình chắc hẳn ai cũng đã biết. Trong CSS cũng vậy, các biến được khai báo trong CSS selector để xác đinh phạm vi của nó. Các trang web phức tạp hiện nay có số lượng CSS rất lớn, thường có rất nhiều giá trị lặp lại, CSS variables có khả năng làm giảm sử lặp lại đó bằng cách cho phép lưu trữ giá trị biến ở 1 nơi và sau đó được tham chiếu ở một nơi khác.

Cách sử dụng CSS Variables
--------------------------

**1
. Khai báo CSS Variables**

Để khai báo một biến, trước tiên bạn cần quyết định phạm vi của biến đó sẽ tồn tại. Đối với global scope bạn có thể sử dụng `:root`, hoặc bạn cũng có thể tạo các biến cục bộ, tên biến phải bắt đầu bằng 2 dấu gạch ngang (--) và được phân biệt chữ hoa và chữ thường,

```
:root {
  --main-color: #ffeead;
  --main-background: #ff0000;
}

```

**2
. Cách sử dụng CSS Variables**

Để truy cập một biến, bạn cần sử dụng hàm var () và truyền tên của biến làm tham số.

```
.title {
  color: var(--main-color);
  background-color:  var(--main-background);
}

```

Kết quả của đoạn mã ở trên giống với `SASS` hoặc `LESS` khi được compiled. Tuy nhiên, so với các chương trình tiền xử lý, CSS variables có những lợi ích nhất định:

-   Được hỗ trợ trực tiếp bởi trình duyệt, không phải biên dịch.
-   Các biến được chia theo tầng (cascading). Cũng như CSS selectors, thuộc tính tùy biển có thể được quy định lại bởi những luật ở tầng thấp hơn.
-   Giúp mã nguồn dễ đọc và có ý nghĩa hơn, nâng cao tính tùy biến và khả năng bảo trì.
-   Hỗ trợ hầu hết các trình duyệt hiện tại
-   Bạn cũng có thể kết hợp với hàm calc() khi sử dụng CSS variables:

```
:root {
  --default-font-size: 1.1rem;
}

h1 {
  font-size: calc(var(--default-font-size) * 5); /* 5.5rem */
}

```

**3
. Cách truy cập các biến bằng JavaScript**

-   Do CSS variables tồn tại trong DOM, có thể được truy xuất và thay đổi bằng JavaScript. Tính năng này mở ra những cơ hội mới rất hữu ích khi lập trình frontend.

```
var root = document.querySelector(':root');
var rootStyles = getComputedStyle(root);
var mainColor = rootStyles.getPropertyValue('--main-color');
console.log(mainColor);
--> '#ffeead'

```

-   Thay đổi giá trị của biến bằng Javascript

```
root.style.setProperty('--main-color', 'red')

```

**4
. Dễ dàng thay đổi giá trị các biến khi responsive**

-   Chúng ta có thể thay đổi giá trị của biến khi sử dụng `@media`, `@document`, hay `@support`...

```
:root {
  --main-font-size: 16px;
}
media all and (max-width: 600px) {
  :root {
    --main-font-size: 12px;
  }
}

```

**5
. Ngoài ra chúng ta có tuỳ chỉnh fallback values của variables**

Sử dụng hàm var (), bạn có thể xác định nhiều giá trị fallback khi biến đã cho chưa được xác định, điều này có thể hữu ích khi làm việc với Custom Elements và Shadow DOM.

```
.el-one {
  color: var(--my-var, red); /* Red if --my-var is not defined */
}

.el-two {
  background-color: var(--my-var, var(--my-background, pink)); /* pink if my-var and --my-background are not defined */
}

```

Kết luận
--------

Tính năng này khá là hữu ích khi các ứng dụng web ngày càng phức tạp về tính năng cũng như giao diện người dùng, mà bạn không muốn sử dụng các chương trình tiền xử lý CSS (CSS pre-processors) như SASS, LESS hay Stylus . Hẹn gặp lại các bạn trong các bài tiếp theo 😃

https://viblo.asia/p/cach-su-dung-co-ban-css-variables-gGJ59kXGZX2

### CSS Units là gì? - Các đơn vị trong CSS

[viblo.asia](https://viblo.asia/p/css-units-em-rem-pt-px-vw-vh-vmin-vmax-ex-ch-Az45brNV5xY)

CSS Units (em, rem, pt, px, vw, vh, vmin, vmax, ex, ch, ...)
============================================================

TuanNM

3--4 minutes

* * * * *

[![Avatar](https://images.viblo.asia/avatar/926a4924-b1dd-4818-a389-10878a17d226.png)](https://viblo.asia/u/NMT)

Đã đăng vào thg 8 20, 2019 6:33 CH 2 phút đọc

Introduction
------------

CSS có nhiều đơn vị đo, phổ biến nhất là pixels, nhưng bên cạnh đó còn khá nhiều đơn vị đo khác tuy không được biết đến nhiều nhưng đôi khi chúng rất hữu dụng trong vài trường hợp cụ thể.

Trong bài viết này đề cập đến **relative units**, **absolute units** và **viewport units**

| Media | Recommended | Occasional use | Infrequent use | Not recommended |
| --- | --- | --- | --- | --- |
| Screen | em, rem, % | px | ch, ex, vw, vh, vmin, vmax | cm, mm, in, pt, pc |
| Print | em, rem, % | cm, mm, in, pt, pc | ch, ex | px, vw, vh, vmin, vmax |

Relative Units
--------------

**Relative units** là loại đơn vị sẽ có giá trị tương đối so với độ dài của thuộc tính.

Ngược lại với **Absolute units** như `pixels`, `points` hay `centimeters`, chúng ta có thể xác định kích thước theo **relative units** như `%`, `em` hoặc `rem`.

Đối với hầu hết các trình duyệt, font-size mặc định sẽ là `16px`, ta có thể lấy giá trị này làm giá trị chuẩn để tính toán (vd: `16px` tương đương với `1em`, `1rem` hoặc `100%`)

| Unit | Description |
| --- | --- |
| % | Có giá trị tương đối so với phần tử cha |
| em | Tương đối so với font-size của phần tử cha (vd `2.5em` tức là font sẽ lớn hơn normal font 2.5 lần) |
| rem | Tương đối so với phần tử gốc. Phần tử gốc ở đây là thẻ html |
| ch | Tương đối so với width của phần tử "0" |
| ex | Tương đối so với x-height của font hiện tại |

![](https://images.viblo.asia/full/9b22883f-5b48-47f3-a01e-08a08fd1e9bd.png)

Absolute Units
--------------

**Absolute units** là loại đơn vị có giá trị không thay đổi theo kích thước màn hình, hướng và các biến thể khác, tuy nhiên chỉ chính xác tuyệt đối khi output có độ phân giải đủ cao.

**Absolute units** sẽ cần thiết trong các trường hợp yêu cầu kích thước phần tử phải chính xác 100% và không được thay đổi. Chúng cũng khá hữu dụng nếu ta muốn cố định một khoảng nào đó để tránh các trường hợp khoảng đó trở nên quá rộng hoặc quá hẹp.

| Unit | Description |

 |
| --- | --- | --- |
| cm | centimeters | 1 cm = 1 cm |
| mm | millimeters | 10 mm = 1 cm |
| in | inches | 1 in = 96px = 2.54 cm |
| px | pixels | 1 px = 1/96th of 1 in |
| pt | points | 1 pt = 1/72 of 1 in |
| pc | pica | 1pc = 12 pt |

![](https://images.viblo.asia/full/96caac3e-d7d3-458a-b3aa-7bbec94b5dc3.png)

Viewport Units
--------------

Các **Viewport Units** đại diện cho một tỉ lệ % của khung nhìn (viewport) của trình duyệt hiện tại.

Sự khác biệt so với **Percentage units** là các **Viewport units** luôn luôn được tính bằng tỉ lệ phần trăm kích thước viewport của trình duyệt, trong khi đó **Percentage units** lại kế thừa kích thước của các phần tử cha của chúng.

| Unit | Description |
| --- | --- |
| vw | 1% chiều rộng của viewport |
| vh | 1% chiều cao của viewport |
| vmin | 1vw hoặc 1vh, tùy theo số nào nhỏ hơn |
| vmax | 1vw hoặc 1vh, tùy theo số nào lớn hơn |

![](https://images.viblo.asia/full/c9da1f8e-7628-4490-8b80-545431b0f841.png)

Browser Support
---------------

Các đơn vị đo được hỗ trợ trong từng phiên bản của trình duyệt, trích từ w3school:

![](https://images.viblo.asia/full/1497afde-8aae-44e8-a90f-1899a7b4e762.png)

Summary
-------

Bài viết nhằm tóm tắt về các đơn vị đo (units) trong CSS và ý nghĩa cũng như đặc điểm của từng unit. Bài viết không tránh khỏi các thiếu sót, cảm ơn các bạn đã dành thời gian đọc bài viết.

Nguồn:

-   <https://www.w3schools.com/cssref/css_units.asp>
-   <https://dev.to/fullstack_to/units-in-css-em-rem-pt-px-vw-vh-vmin-vmax-ex-ch-53l0>

All rights reserved

https://viblo.asia/p/cach-su-dung-co-ban-css-variables-gGJ59kXGZX2

### Thuộc tính Padding trong CSS - CSS Padding
[thuthuat.taimienphi.vn](https://thuthuat.taimienphi.vn/thuoc-tinh-padding-trong-css-50601n.aspx)

Thuộc tính padding trong CSS
============================

Duy Tâm

4--5 minutes

* * * * *

**Trong bài học CSS trước bạn đọc đã cùng Taimienphi.vn tìm hiểu các thuộc tính định dạng danh sách (list) trong CSS, trong bài học tiếp theo dưới đây Taimienphi.vn sẽ giới thiệu tiếp cho bạn thuộc tính [padding](https://thuthuat.taimienphi.vn/thuoc-tinh-padding-trong-css-50601n.aspx) trong CSS.**

Bài viết liên quan

-   [Học thuộc tính cursor trong CSS, có ví dụ](https://thuthuat.taimienphi.vn/thuoc-tinh-cursor-trong-css-50605n.aspx)
-   [Thuộc tính định dạng danh sách (list) trong CSS](https://thuthuat.taimienphi.vn/thuoc-tinh-dinh-dang-danh-sach-list-trong-css-50597n.aspx)
-   [Scrollbar trong CSS, có ví dụ minh họa](https://thuthuat.taimienphi.vn/scrollbar-trong-css-50604n.aspx)
-   [Thuộc tính định dạng bảng trong CSS](https://thuthuat.taimienphi.vn/thuoc-tinh-dinh-dang-bang-trong-css-49679n.aspx)
-   [Thuộc tính Outline trong CSS](https://thuthuat.taimienphi.vn/thuoc-tinh-outline-trong-css-50606n.aspx)

**Thuộc tính padding trong CSS** được sử dụng để tạo khoảng trống giữa nội dung hiển thị của một phần tử với đường viền của nó. Tham khảo tiếp bài [học CSS](https://thuthuat.taimienphi.vn/hoc-css-48838n.aspx) dưới đây của Taimienphi.vn để tìm hiểu các thuộc tính padding trong CSS.

![thuoc tinh padding trong css](https://thuthuat.taimienphi.vn/cf/Images/gl/2019/8/8/thuoc-tinh-padding-trong-css-.jpg)

Thuộc tính padding trong CSS

**1
. Các thuộc tính padding trong CSS**

CSS bao gồm các thuộc tính để chỉ định padding cho từng phần không gian của phần tử:

- Thuộc tính padding-top.

- Thuộc tính padding-right.

- Thuộc tính padding-bottom.

- Thuộc tính padding-left.

Tất cả các thuộc tính padding có thể bao gồm các giá trị dưới đây:

**- length:** chỉ định giá trị padding dưới dạng đơn vị px, pt, cm, ... .

**- %:** chỉ định giá trị padding dưới dạng % chiều rộng của phần tử chứa.

**- inherit:** chỉ định giá trị padding được kế thừa từ phần tử cha.

**Lưu ý**: Các thuộc tính padding không nhận giá trị âm.

**Ví dụ:**

![thuoc tinh padding trong css](https://taimienphi.vn/tmp/cf/aut/thuoc-tinh-padding-trong-css.jpg)

Kết quả đầu ra có dạng như dưới đây:

![thuoc tinh padding trong css 2](https://taimienphi.vn/tmp/cf/aut/thuoc-tinh-padding-trong-css-1.jpg)

***1.1 Thuộc tính padding rút gọn***

Để rút gọn mã, chúng ta có thể chỉ định tất cả các thuộc tính padding trong một khai báo.

Sử dụng thuộc tính **padding** để khai báo tất cả các thuộc tính dưới đây trong một khai báo:

- Thuộc tính padding-top.

- Thuộc tính padding-right.

- Thuộc tính padding-bottom.

- Thuộc tính padding-left.

**Trong đó:**

- Nếu thuộc tính **padding** có 4 giá trị:

**padding: 25px 50px 75px 100px;**

Padding bên trên là 25px

Padding bên phải là 50px

Padding bên dưới là 75px

Padding bên trái là 100px

**Ví dụ 1:**

![thuoc tinh padding trong css 3](https://imgt.taimienphi.vn/cf/Images/gl/2019/7/16/thuoc-tinh-padding-trong-css-2.jpg)

Kết quả đầu ra có dạng như dưới đây:

![thuoc tinh padding trong css 4](https://imgt.taimienphi.vn/cf/Images/gl/2019/7/16/thuoc-tinh-padding-trong-css-3.jpg)

- Nếu thuộc tính **padding** có 3 giá trị:

**padding: 25px 50px 75px;**

Padding bên trên là 25px

Padding bên phải và trái là 50px

Padding bên dưới là 75px

**Ví dụ 2:**

![thuoc tinh padding trong css 5](https://imgt.taimienphi.vn/cf/Images/gl/2019/7/16/thuoc-tinh-padding-trong-css-4.jpg)

Kết quả đầu ra có dạng như dưới đây:

![thuoc tinh padding trong css 6](https://imgt.taimienphi.vn/cf/Images/gl/2019/7/16/thuoc-tinh-padding-trong-css-5.jpg)

- Nếu thuộc tính **padding** có 2 giá trị:

**padding: 25px 50px;**

Padding bên trên và dưới là 25px

Padding bên phải và trái là 50px

**Ví dụ 3:**

![thuoc tinh padding trong css 7](https://imgt.taimienphi.vn/cf/Images/gl/2019/7/16/thuoc-tinh-padding-trong-css-6.jpg)

Kết quả đầu ra có dạng như dưới đây:

![thuoc tinh padding trong css 8](https://imgt.taimienphi.vn/cf/Images/gl/2019/7/16/thuoc-tinh-padding-trong-css-7.jpg)

- Nếu thuộc tính **padding** có 1 giá trị:

**padding: 25px;**

Tất cả các padding là 25px

**Ví dụ 4:**

![thuoc tinh padding trong css 9](https://imgt.taimienphi.vn/cf/Images/gl/2019/7/16/thuoc-tinh-padding-trong-css-8.jpg)

Kết quả đầu ra có dạng như dưới đây:

![thuoc tinh padding trong css 10](https://imgt.taimienphi.vn/cf/Images/gl/2019/7/16/thuoc-tinh-padding-trong-css-9.jpg)

***1.2 Thuộc tính width***

Thuộc tính **width** trong CSS xác định chiều rộng vùng nội dung của phần tử. Vùng nội dung là phần bên trong padding, đường viền và lề của phần tử (gọi là Box Model - định dạng khung, hộp bao quanh một phần tử).

Vì vậy nếu chiều rộng phần tử đã được chỉ định, khi chúng ta thêm padding vào phần tử đó, nó sẽ được tính vào tổng chiều rộng của phần tử.

**Ví dụ 1:**

![thuoc tinh padding trong css 11](https://imgt.taimienphi.vn/cf/Images/gl/2019/7/16/thuoc-tinh-padding-trong-css-10.jpg)

Kết quả đầu ra có dạng như dưới đây:

![thuoc tinh padding trong css 12](https://imgt.taimienphi.vn/cf/Images/gl/2019/7/16/thuoc-tinh-padding-trong-css-11.jpg)

Trong ví dụ này phần tử **div** có chiều rộng được chỉ định là 30px. Tuy nhiên thực tế chiều rộng của phần tử **div** là 350px (300px + 25px padding bên trái + 25px padding bên phải).

Để giữ nguyên chiều rộng phần tử **div** là 300px ngay cả khi thêm padding, chúng ta sử dụng thuộc tính **box-sizing.**

**Ví dụ 2:**

![thuoc tinh padding trong css 13](https://imgt.taimienphi.vn/cf/Images/gl/2019/7/16/thuoc-tinh-padding-trong-css-12.jpg)

Kết quả đầu ra có dạng như dưới đây:

![thuoc tinh padding trong css 14](https://imgt.taimienphi.vn/cf/Images/gl/2019/7/16/thuoc-tinh-padding-trong-css-13.jpg)

***1.3 Thuộc tính padding trong CSS***

Dưới đây là bảng danh sách tất cả các thuộc tính padding trong CSS:

![thuoc tinh padding trong css 15](https://imgt.taimienphi.vn/cf/Images/gl/2019/7/16/thuoc-tinh-padding-trong-css-14.jpg)

https://thuthuat.taimienphi.vn/thuoc-tinh-padding-trong-css-50601n.aspx

Bài học trên đây Taimienphi.vn vừa giới thiệu cho bạn các thuộc tính padding trong CSS. Ngoài ra bạn đọc có thể tham khảo thêm một số bài học CSS khác đã có trên Taimienphi.vn để tìm hiểu thêm [**thuộc tính margin trong CSS**](https://thuthuat.taimienphi.vn/thuoc-tinh-margin-trong-css-50600n.aspx) là gì nhé.

### Thuộc tính Border trong CSS - CSS Border

[thuthuat.taimienphi.vn](https://thuthuat.taimienphi.vn/thuoc-tinh-border-trong-css-50591n.aspx)

Thuộc tính border trong CSS, cú pháp và ví dụ minh họa
======================================================

Duy Tâm

5--6 minutes

* * * * *

**Trong bài học CSS trước Taimienphi.vn đã giới thiệu cho bạn về các thuộc tính định dạng bảng trong CSS. Trong bài viết tiếp theo dưới đây Taimienphi.vn sẽ giới thiệu tiếp cho bạn về thuộc tính border trong CSS.**

Bài viết liên quan

-   [Scrollbar trong CSS, có ví dụ minh họa](https://thuthuat.taimienphi.vn/scrollbar-trong-css-50604n.aspx)
-   [Tìm hiểu Link trong CSS, cú pháp và ví dụ](https://thuthuat.taimienphi.vn/link-trong-css-49088n.aspx)
-   [Học thuộc tính cursor trong CSS, có ví dụ](https://thuthuat.taimienphi.vn/thuoc-tinh-cursor-trong-css-50605n.aspx)
-   [Thuộc tính định dạng bảng trong CSS](https://thuthuat.taimienphi.vn/thuoc-tinh-dinh-dang-bang-trong-css-49679n.aspx)
-   [Thuộc tính Margin trong CSS](https://thuthuat.taimienphi.vn/thuoc-tinh-margin-trong-css-50600n.aspx)

Sử dụng thuộc tính **border** trong CSS để chỉ định kiểu, chiều rộng và màu sắc đường viền của phần tử. Tham khảo tiếp bài viết dưới đây của Taimienphi.vn để tìm hiểu các thuộc tính border trong CSS.

![thuoc tinh border trong css hoc css](https://thuthuat.taimienphi.vn/cf/Images/gl/2019/8/2/thuoc-tinh-border-trong-css-hoc-css.jpg)

Thuộc tính border trong CSS

**Thuộc tính border trong CSS**
-------------------------------

***1
. Thuộc tính border-style trong CSS***

Thuộc tính **border-style** trong CSS xác định loại đường viền sẽ được hiển thị.

Thuộc tính này bao gồm các giá trị:

**- dotted:** xác định đường viền chấm.

**- dashed:** xác định đường viền nét đứt.

**- solid:** xác định đường viền liền.

**- double:** xác định đường viền đôi.

**- groove:** xác định đường viền có rãnh 3D. Hiệu ứng phụ thuộc vào giá trị border-color.

**- ridge:** xác định đường viền cho đường chóp. Hiệu ứng phụ thuộc vào giá trị border-color.

**- inset:** xác định đường viền cho đường bóng bên trong. Hiệu ứng phụ thuộc vào giá trị border-color.

**- outset:** xác địnhđường viền cho đường bóng bên ngoài. Hiệu ứng phụ thuộc vào giá trị border-color.

**- none:** không có đường viền.

**- hidden:** xác định đường viền ẩn.

Thuộc tính **border-style** có thể bao gồm từ 1 đến 4 giá trị (cho đường viền ở trên cùng, đường viền bên phải, đường viền dưới cùng và đường viền bên trái).

**Ví dụ:**

![thuoc tinh border trong css](https://taimienphi.vn/tmp/cf/aut/thuoc-tinh-border-trong-css.jpg)

Kết quả đầu ra có dạng như dưới đây:

![thuoc tinh border trong css 2](https://taimienphi.vn/tmp/cf/aut/thuoc-tinh-border-trong-css-1.jpg)

***2
. Thuộc tính border-width***

Thuộc tính **border-width** trong CSS chỉ định chiều rộng của 4 đường viền.

Đơn vị chiều rộng có thể là px, pt, cm, em, ... hoặc một trong ba giá trị được xác định trước là thin, medium hoặc thick.

Thuộc tính **border-width** có thể bao gồm từ 1 đến 4 giá trị (cho đường viền ở trên cùng, đường viền bên phải, đường viền dưới cùng và đường viền bên trái).

**Ví dụ:**

![thuoc tinh border trong css 3](https://imgt.taimienphi.vn/cf/Images/gl/2019/7/16/thuoc-tinh-border-trong-css-2.jpg)

Kết quả đầu ra có dạng như dưới đây:

![thuoc tinh border trong css 4](https://imgt.taimienphi.vn/cf/Images/gl/2019/7/16/thuoc-tinh-border-trong-css-3.jpg)

***3
. Thuộc tính border-color***

Thuộc tính **border-color** được sử dụng để thiết lập màu sắc cho 4 đường viền.

Giá trị màu sắc được thiết lập bởi:

- Name: chỉ định tên một màu bất kỳ, chẳng hạn như red.

- Hex: chỉ định giá trị hex, chẳng hạn như #ff0000.

- RBG: chỉ định giá trị RBG, chẳng hạn như rgb(255,0,0).

- Thuộc tính transparent.

Thuộc tính nàycó thể bao gồm từ 1 đến 4 giá trị (cho đường viền ở trên cùng, đường viền bên phải, đường viền dưới cùng và đường viền bên trái).

Nếu **border-color** không được thiết lập, màu của đường viền sẽ là màu của phần tử.

**Ví dụ:**

![thuoc tinh border trong css 5](https://imgt.taimienphi.vn/cf/Images/gl/2019/7/16/thuoc-tinh-border-trong-css-4.jpg)

Kết quả đầu ra có dạng như dưới đây:

![thuoc tinh border trong css 6](https://imgt.taimienphi.vn/cf/Images/gl/2019/7/16/thuoc-tinh-border-trong-css-5.jpg)

***4
. Tạo đường viền cho từng phần***

Trong các ví dụ trên chúng ta có thể chỉ định, tạo từng đường viền khác nhau cho từng phần (viền trên, trái, phải và viền dưới).

Trong CSS cũng có các thuộc tính để chỉ định, tạo từng đường viền ( trên, dưới, phải và trái).

**Ví dụ:**

![thuoc tinh border trong css 7](https://imgt.taimienphi.vn/cf/Images/gl/2019/7/16/thuoc-tinh-border-trong-css-6.jpg)

Kết quả đầu ra có dạng như dưới đây:

![thuoc tinh border trong css 8](https://imgt.taimienphi.vn/cf/Images/gl/2019/7/16/thuoc-tinh-border-trong-css-7.jpg)

Trong ví dụ trên:

**-** Nếu thuộc tính **border-style** có 4 giá trị:

**border-style: dotted solid double dashed;**

Đường viền chóp là đường viền nét đứt.

Đường viền bên phải liền.

Đường viền dưới là đường viền đôi.

Đường viền trái là đường viền nét đứt.

**-** Nếu thuộc tính **border-style** có 3 giá trị:

**border-style: dotted solid double;**

Đường viền chóp là đường viền nét đứt.

Đường viền trái và phải là đường viền liền.

Đường viền dưới là đường viền đôi.

**-** Nếu thuộc tính **border-style** có 2 giá trị:

**border-style: dotted solid;**

Đường viền chóp và dưới là đường viền nét đứt.

Đường viền trái và phải là đường viền liền.

**-** Nếu thuộc tính **border-style** có 1 giá trị:

**border-style: dotted;**

Tất cả 4 đường đều là đường viền nét đứt.

***5
. Thuộc tính border rút gọn***

Để rút gọn mã, chúng ta có thể khai báo tất cả các thuộc tính border trong một thuộc tính duy nhất.

**Border** là thuộc tính rút gọn của các thuộc tính dưới đây:

border-width

border-style (bắt buộc)

border-color

**Ví dụ:**

![thuoc tinh border trong css 9](https://imgt.taimienphi.vn/cf/Images/gl/2019/7/16/thuoc-tinh-border-trong-css-8.jpg)

Kết quả đầu ra có dạng như dưới đây:

![thuoc tinh border trong css 10](https://imgt.taimienphi.vn/cf/Images/gl/2019/7/16/thuoc-tinh-border-trong-css-9.jpg)

Ngoài ra chúng ta cũng có thể khai báo tất cả các thuộc tính border riêng lẻ cho một phần (trái, phải, trên, dưới) trong một thuộc tính duy nhất.

**Ví dụ 1:**

![thuoc tinh border trong css 11](https://imgt.taimienphi.vn/cf/Images/gl/2019/7/16/thuoc-tinh-border-trong-css-10.jpg)

Kết quả đầu ra có dạng như dưới đây:

![thuoc tinh border trong css 12](https://imgt.taimienphi.vn/cf/Images/gl/2019/7/16/thuoc-tinh-border-trong-css-11.jpg)

**Ví dụ 2:**

![thuoc tinh border trong css 13](https://imgt.taimienphi.vn/cf/Images/gl/2019/7/16/thuoc-tinh-border-trong-css-12.jpg)

Kết quả đầu ra có dạng như dưới đây:

![thuoc tinh border trong css 14](https://imgt.taimienphi.vn/cf/Images/gl/2019/7/16/thuoc-tinh-border-trong-css-13.jpg)

***6
. Thuộc tính border-radius***

Thuộc tính **border-radius** được sử dụng để bo tròn đường viền cho một phần tử.

![thuoc tinh border trong css 15](https://imgt.taimienphi.vn/cf/Images/gl/2019/7/16/thuoc-tinh-border-trong-css-14.jpg)

Kết quả đầu ra có dạng như dưới đây:

![thuoc tinh border trong css 16](https://imgt.taimienphi.vn/cf/Images/gl/2019/7/16/thuoc-tinh-border-trong-css-15.jpg)

**Lưu ý:** Thuộc tính border-radius không hỗ trợ IE8 và các phiên bản cũ hơn.

***7
. Các thuộc tính border trong CSS***

Dưới đây là bảng danh sách các thuộc tính border trong CSS:

![thuoc tinh border trong css 17](https://imgt.taimienphi.vn/cf/Images/gl/2019/7/16/thuoc-tinh-border-trong-css-16.jpg)

![thuoc tinh border trong css 18](https://imgt.taimienphi.vn/cf/Images/gl/2019/7/16/thuoc-tinh-border-trong-css-17.jpg)

https://thuthuat.taimienphi.vn/thuoc-tinh-border-trong-css-50591n.aspx

Bài [học CSS](https://thuthuat.taimienphi.vn/hoc-css-48838n.aspx) trên đây Taimienphi.vn vừa giới thiệu cho bạn các thuộc tính border trong CSS. Trong các bài học CSS tiếp theo Taimienphi.vn sẽ giới thiệu tiếp cho bạn về **[thuộc tính Margin trong CSS](https://thuthuat.taimienphi.vn/thuoc-tinh-margin-trong-css-50600n.aspx)** nhé.

### Thuộc tính Margin trong CSS - Tư duy sử dụng CSS Margin

[thuthuat.taimienphi.vn](https://thuthuat.taimienphi.vn/thuoc-tinh-margin-trong-css-50600n.aspx)

[TaiMienPhi.Vn] Thuộc tính Margin trong CSS, cấu trúc và ví dụ minh họa
=======================================================================

4--5 minutes

* * * * *

**Bài học CSS trước Taimienphi.vn đã giới thiệu cho bạn về thuộc tính border trong CSS, trong bài học tiếp theo dưới đây Taimienphi.vn sẽ giới thiệu tiếp cho bạn về các thuộc tính [Margin](https://thuthuat.taimienphi.vn/thuoc-tinh-margin-trong-css-50600n.aspx) trong CSS.**

Bài viết liên quan

-   [Thuộc tính định dạng danh sách (list) trong CSS](https://thuthuat.taimienphi.vn/thuoc-tinh-dinh-dang-danh-sach-list-trong-css-50597n.aspx)
-   [Thuộc tính padding trong CSS](https://thuthuat.taimienphi.vn/thuoc-tinh-padding-trong-css-50601n.aspx)
-   [Thuộc tính border trong CSS, cú pháp và ví dụ minh họa](https://thuthuat.taimienphi.vn/thuoc-tinh-border-trong-css-50591n.aspx)
-   [Thuộc tính định dạng bảng trong CSS](https://thuthuat.taimienphi.vn/thuoc-tinh-dinh-dang-bang-trong-css-49679n.aspx)
-   [Scrollbar trong CSS, có ví dụ minh họa](https://thuthuat.taimienphi.vn/scrollbar-trong-css-50604n.aspx)

**Thuộc tính Margin trong CSS** được sử dụng để tạo khoảng trống xung quanh các phần tử, bên ngoài các [tạo viền trong word](https://thuthuat.taimienphi.vn/tao-duong-vien-trong-van-ban-word-719n.aspx). Tham khảo tiếp bài [học CSS](https://thuthuat.taimienphi.vn/hoc-css-48838n.aspx) dưới đây của Taimienphi.vn để tìm hiểu các thuộc tính Margin trong CSS.

![thuoc tinh margin trong css hoc css](https://thuthuat.taimienphi.vn/cf/Images/gl/2019/8/2/thuoc-tinh-margin-trong-css-hoc-css.jpg)

### Thuộc tính Margin trong CSS

**1
. Thuộc tính Margin trong CSS**

CSS bao gồm các thuộc tính để chỉ định, canh lề cho từng phần phần của phần tử:

margin-top

margin-right

margin-bottom

margin-left

Tất cả các thuộc tính margin có thể bao gồm các giá trị:

- **auto**: tính toán canh lề trong trình duyệt.

**- length:** canh lề ở định dạng px, pt, cm, ... .

**- %:** canh lề theo % chiều rộng của phần tử chứa.

**- inherit:** chỉ định lề phải được kế thừa từ phần tử cha.

**Mẹo:** các giá trị âm cũng được cho phép.

**Ví dụ:** Trong ví dụ dưới đây canh 4 lề khác nhau cho 4 phần của phần tử tử **p**:

![thuoc tinh margin trong css](https://taimienphi.vn/tmp/cf/aut/thuoc-tinh-margin-trong-css.jpg)

Kết quả đầu ra có dạng như dưới đây:

![thuoc tinh margin trong css 2](https://taimienphi.vn/tmp/cf/aut/thuoc-tinh-margin-trong-css-1.jpg)

***1.1. Thuộc tính Margin rút gọn***

Để rút gọn mã, chúng ta có thể khai báo tất cả các thuộc tính margin trong một thuộc tính duy nhất.

Thuộc tính **margin** rút gọn, khai báo các thuộc tính dưới đây:

margin-top

margin-right

margin-bottom

margin-left

**Trong đó:**

- Nếu thuộc tính **margin** có 4 giá trị:

**margin: 25px 50px 75px 100px;**

Lề trên là 25px

Lề phải là 50px

Lề dưới là 75px

Lề trái là 100px

**Ví dụ 1:**

![thuoc tinh margin trong css 3](https://imgt.taimienphi.vn/cf/Images/gl/2019/7/16/thuoc-tinh-margin-trong-css-2.jpg)

Kết quả đầu ra có dạng như dưới đây:

![thuoc tinh margin trong css 4](https://imgt.taimienphi.vn/cf/Images/gl/2019/7/16/thuoc-tinh-margin-trong-css-3.jpg)

- Nếu thuộc tính **margin** có 3 giá trị:

**margin: 25px 50px 75px;**

Lề trên là 25px

Lề phải và trái là 50px

Lề dưới là 75px

**Ví dụ 2:**

![thuoc tinh margin trong css 5](https://imgt.taimienphi.vn/cf/Images/gl/2019/7/16/thuoc-tinh-margin-trong-css-4.jpg)

Kết quả đầu ra có dạng như dưới đây:

![thuoc tinh margin trong css 6](https://imgt.taimienphi.vn/cf/Images/gl/2019/7/16/thuoc-tinh-margin-trong-css-5.jpg)

- Nếu thuộc tính **margin** có 2 giá trị:

**margin: 25px 50px;**

Lề trên và dưới là 25px

Lề phải và trái là 50px

**Ví dụ 3:**

![thuoc tinh margin trong css 7](https://imgt.taimienphi.vn/cf/Images/gl/2019/7/16/thuoc-tinh-margin-trong-css-6.jpg)

Kết quả đầu ra có dạng như dưới đây:

![thuoc tinh margin trong css 8](https://imgt.taimienphi.vn/cf/Images/gl/2019/7/16/thuoc-tinh-margin-trong-css-7.jpg)

- Nếu thuộc tính **margin** có 1 giá trị:

**margin: 25px;**

Giá trị 4 lề là 25px.

**Ví dụ 4:**

![thuoc tinh margin trong css 9](https://imgt.taimienphi.vn/cf/Images/gl/2019/7/16/thuoc-tinh-margin-trong-css-8.jpg)

Kết quả đầu ra có dạng như dưới đây:

![thuoc tinh margin trong css 10](https://imgt.taimienphi.vn/cf/Images/gl/2019/7/16/thuoc-tinh-margin-trong-css-9.jpg)

***1.2. Giá trị auto***

Chúng ta có thể thiết lập giá trị thuộc tính margin là **auto** để tự động căn chỉnh giữa các phần tử bên trong container của nó.

Phần tử đó sẽ áp dụng chiều rộng được chỉ định và phần khoảng trống còn lại sẽ được chia đều cho lề trái và lề phải.

**Ví dụ:**

![thuoc tinh margin trong css 11](https://imgt.taimienphi.vn/cf/Images/gl/2019/7/16/thuoc-tinh-margin-trong-css-10.jpg)

Kết quả đầu ra có dạng như dưới đây:

![thuoc tinh margin trong css 12](https://imgt.taimienphi.vn/cf/Images/gl/2019/7/16/thuoc-tinh-margin-trong-css-11.jpg)

***1.3. Giá trị inherit***

Trong ví dụ dưới đây cho phép lề trái của phần tử (p class="ex1") được kế thừa từ phần tử cha (div).

**Ví dụ:**

![thuoc tinh margin trong css 13](https://imgt.taimienphi.vn/cf/Images/gl/2019/7/16/thuoc-tinh-margin-trong-css-12.jpg)

Kết quả đầu ra có dạng như dưới đây:

![thuoc tinh margin trong css 14](https://imgt.taimienphi.vn/cf/Images/gl/2019/7/16/thuoc-tinh-margin-trong-css-13.jpg)

***1.4. Margin Collapse trong CSS***

Đôi khi chúng ta có thể gộp lề trên và dưới của các phần tử thành một lề duy nhất bằng cách lấy giá trị được tính từ tổng 2 lề.

**Lưu ý:** phương pháp này chỉ áp dụng cho lề trên và lề dưới, không áp dụng cho lề trái và lề phải.

**Ví dụ:**

![thuoc tinh margin trong css 15](https://imgt.taimienphi.vn/cf/Images/gl/2019/7/16/thuoc-tinh-margin-trong-css-14.jpg)

Kết quả đầu ra có dạng như dưới đây:

![thuoc tinh margin trong css 16](https://imgt.taimienphi.vn/cf/Images/gl/2019/7/16/thuoc-tinh-margin-trong-css-15.jpg)

Trong ví dụ trên, lề dưới của phần tử **h1** là 50px và lề trên của phần tử **p** là 20px.

Tổng giá trị của 2 lề là 70 px (50px + 20px), tuy nhiên vì thuộc tính margin collapse gộp các lề là 1 nên giá trị lề thực tế là 50px.

***1.5. Các thuộc tính Margin trong CSS***

Dưới đây là bảng danh sách các thuộc tính Margin trong CSS:

![thuoc tinh margin trong css 17](https://imgt.taimienphi.vn/cf/Images/gl/2019/7/16/thuoc-tinh-margin-trong-css-16.jpg)

https://thuthuat.taimienphi.vn/thuoc-tinh-margin-trong-css-50600n.aspx

Bài học CSS trên đây Taimienphi.vn vừa giới thiệu cho bạn về các thuộc tính Margin trong CSS. Trong các bài học tiếp theo Taimienphi.vn sẽ giới thiệu tiếp cho bạn thuộc tính định dạng [**danh sách list trong CSS**](https://thuthuat.taimienphi.vn/thuoc-tinh-dinh-dang-danh-sach-list-trong-css-50597n.aspx) nhé.

### CSS Box-sizing - Tính ứng dụng của Box-sizing

[thachpham.com](https://thachpham.com/web-development/html-css/hoc-css-tim-hieu-box-sizing.html)

Tìm hiểu box-sizing trong CSS3
==============================

Bởi Thạch Phạm

3--4 minutes

* * * * *

Khi các bạn học qua Box Model trong CSS thì sẽ thấy có một đặc điểm khi sử dụng Padding và Border thì cái khung phần tử của bạn sẽ bị biến đổi kích thước nếu bạn có đặt thêm thuộc tính `width` và `height` để thiết lập kích thước cho nó. Ví dụ cái box của bạn có width là 500px và height là 500px (500×500 px)nhưng nếu bạn đặt thêm padding là 15px nữa thì cái khung của bạn sẽ có kích thước là 530×530 px. Bởi vì nếu cộng thêm `pading` là 15px nữa thì cái khung của bạn sẽ tự động cộng thêm 30px (15px cho top và và 15px cho bottom, tương tự với left và right), tương tự với`border`.

[![css-box-sizing-01](https://thachpham.com/wp-content/swift-ai/images/wp-content/uploads/2015/04/css-box-sizing-01-png.webp "[Học CSS] Tìm hiểu box-sizing 4")](https://thachpham.com/wp-content/uploads/2015/04/css-box-sizing-01.png)

Vậy thì nếu bây giờ bạn muốn làm cho phần tử của mình phải giữ nguyên kích thước mặc dù có cộng thêm padding và border thì sẽ cần phải dùng đến thuộc tính box-sizing. box-sizing là một thuộc tính sẽ giúp bạn có thể tính toán và làm chủ được kích thước của một phần tử dựa vào thuộc tính width và height đã được thiết lập bên trong. Hay nói cách khác, là bạn sẽ muốn thuộc tính`width` và `height` là kích thước đã bao gồm border và padding.

### Lưu ý về cách viết

`box-sizing` là một thuộc tính trong CSS3 nên khi viết bạn phải viết thành 3 lần với các tiền tố khác nhau, ví dụ:

box-sizing: border-box;

-moz-box-sizing: border-box;

-webkit-box-sizing: border-box;

Trong đó, nếu viết không có tiền tố là dành cho trình duyệt IE8, Opera 7, Firefox và Google chrome bản mới. `-webkit` là dành cho Google Chrome bản cũ và `-moz` là dành cho Firefox bản cũ.

### Các giá trị của box-sizing

Hiện tại `box-sizing` có hỗ trợ một số giá trị như sau:

-   `content-box`: Giá trị mặc định, nghĩa là giá trị width và height chỉ áp dụng cho khu vực nội dung bên trong, không bao gồm padding, border và margin.
-   `border-box`: Khi thiết lập giá trị này, thì width và heigh sẽ bao gồm cho cả phần nội dung, padding và border nhưng không bao gồm margin.
-   `padding-box`: Với giá trị này thì width và height chỉ bao gồm cho phần nội dung và padding, không bao gồm border và margin.

**Lưu ý**: `padding-box` chỉ có tác dụng với trình duyệt Firefox.

Như vậy với ba giá trị này, mình khuyến khích các bạn chỉ **nên sử dụng giá trị** `border-box` vì nó rất đầy đủ, dễ tính toán cho website.

### Nên sử dụng box-sizing cho toàn bộ phần tử

Theo kinh nghiệm của mình thì khi viết CSS cho website, bạn hãy sử dụng `box-sizing` với giá trị là `border-box` **cho toàn bộ các phần tử** trong website để các phần tử có kích thước chính xác khi bạn khai báo, tránh việc cộng thêm các phần border và padding sẽ gây ra rắc rối nếu bạn dùng hai cái này thường xuyên.

Để thiết lập `box-sizing: content-box` cho toàn bộ phần tử, chúng ta sẽ sử dụng vùng chọn là `*`, nghĩa là bao gồm mọi phần tử.

* {

   box-sizing: border-box;

   -moz-box-sizing: border-box;

   -webkit-box-sizing: border-box;

}

### Lời kết

Mặc dù box-sizing có thể là không quan trọng đến mức bắt buộc sử dụng nhưng có thể nó sẽ giúp bạn giải đáp về thắc mắc là tại sao thiết lập kích thước cho phần tử là như vậy mà thêm padding, border vào nó lại hiển thị theo với kích thước khác. Và trên một số trường hợp, nó sẽ giúp bạn dễ dàng quản lý kích thước các phần tử nhờ vào việc tùy chỉnh lại giá trị box-sizing như mình đã đề cập ở trên.

### CSS Background

[viblo.asia](https://viblo.asia/p/tat-tan-tat-ve-thuoc-tinh-background-trong-css-LzD5dPXW5jY)

Tất tần tật về thuộc tính background trong css
==============================================

Nguyen Manh Tung

7--9 minutes

* * * * *

### background-color

thuộc tính background-color dùng để đặt màu nền cho một thành phần. Nó chấp nhận tất cả giá trị các mã màu hoặc thuộc tính transparent

```
vd:
.left { background-color: #ffdb3a; }
.middle { background-color: #67b3dd; }
.right { background-color: transparent; }

```

![](https://images.viblo.asia/251eff8d-987f-4be5-b4e8-13fea362fcb6.png) Màu nền được xác định trong các ô được xác định bởi thuộc tính background-clip. Nếu có hình nền được đặt cùng thì lớp màu sẽ được đặt ở dưới. Không giống như các lớp hình ảnh có thể sử dụng nhiều lớp, chúng chỉ có thể dùng được một lớp màu cho một thành phần.

### background-image

Thuộc tính background-image định nghĩa cho hình nền của một thành phần. Nó là giá trị được định nghĩa bằng một đường dẫn hình ảnh với ký hiệu url(). Giá trị non có thể được sử dụng, nó được tính là một lớp.

```
vd:
.left { background-image: url('ire.png'); }
.right { background-image: none; }

```

![](https://images.viblo.asia/d0c86207-0bc8-4451-847b-f46b8a31e2a8.png) Chúng ta có thể sử dụng nhiều hình nền, mỗi giá trị được cách nhau bởi một dấu phẩy. Mỗi hình ảnh tiếp theo sẽ được đặt trước trên trục z.

```
vd:
.middle {
  background-image: url('khaled.png'), url('ire.png');

  /* Other styles */
  background-repeat: no-repeat;
  background-size: 100px;
}

```

![](https://images.viblo.asia/eaecd7f4-2c19-49a8-ab3c-0c9eed0a7fda.png)

### background-repeat

Thuộc tính background-repeat kiểm soát cách hình nền sau khi nó được đặt kích thước (bởi thuộc tính background-size) và vị trí (bởi thuộc tính background-position). Giá trị của của thuộc tính này có thể là một trong những từ khóa sau: repeat-x, repeat-y, repeat, space, round, no-repeat. Bên cạnh hai thuộc tính repeat-x và repeat-y, các giá trị khác có thể được định nghĩa một lần cho cả hai trục x và trục y hoặc mỗi chiều riêng biệt.

```
vd:
.top-outer-left { background-repeat: repeat-x; }
.top-inner-left { background-repeat: repeat-y; }
.top-inner-right { background-repeat: repeat; }
.top-outer-right { background-repeat: space; }

.bottom-outer-left { background-repeat: round; }
.bottom-inner-left { background-repeat: no-repeat; }
.bottom-inner-right { background-repeat: space repeat; }
.bottom-outer-right { background-repeat: round space; }

```

![](https://images.viblo.asia/e7fc37e6-38b5-4c59-b07f-3f58ab393ea7.png)

### background-size

Thuộc tính background-size định nghĩa kích thước của hình nền. Giá trị của nó có thể là kích thước chiều dài và rộng hoặc là tỉ lệ phần trăm. Từ khóa có sẵn cho thuộc tính là contain và cover. Giá trị contain sẽ co dãn hình ảnh để phù hợp với khung. giá trị cover, ở một mặt khác nó sẽ kéo dãn hình ảnh sao cho vừa với khung mà ko gây sai lệch tỉ lệ.

```
vd:
.left {
  background-size: contain;
  background-image: url('ire.png');
  background-repeat: no-repeat;
}
.right { background-size: cover; /* Other styles same as .left */ }

```

![](https://images.viblo.asia/78b5574c-644e-416c-9185-a4a7fefc36ae.png) Đối với các giá trị chiều dài và giá trị phần trăm, chúng ta có thể xác định cả chiều rộng và chiều cao của ảnh nền. Tỷ lệ phần trăm giá trị được tính toán liên quan đến kích thước của phần tử.

```
vd:
.left { background-size: 50px; /* Other styles same as .left */ }
.right { background-size: 50% 80%; /* Other styles same as .left */ }

```

![](https://images.viblo.asia/7316f7ec-57cc-4f7c-be36-feabf5bb2bcc.png)

### background-attachment

Thuộc tính background-attachment dùng để kiểm soát hình nền liên quan đến các khung hình và các thành phần. Nó có ba giá trị là: fixec, local, scroll. Fixed nghĩa là hình ảnh nền được cố định vào khung nhìn và không di chuyển, ngay cả khi người dùng đang di chuyển dọc theo khung. Local là hình nền nên được cố định vào vị trí của nó trong phần tử. Nếu phần tử có một cơ chế di chuyển và hình nền được đặt lên hàng đầu, khi người dùng cuộn xuống phần tử, hình nền sẽ di chuyển ra khỏi tầm nhìn. Scroll có nghĩa là các hình nền cố định và sẽ không di chuyển ngay cả với các nội dung của các phần tử của nó.

```
vd:
.left {
  background-attachment: fixed;
  background-size: 50%;
  background-image: url('ire.png');
  background-repeat: no-repeat;
  overflow: scroll;
}
.middle { background-attachment: local; /* Other styles same as .left */ }
.right { background-attachment: scroll; /* Other styles same as .left */ }

```

![](https://images.viblo.asia/facb750c-c886-4a6f-abc3-c2d25ff3b298.gif)

### background-position

Thuộc tính này là sự kết hợp với thuộc tính background-origin, xác định nơi các vị trí bắt đầu cho hình nền nên được. Đó là giá trị có thể là một từ khóa, chiều dài, hoặc một tỷ lệ phần trăm, và chúng tôi có thể xác định vị trí dọc theo trục x cũng như các trục y. Từ khóa có sẵn: top, right, bottom, left và center. Chúng ta có thể sử dụng các từ khóa trong bất kỳ sự kết hợp, và nếu chỉ có một từ khóa được quy định.

```
vd:
.top-left {
  background-position: top;
  background-size: 50%;
  background-image: url('ire.png');
  background-repeat: no-repeat;
}
.top-middle { background-position: right;  /* Other styles same as .top-left */ }
.top-right { background-position: bottom;  /* Other styles same as .top-left */ }
.bottom-left { background-position: left;  /* Other styles same as .top-left */ }
.bottom-right { background-position: center;  /* Other styles same as .top-left */ }

```

![](https://images.viblo.asia/24c2cf18-0abe-4e43-8f05-420ae20b15b4.png) Đối với chiều dài và tỷ lệ phần trăm giá trị, chúng ta cũng có thể xác định vị trí dọc theo trục x và trục y. Tỷ lệ phần trăm giá trị là liên quan đến các yếu tố có chứa.

```
vd:
.left { background-position: 20px 70px; /* Others same as .top-left */ }
.right { background-position: 50%; /* Others same as .top-left */ }

```

![](https://images.viblo.asia/dc9c85eb-c253-4204-93b8-72eda77d2ca9.png)

### background-origin

Thuộc tính background-origin quy định cụ thể trong đó diện tích các mô hình hộp hình nền phải được bố trí theo. Giá trị mặc định là border-box, khi mà vị trí hình ảnh ở sát viền của khung, padding-box khi mà hình ảnh ở trong viền của khung và content-box khi mà hình ảnh ở trong khung

```
vd:
.left {
  background-origin: border-box;
  background-size: 50%;
  background-image: url('ire.png');
  background-repeat: no-repeat;
  background-position: top left;
  border: 10px dotted black;
  padding: 20px;
}
.middle { background-origin: padding-box;  /* Other styles same as .left*/ }
.right { background-origin: content-box;  /* Other styles same as .left*/ }

```

![](https://images.viblo.asia/094c2981-51f5-40dc-9926-3ef43ed0ef50.png)

### background-clip

Thuộc tính background-clip xác định khu vực sơn nền, đó là khu vực mà nền có thể sơn lên, giống như background-origin, nó được dựa trên các lĩnh vực mô hình hộp.

```
vd:
.left{
  background-clip: border-box;
  background-size: 50%;
  background-color: #ffdb3a;
  background-repeat: no-repeat;
  background-position: top left;
  border: 10px dotted black;
  padding: 20px;
}
.middle { background-clip: padding-box;  /* Other styles same as .left*/ }
.right { background-clip: content-box;  /* Other styles same as .left*/ }

```

![](https://images.viblo.asia/f9a6b8a2-f86d-4273-bcf6-368a1c69a007.png)

Thảm khảo: <https://bitsofco.de/the-background-properties/>

https://viblo.asia/p/tat-tan-tat-ve-thuoc-tinh-background-trong-css-LzD5dPXW5jY

## Một số CSS Shorthand hay giúp ích cho lập trình viên

[homiedev.com](https://homiedev.com/css-shorthand-hay/)

Một số CSS Shorthand hay giúp ích cho lập trình viên
====================================================

@devnav

3--4 minutes

* * * * *

**CSS shorthand** giúp chúng ta tiết kiệm thời gian cho việc code, thay vì sử dụng cách viết hết tất cả các thuộc tính, trong một số trường hợp chúng ta có thể gom chúng lại cho gọn hơn. Bài viết này mình sẽ giới thiệu các bạn làm điều đó. Cùng đọc bài viết nhé ^^.

CSS Background
--------------

Thuộc tính `background` cho phép chúng ta kết hợp các thuộc tính `background` khác giúp giảm số dòng code ^^.

**background** viết gọn cho những thuộc tính dưới:

-   background-color
-   background-image
-   background-position
-   background-size
-   background-repeat
-   background-origin
-   background-clip
-   background-attachment

Thay vì sử dụng các thuộc tính này trên mỗi dòng code, chúng ta có thể đơn giản viết gọn chúng lại chỉ với một dòng code 👏

Thay vì viết thế này:

```
.css-shorthand {
  background-color: #ffffff;
  background-image: url("img.png");
  background-repeat: no-repeat;
  background-position: right top;
}
```

Chúng ta có thể viết

```
.css-shorthand {
  background: #ffffff url("img.png") no-repeat right top;
}
```

CSS Border
----------

Khi set `border` cho element chúng ta cũng có thể viết gọn lại như sau:

Thay vì viết:

```
.css-shorthand {
  border-width: 1px;
  border-style: dashed;
  border-color: #fff;
}
```

Ta có thể viết gọn lại thành:

```
.css-shorthand {
  border: 1px dashed #fff;
}
```

Chúng ta có thể viết gộp 3 thuộc tính lại thành 1 dòng. Nhìn ngắn gọn và dễ hiểu đúng không 😁

CSS Font
--------

Khi set **Font** cho element ta có thể sử dụng cách viết ngắn gọn sau:

Thay vì viết:

```
.css-shorthand {
  font-style: italic;
  font-weight: 600;
  font-style: 16px;
  line-height: 1.3;
  font-family: monospace;
}
```

Ta có gộp chúng lại nếu bạn cần:

```
.css-shorthand {
  font: italic 600 16px/1.3 monospace;
}
```

CSS Inset
---------

Thuộc tính **CSS inset** là một cách viết tắt tương ứng với các thuộc tính **top**, **right**, **bottom**, **left**. Nó giống với cú pháp viết tắt như khi dùng `margin` hay `padding`.

Ta có thể viết:

```
.css-shorthand {
  top: 5px;
  right: 10px;
  bottom: 5px;
  left: 10px;
}
```

Thành như sau:

```
.css-shorthand {
  inset: 5px 10px 5px 10px; /* top right bottom left */
}
```

Padding and Margin
------------------

cả `inset`, `padding` và `margin` có cú pháp viết tắt giống nhau.

Thay vì ta viết thế này:

```
.css-shorthand {
  padding-top: 10px;
  padding-right: 20px;
  padding-bottom: 10px;
  padding-left: 20px;
}
```

Ta có thể viết gọn thành:

```
.css-shorthand {
  padding: 10px 20px; /* top/bottom: 10px left/right: 20px */
}
```

Như vậy là mình đã giới thiệu cho các bạn một số cách viết **shorthand**, sử dụng cú pháp viết gọn này có thể giúp chúng ta giảm thời gian viết code, cải thiện tốc độ tải trang vì dung lượng file css được giảm thiểu rất đáng kể.

> Trong một số trường hợp dùng **shorthand** có thể khiến chúng ta khó đọc, có thể gây ra nhầm lẫn. Tuy nhiên chúng ta không thể phủ nhận lợi ích của cách viết **shorthand**. Do đó chúng ta hãy sử dụng chúng một cách hợp lí nhé ^^.

https://homiedev.com/css-shorthand-hay/

### CSS Functions - Hàm trong CSS

### CSS Pseudo classes - Khái niệm lớp giả trong CSS

[viblo.asia](https://viblo.asia/p/tim-hieu-va-van-dung-pseudo-pseudo-class-trong-css-phan-1-maGK7V7D5j2)

Tìm hiểu và vận dụng pseudo (pseudo-class) trong css - phần 1
=============================================================

Pham Thi Ngoc Mai

6--8 minutes

* * * * *

[![Avatar](https://images.viblo.asia/avatar/9f4d0699-ffec-4104-b833-862657ee0c74.jpg)](https://viblo.asia/u/maiptn226)

Đã đăng vào thg 9 10, 2019 1:25 CH 3 phút đọc

Chào các bạn!

Nhìn tiêu đề bài viết có lẽ sẽ có khá nhiều bạn thắc mắc về khái niệm **pseudo** trong css. Nó là cái gì? Mình đã từng sử dụng nó hay chưa? Nó được sử dụng như thế nào? Bài viết này sẽ giải thích qua về khái niệm cho các bạn hiểu nhé.

**Pseudo** trong css được chia làm 2 nhánh: **Peseudo-classes** và **Pseudo-elements**. Ở bài này mình sẽ chỉ nói về **peseudo-classes** còn **pseudo-elements** sẽ được giới thiệu ở bài viết sau nhé.

1
. Khái niệm
-------------

Hiểu một cách đơn giản thì **peseudo-classes** được dùng để xác định 1 trạng thái đặc biệt nào đó của 1 element. Ví dụ, trạng thái chúng ta hay sử dụng nhất đó là **:hover**, **:check**

Cú pháp để viết như sau

```
selector:pseudo-class {
   thuộc tính: giá trị;
}

```

Ví dụ

```
a {
    color: blue;
    transition: color 0.2s;
}

a:hover {
    color: red;
}

```

2
. Danh sách pseudo-classes
----------------------------

Bây giờ nếu bạn đã hiểu về **peseudo-classes** thì bạn nghĩ nó có bao nhiêu loại? Thực chất nó có rất nhiều. Mình sẽ list cho các bạn thấy như dưới đây.

| pseudo-classes | pseudo-classes | pseudo-classes |
| --- | --- | --- |
| :active | :host | :only-child |
| :link | :host() | :only-of-type |
| :blank | :host-context() | :optional |
| :checked | :hover | :out-of-range |
| :current | :indeterminate | :past |
| :default | :in-range | :placeholder-shown |
| :defined | :invalid | :read-only |
| :dir() | :is() | :read-write |
| :disabled | :lang() | :required |
| :drop | :last-child | :right |
| :empty | :last-of-type | :root |
| :enabled | :left | :scope |
| :first | :link | :target |
| :first-child | :local-link | :target-within |
| :first-of-type | :not() | :user-invalid |
| :fullscreen | :nth-child() | :valid |
| :future | :nth-col() | :visited |
| :focus | :nth-last-child() | :where() |
| :focus-visible | :nth-last-col() |

 |
| :focus-within | :nth-last-of-type() |

 |
| :has() | :nth-of-type() |

 |

3
. Cách sử dụng pseudo-classes
-------------------------------

Với số lượng pseudo-classes bên trên thì có lẽ chúng ta không dùng hết tất cả được. Tuy nhiên mình cũng sẽ giới thiệu về cách dùng của 1 số pseudo-classes hay được sử dụng cho các bạn hiểu nhé.

| pseudo-classes | Ví dụ | Mô tả chi tiết |
| --- | --- | --- |
| :link | a:link | Chọn tất cả các liên kết chưa được click |
| :hover | a:hover | Thay đổi trạng thái khi rê chuột qua <a> |
| :active | a:active | Thay đổi trạnh thái của <a> khi click vào nó) |
| :visited | a:visited | Chọn tất cả link đã truy cập |
| :checked | input:checked | Chọn mỗi phần tử <input> đã kiểm tra. |
| :disabled | input:disabled | Chọn mỗi phần tử <input> bị vô hiệu |
| :empty | li:empty | Chọn mỗi phần tử <li> không có con |
| :enabled | input:enabled | Chọn mỗi phần tử <input> được bật |
| :first-child | li:first-child | Chọn tất cả các phần tử <li> đó là con đầu tiên của parent của nó |
| :first-of-type | li:first-of-type | Chọn phần tử p đầu tiên trong những phần tử <li> có trong 1 element |
| :focus | input:focus | Thay đổi trạng thái của <input> khi vừa lựa chọn <input> đó |
| :invalid | input:invalid | Chọn tất cả các phần tử <input> có giá trị không hợp lệ |
| :last-child | li:last-child | Chọn mỗi phần tử <li> là con cuối cùng của parent. Ngược lại với :first-child |
| :last-of-type | li:last-of-type | Chọn phần tử <li> cuối cùng trong những phần tử <li> có trong 1 element. Ngược lại với :first-of-type |
| :not(selector) | :not(li) | Chọn mọi phần tử không phải là phần tử <li> |
| :nth-child(n) | li:nth-child(2) | Chọn mỗi phần tử <li> là con thứ hai của parent. Tức là phần tử thứ 2 từ trên xuống |
| :nth-child(2n), :nth-child(even) | li:nth-child(2n), li:nth-child(even) | Lựa chọn tất cả các phần tử <li> có chỉ số chẵn |
| :nth-child(2n+1), :nth-child(odd) | li:nth-child(2n+1), li::nth-child(odd) | Lựa chọn tất cả các phần tử <li> có chỉ số lẻ |
| :nth-last-child(n) | li:nth-last-child(2) | Chọn mỗi phần tử <li> là con thứ hai của cha / mẹ nó, kể từ con cuối cùng. Tức là phần tử thứ 2 từ dưới lên |
| :nth-last-of-type(n) | li:nth-last-of-type(2) | Chọn mỗi phần tử <li> là phần tử <li> thứ hai của cha / mẹ nó, tính từ con cuối cùng. Tức là trong 1 element parent bao gồm: li, p, span. Khi đó pseudo-classes này sẽ chỉ quét những element nào là <li> sau đó lựa chọn phần tử <li> thứ 2 tính từ dưới lên |
| :nth-of-type(n) | li:nth-of-type(2) | Chọn mỗi phần tử <li> là phần tử <li> thứ hai của cha / mẹ |
| :only-of-type | li:only-of-type | Chọn mỗi phần tử <li> là yếu tố <li> duy nhất của cha mẹ nó. Tức là trong 1 element parent bao gồm: li, p, span. Khi đó pseudo-classes này sẽ chỉ quét những element nào là <li> chỉ xuất hiện đúng 1 lần. Còn nếu xuất hiện từ 2 lần trở nên sẽ không tác dụng |
| :only-child | li:only-child | Chọn mỗi phần tử <li> là con duy nhất của parent của nó |
| :optional | input:optional | Chọn các phần tử <input> không có thuộc tính "required" |
| :read-only | input:read-only | Chọn các phần tử <input> với thuộc tính "readonly" được chỉ định |
| :read-write | input:read-write | Chọn các phần tử <input> mà không có thuộc tính "readonly" |
| :required | input:required | Chọn phần tử <input> với thuộc tính "required" được chỉ định |

4
. Pseudo-classes tác động lên link
------------------------------------

Trong nhóm này chúng ta sẽ có 4 pseudo-class chính đó là **:link, :visited, :hover và :active**. Về cách sử dụng của 4 pseudo-classes này mình cũng đã viết ở bên trên. Mọi người tìm đọc lại nhé

```
/* unvisited link */
a:link {
color: #FF0000;
}

/* visited link */
a:visited {
color: #00FF00;
}

/* mouse over link */
a:hover {
color: #FF00FF;
}

/* selected link */
a:active {
color: #0000FF;
}

```

Một điều chú ý ở đây là các bạn phải viết theo đúng thứ tự như trên thì css mới nhận do độ ưu tiên trong css. Nếu khi chúng ta tráo đổi vị trí như đưa **a:hover** lên trước **a:link** và **a:visited** thì khi ta rê chuột vào link nó sẽ không đổi màu, tương tự với việc nếu chúng ta đảo vị trí của **a:active** với **a:hover**.

Thực chất pseudo-class **:hover ** có thể sử dụng có các element khác chứ không chỉ sử dụng riêng cho <a> như 2 pseudo-classes **a:link** và **a:visited**.

5
. Pseudo-classes tác động lên các element trong form
------------------------------------------------------

Những pseudo-class có tác dụng với các element trong form như **:focus, :checked, :active, :read-only, :disable, :require, :invalid, :optional, :read-write**. Tất cả những pseudo-classes này mình cũng đã giải thích cách sử dụng ở bên trên.

Riêng với **:checked** các bạn có thể tham khảo cách dùng cho input ở bài viết dưới này của mình nhé

<https://viblo.asia/p/bai-10-css-cho-mot-so-tag-dac-biet-nhu-checkbox-radio-button-va-seclect-box-6J3ZgE1q5mB>

Như vậy, qua bài viết này mình đã giới thiệu tới các bạn khái niệm cũng như cách sử dụng của 1 số pseudo-classes hay sử dụng. Hi vọng bài viết này sẽ giúp ích ít nhiều cho các bạn.

All rights reserved

https://viblo.asia/p/tim-hieu-va-van-dung-pseudo-pseudo-class-trong-css-phan-1-maGK7V7D5j2

### Phần tử giả trong CSS - CSS Pseudo-elements

[viblo.asia](https://viblo.asia/p/tim-hieu-va-van-dung-pseudo-pseudo-element-trong-css-phan-2-eW65GRNalDO)

Tìm hiểu và vận dụng pseudo (pseudo-element) trong css - phần 2
===============================================================

Pham Thi Ngoc Mai

6--7 minutes

* * * * *

Chào các bạn!

Trong bài trước mình đã giới thiệu với các bạn về định nghĩa, cách sử dụng cũng như 1 vài loại **pseudo-classes** hay dùng nhất. Bài này mình sẽ giới thiệu về **pseudo-elements** trong css.

1
. Định nghĩa và cấu trúc của pseudo-element
---------------------------------------------

Pseudo-element trong CSS được dùng để định dạng một phần đặc biệt của phần tử. Chẳng hạn bạn muốn sử dụng chúng để:

-   Định dạng chữ hoặc dòng đầu tiên của phần tử
-   Chèn nội dung vào trước hoặc sau nội dung của phần tử

Cấu trúc viết thì không khác so với pseudo-classes lắm.

```
selector::pseudo-element {
    property:value;
}

```

Tuy nhiên, các bạn phải chú 1 vấn đề sau đây:

-   Đối với pseudo-class thì khi gọi là chỉ cần viết 1 dấu 2 chấm. Chẳng hạn **:hover, :focus**,...
-   Còn đối với pseudo-element thì phải viết 2 dấu 2 chấm. Ví dụ **::after, ::before**,...

Nếu như bạn viết 1 dấu 2 chấm đằng trước pseudo-element thì css vẫn có thể đọc được tuy nhiên khi bạn cài style-lint, scss-lint hay check validator w3c thì chắc chắn sẽ bị báo lỗi. Vì vậy chúng ta nên thống nhất cách viết **::after** ngay từ đầu cho quen.

Trong bài này mình sẽ chỉ giới thiệu tới các bạn những pseudo-element hay sử dụng sau đây:

| Selector | Ví dụ | Giải thích |
| --- | --- | --- |
| ::after | p::after | Chèn thêm 1 nội dung nào đó vào đằng sau nội dung của p element |
| ::before | p::before | Chèn thêm 1 nội dung nào đó vào đằng trước nội dung của p element |
| ::first-letter | p::first-letter | Lựa chọn chữ cái đầu tiên của p element |
| ::first-line | p::first-line | Lựa chọn dòng đầu tiên của p element |
| ::selection | p::selection | Dùng để thiết lập style CSS cho 1 vùng văn bản được chọn bởi người dùng (bằng thao tác như double-click vào nội dung hay giữ chuột trái để chọn nội dung) |
| ::placeholder | input::placeholder | Dùng để định dạng cho những text placeholder của **input** hoặc **textarea** element |

2
. Cách sử dụng các pseudo-elements
------------------------------------

### 2.1. ::after

**::after** được dùng để chèn một nội dung nào đó vào đằng sau nội dung của 1 element bất kỳ.

```
blockquote::after {
    content: '>';
}

```

Đối với **::after**, các bạn có thể hiểu nó như 1 element giả lập nào đó của 1 element chính thống. Tức là nó có thể nhận tất cả các thuộc tính css và bạn có thể style cho nó như 1 element. Có thể xét border, background, position, z-index, width, height,...

### 2.2. ::before

Tương tự như **::after**, **::before** được dùng để chèn một nội dung nào đó vào đằng trước nội dung của 1 element bất kỳ.

```
blockquote::before {
    content: '<';
}

```

Tất nhiên, không khác so với **::after**, **::before** cũng được xem như 1 element giả lập và có thể áp dụng các thuộc tính css lên nó như **::after**. Đây chính là điểm khác biệt của **::after** và **::before** với những pseudo-elements còn lại.

***Note:***

Việc sử dụng **::after** và **::before** thực sự rất nhiều. Các bạn có thể tham khảo 1 số bài viết trước đây của mình để style cho các element khác hoặc tạo các hình học bằng cách sử dụng **::after** và **::before** nhé.

<https://viblo.asia/p/bai-10-css-cho-mot-so-tag-dac-biet-nhu-checkbox-radio-button-va-seclect-box-6J3ZgE1q5mB>

<https://viblo.asia/p/bai-24-tao-cac-khoi-hinh-hoc-bang-css3-phan-1-1Je5ExEYlnL>

<https://viblo.asia/p/bai-25-tao-cac-khoi-hinh-hoc-bang-css3-phan-2-Eb85opzjK2G>

<https://viblo.asia/p/bai-26-tao-cac-khoi-hinh-hoc-bang-css3-phan-3-OeVKBDYYlkW>

Ngoài ra còn các bài về **hover đẹp với CSS3**. Đặc biệt **::after** và **::before** là mấu chốt trong việc sử dụng icon-font đó.

### 2.3. ::first-line

**::first-line** được dùng để style cho dòng đầu tiên trong nội dung của 1 element.

```
p::first-line {
    background: yellow;
    font-weight: bold;
}

```

**::first-line** có thể áp dụng được những thuộc tính css sau:

-   Các thuộc tính về font
-   Các thuộc tính về color
-   Các thuộc tính về background
-   word-spacing
-   letter-spacing
-   text-decoration
-   vertical-align
-   text-transform
-   line-height
-   clear

Lưu ý **::first-line** chỉ áp dụng cho các block element như div, p, h1 - h6,...

### 2.4. ::first-letter

**::first-letter** được dùng để style cho ký tự đầu tiên trong nội dung của 1 element.

```
p::first-letter {
    color: red;
    font-weight: bold;
}

```

**::first-letter** có thể áp dụng được những thuộc tính css sau:

-   Các thuộc tính font
-   Các thuộc tính color
-   Các thuộc tính background
-   Các thuộc tính margin
-   Các thuộc tính padding
-   Các thuộc tính border
-   text-decoration
-   vertical-align (chỉ khi "float" là "none")
-   text-transform
-   line-height
-   float
-   clear

Cũng như **::first-line**, **::first-letter** chỉ áp dụng cho các block element như div, p, h1 - h6,...

### 2.5. ::selection

**::selection** dùng để thiết lập style CSS cho nội dung phần tử được chọn bởi người dùng (bằng thao tác như double-click vào nội dung hay giữ chuột trái để chọn nội dung).

```
p::selection {
    color: red;
    background: yellow;
}

```

**::selection** có thể áp dụng được những thuộc tính css sau:

-   Các thuộc tính color
-   Các thuộc tính background
-   Cursor
-   Outline.

Lưu ý **::selection** không được hỗ trợ cho trình duyệt Internet Explorer 8 và phiên bản trước đó. Firefox hỗ trợ pseudo-element thay thế đó là **::-moz-selection**

### 2.6. ::placeholder

**::placeholder** là 1 pseudo-element đặc biệt chỉ áp dụng được cho **input** và **textarea** element. Pseudo-element này được dùng để style cho những text placehoder.

```
input::placeholder {
    color: blue;
    font-size: 1.5em;
}

```

Như vậy, trong bài này mình đã giới thiệu về định nghĩa cũng như cách sử dụng của những pseudo-elements thông dụng nhất. Tất nhiên, các bạn hoàn toàn có thể kết hợp nhiều pseudo-element cho cùng 1 element. Chẳng hạn, bạn tạo 1 hình bình hành thì có thể sử dụng **::after** và **::before** thay vì sử dụng ảnh. Còn tạo thế nào thì các bạn có thể tham khảo về 1 số bài viết mình đã đưa bên trên nhé.

Chúc các bạn thành công!

https://viblo.asia/p/tim-hieu-va-van-dung-pseudo-pseudo-element-trong-css-phan-2-eW65GRNalDO

### Thuộc tính Position trong CSS

[viblo.asia](https://viblo.asia/p/thuoc-tinh-position-trong-css-6J3ZggdqZmB)

Thuộc tính 'position' trong CSS
===============================

manhdatt

7--8 minutes

* * * * *

![](https://images.viblo.asia/e6d33051-2439-4c23-8d36-23ebc486af31.jpeg)

Việc sắp xếp vị trí các element của trang web không dễ dàng như mọi người thường nghĩ, mọi thứ có thể trở nên phức tạp hơn rất nhiều khi trang web của bạn có nhiều element khác nhau. Do đó, điều cần thiết là phải biết cách sử dụng CSS để sắp xếp vị trí các element, từ đó cũng sẽ tiết kiệm thời gian code của chúng ta hơn.

Có nhiều cách / phương pháp khác nhau để sắp xếp các element và dàn trang web. Sử dụng Bootstrap là một cách rất tốt và nhanh gọn, tuy nhiên không phải tất cả các dự án đều sử dụng Bootstrap. Trong bài viết này, mình sẽ giải thích một trong những cách sắp xếp các element với CSS thuần: thuộc tính `position`. Ngoài ra chúng ta có thể dùng thuộc tính Display với các giá trị như flex, grid, inline-block ... Hôm nay mình sẽ chỉ nói về thuộc tính `position` nhé !

CSS Position & các thuộc tính Helper
------------------------------------

Có 5 giá trị chính của `position`:

```
position: static | relative | absolute | fixed | sticky

```

và các thuộc tính có nhiệm vụ căn chỉnh vị trí của element (mình gọi chúng là các thuộc tính `Helper`):

```
top | right | bottom | left | z-index

```

> Note: các thuộc tính Helper không thể hoạt động nếu như không khai báo thuộc tính `position`, hoặc với `position: static`.

z-index là gì?
--------------

Chúng ta có chiều cao (height) và chiều rộng (width) (x,y) là 2 chiều của element. Z chính là chiều thứ 3 của element. Một element hiện thị đè lên trên một element khác có nghĩa là giá trị `z-index` của nó đã được tăng. `z-index` cũng không hoạt động với `position: static` hoặc khi không có thuộc tính `position`

![](https://images.viblo.asia/e058e977-6e29-4409-bc98-fa67bceaa851.png)

Element càng ở bên trên thì `z-index` của nó càng cao.

Bây giờ mình sẽ nói đến các giá trị của thuộc tính `position`

1
. Static
----------

`position: static` là giá trị mặc định của `position`. Dù chúng ta có khai báo chúng hay không thì các element sẽ được sắp xếp vị trí một cách như bình thường trên trang web.

Chúng ta có một đoạn HTML sau:

```
<body>
   <div class="box-orange"></div>
   <div class="box-blue"></div>
</body>

```

Sau đó chúng ta tạo CSS và định nghĩa `position` cho chúng:

```
.box-orange {          // Không khai báo position
  background: orange;
  height: 100px;
  width: 100px;
}
.box-blue {
  background: lightskyblue;
  height: 100px;
  width: 100px;
  position: static;   // Khai báo "static"
}

```

![](https://images.viblo.asia/3797bca1-4f1a-4bf5-a471-5b8ea6e9b734.png) Chúng ta có thể thấy cùng một kết quả trong cả 2 trường hợp

2
. Relative
------------

`position: relative`: Vị trí mới của một element tương quan/ liên hệ tới vị trí mặc định của nó.

Với `position: relative` và các giá trị khác ngoài `static`, chúng ta có thể dễ dàng thay đổi vị trí của chúng. Nhưng chỉ khai báo `position: relative` thôi chưa đủ, chúng ta cần đến việc điều chỉnh vị trí của element bằng các thuộc tính `helper`.

Hãy di chuyển hình vuông màu cam sang bên cạnh hình vuông màu xanh nhé:

```
.box-orange {
  position: relative;  // chúng ta có thể di chuyển được element
  background: orange;
  width: 100px;
  height: 100px;
  top: 100px;         // dịch chuyển xuống 100px từ vị trí ban đầu của nó
  left: 100px;        // dịch chuyển sang phải 100px
}

```

![](https://images.viblo.asia/54bde066-a10f-47c6-8a2b-fca09c0510f1.png)

Hình vuông màu cam đã được dịch 100px xuống phía dưới bên phải so với vị trí bình thường của nó.

> Note: Sử dụng `position: relative` cho một element thì sẽ không ảnh hưởng tới vị trí của các element khác.

3
. Absolute
------------

Với `position: relative`, một element được dịch chuyển tới một vị trí mới dựa trên ví trí bình thường của chính nó. Tuy nhiên, `position: absolute` sẽ dịch chuyển vị trí của nó tương ứng với thẻ cha của nó.

Một element được khai báo với thuộc tính `position: absolute` sẽ được loại bỏ khỏi luồng document (document flow). Vị trí mặc định của element sẽ là điểm bắt đầu (top-left) của element cha. Nếu nó không có bất cứ thẻ cha nào thì thẻ document <html> sẽ là cha của nó.

Vì `position: absolute` đã được loại bỏ khỏi document flow, các element khác do element được định nghĩa `position: absolute` được coi là đã bị xóa khỏi trang web.

Mình sẽ thêm 1 div `container` làm thẻ cha trong ví dụ sau:

```
<body>
   <div class="container">
       <div class="box-orange"></div>
       <div class="box-blue"></div>
   </div>
</body>

```

Và thay đổi một chút về `position` của chúng:

```
.box-orange {
  position: absolute;
  background: orange;
  width: 100px;
  height: 100px;
}

```

![](https://images.viblo.asia/ddb8d063-5eff-406d-8468-67fd2785f2b4.png)

`position: absolute` đưa element về vị trí top-left của cha nó.

Dường như là hình vuông màu xanh đã bị biến mất. Nhưng sự thật là nó đã coi như hình vuông màu cam đã bị xóa, và nó bị đẩy lên vị trí ban đầu của hình vuông màu cam.

Để chứng minh cho điều này, mình sẽ dịch hình vuông cam đi 5px:

```
.box-orange {
  position: absolute;
  background: orange;
  width: 100px;
  height: 100px;
  left: 5px;
  top: 5px;
}

```

![](https://images.viblo.asia/4260b223-2039-43e9-b91b-6f270fdafddf.png)

Bây giờ chúng ta đã nhìn thấy hình vuông xanh.

Vị trí của một element `absolute` sẽ tương quan với vị trí của cha nó nếu thẻ cha được khai báo `position` khác ngoài `static`

```
.container {
  position: relative;
  background: lightgray;
}
.box-orange {
  position: absolute;
  background: orange;
  width: 100px;
  height: 100px;
  right: 5px;    // dịch 5px so với cạnh phải của thẻ cha
}

```

![](https://images.viblo.asia/c6305ce0-0503-47ad-91c9-86a400036dba.png)

4
. Fixed
---------

Giống như `position: absolute`, các element được khai báo với `position` này sẽ được loại bỏ khỏi document flow. Chỉ khác là:

-   Vị trí của chúng **CHỈ** tương quan với thẻ `<html>`
-   Chúng không bị ảnh hưởng bới scroll

Ở ví dụ tiếp theo, mình sẽ thay đổi `position` của hình vuông cam thành `fixed`, và sẽ cách lề phải 5px so với thẻ `<html>`, không phải thẻ cha của nó (container).

Như chúng ta thấy, việc scroll trang web không hề thay đổi vị trí của element `fixed`. Nó được xác định vị trí so với cửa sổ trình duyệt. Và để xác định vị trí của nó thì các bạn cũng phải kết hợp với các thuộc tính top, right, bottom, left như 2 thuộc tính phía trên.

5
. Sticky
----------

`position: sticky` có thể hiểu đơn giản là sự kết hợp của `position: relative` và `position: fixed`.

Nó cũng na ná `fixed` nhưng mà khi các bạn scroll đến vị trí của nó sẽ giống hệt như `fixed` và khi các bạn scroll lên ra khỏi nó thì nó sẽ quay lại vị trí ban đầu dưới dạng `relative`.

Nghe hơi khó hiểu phải không, cùng xem ví dụ nhé:

> Note: `position: sticky` không dùng được trên IE và một số version đầu của Edge nên mình không khuyến khích sử dụng nhé.

![](https://images.viblo.asia/c4eca4d8-5d09-4ff7-988c-a64007f9b64a.png)

Cảm ơn các bạn đã bỏ thời gian để đọc bài viết của mình !

*Nguồn:* [How to use the position property in CSS to align elements](https://medium.freecodecamp.org/how-to-use-the-position-property-in-css-to-align-elements-d8f49c403a26)

https://viblo.asia/p/thuoc-tinh-position-trong-css-6J3ZggdqZmB

### Giới thiệu Flexbox - Thuộc tính Flexbox trong CSS

[viblo.asia](https://viblo.asia/p/huong-dan-day-du-ve-css-flexbox-maGK7J9a5j2)

Hướng dẫn đầy đủ về CSS Flexbox
===============================

Hi im Dương

8--10 minutes

* * * * *

CSS flexbox là một one-dimensional(hay còn gọi là 1D) layout pattern, một trong những pattern giúp bạn dễ dàng thiết kế layout một cách linh hoạt và hiệu quả. Phân chia không gian giữa các items và kiểm soát căn chỉnh chúng trong container flex layout(vùng chứa). Với flexbox, chúng ta có thể dễ dàng sắp xếp các items từ trái sang phải, từ trên xuống dưới, đồng thời kiểm soát khoảng cách và thứ tự của các items trong container.

### Làm thế nào để nó hoạt động?

Trước khi đi vào tìm hiểu sâu hơn về Flexbox, chúng ta cần nắm qua cấu trúc của Flexbox là như thế nào đã:

![](https://images.viblo.asia/full/0c116fbb-972d-4162-8506-bac8605cd704.png)

Trong flexbox thì chủ yếu có hai thành phần chính là: thùng chứa cha (flex container) và các phần tử con nằm bên trong (flex items).

Ngoài ra chúng ta cũng cần quan tâm tới một số thuộc tính sau:

-   **main start, main end, cross start, cross end:** Điểu bắt đầu của container theo main axis được gọi là main start, điểm kết thúc của container theo main axis gọi là main end, với cross start và cross cũng tương tự nhưng dựa theo cross axis.
-   **main axis:** Trục này chính là hướng của các item hiển thị, mặc định thì sẽ `chạy từ trái qua phải.`
-   **cross axis:** Trục này vuông góc với `main axis`, `chạy từ trên xuống dưới.`
-   **main size:** Là kích thước của mỗi item dựa theo trục main axis.
-   **cross size:** Là kích thước của mỗi item dựa theo trục cross axis.

### Các thuộc tính của flex container

Dưới đây là một số thuộc tính có thể sử dụng đối với flex container:

-   display
-   flex-direction
-   flex-wrap
-   flex-flow
-   justified-content
-   align-items
-   align-content

#### Không sử dụng flexbox

```
<div class="box">
    <div class="box-item">1</div>
    <div class="box-item">2</div>
    <div class="box-item">3</div>
</div>

```

![](https://images.viblo.asia/full/190fc1a4-7425-461c-b719-3a10e098136e.png)

#### Dùng display để áp dụng flexbox

Chúng ta cần phải sử dụng thuộc tính `display`. Đây là cách mà chúng ta định nghĩa một flex container, và cũng là việc bắt buộc nếu bạn làm việc với flexbox.

```
<style>
.box {
    display: flex;
}
</style>
<div class="box">
    <div class="box-item">1</div>
    <div class="box-item">2</div>
    <div class="box-item">3</div>
</div>

```

![](https://images.viblo.asia/full/c12d937b-5144-4cb5-a0f2-7eecfdea5d05.png)

#### flex-direction

`flex-direction` dùng để chỉ định hướng hiển thì của các item, việc thay đổi hướng hiển thị flex cũng thể có thể cho phép ta thay đổi vị trí của các flex item.

##### flex-direction: row

`flex-direction: row` là giá trị mặc định khi sử dụng flexbox, không thực hiện bất kỳ thay đổi nào, chỉ đặt các item `từ trái qua phải` theo trục chính.

```
<style>
.box {
    display: flex;
    flex-direction: row;
}
</style>
<div class="box">
    <div class="box-item">1</div>
    <div class="box-item">2</div>
    <div class="box-item">3</div>
</div>

```

![](https://images.viblo.asia/full/a9620b86-cea6-4a9a-aa77-f8d16654a546.png)

##### flex-direction: row-reverse

Giống với tên gọi, `flex-direction: row-reverse` ngược lại với `row`, các item sẽ được đặt `từ phải qua trái`.

```
<style>
.box {
    display: flex;
    flex-direction: row-reverse;
}
</style>
<div class="box">
    <div class="box-item">1</div>
    <div class="box-item">2</div>
    <div class="box-item">3</div>
</div>

```

![](https://images.viblo.asia/full/3c89c655-03e7-4ff3-83aa-eb400da5b81e.png)

##### flex-direction: column

Khi chúng ta xét `flex-direction: column`, lúc này trục chính sẽ đi từ trên xuống dưới vậy nên giờ đây các items sẽ được xếp chồng lên nhau.

```
<style>
.box {
    display: flex;
    flex-direction: column;
}
</style>
<div class="box">
    <div class="box-item">1</div>
    <div class="box-item">2</div>
    <div class="box-item">3</div>
</div>

```

![](https://images.viblo.asia/full/ba02427d-c034-4593-b6d9-ff91201d33c0.png)

##### flex-direction: column-reverse

Khi đó các items sẽ được xếp chống lên nhau nhưng theo chiều ngược lại. Hay để ý sẽ thấy ở ví dụ trên (1) sẽ ở trên cùng, nhưng khi sử dụng `column-reverse` (1) sẽ ở dưới cùng.

```
<style>
.box {
    display: flex;
    flex-direction: column-reverse;
}
</style>
<div class="box">
    <div class="box-item">1</div>
    <div class="box-item">2</div>
    <div class="box-item">3</div>
</div>

```

![](https://images.viblo.asia/full/984336e9-d8f3-4b06-955e-0f54144eb5dc.png)

#### flex-wrap

`flex-wrap` dùng để kiểm soát việc bọc các items nằm gọn trong container. Nếu chúng ta giảm chiều rộng của trình duyệt, chúng ta có thể không nhìn thấy một số item trên cùng một dòng. Thuộc tính `flex-wrap` có thể giải quyết vấn đề đó:

-   nowrap (mặc định): Không có gì thay đổi
-   wrap: các items sẽ được bọc trọn trong container
-   wrap-reverse

```
<style>
.box {
    display: flex;
    flex-wrap: nowrap;
}
</style>
<div class="box">
    <div class="box-item">1</div>
    <div class="box-item">2</div>
    <div class="box-item">3</div>
    <div class="box-item">4</div>
    <div class="box-item">5</div>
    <div class="box-item">6</div>
    <div class="box-item">7</div>
    <div class="box-item">8</div>
    <div class="box-item">9</div>
</div>

```

nowrap

![](https://images.viblo.asia/full/49300129-3f31-4e69-becc-61eb42b234f6.png)

wrap

![](https://images.viblo.asia/full/7b855427-cdd0-423b-8336-9c513649a01e.png)

wrap-reverse

![](https://images.viblo.asia/full/6c2f9d35-2a1b-4500-bfa0-71028cd30a13.png)

#### flex-flow

`flex-flow` là cách viết rút gọn của `flex-direction` và `flex-wrap`. Trong `flex-flow` giá trị đầu tiên là `flex-direction` và thứ 2 là `flex-wrap`

```
<style>
.box {
  display: flex;
  flex-flow: row-reverse wrap;
}
</style>
<div class="box">
    <div class="box-item">1</div>
    <div class="box-item">2</div>
    <div class="box-item">3</div>
    <div class="box-item">4</div>
    <div class="box-item">5</div>
    <div class="box-item">6</div>
    <div class="box-item">7</div>
    <div class="box-item">8</div>
    <div class="box-item">9</div>
</div>

```

![](https://images.viblo.asia/full/8af9974a-8929-438c-9b4d-3f822c91806a.png)

#### justified-content

`justified-content` dùng để căn chỉnh vị trí của các items so với trục chính(main axis). Có 6 giá trị có thể dùng đối với thuộc tính `justified-content`:

-   flex-start: sẽ đặt item bắt đầu từ main start (và đây cũng là giá trị mặc định)
-   flex-end:sẽ đặt item bắt đầu từ main end
-   center: sẽ đặt tất cả item ở giữa trục main axis
-   space-between: sẽ chia đều khoảng cách thừa và thêm nó vào giữa các item
-   space-around: sẽ chia khoảng cách ở đầu và cuối. Khoảng cách ở đầu và cuối sẽ bằng 1 nửa khoảng cách ở giữa 2 item với nhau
-   space-evenly: sẽ chia khoảng cách đều khoảng cách giữa các item với item, item và main start, item với main end bằng nhau

```

<style>
.box {
  display: flex;
  justify-content: flex-start;
}
</style>
<div class="box">
    <div class="box-item">1</div>
    <div class="box-item">2</div>
    <div class="box-item">3</div>
    <div class="box-item">4</div>
</div>

```

flex-start

![](https://images.viblo.asia/full/0f7f0453-65b0-4796-925c-9f04c2318614.png)

flex-end

![](https://images.viblo.asia/full/08c09406-104a-4542-b42c-30be20375698.png)

center

![](https://images.viblo.asia/full/42059f30-a8ed-4c03-8a69-06fb2dce2333.png)

space-between

![](https://images.viblo.asia/full/85000744-07a2-4e7b-994f-0893aacdde92.png)

space-around

![](https://images.viblo.asia/full/d9f57f2e-dbe3-4476-baf9-74e3b7e6cbff.png)

space-evenly

![](https://images.viblo.asia/full/2ded4196-e51e-4fca-b93e-065f432f64f6.png)

#### align-items

Thuộc tính `align-items` dùng để xác định cách mà các flex item được đặt trong container dọc theo chiều cross axis.

-   `align-items: stretch`: Chiều dài của item sẽ bằng chiều dài của cross axis.
-   `align-items: flex-start`: Item được đặt ở điểm bắt đầu của cross start(trên cùng bên trái), và kích thước item không bị thay đổi.
-   `align-items: flex-end`: Item được đặt ở điểm bắt đầu của cross end(dưới cùng bên trái)
-   `align-items: center`: Item được đặt ở giữa điểm bắt đầu của cross start và điểm bắt đầu của cross end (ở giữa bên trái)
-   `align-items: baseline`: Item sẽ được đặt dữ theo các ký tự thuộc item đó. Mục đích chính là căn chỉnh dữa liệu dòng văn bản của các item.

```
<style>
.box {
  height: 300px;
  display: flex;
  align-items: stretch;
}
</style>
<div class="box">
    <div class="box-item">1</div>
    <div class="box-item">2</div>
    <div class="box-item">3</div>
    <div class="box-item">4</div>
</div>

```

align-items: stretch

![](https://images.viblo.asia/full/16d76964-a366-4215-8185-d29bbcf14ab8.png)

align-items: flex-start

![](https://images.viblo.asia/full/c67fcfc4-9a2c-4fdc-9c2b-0764e72eb338.png)

align-items: flex-end

![](https://images.viblo.asia/full/67f0f195-8c8b-4622-b613-3564ed21ca86.png)

align-items: center

![](https://images.viblo.asia/full/0ffe3809-2031-4f0f-90d2-54a69413b7c3.png)

align-items: baseline

![](https://images.viblo.asia/full/481911b3-8171-41f8-bf45-41098e6e8f57.png)

#### align-content

Tương tự như `justify-content` chỉ khác một chỗ là thay vì căn theo trục main axis thì `align-content` căn theo trục cros axis.

-   `align-content: stretch`
-   `align-content: flex-start`
-   `align-content: flex-end`
-   `align-content: center`
-   `align-content: space-between`
-   `align-content: space-around`

```
<style>
.box {
  height: 300px;
  display: flex;
  flex-wrap: wrap;
  align-content: stretch;
}
</style>
<div class="box">
    <div class="box-item">1</div>
    <div class="box-item">2</div>
    <div class="box-item">3</div>
    <div class="box-item">4</div>
</div>

```

align-content: stretch

![](https://images.viblo.asia/full/4d8f9826-81a0-42df-b011-486480a430e8.png)

align-content: flex-start

![](https://images.viblo.asia/full/2214c688-5fde-4f81-b172-8c20b3670dd9.png)

align-content: flex-end

![](https://images.viblo.asia/full/e098b742-b58d-4fc5-9a74-664c0b4519cc.png)

align-content: center

![](https://images.viblo.asia/full/4ab3d28d-8948-4f02-8033-43389f96463c.png)

align-content: space-between

![](https://images.viblo.asia/full/decd5f97-9435-4e36-8936-ff41b9ceaac5.png)

align-content: space-around

![](https://images.viblo.asia/full/60ee30de-b303-4322-8434-378cd6c80be4.png)
https://viblo.asia/p/huong-dan-day-du-ve-css-flexbox-maGK7J9a5j2

### CSS BEM Là Gì? Đặt Tên CSS Class Theo Tiêu Chuẩn BEM
[viblo.asia](https://viblo.asia/p/tim-hieu-ve-bem-trong-15-phut-924lJOk65PM)

Tìm hiểu về BEM trong 15 phút
=============================

ngocyen

6--8 minutes

* * * * *

[![Avatar](https://images.viblo.asia/avatar/d613e65a-9ae4-49bb-871f-a51c47597871.jpeg)](https://viblo.asia/u/ngocyen)

Đã đăng vào thg 10 23, 2017 2:42 CH 4 phút đọc

1
. BEM là gì :
---------------

-   Là một quy ước đặt tên cho các class trong HTML và CSS
-   BEM là viết tắt của từ Block, Element, Modifier.
-   BEM được tạo bởi team của Yandex.

2
. Quy ước đặt tên
-------------------

```
    .block {}   /* Block */
    .block__element {}  /* Element */
    .block--modifier {}  /* Modifier */

```

**.block** Thành phần cấp to nhất của abstraction hoặc component. **.block__element** Thành phần con bên trong của block **.block--modifier** Là 1 phiên bản # của block. Hay những thay đổi style khác so với style ban đầu

3
. Giải Thích về BEM qua ví dụ
-------------------------------

Một ví dụ về HTML sử dụng BEM

**1
. Modifier**

```
    <a class="btn btn--green" href="#">
    </a>

```

Ở đây btn là block .btn---green là modifier. Style của chúng ta như sau

```
   .btn {
      background: gray;
      border: 0;
      border-radius: 3px;
      box-shadow: none;
      padding: 5px 20px;
      color: #fff;
      font-size: 18px;
      line-height: 1.5;
   }
 /* style .btn--green   */

  .btn--green {
      background: green;
  }

```

-   Modifire: Các bạn cứ hiểu như là những thay đổi về style của .btn có 1 số điểm style khác so với .btn ban đầu. Ở đây btn--green thay đổi background từ màu xám sang màu xanh. Các bạn có thể thay đổi màu background, font-size, padding .... Tùy vào cách đặt của các bạn

**2
. Element**

```
<div class="info">
  <div class="info__title">
  </div>
  <div class="info__description">
  </div>
</div>

```

-   Ở đây info__title, info__description là thành phần con bên trong info.

```
  .info {
    background: #f2f4f7;
    margin-top: 23px;
    padding-bottom: 30px;
    &__description {
      font-size: 15px;
      font-family: "Kozuka Gothic Pr6N", sans-serif;
    }
    &__title {
      font-size: 20px;
      font-family: "Kozuka Gothic Pr6N", sans-serif;
      font-weight: bold;
    }
  }

```

4
. Tại sao sử dụng BEM
-----------------------

-   Các bạn có bao giờ đau đầu suy nghĩ với việc nên đặt class html ra sao không? BEM là giải pháp giúp các bạn dễ dàng trong việc đặt class
-   Giúp code viêt đơn giản, dễ hiểu hơn, dễ sửa chữa. Đôi khi bạn style xong bạn còn chả biêt nó nằm ở đâu muốn sửa thì làm sao, nhưng với cách viết BEM bạn sẽ biết vị trí các thành phần HTML nằm đâu thông qua tên class của nó rùi sửa. Với cách viết thông thường bạn sửa lại sợ ảnh hưởng đến chỗ khác.

5
. Biến thể của BEM
--------------------

-   Khi thay đổi về style modifier chúng ta sẽ thêm thuộc tính # chèn lên thuộc tính cũ. Nhưng với nhiều thay đổi chả lẽ bạn lại viết tất cả như thế này sao

```
<a class=" btn btn--primary btn--large btn--font-12 ....">

```

-   Nên chúng ta có biến thể về BEM cho việc viết đơn giản mà cung cấp cho chúng ta sự linh hoạt để cấu hình bất kỳ module nhất định. Nó phù hợp cho module với nhiều sửa đổi. Điều này rất có ích cho các phần tử tạo lên giao diện người dùng. Ví dụ như các button, icon, typography(kiểu chữ). Các bạn có thể đọc link sau <https://webuild.envato.com/blog/chainable-bem-modifiers/>

-   Biến tấu mới sẽ như sau:

```
  <a class="block -modifier">

```

ví dụ:

```
    <!-- Icon -->
    <i class="e-icon -icon-envato -color-green -size-xl -margin-right"></i>

    <!-- Typography -->
    <h2 class="t-heading -size-m -color-light">Heading</h2>
    <p class="t-body -size-s">Paragraph</p>

    <!-- Inputs -->
    <input class="f-input -type-string -width-full">

    <!-- Notifications -->
    <div class="alert-box -type-success">
      <div class="alert-box__icon">
        <i class="e-icon -icon-ok"></i>
      </div>
      <div class="alert-box__message">
        <p class="t-body -size-m h-remove-margin">Success!!</p>
      </div>
    </div>
    <!-- Button -->
    <button class="btn -color-green -bg-blue"></button>

```

Với style scss cho nó chúng ta chỉ cần viết như sau

```
.btn {
  ....
  &.-color-green {
    ....
  }
  &.-bg-blue {
    ...
  }
}

```

-   Vì vậy, đó là BEM (hoặc một biến thể nhẹ của nó), một quy ước đặt tên rất hữu ích, mạnh mẽ và đơn giản để làm cho code của bạn dễ đọc ,rõ ràng hơn và nghiêm ngặt hơn nhiều.

6
. Các bước áp dụng BEM khi làm dự án Front-end thực tế
--------------------------------------------------------

-   Khi bắt đầu 1 dự án chúng ta cần xem rõ guide và style những component dùng chung để có thể tái sử dụng được và tồn tại độc lập với các component khác. Chúng ta hãy xem các component của bootstrap một ví dụ tốt về component

-   Tên selector của component thì đặt là namespace

-   Áp dụng quy tắc BEM ở trên vào xây dựng website

    ```
        <div class="component -modifier">				
          <div class="component__subcomponent -subcomponent-modifier"> ... </div>				
        </div>				

    ```

    ```
         .component {	
         ...	
         &.-modifier { ... }	
         }	

         .component__subcomponent {	
         ...	
         &.-subcomponent-modifier { ... }	
         }	

    ```

### Chú ý : 1 element thì chỉ kế thừa từ 1 component

```
 ``` html
    <!-- NG -->		
    <button class="grid button -center"> ... </button> // -center ko thể kế thừa component của cả grid và button
 ```

 ``` html
    <!-- OK -->		
    <div class="grid -center">		
      <button class="button"> ... </button>		
    </div>
  ```

```

### Kết Luận

-   Ở bài này mình giới thiệu sơ qua về BEM, cách sử dụng của nó. Áp dụng nó vào dự án thực tế. Để hiểu thêm về nó các bạn có thể tìm hiểu qua google hoặc 1 số link dưới đây
    -   <https://webuild.envato.com/blog/chainable-bem-modifiers/>
    -   <https://csswizardry.com/2013/01/mindbemding-getting-your-head-round-bem-syntax/>
    -   <http://apollo13.vn/lap-trinh/css/bem-la-gi.html>
-   Tài liệu BEM cho các bạn đọc thêm do mình soạn thảo <https://docs.google.com/document/d/1r7E_M03LZp_0LJFD6E7Qcdg74mP-ue76E2GzlIMe4Uk/edit?usp=sharing>

https://viblo.asia/p/tim-hieu-ve-bem-trong-15-phut-924lJOk65PM

### CSS selectors

[viblo.asia](https://viblo.asia/p/css-selectors-XogBG2bGxnLd)

CSS Selectors
=============

Tran Duc Thang

8--10 minutes

* * * * *

[![Avatar](https://images.viblo.asia/avatar/4135e729-ce0f-4b21-8ca6-bff98a9b2523.jpg)](https://viblo.asia/u/thangtd90)

Đã đăng vào thg 2 25, 2015 3:27 SA 9 phút đọc

Trong bài viết này, chúng ta sẽ tìm hiểu về một khái niệm không hề mới nhưng không phải ai cũng có thể nắm rõ và sử dụng linh hoạt, CSS Selector.

CSS Selector là gì, nó được chia ra làm những loại như thế nào ?

Selectors là gì ?
-----------------

Selectors không phải là một điều gì mới mẻ của CSS3. Nó vốn đã tồn tại từ CSS1, và là một phần cực kỳ quan trọng của CSS.

Ban đầu, CSS1 mới chỉ bao gồm khoảng 7 selectors, sau đó nó được mở rộng thêm khoảng 12 cái mới trong CSS2, và rồi lại tiếp tục được cải thiện ở CSS3.

Đối với những người có ít kinh nghiệm về CSS, hay chưa nắm rõ về các Selectors thì những đoạn code CSS hầu như chỉ sự dụng id hay class của các elements. Điều này dẫn đến những đoạn code CSS sẽ rất dài, rối rắm và nhiều lúc khó kiểm soát. Sử dụng Selectors một cách linh hoạt sẽ giúp chúng ta tận dụng được sức mạnh của CSS, và đôi lúc sẽ tránh được việc phải viết những đoạn code javascript không cần thiết.

Các loại Selectors
------------------

CSS Selectors có thể được chia ra làm 3 loại chính, ta tạm gói đó là `DOM Selectors`, `Pseudo Selectors` và `Combinator`.

`DOM selectors` bao gồm những bộ chọn cho phép ta select những element được định nghĩa trong document tree (tức có trong code html). Ví dụ như element có tên tag là `div`, có tên class là `myclass`, hay element có attribute `href` bằng một giá trị nào đó. `DOM selectors` bao gồm:

-   Class Selectors: select theo class
-   Id Selectors: select theo id
-   Type Selectors: Select theo type của element
-   Attribute Selectors: Select theo các attribute của element

`Pseudo Selectors` bao gồm những bộ chọn cho phép ta select những element, hay những thông tin về element, dựa vào những thông tin mà không được đề cập trực tiếp trong document tree. Chẳng hạn như phần tử đầu tiên của một list, chữ cái đầu tiên của một từ ... Pseudo Selectors có thể được chia ra làm 2 loại là Pseudo-Classes và Pseudo-Elements

-   Pseudo-classes: Có thể hiểu là "giả class", tức ta coi trạng thái, hay thông tin đặc biệt của element như là một class. Ví dụ như một link với trạng thái là visited hay active, một phần tử trong list có thứ tự là số chẵn ...
-   Pseudo-elements: Có thể hiểu là "giả element", tức nó không phải là một element hoàn chỉnh, mà có thể chỉ là một bộ phận nào đó của một từ, của một đoạn text ...

Cuối cùng, `Combinator` cho phép ta join các selectors lại với nhau. Có những loại Combinator như sau:

-   Descendant combinator: Select những element là con cháu của một element khác.
-   Child combinator: Select những element là con của một element khác. Chú ý ở đây "con cháu" được dùng để chỉ element nằm trong element khác, còn "con" là chỉ element nằm trực tiếp ngay bên trong của element khác.Ví dụ như `<div><span><p>example</p><span></div>` thì chỉ có span là "con" của element `div`, còn cả `span` và `p` đều là "con cháu" của div.
-   Adjacent sibling combinator: Select element nằm liền kề và ngang hàng với element khác. (các element "anh em" kề nhau)
-   General sibling combinator: Select element ngang hàng với element khác. (các element "anh em")

Lịch sử Selectors
-----------------

Tiếp theo hãy cùng nhìn lại lịch sử phát triển của CSS Selectors. Những selectors nào đã được đưa vào qua từng phiên bản CSS level 1 và CSS level 2. Ý nghĩa và cách sử dụng những selectors đó ra sao ?

| Selectors | Ý nghĩa | Loại Selectors | CSS Level |
| --- | --- | --- | --- |
| E | Những element có tên là `E`. Chẳng hạn như `p`, `span`, `div` | Type Selectors | 1 |
| `E:link`, `E:visited` | Dựa vào trạng thái của một link là đã được xem (`:visited`) hay chưa được xem (`:link`) | Pseudo-classes | 1 |
| `E::first-line` | Dòng đầu tiên của element `E` | Pseudo-element | 1 |
| `E::first-letter` | Chữ cái đầu tiên của element `E` | Pseudo-element | 1 |
| `E.myclass` | Những element có `class` là `myclass` | Class Selectors | 1 |
| `E#myid` | Những element có `id` là `myid` | Id Selectors | 1 |
| `E F` | Những element `F` là con cháu của element `E` | Descendant combinator | 1 |
| `*` | Tất cả element | Universal Selectors | 2 |
| `E[foo]` | Những element `E` có chứa attribute `foo` | Attribute Selectors | 2 |
| `E[foo="bar"]` | Những element `E` có attribute `foo` có giá trị là `bar` | Attribute Selectors | 2 |
| `E[foo~="bar"]` | Những element `E` có attribute `foo`, và `foo` là một chuỗi các từ ngăn cách bởi dấu space, và `bar` là một trong số đó | Attribute Selectors | 2 |
| `E[foo|="en"]` | Những element `E` có attribute `foo`, và `foo` có giá trị là một từ có chứa dấu `-`, và bắt đầu của từ đó là `en`. Ví dụ như `<li lang="en-GB">Name</li>` | Attribute Selectors | 2 |
| `E:first-child` | Element là con đầu tiên của bố của nó | Pseudo-classes | 2 |
| `E:active`, `E:hover`, `E:focus` | Dựa trên những thao tác của người dùng, đó là di chuột lên (`hover`), là khoảng từ lúc click chuột đến lúc thả ra (`active`), hay lúc focus vào element (`focus`) | Pseudo-classes | 2 |
| `E:lang(vn)` | Những element có language là `vn`. Chú ý rằng một element có language là `vn` thì những element con của nó nếu không được khai báo attribute lang thì cũng sẽ có language là `vn`. Chẳng hạn như `<body lang=vn><p>Trần Đức Thắng</p></body>` thì element `p` ở trên sẽ vẫn thoả mãn selector `p:lang(vn)`. | Pseudo-classes | 2 |
| `E::before` | Phần content phía trước element `E` | Pseudo-elements | 2 |
| `E::after` | Phần content phía sau element `E` | Pseudo-elements | 2 |
| `E > F` | Element `F` là con của element `E` | Child combinator | 2 |
| `E + F` | Element `F` nằm ngay sau element `E` | Adjacent sibling combinator | 2 |

Cuối cùng, dưới đây là những selectors mới được thêm vào CSS3

-   `E[foo^="bar"]`: Element e có attribute `foo` bắt đầu bằng `bar`. Đây là một Attribute selector.
-   `E[foo$="bar"]`: Element e có attribute `foo` kết thúc bằng `bar`. Đây là một Attribute selector.
-   `E[foo*="bar"]`: Element e có attribute foo có chứa từ `bar`. Đây là một Attribute selector. Chú ý rằng selector này khác với `E[foo~="bar"]` đã có từ CSS2. Phép `~` yêu cầu attribute có chứa nhiều từ được ngăn cách bởi dấu cách, và một trong những từ đó là `bar`, trong khi phép `*` chỉ yêu cầu có chứa từ `bar`.
-   `E ~ F`: Element `F` nằm ngay sau element `E`. Đây là một General sibling combinator. Nó hơi khác với `E + F` đã có từ CSS2 ở chỗ `E + F` yêu cầu `E` đứng ngay phía trước `F`.
-   `E:root`: Select document root
-   `E:nth-child(n)` và `E:nth-of-type(n)`: Đây là 2 pseudo-classes mới được thêm vào. Nó cho phép chúng ta chọn ra những elements dựa vào vị trí của nó trong document tree. `nth-child` cho phép select ra những element là dựa trên vị trí của nó so với những element con khác, còn `nth-of-type` thì không phải là dựa vào vị trí của nó trong toàn bộ những element con, mà chỉ là trong số những element có type nhất định. `(n)` là thông số mang ý nghĩa không quan tâm đến vị trí. Ngoài ra ta có thể sử dụng `2n` hay even với ý nghĩa là những element ở vị trí chẵn, `2n+1` hay odd với ý nghĩa là những element ở vị trí lẻ. Hay ta có thể dùng hẳn giá trị cụ thể, như `nth-child(5)` để chọn element con thứ 5. Chú ý rằng index bắt đầu từ 1. Ta có thể thấy rằng `E:nth-child(n)` và `E:nth-of-type(n)` sẽ cho kết quả là như nhau , bởi nó sẽ cùng select tất cả những element con có type là `E`. Còn `E:nth-child(2n)` và `E:nth-of-type(2n)` sẽ cho kết quả khác nhau, một cái là select những element con ở vị trí chẵn, mà có type là `E`, còn một cái là select những element `E` ở vị trí chẵn trong tập hợp chỉ gồm những element `E`.
-   `E:nth-last-child(n)` và `E:nth-last-of-type(n)`: Hai pseudo-classes này tương tự như `E:nth-child(n)` và `E:nth-of-type(n)`, nhưng thay vì đếm từ trên xuống, chúng sẽ đếm ngược từ dưới lên. Chẳng hạn như `p:nth-last-child(2)` thì sẽ lấy element `p` thứ 2 tính từ cuối lên.
-   `E:first-child`, `E:last-child` và `E:first-of-type`, `E:last-of-type`: Đây là những trường hợp đặc biệt của 4 pseudo-classes đã đề cập ở phía trên. Trong đó `E:first-child` sẽ tương đương với `E:nth-child(1)`, còn `E:last-child` sẽ tương đương với `E:nth-last-child(1)`. Tương tự đối với `E:first-of-type` `E:last-of-type`.
-   `E:only-child` và `E:only-of-type`: Hai pseudo-classes này cho phép ta chọn ra những element mà có cha, nhưng không có những element ngang hàng (đối với `only-child`) hay không có những element cùng loại ở cùng hàng (`only-of-type`).
-   `E:empty`: Select element `E` mà nó là rỗng (không có element con, không có text ...)
-   `E:target`: Element `E` được target bởi URI (Tức là một element được target khi ta click vào một link nào đó trong cùng một page)
-   `E:enabled` và `E:disabled`: User Interface Element `E` được enable hay disable (chẳng hạn như một input của một form ...)
-   `E:checked`: User Interface Element `E` được check (chẳng hạn như radio button hay checkbox ...)
-   `E:not(F)`: Select những element `E` ngoại trừ những element `F`. `F` có thể là cả DOM selectors hay Pseudo selectors.

https://viblo.asia/p/css-selectors-XogBG2bGxnLd
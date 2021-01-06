# Học CSS3 cơ bản

## Giới thiệu CSS

- CSS là viết tắt của Cascading Style Sheets
- CSS dùng để trang trí các phần tử trong HTML

---

## Cú pháp CSS

Cú pháp của CSS bao gồm `selector` (*chọn*) và `declaration` (*khai báo*)

Ví dụ:

```css
p {
  color: red;
  text-align: center;
}
```

kết thúc một câu lệnh là dấu `;`  và khối khai báo nằm trong dấu `{}`

Có 3 cách để chọn 1 phần tử trong CSS đó là :

- **Element Selector** (*dựa theo tên phần tử*)

```css
p {
  text-align: center;
  color: red;
}   
```

- **ID Selector** (*dựa theo id*) : bắt đầu bằng dấu `#` cho id, tương tức với khai báo html là `id="para1"`

```css
#para1 {
  text-align: center;
  color: red;
}
```

> ⚠️ Tên `id` không thể bắt đầu bằng **số**

- **Class Selector** (*dựa trên class*) : bắt bằng bằng dấu `.` cho class, tương tức với khai báo html là `class="center"`

```css
.center {
  text-align: center;
  color: red;
}
```

> 💊 Bạn cũng có thể chỉ định những phần tử nhất định chịu tác dụng của `class.` ví dụ như dưới đây, chỉ có `<p class="center">` là thực thi

```css
p.center {
  text-align: center;
  color: red;
}
```

> 💊 Phần tử HTML có thể đặt nhiều hơn 1 class ví dụ là phần tử `<p>` được tạo theo 2 kiểu `class="center"` và `class="large"`

```html
<p class="center large">Đoạn văn sử dụng hai lớp.</p>
```

> ⚠️ Tên `class` không thể bắt đầu bằng **số**

==>  ⚠️ Cả `id` và `class` đều không thể bắt đầu bằng số

Nếu các phần tử có cùng định dạng style thế này:

```css
h1 {
 text-align: center;
 color: red;
}

h2 {
 text-align: center;
 color: red;
}

p {
 text-align: center;
 color: red;
}
```

Thì ta hoàn toàn có thể viết ngắn gọn thế này:

```css
h1, h2, p {
 text-align: center;
 color: red;
}
```

> 💊 Trong CSS, comment ta dùng giống ngôn ngữ C,C++ có 2 cách comment chính như sau:

```css
p {
 color: red;
 /* Đây là bình luận một dòng */
 text-align: center;
}

/* Đây là
bình luận
nhiều dòng */
```

---

## Vị trí đặt CSS

Có 3 cách để thêm CSS cho HTML:

- **Enternal CSS** ( *Định dạng bên ngoài* )

```html
<head>
    <link rel="stylesheet" href="style.css">
</head>
```

> 💡 Bạn có thể thay đổi CSS của cá trang bằng cách này chỉ với một dòng, và đây là cách **tối ưu nhất**, `href="đường dẫn file css của bạn"`

Ví dụ trong file `style.css` như sau:

```css
h1 {
 color: navy;
 margin-left: 20px;
}
```

> ⚠️ Bạn không được thêm khoảng trắng kết thúc lệnh như này `margin-left: 20px ;` mà phải viết như này `margin-left: 20px;`

- **Internal CSS** (*Định dạng nội bộ*)

```html
<head>
<style>
body {
 background-color: linen;
}

h1 {
 color: maroon;
 margin-left: 40px;
}
</style>
</head>
```

> 💡 Được định nghĩa trong phần tử `<style></style>` nàm trong thẻ `<head>`

- **Inline CSS** (*Định dạng nội dòng*)

```html
<h1 style="color:blue;margin-left:30px;">Tiêu đề</h1>
```

> 💡Dùng thể thay đổi cho một thẻ nhất định 

**Thứ tự phân tầng như sau :** **`Inline`** > **`Internal`** > **`Enternal`**

> 💡 có nghĩa là `Inline` là được ưu tiên nhất sau đó đến `Internal` rồi `Enternal`

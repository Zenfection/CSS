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

---

## CSS-Color

Ta có thể định nghĩa màu sắc bằng những chuẩn khác nhau như : RGB, HEX, HSL, RGBA và HSLA...

> 💡 Nhưng mình thấy phổ biến nhất là **HEX**

### Ta có thể đĩnh nghĩa color phổ biến như sau :

- **Màu nền** : Sử dụng `color:"_màu_";`

```html
<h1 style="background-color:DodgerBlue;">Xin chào</h1>
```

![Ảnh chụp Màn hình 2021-01-06 lúc 12.51.53.png](https://raw.githubusercontent.com/Zenfection/Image/master/2021/01/06-12-51-58-A%CC%89nh%20chu%CC%A3p%20Ma%CC%80n%20hi%CC%80nh%202021-01-06%20lu%CC%81c%2012.51.53.png)

- **Màu văn bản** : Sử dụng `color:"_màu_";`

```html
<h1 style="color:Tomato;">Xin chào</h1>
```

![Ảnh chụp Màn hình 2021-01-06 lúc 12.51.26.png](https://raw.githubusercontent.com/Zenfection/Image/master/2021/01/06-12-51-35-A%CC%89nh%20chu%CC%A3p%20Ma%CC%80n%20hi%CC%80nh%202021-01-06%20lu%CC%81c%2012.51.26.png)

- **Màu viền** : Sử dụng `border:_số_px soild _màu_`

```html
<h1 style="border:2px solid Tomato;">Xin chào</h1>
```

![Ảnh chụp Màn hình 2021-01-06 lúc 12.50.51.png](https://raw.githubusercontent.com/Zenfection/Image/master/2021/01/06-12-51-11-A%CC%89nh%20chu%CC%A3p%20Ma%CC%80n%20hi%CC%80nh%202021-01-06%20lu%CC%81c%2012.50.51.png)

### Ta có các cách định nghĩa màu sau đây:

- **Tên màu** : Ta có thể dùng 140 tên màu mặc định của HTML, [tham khảo tại đây](https://quantrimang.com/mau-sac-trong-html-149960), *ví dụ ở trên*
- **Giá trị RGB** : Màu RGB có cú pháp và công thức nhứ sau

```textile
rgb(red,green,blue)
```

>  💡 Mỗi thông số **red,green,blue** đều nằm trong khoảng từ `0 tới 255`

**Ví dụ:**  `rgb(255,0,0)` là màu đỏ vì `red là 255`, `green là 0` và `blue là 0`

Màu đen là `rgb(0,0,0)` còn màu trắng là `rgb(255,255,255)`

```html
<p style="background-color:rgb(0, 0, 0); color:rgb(255, 255, 255);">rgb(0, 0, 0)</p>
<p style="background-color:rgb(60, 60, 60); color:rgb(255, 255, 255);">rgb(60, 60, 60)</p>
<p style="background-color:rgb(120, 120, 120); color:rgb(255, 255, 255);">rgb(120, 120, 120)</p>
```

![Ảnh chụp Màn hình 2021-01-06 lúc 12.49.54.png](https://raw.githubusercontent.com/Zenfection/Image/master/2021/01/06-12-50-11-A%CC%89nh%20chu%CC%A3p%20Ma%CC%80n%20hi%CC%80nh%202021-01-06%20lu%CC%81c%2012.49.54.png)

- **Giá trị HEX**

Màu sắc được định dạng bằng cơ số 16 dưới dạng:

```textile
#rrggbb
```

>  💡 Trong đó `rr là red`, `gg là green` và `bb là blue` có giá trị từ `00 tới ff` tương tự RGB là từ `0 tới 255`

```html
<p style="background-color:#ff0000; color:#ffffff;">#ff0000</p>
<p style="background-color:#3cb371; color:#ffffff;">#3cb371</p>
```

![Ảnh chụp Màn hình 2021-01-06 lúc 12.49.20.png](https://raw.githubusercontent.com/Zenfection/Image/master/2021/01/06-12-49-35-A%CC%89nh%20chu%CC%A3p%20Ma%CC%80n%20hi%CC%80nh%202021-01-06%20lu%CC%81c%2012.49.20.png)

- **Giá trị HSL**

Màu sắc được định định dạng bằng các **hue** (*vùng màu*), **saturation** (*độ bão hoà*), **lightness** (*độ sáng*)

> 💡 HSL là viết tắt của **hue-saturation-lightness**

| Hue                                      | Saturation                                     | Lightness                               |
| ---------------------------------------- | ---------------------------------------------- | --------------------------------------- |
| Mức độ trên vòng màu sáng từ `0 tới 360` | là giá trị `%` , thể hiện độ tinh kiết của màu | là giá trị `%` thể hiện độ sáng của màu |

Không cần học qua sâu, có thể tìm hiểu kỹ hơn [tại đây](https://www.w3schools.com/colors/colors_hsl.asp)

- **Giá trị RGBA**

Là màu sắc mở rộng của **RGB**, thêm `aplha` (*độ trong suốt của màu sắc*) nằm trong khoảng từ `0.0 tới 1.0`, với cú pháp:

```textile
rgba (red, green, blue, alpha)
```

**Ví dụ:**

```html
<p style="background-color:rgba(255, 99, 71, 0); color:#000000;">rgba(255, 99, 71, 0)</p>
<p style="background-color:rgba(255, 99, 71, 0.4); color:#000000;">rgba(255, 99, 71, 0.4)</p>
<p style="background-color:rgba(255, 99, 71, 0.8); color:#000000;">rgba(255, 99, 71, 0.8)</p>
<p style="background-color:rgba(255, 99, 71, 1); color:#000000;">rgba(255, 99, 71, 1)</p>
```

![Ảnh chụp Màn hình 2021-01-06 lúc 12.48.31.png](https://raw.githubusercontent.com/Zenfection/Image/master/2021/01/06-12-48-44-A%CC%89nh%20chu%CC%A3p%20Ma%CC%80n%20hi%CC%80nh%202021-01-06%20lu%CC%81c%2012.48.31.png)

- **Giá trị màu HSLA**

Là màu sắc mở rộng của **HSL**, thêm `aplha` (*độ trong suốt của màu sắc*) nằm trong khoảng từ `0.0 tới 1.0`, với cú pháp:

```textile
hsl(hue, saturation, lightness, alpha)
```

☣️ **Chỉ cần nhớ RGB và HEX là đủ rồi**

---



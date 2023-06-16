# 1. Giới thiệu về Flexbox

#### Khái niệm về flexbox

> Flexbox là một kỹ thuật trong CSS cho phép chúng ta dễ dàng xây dựng layout linh hoạt và đáp ứng cho website. Với flexbox, chúng ta có thể dễ dàng điều chỉnh và kiểm soát cách các phần tử trên trang web được sắp xếp, căn chỉnh và phân bổ trong không gian một trang web.

#### Các trình duyệt hỗ trợ Flexbox

> Flexbox đã được hỗ trợ trên hầu hết các trình duyệt hiện đại và trở thành một công cụ hữu ích cho các nhà phát triển web.

# 2. Các thuộc tính Flexbox

#### display

> Quan trọng

Thuộc tính này cho phép bạn chỉ định loại hiển thị của một phần tử, với giá trị "flex" để sử dụng Flexbox.

```
.container {
    display: flex;
}
```

**Mặc định khi dùng `display: flex;` thì `flex-direction: row;`**

#### flex-direction

> Quan trọng

Thuộc tính này cho phép bạn chỉ định hướng sắp xếp của các phần tử trong Flexbox, bao gồm "row", "column", "row-reverse" và "column-reverse".

```
.container {
  display: flex;
  flex-direction: row; /* giá trị mặc định */
}

.container {
  display: flex;
  flex-direction: row-reverse;
}

.container {
  display: flex;
  flex-direction: column;
}

.container {
  display: flex;
  flex-direction: column-reverse;
}

```

#### justify-content

> Quan trọng

Thuộc tính này cho phép bạn căn chỉnh các phần tử trong Flexbox theo chiều ngang, bao gồm "flex-start", "flex-end", "center", "space-between" và "space-around".

```
.container {
  display: flex;
  justify-content: flex-start; /* giá trị mặc định */
}

.container {
  display: flex;
  justify-content: flex-end;
}

.container {
  display: flex;
  justify-content: center;
}

.container {
  display: flex;
  justify-content: space-between;
}

.container {
  display: flex;
  justify-content: space-around;
}
```

#### align-items

> Quan trọng

Thuộc tính này cho phép bạn căn chỉnh các phần tử trong Flexbox theo chiều dọc, bao gồm "flex-start", "flex-end", "center", "baseline" và "stretch".

```
.container {
  display: flex;
  align-items: stretch; /* giá trị mặc định, các phần tử cao bằng nhau */
}

.container {
  display: flex;
  align-items: flex-start;
   /* các phần tử canh phía trên đầu */
}

.container {
  display: flex;
  align-items: flex-end;
  /* các phần tử canh phía dưới chân */
}

.container {
  display: flex;
  align-items: center;
  /* các phần tử canh giữa */
}

.container {
  display: flex;
  align-items: baseline;
  /* các phần tử canh theo chữ*/
}
```

#### flex-wrap

Thuộc tính này cho phép bạn xác định liệu các phần tử trong Flexbox có nên wrap hay không khi không đủ không gian, với giá trị "wrap" hoặc "nowrap".

```
.container {
  display: flex;
  flex-wrap: nowrap; /* giá trị mặc định */
}

.container {
  display: flex;
  flex-wrap: wrap;
}

.container {
  display: flex;
  flex-wrap: wrap-reverse;
}
```

#### align-content

> Quan trọng

Thuộc tính này cho phép bạn căn chỉnh các phần tử trong Flexbox theo trục dọc khi chúng wrap, bao gồm "flex-start", "flex-end", "center", "space-between", "space-around" và "stretch".

```
.container {
  display: flex;
  align-content: stretch; /* giá trị mặc định */
}

.container {
  display: flex;
  align-content: flex-start;
  /* các phần tử canh bên trái*/
}

.container {
  display: flex;
  align-content: flex-end;
  /* các phần tử canh bên phải*/
}

.container {
  display: flex;
  align-content: center;
  /* các phần tử canh giữa*/
}

.container {
  display: flex;
  align-content: space-between;
  /* các phần tử canh được canh cách đều nhau đầu cuối */
}

.container {
  display: flex;
  align-content: space-around;
  /* các phần tử canh cách đều nhau nhưng các phần tử có khoảng trống xung quanh */
}
```

#### flex-grow

> Quan trọng

Thuộc tính này cho phép bạn xác định tỷ lệ phần trăm mà một phần tử trong Flexbox sẽ mở rộng để điền vào không gian còn lại.

```
.item {
  flex-grow: 0; /* giá trị mặc định */
}

.item {
  flex-grow: 1;
}

.item {
  flex-grow: 2;
}
```

#### flex-shrink

> Quan trọng

Thuộc tính này cho phép bạn xác định tỷ lệ phần trăm mà một phần tử trong Flexbox sẽ thu nhỏ khi không đủ không gian.

```
.item {
  flex-shrink: 1; /* giá trị mặc định */
}

.item {
  flex-shrink: 0;
}

.item {
  flex-shrink: 2;
}
```

#### order

Thuộc tính này cho phép bạn xác định thứ tự sắp xếp của các phần tử trong Flexbox.

```
.item {
  order: 0; /* giá trị mặc định */
}

.item {
  order: 1;
}

.item {
  order: 2;
}

.item {
  order: 3;
}
```

#### flex-basis

Thuộc tính này cho phép bạn xác định kích thước ban đầu của một phần tử trong Flexbox.

```
.item {
  flex-basis: auto; /* giá trị mặc định */
}

.item {
  flex-basis: 100px;
}

.item {
  flex-basis: 50%;
}
```

# 3. Các thủ thuật chia layout cần biết

**Kỹ thuật căn giữa**

# 4. Sass là gì? Giới thiệu và cài đặt Sass

B1: Cài đặt nodejs: https://nodejs.org/en
B2: terminal chạy lệnh: `npm install -g sass`
B3: Tạo file style.scss cùng thư mục với **index** và **style.css**
B4: chạy lệnh `sass style.scss style.css --watch`

#### Giới thiệu:

Sass (viết tắt của "Syntactically Awesome Style Sheets") là một ngôn ngữ tạo stylesheet mở rộng cho CSS. Nó giúp cho việc viết CSS trở nên dễ dàng và nhanh hơn bằng cách sử dụng các tính năng mở rộng như biến, nesting, mixin, conditional statements, và nhiều hơn nữa. Sass được viết bằng Ruby, nhưng bạn có thể sử dụng nó trong các dự án web của mình thông qua các công cụ như node-sass hoặc koala.

#### Các tính năng của Sass

##### Biến:

Biến cho phép bạn lưu trữ các giá trị và tái sử dụng chúng bằng cách gọi tên biến.

```
$primary-color: #F44336;

header {
  background-color: $primary-color;
}

button {
  color: $primary-color;
}
```

##### Nesting:

Nesting cho phép bạn lồng các lựa chọn trong các lựa chọn khác để tạo ra một cấu trúc code rõ ràng và dễ đọc hơn.

```
nav {
  ul {
    margin: 0;
    padding: 0;
    list-style: none;

    li {
      display: inline-block;
      margin: 0 10px;

      a {
        color: #333;
        text-decoration: none;

        &:hover {
          text-decoration: underline;
        }
      }
    }
  }
}
```

##### Mixin:

Mixin cho phép bạn tạo các đoạn code tái sử dụng được định nghĩa một lần và sử dụng nhiều lần trong code.

```
@mixin size($width, $height) {
  width: $width;
  height: $height;
}

@mixin size($width, $height:$width) {
  width: $width;
  height: $height;
}

items {
  @include size(10rem, 10rem);
}


```

##### Conditional statements:

Sass cung cấp cho bạn cách để kiểm tra các điều kiện và thực hiện các lệnh khác nhau dựa trên kết quả của kiểm tra.

```
$background-color: #FFFFFF;

body {
  @if $background-color == #FFFFFF {
    color: #000000;
  } @else {
    color: #FFFFFF;
  }
}
```

# ?. Thực hành với Flexbox

1. Code giao diện dropdown
   ![alt text](/HTML-CSS-Course/course-images/img0.png)

2. Chia layout form sign-up
   ![alt text](/HTML-CSS-Course/course-images/img7.png)

3. Chia layout giao diện blog
   ![alt text](/HTML-CSS-Course/course-images/img12.png)

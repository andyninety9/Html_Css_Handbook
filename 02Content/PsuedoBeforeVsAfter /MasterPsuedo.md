# :before và :after

## 1. Giới thiệu:

Trong CSS, có hai loại pseudo-class đó là :before và :after. Chúng được sử dụng để thêm nội dung vào trước hoặc sau một phần tử HTML mà không cần phải thay đổi HTML thực sự. Việc sử dụng pseudo-class này làm cho CSS trở nên linh hoạt hơn và giúp chúng ta thiết kế các hiệu ứng động hơn cho trang web.

## 2. Cách sử dụng:

-   ### `Pseudo-class :before`

Pseudo-class :before được sử dụng để thêm nội dung vào phần tử trước nội dung thực sự của phần tử HTML. Bạn có thể sử dụng thuộc tính content để định nghĩa nội dung muốn thêm vào phần tử. Ví dụ:

`index.html`

```
<h2>I am Iron Man</h2>
```

`style.css`

```
h2:before{
    content: "Ronaldo said: "
}
```

`=> Ronaldo said I am Iron Man`

-   ### `Pseudo-class :after`

Pseudo-class :after được sử dụng để thêm nội dung vào phần tử sau nội dung thực sự của phần tử HTML. Cũng giống như :before, bạn có thể sử dụng thuộc tính content để định nghĩa nội dung muốn thêm vào phần tử. Ví dụ:

`index.html`

```
<h2>I am Iron Man</h2>
```

`style.css`

```
h2:after{
    content: "and I am front end developer"
}
```

`=> I am Iron Man and I am front end developer`

### 3. Thực hành

#### Bài 1: Code divider

```
<div class="line">
  <span class="line_text">Header</span>
</div>
```

**style.scss**
```
.line {
    margin-top: 20rem;
    text-align: center;
    position: relative;
    z-index: 0;
    &:before {
        content: "";
        width: 100%;
        height: 1px;
        background-color: orangered;
        position: absolute;
        left: 0;
        top: 50%;
    }
    &_text {
        display: inline-block;
        position: relative;
        background-color: white;
        z-index: 1;
    }
}
```

#### Bài 2: Code nút bấm có hiệu ứng đổ màu:

**index.html**

```
<button>Submit</button>
```

**CSS**

```
button {
  padding: 2rem;
  background-color: white;
  border: 1px solid orangered;
  margin: 5rem;
  transition: color 0.25s linear;
  position: relative;
  z-index: 1;
  border-radius: 4px;
  cursor: pointer;
}
button:before {
  content: "";
  height: 100%;
  width: 0;
  position: absolute;
  top: 0;
  left: 0;
  background-color: orangered;
  z-index: -1;
  transition: width 0.5s linear;
}
button:hover {
  color: white;
}
button:hover:before {
  width: 100%;
}
```

### 4. Tổng kết

#### Những lý do chúng ta lại sử dụng pseudo before và after

- Giảm số lượng HTML được tạo ra, một phần giúp tăng tốc độ tải trang và cài thiện hiệu suất web

- Dễ dàng quản lý, nếu sử dụng một thẻ HTML khác chẳng hạn như div để thay thế cho before và after thì về mặt lý thuyết ta vẫn có thể làm được nhưng phần CSS sẽ trở nên phức tạp và khó quản lý

- Tóm lại tuỳ trường hợp và ngữ cảnh, làm nhiều sẽ nhận ra lúc nào nên dùng công cụ nào
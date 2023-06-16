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

# THUỘC TÍNH TRANSFORM

> Dùng để di chuyển, scale một phần tử HTML nào đó nhưng không làm thay đổi kích thước đã chiếm ban đầu của phần tử

## Scale

```
.boxes{
    transform: scale(0.5, 0.5);
    transform: scaleX(2) scaleY(2);
}
```

## Rotate

```
.boxses{
    transform: rotate(-45deg);
}
```

## Translate

```
.boxes{
    transform: translate(10px, 10px);
    transform: translateX(10px);
    transform: translateY(10px);
}
```

Chúng ta có thể viết gộp nhiều thuộc tính lại như sau:

```
transform: scale(2) rotate(45deg) translate(200%, 100%);
```

# THUỘC TÍNH POSITION RELATIVE

> Cũng có thể xem là thuộc tính dùng để di chuyển các phần tử HTML tương tự transform nhưng sẽ không có value là rotate

```
.boxes{
    position: relative;
    top: 10px;
    left: 10px;
    right: 10px;
    bottom: 10px;
}
```

# KẾT HỢP POSITION RELATIVE VỚI POSITION ABSOLUTE

Thực hành làm Badge

```
    <div class="wrap">
        <div class="boxes2">
            <i class="fa fa-envelope"></i>
            <div class="noti">20</div>
        </div>
    </div>
```

```
.wrap {
    height: 30rem;
    width: 30rem;
    background-color: gainsboro;
    margin: 0 auto;
    padding-top: 10rem;
}

.boxes2 {
    width: 5rem;
    background-color: white;
    margin: 0 auto;
    border-radius: 8px;
    box-shadow: rgba(149, 157, 165, 0.2) 0px 8px 24px;
    text-align: center;
    position: relative;
    box-shadow: rgba(149, 157, 165, 0.2) 0px 8px 24px;
}

.fa-envelope {
    color: #aaa;
    font-size: 40px;
}

.noti {
    height: 2rem;
    min-width: 2rem;
    background-color: red;
    border-radius: 50%;
    color: white;
    font-weight: 500;
    font-size: 12px;
    display: flex;
    align-items: center;
    justify-content: center;
    position: absolute;
    top: 0;
    right: 0;
    transform: translateX(10px) translateY(-10px);
    box-shadow: rgba(149, 157, 165, 0.2) 0px 8px 24px;
}
```

Những kỹ thuật liên quan đến absolute và relative

```
    <div class="wrap">
        <div class="boxed"></div>
    </div>
```

1. Kỹ thuật center theo chiều ngang và chiều dọc

```
    .wrap{
        width: 100%;
        height: 50rem;
        background-color: black;
        position: relative;
    }

    .boxed {
        height: 5rem;
        width: 5rem;
        background-color: rebeccapurple;
        position: absolute;
        left: 50%;
        top: 50%;
        transform: translate(-50%, -50%);
    }
```

2. Kỹ thuật center theo chiều ngang

```
    .wrap{
        width: 100%;
        height: 50rem;
        background-color: black;
        position: relative;
    }

    .boxed {
        height: 5rem;
        width: 5rem;
        background-color: rebeccapurple;
        position: absolute;
        left: 50%;
        transform: translateX(-50%);
    }
```

3. Kỹ thuật center theo chiều dọc

```
    .wrap{
        width: 100%;
        height: 50rem;
        background-color: black;
        position: relative;
    }

    .boxed {
        height: 5rem;
        width: 5rem;
        background-color: rebeccapurple;
        position: absolute;
        top: 50%;
        transform: translateY(-50%);
    }
```

4. Kỹ thuật overlay all

```
    .wrap {
    width: 100%;
    height: 50rem;
    background-color: black;
    position: relative;
}

.boxed {
    height: 5rem;
    width: 5rem;
    background-color: rebeccapurple;
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
}
```

Cách 02:

```
.boxed {
    height: auto;
    width: auto;
    background-color: rebeccapurple;
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
}
```

5. Kỹ thuật overlay theo chiều ngang

```
.boxed {
    height: 5rem;
    width: auto;
    background-color: rebeccapurple;
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
}
```

6. Kỹ thuật center theo chiều dọc:

```
.boxed {
    width: 5rem;
    height: 100%;
    background-color: rebeccapurple;
    position: absolute;
    top: 0;
}
```

# Z-index

> Z-index chỉ hoạt động khi đi kèm với thuộc tính position-relative

# Position fixed

> Dùng để cố định 1 phần tử HTML nào đó như header, footer, sidebar...

* Tạo header
```
    <div class="header"></div>
    <p>
        Lorem ipsum dolor sit amet consectetur, adipisicing elit. In, quae
        iure. Sapiente similique iste saepe, vel fugit voluptates molestias
        accusantium alias quibusdam recusandae, amet eos cupiditate id!
        Corrupti, suscipit aperiam?
    </p>
```

```
.header{
    width: 100%;
    height: 5rem;
    background-color: blue;
    position: fixed;
    top: 0;
    left: 0;
}

body{
    padding-top: 5rem;
}

```

# Animation

Animation và một tính năng của CSS cho phép tạo ra các hiệu ứng chuyển động và thay đổi trạng thái của các phần tử trên trang web.

## Keyframe

Để sử dụng tính năng animation trong CSS, chúng ta cần định nghĩa các keyframe cho animation. ```keyframe``` là một mốc thời gian cụ thể mà tại thời điểm đó các animation được thực hiện.

#### Syntax

##### Cách tạo

```
@keyframes nameOfAnimation{
    from {
        transform: translateX(0)
    }
    to {
        transform: translateX(20rem)
    }
}
```

**Lưu ý**: mặc định `From -> To` sẽ chạy từ 0% đến 100%

##### Cách sử dụng

```
    animation-name: nameOfAnimation;
    animation-duration: 2s;
    animation-direction: alternate;
    animation-interation-count: 2;
    animation-timing-function: kiểu hiệu ứng;
    animation-fill-mode: forward / backwards
```

    Cách sử dụng rút gọn:

```
animation: move 2s forwards infinite alternate cubic-bezier;
```

#### Thực hành

##### 1. Tạo circle loading:

```

   <div class="circle-loading"></div>
```

```
.circle-loading{
    margin: 0 auto;
    width: 5rem;
    height: 5rem;
    background-color: violet;
    border-radius: 50%;
    // transform: scale(2);
    // opacity: 0;
    // animation: fade 1s forwards linear infinite;
    position: relative;
    &::before{
        content: "";
        position: absolute;
        top: 0;
        left: 0;
        width: 5rem;
        height: 5rem;
        background-color: violet;
        border-radius: 50%;
        transform: scale(2);
        opacity: 0;
        animation: fade 1s forwards linear infinite;
    }
}
```

```
    @keyframes fade{
        from{
            transform: scale(1);
            opacity: 1;
        }
        to{
            transform: scale(2);
            opacity: 0;
        }
    }
```

##### 2. Tạo circle loading 2:

```
<div class="circles">
    <div class="circles-item"></div>
    <div class="circles-item"></div>
</div>
```

```
.circles {
    text-align: center;
    // transform: rotate(180deg);
    // transform: rotate(160deg);
    // transform: rotate(200deg);
    animation: loading 1s infinite;
    &-item {
        margin: 0rem 0.5rem;

        width: 3rem;
        height: 3rem;
        border: 3px solid rgba(0, 0, 255, 0.742);
        display: inline-block;
        border-radius: 3rem;
        &:first-child {
            border-color: cyan;
        }
    }
}

@keyframes loading {
    50%{
        transform: rotate(200deg);
    }
    75%{
        transform: rotate(160deg);
    }
    100%{
        transform: rotate(180deg);
    }

}
```

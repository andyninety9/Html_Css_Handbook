# Kiến thức về Form trong HTML

## 1. Tổng quan về Form

Form là một thành phần quan trọng trong việc tạo ra các trang web tương tác. Form cho phép người dùng nhập dữ liệu vào trang web và gửi thông tin đó đến máy chủ để xử lý. Form có thể chứa các loại input như văn bản, số, email, mật khẩu và nút submit.

## 2. Các thành phần trong Form

`<form> `: Thẻ HTML định nghĩa một form.
`<input>`: Thẻ HTML cho phép người dùng nhập dữ liệu vào form.
`<textarea>`: Thẻ HTML cho phép người dùng nhập văn bản dài vào form.
`<select>`: Thẻ HTML cho phép người dùng chọn một giá trị từ danh sách các giá trị được định nghĩa.
`<option>`: Thẻ HTML định nghĩa một giá trị trong danh sách của thẻ `<select>`
`<label>`: Thẻ HTML để định nghĩa một nhãn cho một input.

## 3. Các loại input type của Form

`text`: Cho phép người dùng nhập văn bản vào form.
`email`: Cho phép người dùng nhập địa chỉ email vào form.
`password`: Cho phép người dùng nhập mật khẩu vào form, với tính năng ẩn hiện chữ.
`number`: Cho phép người dùng nhập số vào form.
`checkbox`: Cho phép người dùng chọn một hoặc nhiều giá trị từ danh sách các giá trị được định nghĩa.
`radio`: Cho phép người dùng chọn một giá trị trong nhiều giá trị
`file` : Cho phép người dùng thêm vào một tệp tin
`phone` : Chỉ cho phép nhập vào số điện thoại
`date` chỉ cho phép nhập vào ngày

## 4. Các thuộc tính trong Form:

Các thuộc tính cơ bản của input trong Form

-   `id`: là duy nhất
-   `name`: tên của input, được sử dụng để truyền dữ liệu đến máy chủ
-   `value`: Giá trị được gán cho input.
-   `placeholder`: Văn bản gợi ý được hiển thị trong input để hướng dẫn người dùng.
-   `required`: Yêu cầu người dùng nhập giá trị vào input.
-   `readonly`: Cho phép người dùng xem giá trị của input nhưng không thay đổi nó.
-   `disabled`: Vô hiệu hóa input, ngăn người dùng nhập giá trị vào nó.
-   `maxlength`: Giới hạn ký tự tối đa được nhập vào input.
-   `min`: Giới hạn giá trị tối thiểu được nhập vào input.
-   `max`: Giới hạn giá trị tối đa được nhập vào input.

## 5. Thực hành

**Làm custom checkbox**

```
<div class="checkbox">
    <input
        type="checkbox"
        id="checkbox_term"
        class="checkbox_term" />
    <label for="checkbox_term" class="checkbox_label">
        I agree with term
    </label>
</div>
```

```
.checkbox {
    display: flex;
    align-items: center;
    gap: 1rem;
    &_term {
        display: none;
        &:checked + .checkbox_label::after {
            opacity: 1;
            visibility: visible;
        }
    }
    &_label {
        position: relative;
        padding-left: 5rem;
        &::before {
            content: "";
            height: 4rem;
            width: 4rem;
            background-color: #fc556f;
            position: absolute;
            top: 50%;
            left: 0;
            transform: translateY(-50%);
            border-radius: 1rem;
            cursor: pointer;
        }
        &::after {
            content: "";
            height: 3rem;
            width: 1.5rem;
            // background-color: black;
            position: absolute;
            top: 50%;
            left: 0;
            transform: translate(90%, -50%) rotate(45deg);
            border-right: 7px solid white;
            border-bottom: 7px solid white;
            opacity: 0;
            visibility: hidden;
            transition: all 0.25s linear;
        }
    }
}
```

**Làm custom radio**

```
<div class="radio">
    <input type="radio" id="radio_term" class="radio_term" />
    <label for="radio_term" class="radio_label">
        I agree with term
    </label>
</div>
```

```
.radio {
    display: flex;
    align-items: center;

    &_term {
        display: none;
        &:checked + .radio_label::after {
            opacity: 1;
            visibility: visible;
        }
    }
    &_label {
        cursor: pointer;
        position: relative;
        padding-left: 4rem;
        &::before {
            content: "";
            height: 3rem;
            width: 3rem;
            border-radius: 100%;
            background-color: #fc556f;
            position: absolute;
            top: 50%;
            left: 0;
            transform: translateY(-50%);
        }
        &::after {
            content: "";
            position: absolute;
            height: 3rem;
            width: 3rem;
            border-radius: 100%;
            background-color: transparent;
            border: 5px solid white;
            top: 50%;
            left: 0;
            transform: translateY(-50%) scale(0.9);
            opacity: 0;
            visibility: hidden;
            transition: all 0.2s ease;
        }
    }
}

```

**Làm custom input**

**Làm custom checkbox toggle**

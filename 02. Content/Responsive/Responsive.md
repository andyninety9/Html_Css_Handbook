# Responsive

Hiểu đơn giản, responsive là việc sử dụng các thuộc tính CSS để tuỳ biến giao diện Website sao cho tương thích với tất cả thiết bị(máy tính, điện thoại, tablet...). Việc responsive tốt sẽ giúp tăng trải nghiệm người dùng


## 1. Các khái niệm responsive phổ biến:

**Mobile first**: code giao diện trên các thiết bị di động trước, rồi sau đó responsive cho các thiết bị có kích thước màn hình hiển thị lớn hơn như desktop, laptop...
> Các kích thước màn hình phổ biến: 320, 480, 768, 1024, 1280, 1366, 1440, 1600, 1920px
**Lưu ý**: Sử dụng ```@media screen and (min-width: kích thước)``` khi code mobile first

**Desktop first**: Ngược lại với "mobile first", "desktop first" là code giao diện cho các thiết bị màn hình lớn trước sau đó mới responsive cho các thiết bị di động
> Các kích thước màn hình lớn phổ biến: 
**Lưu ý 1**: Sử dụng ```@media screen and (max-width: kích thước)``` khi code desktop first

> Việc chọn "mobile first" hay "desktop first" phụ thuộc vào sở thích, kinh nghiệm hoặc CSS library đang sử dụng

**Lưu ý 2**:

min-width + ```kích thước```: lớn hơn hoặc bằng
max-width + ```Kích thước - 1```: nhỏ hơn hoặc bằng


## 2. Hướng dẫn: 

Để sử dụng Responsive CSS, chúng ta sẽ thêm các media queries vào file CSS để định nghĩa các điều kiện cho trang web được hiển thị trên các thiết bị khác nhau

#### Demo code

```
// Thiết lập cách hiển thị cho màn hình lớn
.container{
	display: grid;
	grid-template-columns: 1fr 1fr;
}

// Thiết lập hiển thị cho màn hình có kích thước màn hình nhỏ hơn 600px
@media screen and (max-width: 600px){
	.container{
		display: block;
	}
}

```
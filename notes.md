- [1. Những thành phần cơ bản thường gặp của 1 website:](#1-những-thành-phần-cơ-bản-thường-gặp-của-1-website)
- [2. Các bước dựng khung HTML \& CSS](#2-các-bước-dựng-khung-html--css)
- [3. Các lưu ý khác trong quá trình viết CSS.](#3-các-lưu-ý-khác-trong-quá-trình-viết-css)

# 1. Những thành phần cơ bản thường gặp của 1 website:

1. Header.
2. Navigation.
3. Breadcrum = Indicator/ giúp user biết mình đang ở đâu trên trang web.
4. Sidebar.
5. Content.
6. Slider.
7. Banner.
8. Footer.

# 2. Các bước dựng khung HTML & CSS

1. Vị trí
2. Kích thước
3. Màu sắc
4. Styles

- Nên viết CSS từ trên xuống dưới, từ ngoài vào trong và sử dụng kết hợp mục Outline của VSCode.

# 3. Các lưu ý khác trong quá trình viết CSS.

- Quy tắc hiển thị ảnh: giữ đúng tỷ lệ gốc. Có thể tính được tỷ lệ này khi xem intrinsic size của ảnh nếu đang clone từ một trang có sẵn.
- Nên sử dụng background-image với cú pháp short-hand (gộp nhiều thuộc tính, sau dấu / là các thuộc tính kích thước và repeatation):
``` 
    #slider {
    background-color: gray;
    margin-top: 46px;
    padding-top: 50%;
    background: url("/w3_band/assets/img/slider/slider1.jpg") top center / cover
    no-repeat;
    }
```
- Khi nhập sai đường dẫn ảnh, 1 mẹo để kiểm tra nhanh là check error warning của browser console.
- Lưu ý sự tương quan về position giữa các element cha-con để tránh sự thay đổi box-sizing không mong muốn, đặc biệt khi chèn chữ vào ảnh để tránh làm thay đổi tỷ lệ ảnh.
- Nên CSS kiểu **"cha dắt con"**, tối ưu là 2 cấp (cd: #content .member-item), tối đa 3 cấp nếu cần select đến một tag HTML cụ thể (vd: #content .member-item > img). Cách này sẽ giúp tránh trường hợp đặt trùng tên id/class sau này.
- Viết thêm các id/class phụ cho một thuộc tính dạng "khác biệt với số đông" (vd: tất cả text đều màu đen => có thể css chung toàn bộ với class "text; nhưng lại có 1 số đoạn text lại màu trắng => tạo class "white-text" và gắn thêm vào lass chung thành "text white-text")
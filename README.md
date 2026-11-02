# Bài 3 : Xử lý Sự cố Giao diện Website Doanh nghiệp

## ***Phần 1: Báo cáo phân tích (I/O)***
### Phác thảo sơ đồ Box Model hiện tại của phần tử bị lỗi qua việc soi thực tế.
- Margin (Lề ngoài): margin-top: -32px (nguyên nhân chính gây chồng lấn lên khung phía trên), margin-bottom: 16px.
- Border (Viền): 1px solid rgba(229, 231, 235, 1).
- Padding (Đệm trong): 24px toàn bộ các phía.
- Content (Nội dung): width: 100%.

## PHẦN 2: THIẾT KẾ GIẢI PHÁP KHẮC PHỤC
### Sửa thông số tại bảng Styles để tách biệt hai khung nội dung


```css
.lesson-content-wrapper {
    margin-top: 16px !important; /* Thay lề âm thành lề dương để tránh đè khung */
    box-sizing: border-box;     /* Chuẩn hóa cách tính toán kích thước bao gồm padding và border */
    position: relative;
    z-index: 10;                /* Cố định tầng hiển thị, tránh chồng lấn giao diện */
}

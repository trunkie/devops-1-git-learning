# Các lệnh Git

## 1. Cấu hình và khởi tạo Repo
### $\mathcal{\color{purple}{git \ config \ --global \ user.name} \ \color{yellow}{newname}}$
> Đổi tên người dùng

$\mathcal{\color{purple}{git \ config \ --global \ user.email} \ \color{yellow}{newmail@domain.com}}$
> Đổi email người dùng

### ${\color{purple}{git \ init}$
> Khởi tạo một Local Repository mới

### ${\color{purple}{git \ init \ --bare}$
> Khởi tạo một Remote Repository mới ở Git Server

## 2. Làm việc với Local Repo

### ${\color{purple}{git \ status}$
> Trạng thái của Repo

### ${\color{purple}{git \ status \ -s}$
> Trạng thái của Repo ngắn gọn

### ${\color{purple}{git \ clone} \ \color{yellow}{path}}$
> Sao chép một Repository có địa chỉ là path

### ${\color{purple}{git \ add}$
> Cập nhật vào staged

### ${\color{purple}{git \ add} \ \color{yellow}{filename}}$
> Thêm file vào staged

### ${\color{purple}{git \ add} \ \color{yellow}{*.c}}$
> File có phần mở rộng .c

### ${\color{purple}{git \ add \ -A}$
> Thêm mọi thứ có sự thay đổi (file mới, xóa file, nội dung thay đổi ...)

### ${\color{purple}{git \ add \ .}$
> Thêm mọi thứ trừ loại xóa file

### ${\color{purple}{git \ add -}$
> Thêm mọi thứ trừ file mới

### ${\color{purple}{git \ commit \ -m } \ \color{yellow}{"Thông báo ..."}}$
> Commit mới

### ${\color{purple}{git \ commit \ --amend \ -m} \ \color{yellow}{"Thông báo ..."}}$
> Commit + cập nhật vào commit cuối

### ${\color{purple}{git \ log}$
> Lịch sử commit

### ${\color{purple}{git \ log \ -4}$
> Lịch sử 4 commit

### ${\color{purple}{git \ log \ -4 \ -p}$
> Lịch sử 4 commit + chi tiết thay đổi

### ${\color{purple}{git \ log \ --pretty=oneline}$
> Hiện thị trực quan trên 1 dòng

### ${\color{purple}{git \ log \ --oneline}$
> Hiện thị trên 1 dòng

### ${\color{purple}{git \ diff}$
> Xem sự khác biệt giữa thư mục làm việc và staged

### ${\color{purple}{git \ diff \ --staged}$
> Xem sự khác biệt giữa staged và commit cuối

### ${\color{purple}{git \ rm} \ \color{yellow}{filename}}$
> Xóa file

### ${\color{purple}{git \ reset \ HEAD} \ \color{yellow}{filename}}$
> Hủy thay đổi của file

### ${\color{purple}{git \ checkout \ -- filename}$
> Khôi phục thay đổi của file

### ${\color{purple}{git \ checkout \ [hash]} \ \color{yellow}{filename}}$
> Khôi phục từ commit có mã hash

### ${\color{purple}{git \ checkout \ [hash] .}$
> Khôi phục các file từ commit có mã hash

### ${\color{purple}{git \ clean \ -d \ -fx \ .}$
> Xóa các file không được theo dõi, có ích khi muốn xóa bỏ nhanh các file không được theo dõi
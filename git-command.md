
# Các lệnh ### git

## 1.Cấu hình và khởi tạo Repo

### git config --global user.name newname
> Đổi tên người dùng
### git config --global user.email newmail@domain.com
> Đổi email người dùng
### git init
> Khởi tạo một Local Repository mới
### git init --bare
> Khởi tạo một Remote Repository mới ở ### git Server

## 2.Làm việc với Local Repo

### git status
> Trạng thái của Repo

### git status -s
> Trạng thái của Repo ngắn gọn

### git clone path
> Sao chép một Repository có địa chỉ là path

### git add
> Cập nhật vào staged

### git add filename
> Thêm file vào staged

### git add *.c
> File có phần mở rộng .c

### git add -A
> Thêm mọi thứ có sự thay đổi (file mới, xóa file, nội dung thay đổi ...)

### git add .
> Thêm mọi thứ trừ loại xóa file

### git add -
> Thêm mọi thứ trừ file mới

### git commit -m "Thông báo ..."
> Commit mới

### git commit --amend -m "Thông báo ..."
> Commit + cập nhật vào commit cuối

### git log
> Lịch sử commit

### git log -4
> Lịch sử 4 commit

### git log -4 -p
> Lịch sử 4 commit + chi tiết thay đổi

### git log --pretty=oneline
> Hiện thị trực quan trên 1 dòng

### git log --oneline
> Hiện thị trên 1 dòng

### git diff
> Xem sự khác biệt giữa thư mục làm việc và staged

### git diff --staged
> Xem sự khác biệt giữa staged và commit cuối

### git rm filename
> Xóa file

### git reset HEAD filename
> Hủy thay đổi của file

### git checkout -- filename
> Khôi phục thay đổi của file

### git checkout [hash] filename
> Khôi phục từ commit có mã hash

### git checkout [hash] .
> Khôi phục các file từ commit có mã hash

### git clean -d -fx .
> Xóa các file không được theo dõi, có ích khi muốn xóa bỏ nhanh các file không được theo dõi

## 3.Làm việc với Remote Repo

### git remote
> Xem các Remote

### git remote -v
> Xem các Remote

### git remote add name_remote addr_remote
> Thêm một Remote vào Local

### git fetch name_remote
> Cập nhật Local Repo từ Remote Repo

### git pull name_remote name_branch
> Cập nhật Local Repo từ Remote Repo

### git push name_remote name_branch
> Cập nhật Local Repo từ Remote Repo

### git remote show name_remote
> Xem thông tin về Remote

### git remote rename abc xyz
> Đổi tên Remote

## 4.Làm việc với Tag

### git tag
> Xem danh sách tag

### git tag -a tagname -m "Ghi chú"
> Tạo tag cho commit hiện tại

### git tag -a tagname -m "Ghi chú" hash
> Tạo tag cho commit cũ

### git show tagname
> Thông tin về commit có tagname

### git push origin tagname
> Cập nhận lên remote tất cả tagname

### git push origin --tags
> Cập nhận lên remote tất cả tag

### git checkout tagname
> Về phiên bản commit có tagname

### git checkout -b newbranchname tagname
> Tạo nhánh mới từ phiên bản tagname

### git push --delete origin tagname
> Xóa tag ở remote

### git tag -d tagname
> Xóa tag ở local

## 5.Làm việc với nhánh

### git branch
> Liệt kê các nhánh

### git branch -v
> Liệt kê các nhánh + commit cuối

### git branch --merged
> Các nhánh gộp vào nhánh này

### git branch --no-merged
> Các nhánh không gộp vào nhánh này

### git branch branchname
> Tạo nhánh mới

### git checkout -b branchname
> Tạo nhánh mới, khi đang đứng ở một snapshot cũ

### git checkout branchname
> Chuyển nhánh

### git merge branchname
> Gộp nhánh với nhánh hiện tại

### git base branchname
> Gộp nhánh với nhánh hiện tại

### git mergetool
> Công cụ trực quan xử lý xung đột merge

### git branch -d branchname
> Xóa nhánh

## 6.Xóa toàn bộ lịch sử Commit

## Xóa lịch sử toàn bộ commit trên nhánh : master

### git checkout master                                 
> Chuyển về nhánh master

### git checkout --orphan temp_branch                   
> Tạo nhánh temp_branch không chứa lịch sử commit

### git add -A                                          
> Thêm các file vào nhánh

### git commit -am "Init"                               
> Commit đầu tiên

### git branch -D master                                
> Xóa nhánh master

### git branch -m master                                
> Đổi tên nhánh hiện tại (temp_branch) thành master

### git push -f origin master                           
> Push thay đổi lên Remote

### git checkout IDcommitB --  $(git diff --name-only IDcommitA IDcommitB)
> Phục hồi các file bị sửa đổi từ một commit, so với commit khác
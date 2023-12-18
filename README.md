Kịch bản:
- Task 1: Check đầu vào, quét để xác nhận các cổng 5432 và 22 mở
- Task 2: Khai thác lỗi đăng nhập trên PostgreSQL, cổng 5432 -> Đăng nhập thành công
- Task 3: Đăng nhập thành công thì có thể thực hiện mọi hành động trên csdl -> tạo superuser, tạo bảng ->  lấy được public key thông qua bảng
- Task 4: Tìm hiểu về chmod + Fix lỗi hay gặp không kết nối được ssh key: thường là lưu file public key ở Server ở các thư mục không được chmod phù hợp. Khai thác lỗi trên PostgreSQL cho phép mở shell chạy với quyền root. Trước khi chmod thì có thể đọc các file trên victim qua shell, sau khi chmod thì không đọc được file.
- Task 5: Sau khi lấy được public key từ đó dùng brute force để tìm ra được private key -> ssh login thành công và mở được file được cá nhân hóa trong máy victim và thu được chuỗi ký tự.

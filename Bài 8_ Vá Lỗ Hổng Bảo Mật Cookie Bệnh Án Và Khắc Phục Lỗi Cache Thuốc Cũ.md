Phần 1: Nguyên nhân & Lỗ hổng  
Lỗi hiển thị dữ liệu cũ: Do trình duyệt sử dụng lại file lưu sẵn trong bộ nhớ đệm (Browser Cache) thay vì tải mới từ máy chủ.  
Nguy cơ mất tài khoản (Session Hijacking): Cookie thiếu cờ HttpOnly nên tin tặc có thể dùng JavaScript (document.cookie) đánh cắp phiên đăng nhập. Việc thiếu cờ Secure cũng khiến dữ liệu dễ bị nghe lén trên đường truyền mạng.  
Phần 2: Cách khắc phục & Kiểm tra  
Sửa lỗi giao diện ngay lập tức: Bấm Ctrl \+ Shift \+ R (hoặc Ctrl \+ F5) để ép trình duyệt tải mới toàn bộ dữ liệu (Hard Reload).  
Bảo mật Cookie: Phải thêm các từ khóa HttpOnly; Secure; vào cuối đoạn mã Set-Cookie.  
Thao tác trên DevTools (F12):  
Sang tab Network, tích chọn Disable cache để vô hiệu hóa bộ nhớ đệm.  
Sang tab Application, vào mục Cookies, kiểm tra xem các cột HttpOnly và Secure đã được đánh dấu tích (✓) chưa.  

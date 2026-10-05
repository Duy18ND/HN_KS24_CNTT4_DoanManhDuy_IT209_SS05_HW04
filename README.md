# Báo cáo Bài 4: Mô phỏng quy trình Hotfix & Gitflow thực tế

## 1. Giải thích quy trình xử lý lỗi khẩn cấp
- Khởi tạo bối cảnh: Hệ thống đang chạy ổn định phiên bản `v1.0.0` trên nhánh `main`. Nhánh `develop` đang chứa code tính năng mới.
- Xử lý sự cố: Khi phát hiện lỗi lộ dữ liệu, em đã tách nhánh khẩn cấp `hotfix/v1.0.1` trực tiếp từ nhánh `main`.
- Đưa bản vá lên Production: Sau khi sửa xong lỗi trên nhánh hotfix, em tiến hành gộp (merge) lại vào `main` và đánh tag `v1.0.1` để chuẩn bị release bản vá.
- Đồng bộ lại code: Để tránh nhánh phát triển sau này bị lặp lại lỗi cũ, em tiếp tục gộp nhánh `hotfix/v1.0.1` vào nhánh `develop`. Sau khi hoàn tất tiến trình, nhánh hotfix được xóa để dọn dẹp kho lưu trữ.

## 2. Sơ đồ lịch sử gộp nhánh (Git Graph)
Dưới đây là kết quả chạy lệnh `git log --graph --oneline --all` minh chứng cho quy trình Gitflow phân nhánh và gộp nhánh thành công:

(Bạn dán kết quả toàn bộ đoạn mã đồ thị ASCII có các đường chéo / \ vào đây. Hoặc nếu bạn đã chụp ảnh, hãy xóa dòng này đi và thay bằng cú pháp chèn ảnh: <img width="739" height="151" alt="Ảnh chụp màn hình 2026-10-05 094735" src="https://github.com/user-attachments/assets/072f693d-ed39-4875-8384-841a7538f2fa" />

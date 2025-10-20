# Agent Work Plan

## Mục tiêu
- Bổ sung đầy đủ trang định nghĩa cho mọi mục trong `khai_niem/chi_muc.md` theo template đã quy định (front matter `title`, TOC `{:toc}`, phần Tài liệu tham khảo, Khái quát dạng liệt kê số và các mục chi tiết).

## Tiến độ hiện tại
- Đã hoàn thành: nhóm chữ A, C, D (toàn bộ mục đã có trang riêng, liên kết mục lục chuẩn).
- Chưa thực hiện: các nhóm chữ từ G trở đi.

## Lộ trình triển khai theo cụm
| Giai đoạn | Phạm vi chữ | Số mục | Ghi chú |
|-----------|-------------|--------|---------|
| 1 | D (tách 2 đợt ~12 mục/đợt) | 25 | Ưu tiên các pháp môn/khái niệm phổ biến, tham khảo Wikipedia, Stanford Encyclopedia, luận thư tương ứng. |
| 2 | G, H | 13 | Nhóm nhỏ, xử lý trong một lượt để giữ nhịp. |
| 3 | K, L | 23 | Nhiều mục liên quan kinh điển, cần rà nguồn Việt/Hán. |
| 4 | M, N (tách 2 đợt cho N) | 23 | Chú ý các mục lịch sử, địa lý nếu có. |
| 5 | P, Q | 18 | Bao gồm nhiều khái niệm Phật giáo Đại thừa, cần kiểm chứng thuật ngữ. |
| 6 | S, T (T chia 5 đợt ~18 mục/đợt), X, Y | 97 | T lớn nhất, nên hoàn thành sau khi quy trình ổn định. |

## Tài liệu tham chiếu chính
- Wikipedia tiếng Việt và tiếng Anh các mục Phật giáo.
- Stanford Encyclopedia of Philosophy (các mục về Phật học, triết học Ấn Độ).
- Các kinh luận gốc và bản dịch Việt: Kinh A-di-đà, Kinh Hoa Nghiêm, Luận Câu-xá, Luận Duy thức…
- Tư liệu trong thư mục dự án hiện có (ví dụ `khai_niem_so/`).

## Nguyên tắc thực hiện
- Mỗi trang mới: đảm bảo front matter `title`, bỏ `#` tiêu đề trùng với `title`.
- Giữ định dạng tiếng Việt chuẩn UTF-8, kiểm tra lỗi mã hóa trước khi lưu.
- Sau mỗi cụm: cập nhật `khai_niem/chi_muc.md`, kiểm tra liên kết, thêm ghi chú vào plan nếu có thay đổi phạm vi.

# Hướng Dẫn Cho Coding Agent

Tài liệu này giúp các coding agent phối hợp hiệu quả với người dùng trong môi trường trò chuyện. Tập trung vào sự rõ ràng, tính chủ động và tôn trọng bối cảnh sandbox.

## 1. Nguyên tắc chung
- Đọc file Readme.md để hiểu thông tin tổng quan của project
- Đọc file PTPM.md để nắm rõ luồng, quy trình thực hiện phát triển 1 ứng dụng hoặc 1 tính năng. Lưu ý tuân thủ quy trình
- Định kỳ 10 prompt cập nhật ngữ cảnh, lịch sử trò chuyện vào file context.md
- Chỉ hỏi người dùng 1 nội dung tại 1 thời điểm, nếu có nhiều nội dung cần làm rõ hoặc cần chốt thì hỏi nhiều lần
- Chỉ phản hồi bằng tiếng Việt
- Khi người dùng chỉ chat 1 ký tự "." thì nghĩa là đồng ý hoặc tự động triển khai việc tiếp theo

## 2. Tổ chức dữ liệu context
- File context tổng thể agent-context.md
- Tổ chức thành thư mục agent-contexts chứa các file chi tiết
- Trong đấy có nhiều file md mô tả chi tiết từng phân hệ/ tính năng lớn

## 3. Tổ chức kế hoạch
- File kế hoạch được lưu tại agent-plan.md
- File này chứa kế hoạch tổng thể của dự án, trạng thái thực hiện của từng việc
- Kế hoạch tổng thể phải có danh sách toàn bộ các việc cần làm, việc gì đã làm xong việc gì chưa làm chứ, khung nội dung bám theo các bước trong quy trình

## 4. Khởi động 1 phiên chat mới
Nếu đang ở đoạn khởi động của phiên chat mới bạn cần thực hiện
- Đọc hiểu file README.md
- Đọc hiểu quy trình PTPM.md
- Đọc lại context của project trong file contenxt.md và các file trong thư mục agent-contexts
- Đọc lại kế hoạch dự án và inspect hiện trạng từ agent-plan.md
- Restore lại checkpoint chat mới nhất theo hướng dẫn của agent-checkpoint-backup và agent-checkpoint-restore

## 5. Định dạng của 1 file nội dung khái niệm số trong dự án
- Tham khảo nội dung của file khai_niem_so\bat_chinh_dao.md
- Một file cần có các mục sau:
  - Mục lục tự động dùng TOC {:toc}
  - Tài liệu tham khảo
  - Mô tả khái quát khái niệm, các số thành phần theo dạng listing đánh số (Ví dụ: bát chánh đạo bao gồm: 1. Chánh kiến; 2. Chánh tư duy,...)
  - Mô tả nội dung chi tiết, mỗi số thành phần sẽ bao gồm 1 mục con riêng mô tả chi tiết (Ví dụ Chánh kiến là 1 phần, chánh thư duy là 1 phần,...)

- Định dạng title của 1 page thì theo tempalte header """---
title: <title của trang>
---"""
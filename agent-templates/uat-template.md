# User Acceptance Test Report (UAT)

**Project:** [Tên dự án]  
**Version:** [v1.0]  
**UAT Cycle:** [Lần chạy UAT thứ mấy]  
**Date Created:** [YYYY-MM-DD]  
**Prepared by:** [BA / QA Name]  
**Reviewed by:** [PO / QA Lead]  

---

## 1. Overview
- **Mục tiêu:** [Mô tả ngắn mục tiêu đợt UAT]  
- **Phạm vi kiểm thử:** [Module / chức năng / user flow liên quan]  
- **Tài liệu tham chiếu:**  
  - [FSD_ID]  
  - [BRD_ID]  
  - [Feature_ID / Story_ID]

---

## 2. Test Environment
| Thành phần | Mô tả / Phiên bản | Ghi chú |
|-------------|--------------------|----------|
| Server | [UAT / Staging URL] | [Địa chỉ truy cập] |
| Build Version | [Tên hoặc mã build] | [Ngày deploy] |
| Data Set | [Môi trường dữ liệu / loại dữ liệu] | [Có mask dữ liệu thật không] |

---

## 3. UAT Test Scenarios

| STT | Scenario | Mô tả ngắn | Liên kết FSD | Người test | Kết quả | Ghi chú |
|------|-----------|-------------|----------------|--------------|----------|----------|
| 1 | [Tên scenario] | [Mục tiêu kiểm thử] | [FSD-01] | [Tên user/role] | Pass / Fail | [Chi tiết nếu fail] |
| 2 | ... | ... | ... | ... | ... | ... |

---

## 4. Detailed Test Cases
> Mỗi test case mô tả hành vi người dùng và kết quả mong đợi.

| ID | User Story | Preconditions | Steps | Expected Result | Actual Result | Status |
|----|-------------|---------------|--------|-----------------|----------------|---------|
| TC-01 | [US-01] | [Điều kiện ban đầu] | [Các bước cụ thể] | [Kết quả mong đợi] | [Kết quả thực tế] | Pass / Fail |
| TC-02 | ... | ... | ... | ... | ... | ... |

---

## 5. Defects & Deviations
| ID | Liên kết Test Case | Mức độ nghiêm trọng | Mô tả lỗi | Ghi chú / Ảnh minh họa | Trạng thái |
|----|---------------------|----------------------|-----------|------------------------|-------------|
| BUG-01 | TC-02 | Cao | [Mô tả ngắn] | [Ảnh / link Jira] | Open / Fixed / Retest |
| BUG-02 | ... | ... | ... | ... | ... |

---

## 6. User Feedback Summary
> Tổng hợp phản hồi định tính từ người dùng / PO sau UAT.

| Người phản hồi | Vai trò | Nội dung phản hồi | Đánh giá (1–5) | Hành động tiếp theo |
|----------------|----------|--------------------|-----------------|----------------------|
| [Tên] | [Role] | [Nội dung] | [Mức độ hài lòng] | [PO/BA ghi chú hành động] |

---

## 7. Acceptance Decision
| Tiêu chí | Kết quả | Ghi chú |
|-----------|----------|----------|
| Tỷ lệ test case Pass ≥ 90% | ✅ Đạt / ❌ Không đạt |  |
| Không có lỗi nghiêm trọng (Critical bug) | ✅ / ❌ |  |
| PO xác nhận hành vi sản phẩm đúng giá trị nghiệp vụ | ✅ / ❌ |  |
| QA xác nhận tính ổn định môi trường | ✅ / ❌ |  |

**Quyết định cuối:**  
> ✅ **Approved for Production** / ❌ **Need Fixes & Retest**

**Người phê duyệt:** [Tên PO / QA Lead]  
**Ngày:** [YYYY-MM-DD]

---

## 8. Lessons Learned (Rút kinh nghiệm)
- [Ghi nhận điểm tốt trong quy trình UAT]  
- [Các vấn đề lặp lại cần tránh]  
- [Đề xuất cải tiến cho vòng sau]

---

## 9. Acceptance Criteria (UAT Ready)
- Có **≥1 vòng test hoàn chỉnh với log Pass/Fail rõ ràng**.  
- Có **kết luận phê duyệt của PO/QA Lead**.  
- Có **phản hồi người dùng được ghi nhận**.  
- Có **liên kết rõ đến các FSD và Story tương ứng**.

---

## Metadata
- **File name format:** `[PROJECT]_UAT_Report_[VERSION]_YYYYMMDD.md`  
- **Example:** `CyberGuard_UAT_Report_v1_20251016.md`

# Business Requirement Document (BRD)

**Project:** [Tên dự án]  
**Version:** [v1.0]  
**Date Created:** [YYYY-MM-DD]  
**Created by:** [BA Name]  
**Reviewed by:** [Product Owner / Tech Lead]  

---

## 1. Executive Summary
- **Mục tiêu kinh doanh:** [Mô tả ngắn gọn giá trị / KPI sản phẩm hướng tới]  
- **Tình trạng hiện tại:** [Tóm tắt vấn đề hoặc hạn chế đang tồn tại]  
- **Phạm vi thực hiện:** [Các module / nghiệp vụ liên quan]  
- **Kết quả mong đợi:** [Chỉ tiêu định lượng, ví dụ: giảm 30% thời gian thao tác, tăng 20% độ chính xác,…]

---

## 2. Business Context
- **Nguồn gốc yêu cầu:** [HMW, Persona, Empathy Map, Feature List đã duyệt]  
- **Người dùng mục tiêu:** [Tên Persona hoặc nhóm user]  
- **Bối cảnh nghiệp vụ:** [Tình huống / quy trình thực tế khi họ tương tác với sản phẩm]  
- **Giá trị mang lại:** [Tác động định lượng và định tính]

---

## 3. Functional Requirements (Yêu cầu chức năng)
| ID | Tên chức năng | Mô tả | Người dùng mục tiêu | Luồng hành động chính | Liên kết Feature | Ưu tiên | Ghi chú |
|----|----------------|-------|--------------------|----------------------|-----------------|----------|----------|
| FR-01 | [Tên chức năng] | [Mô tả nghiệp vụ] | [Persona] | [Luồng thao tác cơ bản] | [FeatureID] | Cao / TB / Thấp | [Chi tiết thêm] |
| FR-02 | ... | ... | ... | ... | ... | ... | ... |

---

## 4. Non-Functional Requirements (Phi chức năng)
| ID | Loại yêu cầu | Mô tả | Tiêu chí đo lường | Ghi chú |
|----|----------------|-------|------------------|----------|
| NFR-01 | Hiệu năng | [Ví dụ: phản hồi < 2s cho 95% request] | [Công cụ đo / tiêu chuẩn] |  |
| NFR-02 | Bảo mật | [Ví dụ: xác thực 2 lớp cho tài khoản quản trị] | [Tiêu chuẩn hoặc chính sách] |  |
| NFR-03 | Khả dụng | [Ví dụ: uptime ≥ 99.5%] | [SLA hoặc chỉ số giám sát] |  |

---

## 5. Business Rules (Quy tắc nghiệp vụ)
| ID | Mô tả quy tắc | Tình huống áp dụng | Ngoại lệ | Ghi chú |
|----|----------------|--------------------|----------|----------|
| BR-01 | [Quy tắc tính điểm rủi ro] | [Áp dụng cho user nhóm A] | [Trường hợp ngoại lệ] |  |
| BR-02 | [Quy tắc hiển thị cảnh báo] | [Áp dụng cho sự kiện loại X] | [Nếu … thì …] |  |

---

## 6. Process Flow (Luồng nghiệp vụ)
**Mô tả dạng text hoặc sơ đồ (đính kèm file BPMN nếu có):**  
1. [Người dùng hành động]  
2. [Hệ thống phản hồi]  
3. [Kết quả / dữ liệu phát sinh]  
4. [Ngoại lệ hoặc xử lý lỗi]

---

## 7. Data Requirement (Yêu cầu dữ liệu)
| Trường dữ liệu | Nguồn | Kiểu dữ liệu | Bắt buộc | Ghi chú |
|----------------|--------|---------------|-----------|----------|
| user_id | Hệ thống đăng nhập | string | Có |  |
| alert_type | Hệ thống log | enum | Có | [Danh sách giá trị hợp lệ] |
| created_at | System | datetime | Có |  |

---

## 8. Acceptance Criteria (Điều kiện nghiệm thu)
- Mỗi **Functional Requirement** có mô tả hành vi kiểm thử được.  
- Có **Business Rules và Data Requirement rõ ràng**.  
- PO xác nhận rằng yêu cầu này **phản ánh đúng nhu cầu người dùng và mục tiêu sản phẩm**.  
- Tài liệu được **Tech Lead và QA Lead phê duyệt** trước khi chuyển sang FSD.

---

## 9. Change Control (Kiểm soát thay đổi)
| Lần thay đổi | Mô tả | Người đề xuất | Người duyệt | Ngày |
|---------------|--------|---------------|--------------|------|
| 1 | [Thay đổi mô tả nghiệp vụ module X] | [Tên] | [PO] | [Ngày] |

---

## Metadata
- **File name format:** `[PROJECT]_BRD_[MODULE]_[VERSION]_YYYYMMDD.md`  
- **Example:** `CyberGuard_BRD_AlertModule_v1_20251016.md`

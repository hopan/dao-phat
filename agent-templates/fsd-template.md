# Functional Specification Document (FSD)

**Project:** [Tên dự án]  
**Module:** [Tên module / chức năng chính]  
**Version:** [v1.0]  
**Date Created:** [YYYY-MM-DD]  
**Created by:** [BA Name]  
**Reviewed by:** [Tech Lead / QA Lead / PO]  

---

## 1. Overview
- **Mục tiêu:** [Tóm tắt mục tiêu nghiệp vụ của module này]  
- **Phạm vi:** [Các phần hệ thống có liên quan]  
- **Liên kết:** [BRD_ID / Feature_ID / Story_ID]  

---

## 2. Functional Summary
> Liệt kê toàn bộ các chức năng trong module.

| ID | Tên chức năng | Mô tả ngắn | Nguồn BRD/Story | Trạng thái |
|----|----------------|-------------|------------------|-------------|
| F1 | [Tên] | [Tóm tắt hành vi] | [BRD-01 / US-01] | Planned / Done |
| F2 | ... | ... | ... | ... |

---

## 3. Functional Details

### F[ID] – [Tên chức năng]
- **Mục tiêu:** [Mô tả hành vi mong đợi]  
- **Actor chính:** [User / System / Admin / Integration]  
- **Luồng chính (Main Flow):**
  1. [Mô tả step-by-step người dùng và hệ thống tương tác]
  2. [Phản hồi từ hệ thống]
  3. [Điều kiện kết thúc]
- **Luồng phụ (Alternate / Exception Flow):**
  - Nếu [điều kiện], thì [hành vi thay thế].  
  - Nếu lỗi [X], hệ thống [phản ứng].  
- **Input / Output:**
  | Trường | Nguồn | Loại dữ liệu | Bắt buộc | Ghi chú |
  |---------|--------|---------------|-----------|----------|
  | [field_name] | [User/System] | [String/Date/Enum] | Có/Không | [Mô tả] |
- **Validation Rules:**  
  - [Điều kiện hợp lệ 1]  
  - [Điều kiện hợp lệ 2]
- **Error Handling:**  
  - [Thông báo lỗi và hành vi hệ thống]
- **Giao diện liên quan (UI/UX):**  
  - [Tên màn hình / prototype link]  
  - [Tham chiếu figma / wireframe nếu có]
- **API / Integration (nếu có):**  
  | API | Mục đích | Phương thức | Endpoint | Ghi chú |
  |------|-----------|--------------|-----------|----------|
  | [Tên API] | [Mục đích] | [GET/POST/PUT] | [Endpoint] | [Tham chiếu API doc] |

---

## 4. Business Rules & Constraints
| ID | Quy tắc / Ràng buộc | Liên kết BRD | Ghi chú |
|----|----------------------|----------------|----------|
| BR-01 | [Mô tả quy tắc nghiệp vụ] | [BRD-02] | [Chi tiết nếu có] |
| BR-02 | ... | ... | ... |

---

## 5. UI & Navigation Flow
> Mô tả hành trình người dùng trên hệ thống, các màn hình liên kết.

| Màn hình | Hành động / Trigger | Dẫn đến màn hình | Ghi chú |
|-----------|--------------------|------------------|----------|
| [Screen A] | [Click nút “…”] | [Screen B] | [Mô tả hành vi] |

---

## 6. System Interaction (nếu có)
> Mô tả các thành phần kỹ thuật và giao tiếp giữa các module / hệ thống.

| Thành phần | Tương tác với | Kiểu trao đổi | Ghi chú |
|-------------|----------------|----------------|----------|
| Module A | Module B | REST / Queue / Event | [Mục đích] |
| Module A | Database | CRUD | [Chi tiết] |

---

## 7. Performance & Security Constraints
- **Hiệu năng:** [Ví dụ: thời gian phản hồi < 2s cho 95% request]  
- **Bảo mật:** [Ví dụ: chỉ người dùng có role Admin mới truy cập được endpoint này]  
- **Audit / Logging:** [Yêu cầu log hoặc tracking bắt buộc]  

---

## 8. Acceptance Criteria (FSD Ready)
- Có **trace đầy đủ** từ BRD → Feature → Story → FSD.  
- Mỗi chức năng có **luồng chính, luồng phụ, validation, error handling rõ ràng**.  
- Có mô tả **UI / API / Integration** cụ thể.  
- Được **Tech Lead & QA Lead phê duyệt** trước khi triển khai Dev Sprint.

---

## Metadata
- **File name format:** `[PROJECT]_FSD_[MODULE]_[VERSION]_YYYYMMDD.md`  
- **Example:** `CyberGuard_FSD_AlertModule_v1_20251016.md`

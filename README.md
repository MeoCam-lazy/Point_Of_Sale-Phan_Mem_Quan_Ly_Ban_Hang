# Phần Mềm Quản Lý Bán Hàng (POS)

> **Xây dựng hệ thống tính tiền, quản lý kho hàng và báo cáo doanh thu cho cửa hàng bán lẻ**

## 📌 Thông tin đồ án
- **Trường / Khoa:** Trường Đại học Khoa học, Đại học Huế (HUSC) – Khoa Công nghệ Thông tin
- **Học phần:** Phân tích Thiết kế Hướng đối tượng (OOAD)
- **Năm học:** 2025 – 2026
- **Giáo viên hướng dẫn:** ThS. Phan Nguyễn Ý Nhi
- **Nhóm thực hiện:** Nhóm Nghiên cứu & Phát triển Hệ thống POS

## 👥 Thành viên thực hiện
| STT | Họ và tên | Vai trò / Ghi chú |
| :---: | :--- | :--- |
| 1 | **Nguyễn Trương Văn Khoa** | Nhóm trưởng · [@MeoCam-lazy](https://github.com/MeoCam-lazy) |
| 2 | **Trương Quỳnh Hoa** | Thành viên |
| 3 | **Vũ Trần Đăng Nguyên** | Thành viên |
| 4 | **Đặng Tiến Lực** | Thành viên |

## 🧩 Tổng quan hệ thống
Hệ thống được phân tích và thiết kế theo phương pháp Hướng đối tượng (UML 2.x) với kiến trúc 3 tầng (**Presentation** – **Business Logic** – **Data & Integration**), gồm 3 phân hệ nghiệp vụ cốt lõi:

1. **Tính tiền tại quầy (POS Checkout & Billing):** Quét mã vạch Barcode 1D/2D, tra cứu giá & tồn kho real-time, tích điểm thành viên, tính chiết khấu/VAT, thanh toán tiền mặt hoặc QR động (VietQR / VNPay / MoMo) và in hóa đơn nhiệt 80mm (ESC/POS).
2. **Quản lý Kho hàng (Inventory & Stock Management):** Quản lý danh mục sản phẩm, nhà cung cấp, lập & phê duyệt phiếu nhập kho, tự động cộng/trừ tồn kho theo giao dịch, lưu thẻ kho biến động và cảnh báo chạm ngưỡng tồn tối thiểu.
3. **Báo cáo Doanh thu & Quản trị (Revenue & Analytics Reporting):** Quản lý mở/đóng ca thu ngân và đối soát tiền mặt, thống kê doanh thu thuần, giá vốn hàng bán (COGS), lợi nhuận gộp, Top sản phẩm bán chạy và xuất báo cáo Excel (`.xlsx`) / PDF (`.pdf`).

## 🏗️ Thiết kế kỹ thuật (Tóm tắt)
- **Phân tích nghiệp vụ:** 5 tác nhân (Thu ngân, Thủ kho, Quản lý, Cổng thanh toán, Thiết bị ngoại vi POS) & 11 Use Cases cốt lõi.
- **CSDL quan hệ (chuẩn 3NF):** 12 bảng (`DANH_MUC_SP`, `SAN_PHAM`, `NHA_CUNG_CAP`, `NHAN_VIEN`, `CA_LAM_VIEC`, `KHACH_HANG`, `HOA_DON`, `CHI_TIET_HOA_DON`, `THANH_TOAN`, `PHIEU_NHAP_KHO`, `CHI_TIET_PHIEU_NHAP`, `THE_KHO_LICH_SU`).
- **Tài liệu báo cáo:** [BaoCao_POS_Co_MucLuc_Trai](https://docs.google.com/document/d/1gmIpKHZxjDnauMInnZMXxwQC-lt9RPT1INnMHiATNWs/edit?usp=drivesdk)

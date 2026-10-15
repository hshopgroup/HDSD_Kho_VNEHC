# HƯỚNG DẪN SỬ DỤNG HỆ THỐNG QUẢN LÝ SẢN XUẤT & ĐỊNH MỨC BOM (HSHOP)

> **Phiên bản tài liệu:** 2.0  
> **Cập nhật ngày:** 14/10/2026  
> **Áp dụng cho:** Toàn thể Cán bộ - Nhân viên và Quản trị viên hệ thống Sản xuất & Kho.

---

## 📑 MỤC LỤC NHANH

## 📑 MỤC LỤC NHANH

1. [1. Tổng quan Hệ thống & Đăng nhập](#1-tổng-quan-hệ-thống--đăng-nhập)
2. [2. Dashboard (Bảng Thống kê & Giám sát)](#2-dashboard-bảng-thống-kê--giám-sát)
3. [3. Quản lý Thành phẩm (Finished Products)](#3-quản-lý-thành-phẩm-finished-products)
4. [4. Quản lý Nguyên vật liệu (Materials)](#4-quản-lý-nguyên-vật-liệu-materials)
5. [5. Danh mục Loại sản phẩm (Categories)](#5-danh-mục-loại-sản-phẩm-categories)
6. [6. Danh mục Nhà cung cấp (Suppliers)](#6-danh-mục-nhà-cung-cấp-suppliers)
7. [7. Quản lý Đặt hàng Nhà cung cấp (Purchase Orders - PO)](#7-quản-lý-đặt-hàng-nhà-cung-cấp-purchase-orders---po)
8. [8. Nhập kho (Goods Import - PN)](#8-nhập-kho-goods-import---pn)
9. [9. Xuất kho (Goods Export - PX)](#9-xuất-kho-goods-export---px)
10. [10. Quản lý Xuất Nhập hàng Hợp nhất (Kho Logs)](#10-quản-lý-xuất-nhập-hàng-hợp-nhất-kho-logs)
11. [11. Định mức BOM (Bill of Materials)](#11-định-mức-bom-bill-of-materials)
12. [12. Lệnh sản xuất (Work Orders)](#12-lệnh-sản-xuất-work-orders)
13. [13. Quản lý Hàng đang xử lý (Processing / Bảo hành)](#13-quản-lý-hàng-đang-xử-lý-processing--bảo-hành)
14. [14. Lịch sử Biến động Tồn kho & Audit Log](#14-lịch-sử-biến-động-tồn-kho--audit-log)
15. [15. Quản lý Tài khoản & Ma trận Phân quyền](#15-quản-lý-tài-khoản--ma-trận-phân-quyền)
16. [16. Nhật ký Hoạt động Hệ thống (Activity Log)](#16-nhật-ký-hoạt-động-hệ-thống-activity-log)
17. [17. Quản trị Hệ thống, Sao lưu & Cấu hình Link HDSD](#17-quản-trị-hệ-thống-sao-lưu--cấu-hình-link-hdsd)
18. [18. Quy định Phím tắt & Trải nghiệm Nhanh](#18-quy-định-phím-tắt--trải-nghiệm-nhanh)

---

## 1. TỔNG QUAN HỆ THỐNG & ĐĂNG NHẬP

### 1.1. Mục đích
Hệ thống **Quản lý Sản xuất & Định mức BOM** được xây dựng nhằm chuẩn hóa toàn bộ quy trình:
- Định mức nguyên vật liệu (BOM) và giá vốn sản phẩm nhiều tầng (Giá nhập 1: linh kiện, Giá nhập 2: hoàn thiện/đóng gói).
- Kiểm soát tiến độ đặt hàng nhà cung cấp (PO), tự động theo dõi số lượng đã giao và bình luận trao đổi thời gian thực.
- Xuất nhập kho chính xác, tích hợp cơ chế tự động xuất sản phẩm kèm theo (bundle items).
- Chạy lệnh sản xuất tự động trừ kho linh kiện và cộng tồn kho thành phẩm.
- Quản lý hàng bảo hành, sửa chữa, tách phế phẩm hoặc trả về kho lành.
- Sao lưu tự động và phân quyền ma trận bảo mật đến từng chức năng của từng phân hệ.

### 1.2. Đăng nhập & Điều hướng
- **Đăng nhập:** Người dùng sử dụng tài khoản được cấp từ hệ thống website chính để đăng nhập.
- **Thanh menu trái (Sidebar):** Được chia thành 4 khối chức năng:
  - *Tổng quan:* Dashboard.
  - *Danh mục:* Thành phẩm, Nguyên vật liệu, Loại sản phẩm, Nhà cung cấp.
  - *Sản xuất & Kho:* Đặt hàng, Nhập hàng, Xuất hàng, Quản lý Xuất Nhập, Định mức BOM, Lệnh sản xuất, Hàng đang xử lý, Lịch sử giao dịch.
  - *Hệ thống:* Tài khoản & Phân quyền, Nhật ký hệ thống, Quản trị & Sao lưu.
- **Chế độ Giao diện:** Hỗ trợ chuyển đổi nhanh giao diện **Tối (Dark Mode)** và **Sáng (Light Mode)** ở chân menu.
- **Nút "Hướng dẫn" trên từng trang:** Tại mỗi màn hình, bên cạnh tiêu đề luôn có nút **`📖 Hướng dẫn ↗`**. Nhấn vào sẽ tự động mở tài liệu hướng dẫn chuyên biệt của phân hệ đó ở một tab mới.

---

## 2. DASHBOARD (BẢNG THỐNG KÊ & GIÁM SÁT)

### 2.1. Ý nghĩa & Vai trò
Màn hình trung tâm giúp Ban Giám đốc và Trưởng bộ phận nắm bắt tức thì nhịp độ vận hành của toàn bộ xưởng sản xuất và kho bãi mà không cần lục tìm từng báo cáo.

### 2.2. Các khối thông tin quan trọng
1. **Thống kê Tổng quan (Stat Cards):**
   - **Thành phẩm:** Tổng số mã sản phẩm thành phẩm đang quản lý. Bấm vào chuyển nhanh sang tab Thành phẩm.
   - **Nguyên vật liệu:** Tổng số linh kiện, phụ kiện, vật tư trong kho.
   - **Cảnh báo Sắp hết hàng:** Số mặt hàng có tồn kho nhỏ hơn hoặc bằng Tồn tối thiểu (`quantity <= minQuantity`). Bấm vào để lọc ngay danh sách cần nhập thêm.
   - **Đang xử lý / Bảo hành:** Số lượng mặt hàng đang nằm trong kho kỹ thuật chờ xử lý.
   - **Lệnh sản xuất:** Số lệnh sản xuất đang chạy hoặc hoàn tất.
   - **Đơn đặt hàng (PO):** Số đơn hàng mua linh kiện đang theo dõi với nhà cung cấp.
2. **Nhật ký Giao dịch gần nhất:** Bảng 10 biến động kho phát sinh mới nhất (Nhập, Xuất, Sản xuất...) kèm người thực hiện và liên kết xem phiếu gốc.

---

## 3. QUẢN LÝ THÀNH PHẨM (FINISHED PRODUCTS)

### 3.1. Ý nghĩa
Quản lý các mặt hàng sản phẩm hoàn thiện được lắp ráp từ linh kiện hoặc mua trọn gói để bán cho khách hàng.

### 3.2. Các tính năng chính
- **Thêm mới thành phẩm:** Nhấn nút `[+ Thêm thành phẩm]`, nhập SKU, Tên, Loại SP, Nhà cung cấp, ĐVT, Tồn tối thiểu, Giá nhập 1 (vốn gốc linh kiện) và Giá nhập 2 (vốn hoàn thiện).
- **Mã SKU kèm theo (Tự nhảy khi xuất kho):**
  - Nhập các mã SKU linh kiện/phụ kiện luôn đi kèm khi bán (Ví dụ: `DAY_NGUON, OC_VIT_M3, HOP_DONG_GOI`).
  - Hệ thống tự động kiểm tra tính hợp lệ và hiển thị thẻ xem trước (badge xanh cho Thành phẩm, tím cho NVL, đỏ nếu sai mã).
  - Ngoài bảng danh sách, sản phẩm kèm được thu gọn thành **1 biểu tượng nhỏ gọn tím** (`fa-boxes-packing`). Khi rê chuột vào biểu tượng, bảng nổi (Hover Popover) sẽ hiển thị chi tiết tên và mã của từng món kèm theo.
- **Tùy chỉnh Cột hiển thị (Column Reordering & Visibility):**
  - Nhấn nút `[Tùy chỉnh cột]` trên thanh công cụ.
  - Kéo thả hoặc dùng mũi tên ▲ / ▼ để đổi thứ tự cột theo ý muốn.
  - Bật/tắt ô checkbox để ẩn hoặc hiện các cột (Hình ảnh, Giá vốn, Đang XL, Tags, Ghi chú...).
  - Thiết lập được lưu vĩnh viễn trên trình duyệt của bạn (F5 không mất).
- **Sao chép tạo nhanh (`[📋 Sao chép]`):** Tự động nhân bản thông số sản phẩm sang mặt hàng mới với mã `SKU-COPY`, giữ nguyên cấu hình loại, NCC, giá vốn và đặt tồn kho ban đầu về 0.
- **Nhập & Xuất Excel:**
  - Nhập file Excel thông minh: Tự nhận diện mọi biến thể tiêu đề (Tên thành phẩm, SKU, ĐVT, Giá nhập 1, Loại...). Tự động tạo mới Loại SP hoặc NCC nếu chưa có trong dữ liệu.
  - Có modal xem trước phân loại rõ dòng `[+ Mới]` và dòng `[Sửa]`.
  - Xuất Excel: Hỗ trợ Xuất tất cả, Xuất kết quả lọc, Xuất các mục đã chọn.
- **Xem Lịch sử (`🕒`):** Bấm vào icon đồng hồ để mở modal xem hai tab: *Biến động kho* và *Nhật ký chỉnh sửa* giá/thông tin với phân trang 20, 50, 100 dòng.

---

## 4. QUẢN LÝ NGUYÊN VẬT LIỆU (MATERIALS)

### 4.1. Ý nghĩa
Quản lý chi tiết toàn bộ danh mục linh kiện rời, bo mạch, phụ kiện ốc vít, bao bì dùng để cấu thành nên thành phẩm thông qua công thức BOM.

### 4.2. Các tính năng chính
- **Quản lý Tồn kho Tối thiểu:** Cài đặt ngưỡng `Tồn tối thiểu` cho từng linh kiện. Khi tồn kho thực tế chạm hoặc dưới ngưỡng này, hệ thống sẽ tự động đổi màu cảnh báo đỏ và gom vào danh sách cảnh báo trên Dashboard.
- **Bảo mật Giá vốn (`sanXuat_viewCost`):** Nhân viên không được phân quyền xem giá vốn sẽ hoàn toàn bị ẩn hai cột Giá nhập 1 và Giá nhập 2, đảm bảo bí mật chi phí kinh doanh.
- **Tùy chỉnh Cột NVL:** Tương tự như bảng Thành phẩm, bảng NVL hỗ trợ tùy chỉnh thứ tự cột và ẩn/hiện cột linh hoạt.
- **Lịch sử biến động giá:** Mọi thao tác sửa giá thủ công hoặc cập nhật giá khi nhập kho đều được tự động lưu vết chính xác kèm tên người sửa và thời gian.

---

## 5. DANH MỤC LOẠI SẢN PHẨM (CATEGORIES)

### 5.1. Ý nghĩa
Dùng để phân loại nhóm mặt hàng (ví dụ: *Module Cảm biến, Mạch điều khiển, Nguồn & Pin, Dụng cụ đóng gói...*) giúp việc tìm kiếm, lọc dữ liệu và xuất báo cáo được khoa học.

### 5.2. Hướng dẫn thao tác
- **Tạo loại mới:** Nhấn `[+ Thêm loại]`, nhập tên danh mục và mô tả.
- **Sử dụng:** Danh mục này được dùng chung cho cả Thành phẩm và Nguyên vật liệu.
- **Xóa loại:** Chỉ cho phép xóa khi danh mục không còn chứa bất kỳ mặt hàng nào bên trong để bảo đảm tính toàn vẹn dữ liệu.

---

## 6. DANH MỤC NHÀ CUNG CẤP (SUPPLIERS)

### 6.1. Ý nghĩa
Lưu trữ hồ sơ các đối tác sản xuất, đại lý linh kiện và xưởng gia công cung cấp hàng hóa cho doanh nghiệp.

### 6.2. Các trường thông tin
- Tên nhà cung cấp / Công ty đối tác.
- Số điện thoại liên hệ, Email, Địa chỉ kho hàng.
- Người phụ trách kinh doanh.
- Ghi chú điều khoản bảo hành, công nợ hoặc thời gian giao hàng định kỳ.

---

## 7. QUẢN LÝ ĐẶT HÀNG NHÀ CUNG CẤP (PURCHASE ORDERS - PO)

### 7.1. Ý nghĩa
Kiểm soát chặt chẽ toàn bộ chu trình mua sắm vật tư: Từ khâu lên kế hoạch đặt hàng, theo dõi nhà cung cấp xác nhận, đến lúc hàng về kho từng phần hoặc đủ số lượng.

### 7.2. Chu trình trạng thái Đơn hàng PO
```
[BẢN NHÁP] ➔ [ĐANG ĐẶT] ➔ [ĐANG GIAO] ➔ [NHẬN 1 PHẦN] ➔ [HOÀN TẤT] (hoặc [ĐÃ HỦY])
```

### 7.3. Các tính năng nổi bật
1. **Tạo đơn PO mới (`[+ Tạo đơn đặt hàng]`):**
   - Chọn Nhà cung cấp.
   - Thêm các mặt hàng linh kiện cần mua, số lượng dự kiến và đơn giá thỏa thuận.
   - Hệ thống tự động tính thành tiền tổng cộng của đơn hàng.
2. **Bình luận & Trao đổi Thời gian thực (Live Comments):**
   - Từng đơn PO có khung trao đổi nội bộ riêng biệt.
   - Nhân viên thu mua và thủ kho có thể nhắn tin trao đổi về tình trạng giao hàng, đính kèm ghi chú.
   - Huy hiệu đỏ trên menu Đặt hàng tự động báo số lượng bình luận mới chưa đọc.
3. **Chuyển đổi thành Phiếu Nhập kho (PO ➔ PN):**
   - Khi hàng về đến cửa kho, nhân viên chỉ cần nhấn **`[📥 Nhập kho]`** ngay tại dòng PO.
   - Hệ thống tự động chuyển toàn bộ danh sách mặt hàng và số lượng còn thiếu sang giao diện Nhập kho mà không cần gõ lại thủ công.

---

## 8. NHẬP KHO (GOODS IMPORT - PN)

### 8.1. Ý nghĩa
Tạo phiếu nhập kho chính thức (`PN-xxxxxx`), tự động cộng số dư tồn kho tức thời và cập nhật giá vốn mặt hàng vào cơ sở dữ liệu.

### 8.2. Hướng dẫn lập phiếu nhập kho
1. Vào tab **Nhập kho**.
2. **Tìm kiếm mặt hàng:** Gõ tên hoặc mã SKU tại ô tìm kiếm, chọn mặt hàng từ menu gợi ý thông minh.
3. **Nhập thông số:**
   - Số lượng nhập thực tế.
   - Giá nhập 1 và Giá nhập 2 (nếu có biến động giá so với trước).
4. **Nhập ghi chú:** Điền lý do nhập (ví dụ: *Nhập theo PO-1234, Nhập bổ sung vật tư đại lý A...*).
5. **Xác nhận Nhập kho:**
   - Nhấn **`[Xác nhận Nhập kho]`**.
   - Tồn kho của từng mặt hàng được cộng thêm ngay lập tức.
   - Lịch sử biến động giá được tự động ghi vào `AuditLog`.
   - Một phiếu nhập kho `PN-xxxxxx` được khởi tạo và lưu vào lịch sử.

---

## 9. XUẤT KHO (GOODS EXPORT - PX)

### 9.1. Ý nghĩa
Tạo phiếu xuất kho chính thức (`PX-xxxxxx`), trừ số dư tồn kho, áp dụng cho các mục đích: Xuất bán hàng, Xuất linh kiện gia công sản xuất, Xuất điều chuyển hoặc Xuất hủy.

### 9.2. Cơ chế Tự Động Nhảy Mặt Hàng Kèm Theo (Bundle Auto-add)
- Khi bạn chọn xuất 1 Thành phẩm có cấu hình sản phẩm kèm theo (ví dụ: *Bo mạch ESP32 kèm theo Cáp nạp và Túi chống ẩm*):
  - Hệ thống sẽ **tự động chèn thêm các mặt hàng kèm theo vào bảng xuất** với số lượng tương ứng.
  - Mặt hàng kèm theo được gắn huy hiệu tím rõ ràng: `(Kèm theo: [Mã SKU chính])`.
  - Thông báo Toast hiển thị chi tiết số món phụ đã được đưa vào phiếu xuất.
  - Người dùng vẫn có thể điều chỉnh số lượng hoặc xóa bỏ mặt hàng kèm nếu đơn hàng này không yêu cầu.

### 9.3. Cảnh báo an toàn kho
- Nếu số lượng xuất vượt quá tồn kho khả dụng hiện có, hệ thống sẽ đổi màu đỏ cảnh báo và yêu cầu xác nhận trước khi trừ kho để ngăn ngừa âm kho ngoài ý muốn.

---

## 10. QUẢN LÝ XUẤT NHẬP HÀNG HỢP NHẤT (KHO LOGS)

### 10.1. Ý nghĩa
Nơi hợp nhất toàn bộ lịch sử các phiếu Nhập kho (`PN`) và phiếu Xuất kho (`PX`) trên cùng một màn hình tập trung.

### 10.2. Các bộ lọc thông minh
- **Tab chuyển đổi nhanh:**
  - `Tất cả`: Xem toàn bộ lịch sử xuất và nhập.
  - `📥 Nhập kho`: Chỉ lọc các phiếu nhập PN.
  - `📤 Xuất kho`: Chỉ lọc các phiếu xuất PX.
- **Tìm kiếm đa năng:** Tìm nhanh theo mã phiếu (`PN-xxxx`, `PX-xxxx`), tên nhân viên tạo, mã SKU mặt hàng hoặc ghi chú.
- **Xem chi tiết phiếu:** Nhấn vào mã phiếu bất kỳ để mở popup hiển thị trọn vẹn danh sách mặt hàng, số lượng và tổng giá trị của phiếu đó.
- **Xuất Excel:** Hỗ trợ trích xuất toàn bộ bảng lịch sử ra file Excel báo cáo.

---

## 11. ĐỊNH MỨC BOM (BILL OF MATERIALS)

### 11.1. Ý nghĩa
BOM là **"Trái tim của hệ thống sản xuất"**. Đây là công thức cấu thành quy định rõ: *Để chế tạo 1 đơn vị Thành phẩm X thì cần chính xác bao nhiêu đơn vị Linh kiện A, B, C...*

### 11.2. Hướng dẫn thiết lập Định mức BOM
1. Vào tab **Định mức BOM**, nhấn `[+ Tạo định mức BOM mới]`.
2. Chọn Thành phẩm đích cần lập công thức.
3. Thêm từng thành phần nguyên vật liệu cấu thành:
   - Chọn linh kiện từ danh mục.
   - Nhập định mức tiêu hao (ví dụ: *01 Thân máy cần 04 Ốc vít M3, 01 Bo mạch chính, 0.5m Dây điện*).
4. Hệ thống tự động nhân định mức với giá vốn linh kiện để đưa ra **Tổng giá vốn dự toán** của thành phẩm.
5. Nhấn `[Lưu định mức]`. Định mức này sẽ là cơ sở cho Phân hệ Lệnh sản xuất hoạt động.

---

## 12. LỆNH SẢN XUẤT (WORK ORDERS)

### 12.1. Ý nghĩa
Tổ chức và điều hành quy trình sản xuất thực tế tại xưởng dựa trên công thức định mức BOM đã duyệt.

### 12.2. Quy trình Chạy Lệnh Sản Xuất
1. Nhấn `[+ Tạo lệnh sản xuất mới]`.
2. Chọn Thành phẩm cần chế tạo và nhập **Số lượng muốn sản xuất** (ví dụ: 50 bộ).
3. Hệ thống tự động tính toán tổng số lượng từng loại nguyên vật liệu cần tiêu thụ.
4. **Kiểm tra Tồn kho Vật tư:**
   - Nếu kho đủ linh kiện: Nút `[Chạy sản xuất]` sáng xanh.
   - Nếu thiếu linh kiện: Hệ thống báo đỏ chính xác món hàng đang thiếu và số lượng thiếu hụt để thủ kho kịp đặt hàng PO.
5. **Thực thi:**
   - Khi hoàn tất, hệ thống tự động:
     - **Trừ kho** toàn bộ linh kiện đã dùng theo định mức.
     - **Cộng tồn kho** thành phẩm hoàn thiện.
     - Ghi nhận giao dịch sản xuất vào sổ cái lịch sử biến động kho.

---

## 13. QUẢN LÝ HÀNG ĐANG XỬ LÝ (PROCESSING / BẢO HÀNH)

### 13.1. Ý nghĩa
Cách ly các mặt hàng lỗi kỹ thuật, hàng khách gửi bảo hành, hoặc hàng bể vỡ chờ kiểm định ra khỏi tồn kho bán hàng thông thường, tránh việc nhân viên xuất nhầm hàng lỗi cho khách.

### 13.2. Quy trình xử lý 3 bước
1. **Nhập vào Xử lý:**
   - Chọn mặt hàng, số lượng và lý do (Bảo hành khách, Lỗi nhà sản xuất, Rơi vỡ...).
   - Hàng được trừ khỏi kho chính và chuyển vào số dư "Đang xử lý".
2. **Sửa chữa / Thao tác kỹ thuật:** Bộ phận kỹ thuật kiểm tra và tiến hành khắc phục.
3. **Kết thúc Xử lý (2 hướng ra):**
   - **Trả lại kho lành (`Xuất trả kho`):** Hàng sau khi sửa xong đạt chuẩn sẽ được cộng lại vào tồn kho khả dụng để tiếp tục bán hàng.
   - **Hủy phế phẩm (`Hủy hàng`):** Hàng hỏng hoàn toàn không thể cứu vãn sẽ được xuất hủy vĩnh viễn kèm biên bản ghi nhận tổn thất.

---

## 14. LỊCH SỬ BIẾN ĐỘNG TỒN KHO & AUDIT LOG

### 14.1. Ý nghĩa
Sổ cái điện tử bất biến ghi nhận từng lần tăng/giảm tồn kho của từng món hàng trong hệ thống. Đảm bảo tính minh bạch, hỗ trợ đối soát kho và kiểm toán nội bộ bất kỳ thời điểm nào.

### 14.2. Cấu trúc bảng giao dịch
- **Loại GD:** Nhập kho (Xanh lá), Xuất kho (Đỏ), Sản xuất (Tím)...
- **Đối tượng:** Tên mặt hàng và mã SKU. Đã được tối ưu tự động ngắt dòng xuống hàng chuẩn đẹp, không bao giờ tràn đè chữ.
- **S.Lượng biến động:** Số lượng tăng (+) hoặc giảm (-).
- **Tồn kho sau GD:** Số lượng tồn kho thực tế ngay sau khi giao dịch hoàn tất.
- **Thời gian:** Ngày giờ phát sinh giao dịch đến từng giây.
- **Chi tiết / Ghi chú:** Mã phiếu kèm theo (`PN-xxxx`, `PX-xxxx`). Bấm vào mã phiếu để xem trực tiếp chi tiết phiếu.

### 14.3. Phân trang
- Hỗ trợ xem phân trang linh hoạt: `20`, `50`, hoặc `100` giao dịch trên một trang.

---

## 15. QUẢN LÝ TÀI KHOẢN & MA TRẬN PHÂN QUYỀN

### 15.1. Ý nghĩa
Bảo mật hệ thống thông tin, đảm bảo mỗi nhân viên chỉ được phép xem và thao tác trên đúng phân hệ và quyền hạn được phân công.

### 15.2. Các cấp độ quyền hạn
- **Quản trị viên (ADMIN):** Toàn quyền kiểm soát toàn bộ 16 phân hệ, cấu hình hệ thống, quản lý tài khoản và phân quyền, cấu hình link hướng dẫn, khôi phục dữ liệu.
- **Nhân viên (STAFF):** Phân quyền chi tiết theo ma trận:
  - `Xem (View)`
  - `Tạo mới (Create)`
  - `Chỉnh sửa (Edit)`
  - `Xóa (Delete)`
  - `Xuất/Nhập Excel`
  - `Xem Giá vốn (sanXuat_viewCost)`: Quyết định quyền được xem hay bị ẩn 2 cột giá nhập.

### 15.3. Đồng bộ Tài khoản
- Hệ thống hỗ trợ nút **`[Đồng bộ từ Website]`** để nạp danh sách tài khoản từ cơ sở dữ liệu chính của doanh nghiệp mà không cần tạo lại thủ công.

---

## 16. NHẬT KÝ HOẠT ĐỘNG HỆ THỐNG (ACTIVITY LOG)

### 16.1. Ý nghĩa
Lưu lại toàn bộ nhật ký thao tác người dùng (Ai đã thêm sản phẩm gì? Ai đã sửa giá lúc mấy giờ? Ai đã xóa đơn hàng? Từ địa chỉ IP nào?).

### 16.2. Các tính năng
- Tra cứu nhanh theo từ khóa người dùng hoặc hành động.
- Lọc theo từng phân hệ.
- Phân trang `20`, `50`, `100` dòng/trang.
- Xuất file Excel báo cáo nhật ký kiểm toán.

---

## 17. QUẢN TRỊ HỆ THỐNG, SAO LƯU & CẤU HÌNH LINK HDSD

### 17.1. Sao lưu Dữ liệu (Backup)
- **Tải file Sao lưu JSON (.json):** Xuất toàn vẹn 100% toàn bộ cơ sở dữ liệu hệ thống (24 bảng dữ liệu) về máy tính, bao gồm:
  - Danh mục & Sản phẩm: Thành phẩm, Nguyên vật liệu, Loại sản phẩm, Nhà cung cấp, cấu hình Mã SKU kèm theo (`bundleItems`).
  - Định mức & Sản xuất: Công thức BOM, Chi tiết BOM, Lệnh sản xuất, Chi tiết vật tư sản xuất.
  - Mua hàng (PO): Đơn đặt hàng PO, Chi tiết đặt hàng, Bình luận trao đổi nội bộ trên từng PO, Trạng thái đã đọc bình luận.
  - Kho vận & Giao dịch: Phiếu nhập hàng (PN), Phiếu xuất hàng (PX), Lịch sử biến động tồn kho (Transactions).
  - Kỹ thuật & Bảo hành: Hàng đang xử lý/sửa chữa (Processing), Mã phiếu gốc (`parentCode`), Số lượng ban đầu (`initialQuantity`), Toàn bộ nhật ký thao tác sửa chữa/hoàn trả/xuất phế phẩm (ProcessingItemLogs), Danh mục lý do xử lý.
  - Giám sát & Quản trị: Nhật ký chỉnh sửa giá/thông tin (AuditLog), Nhật ký hoạt động hệ thống (ActivityLog), Cấu hình Link hướng dẫn sử dụng (GuideLink) và Ma trận phân quyền người dùng.
- **Khuyến nghị:** Thực hiện sao lưu định kỳ hàng tuần hoặc trước mỗi đợt bảo trì, nâng cấp dữ liệu lớn.

### 17.2. Khôi phục Dữ liệu (Restore)
- Chọn file `.json` đã sao lưu trước đó để nạp lại toàn bộ dữ liệu khi chuyển máy chủ hoặc phục hồi sau sự cố.
- **Độ tin cậy & An toàn tuyệt đối:**
  - Tự động xóa và tái tạo lại toàn bộ 24 bảng dữ liệu theo đúng thứ tự ràng buộc khóa ngoại (Foreign Keys).
  - Khôi phục chính xác từng trường dữ liệu chuyên sâu (Mã SKU kèm theo, Mã phiếu gốc, Số lượng ban đầu, Lịch sử trao đổi PO, v.v.).
  - **Bảo toàn tài khoản nhân viên 100%:** Toàn bộ tài khoản và mật khẩu đăng nhập của nhân viên từ website chính luôn được giữ nguyên vẹn, không bao giờ bị gián đoạn quyền truy cập.

### 17.3. Cấu hình Link Hướng dẫn Sử dụng từng Danh mục (Chỉ Admin)
- **Truy cập:**
  - Nhấn nút **`📖 Quản lý Link HDSD`** ở thanh menu trái.
  - Hoặc nhấn nút **`[Cấu hình Link HDSD]`** tại thẻ chức năng trong tab Hệ thống.
  - Hoặc nhấn icon bánh răng `⚙️` cạnh nút Hướng dẫn ở mỗi phân hệ.
- **Thao tác:**
  - Nhập đường dẫn tài liệu tương ứng cho từng danh mục (Ví dụ: Link Google Docs, video YouTube, Notion, Google Drive...).
  - Bấm icon **`↗` (Mở thử)** để kiểm tra liên kết có hoạt động chuẩn xác ở tab mới không.
  - Bấm **`[Lưu tất cả cấu hình]`**. Ngay lập tức toàn bộ nhân viên khi bấm nút "Hướng dẫn" ở mỗi phân hệ sẽ được mở thẳng đến tài liệu này.

### 17.4. Khôi phục Cài đặt gốc (Factory Reset)
- Nằm trong **Vùng nguy hiểm**.
- Xóa sạch dữ liệu sản xuất thử nghiệm để chuẩn bị đưa vào vận hành thực tế.
- Được bảo vệ bằng 2 tầng hộp thoại cảnh báo xác nhận. Toàn bộ tài khoản người dùng vẫn được bảo toàn nguyên vẹn.

---

## 18. QUY ĐỊNH PHÍM TẮT & TRẢI NGHIỆM NHANH

| Phím tắt | Chức năng | Áp dụng tại |
|---|---|---|
| `Esc` | Đóng ngay cửa sổ Modal hoặc bảng nổi đang mở | Toàn bộ ứng dụng |
| `Ctrl + F5` | Làm mới giao diện và xóa bộ nhớ đệm trình duyệt | Trình duyệt Web |
| `Click chuột ngoài` | Đóng các menu thả xuống và gợi ý tìm kiếm | Thanh công cụ |
| `Enter` | Xác nhận tìm kiếm hoặc lưu nhanh trên một số form | Các ô nhập liệu |

---

> 💡 **Mẹo:** Quản trị viên (Admin) có thể tải file này lên **Google Drive / Google Docs / Notion**, sau đó copy đường dẫn của từng phần để dán vào giao diện **Cấu hình Link HDSD** trong hệ thống. Nhân viên chỉ cần nhấp chuột vào nút `📖 Hướng dẫn` là sẽ mở ngay tài liệu hướng dẫn tương ứng!

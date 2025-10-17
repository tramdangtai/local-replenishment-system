# 📊 Local Replenishment System – Data-Driven Purchasing Optimization

> _“Từ cảm tính sang dữ liệu – từ phản ứng sang chủ động.”_  
> Đây là một trong những dự án mà tôi tâm đắc nhất, vì nó không chỉ giải quyết vấn đề kỹ thuật mà còn thay đổi cả **tư duy vận hành của phòng Merchandise** trong việc ra quyết định mua hàng.

---

## 📘 Giới thiệu
Trước đây, việc mua hàng nội địa được thực hiện dựa vào **kinh nghiệm cá nhân của Buyer**, thường theo nguyên tắc đơn giản:  
> “Bán được 10 thì mua lại 10.”  

Cách làm này tuy hiệu quả với ít cửa hàng, nhưng khi hệ thống mở rộng, nó bộc lộ hai vấn đề lớn:

1. **Thiếu hàng cho SKU bán chạy**, khiến cơ hội bán bị bỏ lỡ.  
2. **Tồn kho cao cho SKU bán chậm**, gây ra vốn bị “kẹt” trong tồn kho.  

Thêm vào đó, việc ra quyết định mua hàng hoàn toàn **không có dữ liệu chứng minh**. Quản lý phòng Merchandise không thể kiểm chứng được **Purchase Order** được tạo ra dựa trên cơ sở nào, và liệu quyết định đó có thực sự hợp lý hay không.

---

## 🎯 Mục tiêu dự án
- Xây dựng một **bộ công cụ Local Replenishment** giúp tất cả Buyer ra quyết định dựa trên **dữ liệu thống nhất và được cập nhật hằng ngày**.  
- Cung cấp **toàn bộ thông tin quan trọng** để Buyer ra quyết định mua hàng:
  - Lịch sử bán hàng có thể lọc theo thời gian  
  - Thông tin vendor, ngành hàng, cửa hàng  
  - Giá cost, tồn kho hiện tại, tồn kho lý tưởng (Ideal Stock)  
  - Các chỉ số bổ trợ: frequency, suggest order qty...

---

## 🧩 Giải pháp thực hiện
1. **Xây dựng hệ thống lưu trữ dữ liệu chuẩn**  
   - Thiết lập cấu trúc folder và file đồng nhất để đảm bảo dữ liệu có thể được cập nhật tự động.  
   - Chuẩn hóa quy trình đặt tên, liên kết và cập nhật dữ liệu.

2. **Tổng hợp & xử lý dữ liệu bằng Power Query**  
   - Kết nối và làm sạch dữ liệu từ nhiều nguồn: Sales, Inventory, Vendor Info, Ideal Stock, Cost Price.  
   - Chuẩn hóa định dạng và xử lý các vấn đề về thiếu dữ liệu hoặc sai lệch thông tin.  

3. **Xây dựng Data Model bằng Power Pivot**  
   - Tạo mối quan hệ giữa các bảng để phản ánh đúng logic kinh doanh.  
   - Tính toán các chỉ số như Frequency, Suggested Order Quantity... bằng DAX.  

4. **Thiết kế giao diện báo cáo trực quan, thân thiện**  
   - Cho phép Buyer lọc theo thời gian, vendor, ngành hàng, hoặc từng cửa hàng.  
   - Thảo luận cùng team để đảm bảo report phù hợp và dễ hiểu cho mọi thành viên.  

---

## 📊 Kết quả đạt được
- **Mỗi Purchase Order đều có căn cứ dữ liệu rõ ràng**, giúp quản lý dễ dàng phê duyệt và theo dõi.  
- **Toàn bộ phòng Merchandise làm việc trên cùng một nguồn dữ liệu**, đảm bảo tính thống nhất và minh bạch.  
- **Tăng tốc độ ra quyết định** và giảm rủi ro mua hàng sai SKU, sai lượng.  
- **Khả năng mở rộng cao:** Khi mở thêm cửa hàng, hệ thống vẫn hoạt động ổn định mà không cần chỉnh sửa cấu trúc báo cáo.  

---

## 🛠️ Công cụ & Kỹ thuật sử dụng
| Công cụ / Kỹ thuật | Mục đích sử dụng |
|--------------------|----------------|
| **Excel Power Query** | Tổng hợp và làm sạch dữ liệu từ nhiều nguồn |
| **Power Pivot (Data Model)** | Tạo mối quan hệ giữa các bảng dữ liệu |
| **DAX** | Tính toán các chỉ số kinh doanh và chỉ báo hỗ trợ ra quyết định |
| **Pivot Table / Chart** | Trực quan hóa kết quả và phân tích nhanh |
| **Folder Structure Optimization** | Quản lý và mở rộng quy trình dữ liệu dễ dàng |

---

## 📸 Kết quả

<p align="center">
  <img src="./Image/StockReplenishment.PNG" alt="Preview thư mục kết quả" width="650">
</p>


---

## ✉️ Tác giả
**Tram Dang Tai**  
📍 Merchandise Assistant Database  
📧 [Liên hệ qua LinkedIn](https://www.linkedin.com/in/tramdangtai)

# BÀI LÀM PHA 1 – HACKATHON 02

- **Mã đề:** 05
- **Họ tên:**Cao Trần Tuấn Kiệt
- **Lớp:**CNTT1
- **Link repository Pha1:**

> Pha 1 (70 phút đầu, KHÔNG dùng AI). Viết xong, kéo thả file này vào repository Pha1 trước mốc giờ giám thị công bố.

## 4.1. Bảo vệ dữ liệu và chống ảo giác

### a) Ghi chú đã ẩn danh hoá

**GHI CHU DA AN DANH**

```text
Khách hàng[KHACHHANG], số điện thoại[SDT], số cccd[CCCD], email[EMAIL], đặt 2 vé người lớn và 1 vé trẻ em phòng chiếu Gold Class (mã GOLD) ngày 21/12/2026. Khách đã chuyển khoản trước 300.000 đồng. Khách yêu cầu ghế hàng giữa.


### b) Hai câu lệnh chống ảo giác

**CAU LENH**

```text
- không tự bịa giá vé, lịch chiếu hoặc thông tin phim
- CHỉ sử dụng thông tin đã cung cấp trực tiếp
```

## 4.2. Trích xuất tin nhắn đặt vé xem phim ra JSON

**PROMPT**

```text
(Viết prompt vào đây – xoá dòng này)
```

## 4.3. Báo giá bằng Chain-of-Thought

### a) Prompt

**PROMPT**

```text
[bối cảnh]
bạn đang làm nhân viên tại rap phim, có nhiệm vụ tư vấn và tính giá vé
[vai trò]
bạn là nhân viên tư vấn bán vé chuyên nghiệp, thân thiện, có khả năng tính toán chính xác
[nhiệm vụ cụ thể]
tiếp nhận thông tin khách hàng,xác định loại vé,số lượng người 
[hành động]
BẢNG GIÁ VÉ (đồng/vé người lớn)
P2D – Phim 2D: 90.000
P3D – Phim 3D: 130.000
GOLD – Phòng chiếu Gold Class: 250.000
1. Trẻ em cao từ 1 m đến 1,3 m tính 70% giá vé người lớn. Trẻ dưới 1 m ngồi cùng người lớn miễn phí.
2. Nhóm từ 5 người lớn trở lên được giảm 10% trên tiền vé (tiền vé người lớn + tiền vé trẻ em).
3. Phụ thu combo bắp nước: 75.000 đồng/combo. Combo không được giảm giá.
4. Tổng tiền = tiền vé sau giảm + tiền combo.
[giọng điệu]
thân thiện,lịch sự,dễ hiểu,chuyên nghiệp và rõ ràng
[đầu ra]
loại vé và số lượng
tiền vé người lớn
tiền vé trẻ em 
tiền combo
tổng tiền thanh toán


```

## 4.4. Dây chuyền xử lý khiếu nại (Prompt Chaining)

### a) Prompt Trạm 1

**PROMPT**

```text
[bối cảnh]
rạp phim ánh dương tiếp nhận khiếu nai từ khách hàng về giá vé, đặt vé, thanh toán, hủy dịch vụ
[vai trò]
bạn là nhân viên tiếp nhận và phân tích khiếu nại
[nhiệm vụ]
đọc nội dung khiếu nại, xác định vấn đề và phân loại khiếu nại của khách hàng
[hành động]
- Trích xuất tên vấn đề, nội dung khiếu nại và yêu cầu của khách
- Ẩn danh thông tin cá nhân
- Không tự suy đoán hoặc bịa thông tin
[giọng điệu]
chính xác, khách quan, chuyên nghiệp
[đầu ra]


```

### b) Hai điều cần kiểm tra ở JSON đầu ra của Trạm 1

1. (Viết câu trả lời vào đây – xoá dòng này)

2.

### c) Câu lệnh viết tiếp

**CAU LENH**

```text
(Viết câu lệnh vào đây – xoá dòng này)
```

## 4.5. Prompt chấm bài theo Rubric

**PROMPT**

[bối cảnh]
bạn đang hỗ trợ rạp phim ánh dương đá giá chất lượng phản hồi của nhân viên
[nhiệm vụ]


## 4.6. Hoàn thiện System Prompt

> Phần Vai trò và Chuẩn đầu ra đã cho sẵn. Viết tiếp phần Quy tắc ràng buộc và Xử lý ngoại lệ.

```text
[Vai trò]
Bạn là "Trợ lý Ánh Dương", nhân viên tư vấn trên website của Rạp phim Ánh Dương, giúp khách chọn và đặt một trong 3 loại vé: P2D (Phim 2D), P3D (Phim 3D), GOLD (Phòng chiếu Gold Class).

[Quy tắc ràng buộc]
1. (Viết quy tắc 1 – xoá dòng này)
2.
3.

[Chuẩn đầu ra]
Trả lời bằng tiếng Việt, lịch sự, tối đa 120 từ. Giá vé trình bày dạng gạch đầu dòng. Kết thúc bằng một câu hỏi về nhu cầu tiếp theo của khách.

[Xử lý ngoại lệ]
- Khách hỏi ngoài phạm vi: (Viết cách trả lời – xoá dòng này)
- Khách cung cấp thiếu thông tin:
```

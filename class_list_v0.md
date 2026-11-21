# Danh sách lớp v1 — Trịnh Vinh Khánh · G05

## DMS

| # | Lớp / thuộc tính | Giá trị | Mục đích | Nhìn được trên IR? |
|---|---|---|---|---|
| 1 | `eye_left`, `eye_right` | open / closed / unknown | Nhận biết tài xế buồn ngủ (mắt nhắm trong thời gian dài) | Có, trừ khi kính gây phản xạ |
| 2 | `gaze_zone` | road / mirror_* / cluster / center / lap / other | Cảnh báo khi tài xế không nhìn về phía đường | Có (qua hướng đầu và mắt) |
| 3 | `face13` | 13 điểm kèm cờ occluded / outside | Ước lượng hướng đầu và độ mở của mắt, miệng | Có; điểm bị che thì gắn cờ |
| 4 | `glasses` | unknown / none / clear / sun | Xác định lúc nào kết quả đọc mắt kém đáng tin | Một phần (kính râm có thể trông trong suốt) |
| 5 | `hand` → `on_wheel` | yes / no / unknown | Kiểm tra tay đã đặt trên vô lăng khi chuyển sang lái thủ công | Có |
| 6 | `phone` → `state` | held / mounted / lap | Cảnh báo khi dùng điện thoại trong lúc lái | Có, nếu nhìn thấy hình dạng máy |
| 7 | `seatbelt` (tài xế) | worn_correct / worn_incorrect / not_worn / unknown | Nhắc thắt dây và phát hiện trường hợp thắt sai cách | Một phần (dây có thể bị chìm trong bóng tối) |

## OMS

| # | Lớp / thuộc tính | Giá trị | Mục đích | Nhìn được trên IR? |
|---|---|---|---|---|
| 1 | `person` → `seat` | driver / front_passenger / rear_* | Đếm người theo từng ghế và nhắc dây an toàn đúng ghế | Có |
| 2 | `seatbelt` (hàng sau) | not_worn / unknown | Nhắc hành khách ngồi sau thắt dây | Một phần |
| 3 | `child_seat` → `occupied` | no / unknown | Tắt túi khí ghế trước và nhắc kiểm tra trẻ khi khóa xe | Có (qua hình dạng) |
| 4 | `infant_seat` → `facing` | rear / front | Ghế quay ngược đặt ở ghế trước thì phải tắt túi khí | Có (qua hình dạng) |
| 5 | `object` → `type` | bag / box / cup / other | Phân biệt đồ vật với người và nhắc khi quên đồ | Có (qua hình dạng, không dựa vào màu) |
| 6 | `face` (chỉ box) | box | Xác nhận đối tượng là người thật, không phải túi hay gối | Có |
| 7 | `frame_meta` → `camera_blocked` | yes / no | Báo khi camera bị che, thay vì kết luận nhầm là ghế trống | Có

## 2 câu hỏi leo thang

1. Câu hỏi: Với người đang đang thắt dây an toàn, nên đặt nhãn thế nào cho chính xác? 
   Khung ví dụ: ảnh D03
   Tạm gán: Unknow.
2. Câu hỏi: Ảnh NIR thật có ghi `light = night` được không, khi ảnh không cho biết giờ trong ngày?
   Khung ví dụ: G05 D01–D06 (bạn ghi `night`, mình ghi `unknown`).
   Tạm gán: `unknown`, theo 4.4-1 (không thấy thì unknown).

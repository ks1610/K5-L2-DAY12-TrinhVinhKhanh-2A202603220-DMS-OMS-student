# Tự đánh giá — Trịnh Vinh Khánh· G05

## 1. Tự rà soát 4 cảnh

Nghỉ tay 1 phút, mở lại bài của mình, chọn 4 ảnh (2 S##, 2 D##), đọc như người lạ.

Loại lỗi: `seat_flip`, `wrong_class`, `guess`, `box`, `missing`, `extra`, `lr_flip` (trái/phải mặt), `flag` (thiếu cờ điểm), `ok`.

| Ảnh | Đối tượng | Loại lỗi | Ghi chú | Đã sửa? |
|---|---|---|---|---|
| D02 | hand | wrong_class | Cả 2 nhãn hand đều mang thuộc tính hand | sửa lại thuộc tính right cho tay phải|
| D06| frame_meta | missing | Thiếu tag frame_meta | Thêm tag cho ảnh |
| S04_rgb | frame_meta | wrong_class | Đặt thuộc tính light là day | Sửa thuộc tính thành Unknow do ảnh là ảnh dựng|
| S01_rgb | child_seat | lr_flip | Vị trí đặt trong thuộc tính seat là rear_right | Sửa lại thành rear_left |


## 2. Lỗi mình lặp lại nhiều nhất hôm nay

Lỗi: Nhầm vị trí left/right của bàn tay, thiếu thuộc tính right cho tay.

Vì sao mình mắc: Quá trình gán, chưa kiểm tra kỹ thuộc tính của nhãn.

Lần sau tránh bằng cách: Đảm bảo hoàn thành các thuộc tính sau mỗi nhãn.

## 3. Ghi chú về disagreement_log

Các ảnh D04, D05, D06, bạn đã điền đầy đủ các thuộc tính cho hand nhưng tôi vẫn để mặc định unknow. Sau kiểm tra, tôi đã chỉnh sửa lại với ảnh bạn đã làm đúng. 

Sau qc cho bài làm của bạn, tôi nhận thấy mình cần cẩn thận hơn trong kiểm tra các thuộc tính, tôi cần hoàn thành các thuộc tinh sau khi gán xong một nhãn và trước khi gãn một nhãn mới.

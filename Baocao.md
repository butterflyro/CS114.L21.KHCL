# MÔ TẢ ĐỒ ÁN
# PHÁT HIỆN CÁC LOẠI PHƯƠNG TIỆN ĐANG THAM GIA GIAO THÔNG
## 1. Mô tả bài toán
Phát hiện phương tiện đang tham gia giao thông

* Bằng cách sử dụng hình ảnh từ camera lắp đặt trên cao ở các góc đường thuộc một khu vực cụ thể trong TPHCM, đồphát hiện và phân loại các phương tiện đang tham gia giao thông.
từ đó kiểm soát được mật độ người tham gia giao thông theo thời gian thực tại khu vực này, hỗ trợ việc kiểm soát các luồng giao thông để hạn chế tình trạng kẹt xe.
* **Input**: Ảnh chụp từ camera được đặt tại các vị trí cao trên những con đường thuộc một khu vực xác định
* **Output**: Phát hiện loại phương tiện có trong ảnh

## 2.Mô tả về bộ dữ liệu
Cách thức xây dựng bộ dữ liệu:
* Sử dụng hình ảnh thời gian thực lấy từ camera của sở giao thông vận tải TPHCM, ước tính với mỗi camera cứ 12s sẽ chụp ra một ảnh
![anh_minh_hoa](https://user-images.githubusercontent.com/80096230/120655439-e1676200-c4ac-11eb-905b-67d5562120e4.png)
(Nguồn: http://giaothong.hochiminhcity.gov.vn/map.aspx)

## 3.Mô tả về đặc trưng
Sử dụng thuật toán yolov4

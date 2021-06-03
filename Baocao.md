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
* Sử dụng labelMe để gán nhãn, bài toán gồm 5 class chính là: xe đạp, xe máy, xe oto, xe tải, xe buýt, xe khách.
* Bộ dữ liệu là hình ảnh giao thông tại các khu vực trong thành phố Hồ Chí Minh, được quay từ trên cao, số lượng ảnh được raw dự kiến tầm 1500 - 2000 ảnh.
## 3.Mô tả về đặc trưng
* Dữ liệu có góc quay, thời gian ban ngày, ban đêm, ánh sáng, mật độ giao thông đa dạng. 
* Ảnh được raw về có kích thước, độ phân giải, chất lượng ảnh không cố định đa dạng tùy vào camera mỗi địa điểm, đây cũng là một thách thức khi phải xử lý như nào để đảm bảo thông tin không bị mất mát nhiều.
* Tập dữ liệu được raw gồm các địa điểm như đường quốc lộ, đường nhỏ, ngã 3, ngã 4, đường một chiều, trên cầu vượt.
* Mật độ giao thông đa dạng.
## 4.Mô tả thuật toán
* Nhóm em chọn thuật toán YOLOv4 để làm phần phát hiện đối tượng vì có thời gian dự đoán nhanh độ chính xác cao. Và sẽ phân tích thêm về phần tiền xử lý những ảnh bị các thách thức như ban đêm, đèn pha của xe làm ảnh khó phát hiện, mật độ giao thông đông đúc, ảnh có độ phân giải thấp, thời tiết mưa để tìm ra phương pháp tiền xử lý hợp lý trước khi đưa vào thuật toán phát hiện đối tượng.
*![187529955_320378539584060_4500346516519094400_n](https://user-images.githubusercontent.com/64973267/120692734-5dc06c00-c4d2-11eb-8cf2-9e28bb5c327e.png)
![190801246_125812539562700_1721751272422692417_n](https://user-images.githubusercontent.com/64973267/120692742-6022c600-c4d2-11eb-9d52-860920e94389.png)
![a](https://user-images.githubusercontent.com/64973267/120692753-631db680-c4d2-11eb-8138-9185ca864bb6.png)
![aa](https://user-images.githubusercontent.com/64973267/120692759-64e77a00-c4d2-11eb-8bec-6238e3b4a7eb.png)

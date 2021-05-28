# MÔ TẢ ĐỒ ÁN
## 1. Mô tả bài toán
Phân loại vị kem theo ảnh.

* Đối với những nơi phân phối kem với giá sỉ, kem được đóng hộp lớn và đề nhãn, hương vị rõ ràng. 
Nhưng khi các nhà phân phối kem nhỏ lẻ nhập kem giá sỉ về, để tăng lợi nhuận và thuận tiện cho việc bán lẻ, 
họ thường chia kem trong hộp lớn vào từng hộp nhỏ hơn rồi đem bán ra thị trường. 
Điều này dẫn đến việc đề nhãn cho kem thường không được rõ ràng và hương vị của kem khó có thể nhận biết 
* **Input**: Ảnh kem bất kỳ 
* **Output**: Vị kem của ảnh

## 2.Mô tả về bộ dữ liệu
Cách thức xây dựng bộ dữ liệu:
* Raw dữ liệu trên mạng (Google, Insta)
Số lượng, độ da dạng:
* Gồm 8 lớp:
* Dừa: 668
* Bạc hà: 609
* Dâu: 711
* Chuối: 447
* Sầu riêng: 497
* Socola: 748
* Vanilla: 793
* Khoai môn: 709
Phân chia (split) - train/dev/test
* Train 80%
* Val 20%
* Test chưa tính

## 3.Mô tả về đặc trưng
Sử dụng CNN để tự động rút trích đặc trưng

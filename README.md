# Face Recognition Colab

## 1. Giới thiệu
Dự án này thực hiện nhận diện khuôn mặt bằng Google Colab.  
Hệ thống sử dụng dữ liệu ảnh khuôn mặt đã được chia theo từng người, sau đó huấn luyện mô hình học sâu để phân loại khuôn mặt trong ảnh.

Dự án chỉ chạy trên Google Colab, không xây dựng ứng dụng web hoặc app.

## 2. Nội dung project
Các file chính trong repository gồm:

- `Face_Recognition_Colab.ipynb`: notebook chính dùng để train và test mô hình.
- `requirements.txt`: danh sách thư viện cần sử dụng.
- `dataset_stats.json`: thống kê dữ liệu.
- `label_map.json`: ánh xạ nhãn/tên lớp.
- `README.md`: mô tả dự án.

## 3. Dữ liệu
Dữ liệu gồm các ảnh khuôn mặt được chia thành nhiều thư mục.  
Mỗi thư mục tương ứng với một người/một lớp.

Do dữ liệu có khuôn mặt thật nên không nên công khai dataset nếu chưa có sự cho phép của người trong ảnh.

## 4. Quy trình thực hiện
Notebook thực hiện các bước chính:

1. Import thư viện.
2. Upload file dataset dạng `.zip`.
3. Giải nén và chuẩn hóa dữ liệu.
4. Hiển thị ảnh mẫu.
5. Chia dữ liệu thành train, validation và test.
6. Tạo TensorFlow Dataset.
7. Xây dựng mô hình nhận diện khuôn mặt.
8. Huấn luyện mô hình.
9. Vẽ biểu đồ accuracy/loss.
10. Đánh giá mô hình trên tập test.
11. Dự đoán thử ảnh mới.
12. Lưu model và kết quả.

## 5. Mô hình sử dụng
Dự án sử dụng mô hình học sâu dựa trên MobileNetV2 để trích xuất đặc trưng ảnh khuôn mặt và phân loại người trong ảnh.

## 6. Kết quả
Sau khi huấn luyện, notebook hiển thị:

- Biểu đồ accuracy và loss.
- Độ chính xác trên tập test.
- Confusion matrix.
- Kết quả dự đoán thử ảnh mới.
- File kết quả `face_recognition_results.zip`.

## 7. Cách chạy
1. Mở file `Face_Recognition_Colab.ipynb` trên Google Colab.
2. Bật GPU trong phần Runtime.
3. Chạy lần lượt các cell từ trên xuống.
4. Upload file dataset `.zip` khi notebook yêu cầu.
5. Xem kết quả train, test và dự đoán ảnh mới.

## 8. Ghi chú
Bài làm phục vụ mục đích học tập môn Trí tuệ nhân tạo.  
Dự án không làm app, chỉ nộp code Colab, dữ liệu và video demo.

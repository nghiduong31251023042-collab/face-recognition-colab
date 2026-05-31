# Script quay video demo - Nhận diện khuôn mặt bằng Google Colab

Thời lượng gợi ý: 3 đến 5 phút.

## Phần 1: Giới thiệu

Xin chào thầy/cô và các bạn. Đây là bài demo đề tài nhận diện khuôn mặt bằng Google Colab. Dự án này không làm app, mà chạy toàn bộ quá trình xử lý dữ liệu, huấn luyện mô hình và dự đoán trực tiếp trên notebook Colab.

## Phần 2: Giới thiệu file nộp

Trong thư mục nộp có notebook `Face_Recognition_Colab.ipynb`, file dữ liệu `face_dataset_clean_39classes.zip`, file hướng dẫn `README.md`, file thư viện `requirements.txt` và script video demo.

## Phần 3: Mở Colab và upload dữ liệu

Em mở notebook trên Google Colab, bật GPU để tăng tốc quá trình train. Sau đó em chạy bước upload dữ liệu và chọn file `face_dataset_clean_39classes.zip`.

## Phần 4: Kiểm tra dữ liệu

Notebook tự giải nén dữ liệu, đọc các thư mục ảnh theo từng người và thống kê số lượng ảnh. Sau đó em chạy bước xem ảnh mẫu để kiểm tra dữ liệu hiển thị đúng.

## Phần 5: Chia dữ liệu và train model

Dữ liệu được chia thành ba phần: train, validation và test. Model sử dụng MobileNetV2 pretrained, sau đó thêm lớp phân loại để nhận diện các người trong tập dữ liệu. Em tiến hành train và theo dõi accuracy, loss qua từng epoch.

## Phần 6: Đánh giá kết quả

Sau khi train xong, notebook đánh giá model trên tập test. Kết quả gồm test accuracy, classification report và confusion matrix. Các kết quả này giúp kiểm tra mô hình nhận diện đúng hay sai ở từng lớp.

## Phần 7: Dự đoán ảnh mới

Em upload một ảnh khuôn mặt mới thuộc một trong các người đã train. Mô hình sẽ hiển thị ảnh, tên dự đoán và độ tin cậy. Đây là phần demo chính của bài.

## Phần 8: Kết luận

Dự án đã xây dựng được quy trình nhận diện khuôn mặt bằng Google Colab, bao gồm chuẩn bị dữ liệu, train model, đánh giá kết quả và dự đoán ảnh mới. Hạn chế là độ chính xác phụ thuộc vào chất lượng ảnh, góc chụp và ánh sáng. Trong tương lai có thể tăng dữ liệu và cải thiện bước tiền xử lý khuôn mặt.

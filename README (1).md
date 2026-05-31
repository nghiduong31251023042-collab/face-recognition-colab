# Face Recognition Colab - Nhận diện khuôn mặt bằng ảnh

Dự án này dùng Google Colab để huấn luyện mô hình nhận diện khuôn mặt từ tập ảnh đã chia theo từng người.

> Lưu ý: Đây không phải app/web. Toàn bộ demo chạy trong Google Colab.

## 1. File cần nộp

- `Face_Recognition_Colab.ipynb`: notebook Colab chứa toàn bộ code train/test.
- `face_dataset_clean_39classes.zip`: dữ liệu ảnh khuôn mặt đã chuẩn hóa.
- `README.md`: hướng dẫn chạy.
- `requirements.txt`: thư viện sử dụng.
- `video_script_demo.md`: lời thoại gợi ý để quay video.
- `face_recognition_results.zip`: kết quả sinh ra sau khi chạy Colab, gồm model, biểu đồ và file đánh giá.

## 2. Cấu trúc dữ liệu

Dữ liệu cần có cấu trúc:

```text
face_dataset_clean_39classes/
├── Person_A/
│   ├── img_0001.jpg
│   ├── img_0002.jpg
│   └── ...
├── Person_B/
│   ├── img_0001.jpg
│   └── ...
└── ...
```

Mỗi thư mục con là một lớp/người.

## 3. Cách chạy trên Google Colab

1. Mở Google Colab.
2. Upload notebook `Face_Recognition_Colab.ipynb`.
3. Bật GPU: `Runtime` → `Change runtime type` → chọn `GPU`.
4. Chạy lần lượt từng cell từ trên xuống.
5. Ở bước upload dữ liệu, chọn file `face_dataset_clean_39classes.zip`.
6. Chạy train model.
7. Xem kết quả accuracy, classification report và confusion matrix.
8. Upload một ảnh mới để thử dự đoán.
9. Chạy bước cuối để tải `face_recognition_results.zip`.

## 4. Mô hình sử dụng

Notebook dùng MobileNetV2 pretrained trên ImageNet và thêm lớp phân loại theo số người trong dataset.

## 5. Gợi ý nộp GitHub

Nên tạo repository mới, ví dụ:

```text
face-recognition-colab
```

Upload các file:

```text
Face_Recognition_Colab.ipynb
face_dataset_clean_39classes.zip
README.md
requirements.txt
video_script_demo.md
```

Nếu repository public, cần cân nhắc quyền riêng tư vì dữ liệu là ảnh khuôn mặt.

# Speech Emotion Recognition

Một hệ thống **Speech Emotion Recognition (SER)**, dùng để phân loại cảm xúc trong giọng nói (speech) bằng cách trích xuất đặc trưng âm thanh (audio) và huấn luyện mô hình Machine Learning / Deep Learning.  

## Mục tiêu (Goal)

- Nhận diện cảm xúc (ví dụ: vui, buồn, giận, sợ, trung tính, ...) từ file âm thanh speech.  
- Hiển thị kết quả dự đoán cảm xúc thông qua một ứng dụng **Streamlit**.  
- Hỗ trợ quy trình từ **tiền xử lý dữ liệu**, trích xuất đặc trưng, huấn luyện mô hình → đến deployment inference.

## Cấu trúc dự án (Project Structure)

├── data_preprocessing/ # Mã để xử lý dữ liệu (load audio, xử lý, chia train/test)

├── model_training/ # Mã huấn luyện mô hình

├── streamlit_app/ # Ứng dụng Streamlit để inference cảm xúc

├── notebooks/ # (nếu có) các notebook phân tích, visual feature, thử nghiệm mô hình

└── README.md # File hướng dẫn này

# Sử dụng (Usage)
1. Tiền xử lý dữ liệu (Preprocessing)
Chạy mã trong thư mục data_preprocessing/ để load các file âm thanh, xử lý (ví dụ: chuẩn hóa, cắt đoạn), và trích xuất các đặc trưng (features) như MFCC, Mel-spectrogram

Chia dữ liệu thành tập huấn luyện (train), validation, test nếu muốn.

2. Huấn luyện mô hình (Model Training)
Vào thư mục model_training/: chạy script hoặc notebook để huấn luyện mô hình ML / DL nhận diện cảm xúc.

Lưu mô hình đã huấn luyện (checkpoint) để dùng sau khi deploy.

3. Ứng dụng Streamlit (Inference)
Vào streamlit_app/ và chạy:

streamlit run app.py
Ứng dụng web sẽ chạy local, bạn có thể upload file âm thanh và xem dự đoán cảm xúc.


# Phần mở rộng (Future Work / Roadmap)

Thử nghiệm với các mô hình nâng cao như LSTM, CNN, hoặc Transformer để cải thiện độ chính xác.

Sử dụng thêm dữ liệu: các bộ dữ liệu nổi tiếng như RAVDESS, TESS, CREMA-D,… để huấn luyện đa dạng hơn.

Deploy mô hình lên web thật sự (production): dùng Docker, Heroku, hoặc các cloud như AWS / GCP.

Tối ưu thời gian inference, giảm latency cho real-time speech emotion detection.

Thêm chức năng realtime (microphone): để ứng dụng nghe giọng nói và detect cảm xúc ngay lập tức.

Tham khảo & Tài liệu (References)
Mô hình Speech Emotion Recognition tương tự: các project open-source khác dùng MFCC, LSTM, CNN. 
GitHub
+2
GitHub
+2

Các kỹ thuật trích xuất đặc trưng âm thanh (audio features): MFCC, Mel-spectrogram, sử dụng thư viện librosa. 
GitHub
+1

Công cụ trích xuất audio features mạnh mẽ như openSMILE

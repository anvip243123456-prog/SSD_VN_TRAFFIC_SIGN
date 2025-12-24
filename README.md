SSD-based Vietnamese Traffic Sign Detection



Nhận dạng Biển báo Giao thông Việt Nam bằng SSD



---



1\. Introduction | Giới thiệu



\### 🇬🇧 English



Traffic sign detection is a fundamental task in computer vision and intelligent transportation systems.

This project implements a \*\*Single Shot MultiBox Detector (SSD)\*\* model for \*\*Vietnamese traffic sign detection\*\*, serving as a \*\*baseline method\*\* for comparison with more advanced detectors such as YOLOv8.



The project is developed for \*\*academic and thesis purposes\*\*, focusing on evaluating SSD performance on both images and videos.



\### 🇻🇳 Tiếng Việt



Nhận dạng biển báo giao thông là một bài toán quan trọng trong thị giác máy tính và hệ thống giao thông thông minh.

Dự án này triển khai mô hình \*\*SSD (Single Shot MultiBox Detector)\*\* cho bài toán \*\*phát hiện biển báo giao thông Việt Nam\*\*, đóng vai trò \*\*mô hình baseline\*\* để so sánh với các phương pháp hiện đại hơn như YOLOv8.



Dự án được thực hiện phục vụ \*\*mục đích học thuật và luận văn\*\*, tập trung đánh giá hiệu năng SSD trên ảnh và video.



---



2\. Model Overview | Tổng quan mô hình



\### 🇬🇧



\* Model: \*\*SSD300\*\*

\* Backbone: \*\*VGG16\*\*

\* Type: One-stage object detector

\* Characteristics:



&nbsp; \* Simple architecture

&nbsp; \* Stable performance on static images

&nbsp; \* Limited robustness on real-time video



\### 🇻🇳



\* Mô hình: \*\*SSD300\*\*

\* Backbone: \*\*VGG16\*\*

\* Loại: Bộ phát hiện đối tượng một giai đoạn

\* Đặc điểm:



&nbsp; \* Kiến trúc đơn giản

&nbsp; \* Hoạt động ổn định trên ảnh tĩnh

&nbsp; \* Hạn chế khi xử lý video thời gian thực



---



3\. Dataset | Dữ liệu



\### 🇬🇧



\* Dataset: \*\*Vietnamese Traffic Signs\*\*

\* Source: Kaggle

\* Annotation format: YOLO-style labels

\* Classes: Vietnamese traffic sign categories



Due to large storage size, \*\*datasets, checkpoints, and videos are not included\*\* in this repository.



\### 🇻🇳



\* Bộ dữ liệu: \*\*Vietnamese Traffic Signs\*\*

\* Nguồn: Kaggle

\* Định dạng nhãn: YOLO

\* Số lớp: Các loại biển báo giao thông Việt Nam



Do dung lượng lớn, \*\*dữ liệu, trọng số và video không được đưa lên GitHub\*\*.



---



4\. Project Structure | Cấu trúc thư mục



```text

ssd\_traffic\_sign/

├── .gitignore              # Ignore dataset, checkpoints, videos

├── README.md               # Project documentation

├── classes\_en.txt          # English class labels

├── classes\_vie.txt         # Vietnamese class labels

├── demo.py                 # Image inference script

└── demovideo.py            # Video inference script

```



---



5\. Installation | Cài đặt



\### 🇬🇧



Install required dependencies:



```bash

pip install torch torchvision opencv-python numpy

```



\### 🇻🇳



Cài đặt các thư viện cần thiết:



```bash

pip install torch torchvision opencv-python numpy

```



---



6\. Training | Huấn luyện mô hình



\### 🇬🇧



The SSD model is trained using preprocessed Vietnamese traffic sign data.

Training checkpoints are stored locally and excluded from version control.



\### 🇻🇳



Mô hình SSD được huấn luyện trên dữ liệu biển báo giao thông Việt Nam đã xử lý trước.

Các file trọng số được lưu cục bộ và không đưa lên GitHub.



---



7\. Image Inference | Nhận dạng trên ảnh



\### 🇬🇧



```bash

python demo.py

```



The script loads a trained SSD model and performs detection on static images.



\### 🇻🇳



Chạy nhận dạng trên ảnh:



```bash

python demo.py

```



Chương trình sẽ phát hiện biển báo và hiển thị bounding box cùng nhãn.



---



8\. Video Inference | Nhận dạng trên video



\### 🇬🇧



```bash

python demovideo.py

```



SSD can detect traffic signs in video, but may suffer from:



\* Temporal instability

\* Missed detections

\* Flickering bounding boxes



\### 🇻🇳



Chạy nhận dạng trên video:



```bash

python demovideo.py

```



SSD có thể phát hiện biển báo trong video nhưng thường gặp:



\* Dao động kết quả giữa các frame

\* Bỏ sót biển

\* Bounding box không ổn định



---



9\. Experimental Observations | Nhận xét thực nghiệm



\### 🇬🇧



\* High accuracy on static images

\* Reduced performance on video sequences

\* Serves well as a \*\*baseline detector\*\*



\### 🇻🇳



\* Độ chính xác cao trên ảnh tĩnh

\* Hiệu năng giảm rõ rệt trên video

\* Phù hợp làm \*\*mô hình baseline để so sánh\*\*



---



10\. Comparison with YOLOv8 | So sánh với YOLOv8



\### 🇬🇧



Compared to YOLOv8:



\* SSD is less robust on video

\* YOLOv8 provides more stable and accurate real-time detection



\### 🇻🇳



So với YOLOv8:



\* SSD kém ổn định hơn trên video

\* YOLOv8 cho kết quả chính xác và ổn định hơn trong thời gian thực







11\. Academic Use | Ứng dụng học thuật



\### 🇬🇧



This repository is intended for:

\* Baseline comparison in thesis

\* Computer vision coursework

\* Object detection experiments



\### 🇻🇳



Repo này được sử dụng cho:

\* So sánh baseline trong luận văn

\* Học phần thị giác máy tính

\* Thực nghiệm phát hiện đối tượng



Author | Tác giả

\*\*Le Nguyen Hai An\*\*
\*\*HUYNH VU MINH HIEU\*\*

Faculty of Information Technology

Ton Duc Thang University

Vietnam 🇻🇳




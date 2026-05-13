 Hệ thống Phát hiện Tin giả  bằng Qwen2.5-1.5B kết hơp MBert
> Mô hình Ngôn ngữ Lớn (LLM) tinh chỉnh cho bài toán Phân loại Văn bản Nhị phân trên tập dữ liệu ViFactCheck.**

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![Python 3.10+](https://img.shields.io/badge/python-3.10+-blue.svg)](https://www.python.org/downloads/)
[![Unsloth](https://img.shields.io/badge/Accelerated%20by-Unsloth-orange)](https://github.com/unslothai/unsloth)

Dự án này tập trung vào việc nghiên cứu và ứng dụng Mô hình Ngôn ngữ Lớn (LLM) để nhận diện tin tức giả mạo trong ngữ cảnh tiếng Việt.Đối chứng so sánh ngữ cảnh giữa 2 mô hình Encoder và Decoder đại diện như mBERT và Qwen2.5-1.5B-Instruc sử dụng kỹ thuật tinh chỉnh nhằm tăng cường khả năng đọc hiểu ngữ cảnh dài và lập luận từ vựng.


📊 Bộ dữ liệu (Dataset)
Nguồn: ViFactCheck.
Cấu trúc được chuyển đổi sang định dạng hội thoại `ChatML` để phù hợp với kiến trúc của mô hình Instruct.
Tiền xử lý Xử lý triệt để sự chênh lệch số lượng mẫu giữa hai nhãn trước khi đưa vào huấn luyện.
Hiệu năng

| Mô hình | Accuracy | Precision | Recall | F1-Score |
| mBERT  | 76.02% | ~54.00% | ~44.00% | 48.70% |
| Qwen2.5-1.5B | 69,95% |50,56%| 67,66% | 57,87%|

pip install "unsloth[colab-new] @ git+[https://github.com/unslothai/unsloth.git](https://github.com/unslothai/unsloth.git)"
pip install --no-deps "xformers<0.0.27" "trl<0.9.0" peft accelerate bitsandbytes

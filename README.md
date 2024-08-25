# 100 bài tập xử lý dữ liệu với Pandas

## Tổng quan

- Chào mừng bạn đến với bộ tài liệu "100 bài tập xử lý dữ liệu với Pandas" do Nguyen Ha DS biên dịch. Đây là một tài liệu tuyệt vời giúp bạn rèn luyện và nâng cao kỹ năng phân tích dữ liệu với thư viện Pandas trong Python. Với 100 bài tập phong phú và đa dạng, tài liệu này bao quát nhiều khía cạnh của công việc phân tích dữ liệu, từ xử lý dữ liệu cơ bản đến những kỹ thuật nâng cao.

- Những bài tập trong tài liệu này được thiết kế sát với thực tiễn và đã được kiểm chứng bởi cộng đồng các nhà phân tích dữ liệu tại Nhật Bản. Được công bố bởi Hiệp hội Khoa học Dữ liệu Nhật Bản (The Data Scientist Society Japan) [[1]](https://github.com/The-Japan-DataScientist-Society/100knocks-preprocess), tài liệu này đã nhận được sự ưa chuộng và đánh giá cao từ giới chuyên môn.

- Nguyen Ha DS đã dịch và biên soạn lại tài liệu này với mục tiêu giúp các bạn dễ dàng tiếp cận hơn và cung cấp phần lời giải dễ hiểu và phong cách viết code pandas hiệu quả hơn. Mình hy vọng tài liệu này sẽ trở thành một công cụ hữu ích trong việc học tập và nâng cao kỹ năng của bạn.

- Với kinh nghiệm nhiều năm trong lĩnh vực phân tích dữ liệu, mình tin tưởng rằng nếu bạn kiên nhẫn hoàn thành hết 100 bài tập Pandas này, bạn sẽ trở nên thành thạo và tự tin xử lý mọi loại dữ liệu dạng bảng bạn gặp trong công việc của mình. Chúc các bạn thành công.

## Cài đặt

### Clone thư mục GitHub này

```shell
git clone https://github.com/datasciencelab-ai/100_bai_tap_pandas.git
cd 100_bai_tap_pandas
```

### Cài đặt môi trường ảo và các thư viện cần thiết

```shell
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

### Cài đặt và Khởi động Jupyter Lab

```shell
# Cài đặt lại ipykernel cho Jupyter
python -m ipykernel install --user

# Khởi chạy jupyter lab
jupyter lab
```

### Kiểm tra cấu hình Kernal (Tham khảo)

- Đôi khi, việc cấu hình kernel có thể bị sai. Bạn có thể xóa các kernel cũ và cấu hình lại kernel mới.

```shell
# Kiểm tra cấu hình kernel
jupyter kernelspec list

# Xoá các cấu hình cũ
jupyter kernelspec uninstall unwanted-kernel

```

## Cấu trúc thư mục này

```plaintext
.
├── LICENSE
├── README.md
├── data
│   ├── export_from_exercises
│   ├── preprocessed
│   │   ├── category_eng.csv
│   │   ├── customer_eng.csv
│   │   ├── geocode_eng.csv
│   │   ├── product.csv
│   │   ├── receipt.csv
│   │   └── store_eng.csv
│   └── raw
├── docs
│   ├── ER_diagram.png
│   ├── ER_diagram.pptx
│   └── how_to_read_ER_diagram.md
├── notebooks_en
│   ├── answer
│   └── exercises
│       └── 100_pandas_exercises_en.ipynb
├── notebooks_vn
│   ├── answer
│   │   ├── 100_bai_tap_pandas_vn_ans.ipynb
│   │   ├── bonus_Q40_cross_join.ipynb
│   │   ├── bonus_Q43_pivot_table.ipynb
│   │   ├── bonus_Q45_pd_time_series.ipynb
│   │   ├── bonus_Q59_Q60_normalization_technique.ipynb
│   │   ├── bonus_Q86_visualize_customer_and_store_address.ipynb
│   │   ├── bonus_Q90_time_series_prediction.ipynb
│   │   └── map.html
│   ├── exercises
│   │   └── 100_bai_tap_pandas_vn_exes.ipynb
│   └── pandas_basic
│       └──  pandas_basic.ipynb
└── requirements.txt
```

### Giải thích chi tiết

- `LICENSE`: Tập tin chứa thông tin về giấy phép sử dụng của tài liệu.
- `README.md`: Tập tin hướng dẫn, cung cấp thông tin tổng quan về tài liệu và cách sử dụng.
- `data`: Thư mục chứa dữ liệu sử dụng trong các bài tập.
  - `export_from_exercises`: Chứa dữ liệu xuất ra từ các bài tập.
  - `preprocessed`: Chứa dữ liệu đã được dịch sang tiếng Anh.
    - `category_eng.csv`: Dữ liệu về danh mục sản phẩm.
    - `customer_eng.csv`: Dữ liệu về khách hàng.
    - `geocode_eng.csv`: Dữ liệu về mã địa lý.
    - `product.csv`: Dữ liệu về sản phẩm.
    - `receipt.csv`: Dữ liệu về hóa đơn.
    - `store_eng.csv`: Dữ liệu về cửa hàng.
  - `raw`: Chứa dữ liệu gốc bằng tiếng Nhật.
- `docs`: Thư mục chứa các tài liệu tham khảo.
  - `ER_diagram.png`: Hình ảnh sơ đồ ER (Entity-Relationship).
  - `ER_diagram.pptx`: Slide thể hiện ER diagram.
  - `how_to_read_ER_diagram.md`: Hướng dẫn đọc sơ đồ ER.
- `notebooks_en`: Thư mục chứa các notebook bài tập và lời giải bằng tiếng Anh.
  - `answer`: Chứa các notebook lời giải.
  - `exercises`: Chứa các notebook bài tập.
    - `100_pandas_exercises_en.ipynb`: Notebook chứa 100 bài tập Pandas bằng tiếng Anh.
- `notebooks_vn`: Thư mục chứa các notebook bài tập và lời giải bằng tiếng Việt.
  - `answer`: Chứa các notebook lời giải.
    - `100_bai_tap_pandas_vn_ans.ipynb`: Notebook chứa 100 lời giải bài tập Pandas bằng tiếng Việt.
    - `bonus_Q40_cross_join.ipynb`: Notebook về bài tập bổ sung - Cross Join.
    - `bonus_Q43_pivot_table.ipynb`: Notebook về bài tập bổ sung - Pivot Table.
    - `bonus_Q45_pd_time_series.ipynb`: Notebook về bài tập bổ sung - Time Series.
    - `bonus_Q59_Q60_normalization_technique.ipynb`: Notebook về bài tập bổ sung - Normalization Technique.
    - `bonus_Q86_visualize_customer_and_store_address.ipynb`: Notebook về bài tập bổ sung - Visualize Customer and Store Address.
    - `bonus_Q90_time_series_prediction.ipynb`: Notebook về bài tập bổ sung - Time Series Prediction.
    - `map.html`: Tập tin HTML chứa bản đồ.
  - `exercises`: Chứa các notebook bài tập.
    - `100_bai_tap_pandas_vn_exes.ipynb`: Notebook chứa 100 bài tập Pandas bằng tiếng Việt.
  - `pandas_basic`: Chứa các notebook hướng dẫn cơ bản về Pandas.
    - `pandas_basic.ipynb`: Notebook hướng dẫn cơ bản về Pandas.
    - `time_series_example.csv`: Dữ liệu ví dụ về chuỗi thời gian.
    - `time_series_example.xlsx`: Dữ liệu ví dụ về chuỗi thời gian ở định dạng Excel.
- `requirements.txt`: Tập tin chứa danh sách các thư viện cần thiết để chạy các notebook.

## Tài liệu tham khảo

- [[1]](https://github.com/The-Japan-DataScientist-Society/100knocks-preprocess) Tài liệu gốc bằng tiếng Nhât được phát hành từ Hiệp hội Khoa học Dữ liệu Nhật Bản (The Data Scientist Society Japan)
- [Chuỗii videos live code được Nguyen Ha DS biên soạn](https://www.youtube.com/playlist?list=PL85bwuRqeUWYccgtXOxLt68YwyPo6g2W9)

## Tác giả

- Hiệp hội Khoa học Dữ liệu Nhật Bản (The Data Scientist Society Japan)
- Bản dịch tiếng Việt và lời giải: Nguyen Ha DS

## LICENSE

Tài liệu này được cấp phép dưới giấy phép Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International (CC BY-NC-ND 4.0).

Bạn có thể xem chi tiết về giấy phép này tại [đây](https://creativecommons.org/licenses/by-nc-nd/4.0/).

![CC BY-NC-ND 4.0](https://licensebuttons.net/l/by-nc-nd/4.0/88x31.png)

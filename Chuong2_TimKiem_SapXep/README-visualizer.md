# Sorting Visualizer

Ứng dụng web mô phỏng trực quan 5 giải thuật sắp xếp — chạy thẳng trên trình duyệt, không cần cài đặt.

---

## Chạy ngay

```
Mở file sorting-visualizer.html trên trình duyệt
```

Không cần server, không cần cài thêm gì.

---

## Giao diện

```
┌─────────────────────────────────────────────────────────────┐
│  SortViz  [Selection] [Insertion] [Bubble] [Quick] [Heap]   │  ← chọn thuật toán
├─────────────────────────────────────────────────────────────┤
│  N = [16]  ⇌ Random   Nhập tay: [_____________]  Áp dụng   │  ← nhập dữ liệu
├─────────────────────────────────────────────────────────────┤
│  Mảng: [64] [25] [12] [22] [11] ...                         │  ← chip array
├──────────────────────────────┬──────────────────────────────┤
│                              │  selection_sort.cpp    [C++] │
│    ████ ██ ████ ██ ████      │   1  void SelectionSort(...  │
│    ████ ██ ████ ██ ████      │   2    int vt;               │
│    ████ ██ ████ ██ ████      │ ► 3    for (int i=0; ...     │  ← dòng đang chạy
│     i        j               │   4      vt = i;             │
├──────────────────────────────┤   ...                        │
│  So sánh: 12  Hoán vị: 4    ├──────────────────────────────┤
│  [▶ Chạy] [■] [↺]  Tốc độ  │  Tốt nhất  Trung bình  ...   │
└──────────────────────────────┴──────────────────────────────┘
```

---

## Cách dùng

### Nhập dữ liệu

| Cách | Thao tác |
|------|---------|
| Random | Gõ số vào ô **N =** (2–60) → nhấn **⇌ Random** |
| Nhập tay | Gõ số vào ô text, cách nhau bởi dấu phẩy hoặc khoảng trắng → nhấn **Áp dụng** hoặc `Enter` |

Ví dụ nhập tay: `64 25 12 22 11 90` hoặc `5,3,8,1,9`

### Điều khiển

| Nút | Chức năng |
|-----|----------|
| ▶ Chạy | Bắt đầu mô phỏng |
| ■ Dừng | Dừng giữa chừng |
| ↺ Reset | Quay lại mảng gốc đã nhập |
| Tốc độ | Kéo slider để chậm/nhanh hơn |

---

## Tính năng

- **Code C++ highlight realtime** — dòng đang thực thi tự động sáng lên và cuộn theo
- **Con trỏ i / j / p / ↑** — hiển thị ngay dưới từng thanh bar
- **Chip array** — mỗi phần tử đổi màu theo trạng thái đang xử lý
- **Thống kê** — đếm số lần so sánh, hoán vị, bước, thời gian chạy
- **Bảng độ phức tạp** — cập nhật theo thuật toán đang chọn

### Màu sắc

| Màu | Ý nghĩa |
|-----|---------|
| Tím | Phần tử đang được xét |
| Vàng | Phần tử đang so sánh |
| Hồng | Pivot (Quick Sort) |
| Xanh dương | Min hiện tại (Selection Sort) |
| Xanh lá | Đã sắp xong |

---

## Thuật toán

| Thuật toán | Ý tưởng | Best | Avg | Worst |
|-----------|---------|------|-----|-------|
| Selection Sort | Tìm min từng lượt, đưa về đầu | O(N²) | O(N²) | O(N²) |
| Insertion Sort | Chèn từng phần tử vào đúng chỗ | O(N) | O(N²) | O(N²) |
| Bubble Sort | Đổi chỗ cặp kề sai thứ tự | O(N) | O(N²) | O(N²) |
| Quick Sort | Chọn pivot, phân hoạch, đệ quy | O(N logN) | O(N logN) | O(N²) |
| Heap Sort | Xây max-heap, lấy dần phần tử lớn | O(N logN) | O(N logN) | O(N logN) |

---

## Yêu cầu

Trình duyệt hiện đại — Chrome, Firefox, Edge, Safari. Không cần kết nối internet (font load từ Google Fonts, mất font thì dùng font hệ thống).

---

*Khoa CNTT — CĐ Công Thương TP.HCM*

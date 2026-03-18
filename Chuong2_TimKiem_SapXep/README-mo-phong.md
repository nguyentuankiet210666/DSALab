# Mo_phong_sap_xep.cpp

Mô phỏng từng bước 5 giải thuật sắp xếp trên terminal — có màu sắc, thống kê so sánh và hoán vị.

## Chạy ngay

```bash
g++ -o mo_phong Mo_phong_sap_xep.cpp
./mo_phong
```

## Cách dùng

1. Nhập số phần tử (2–20)
2. Chọn nhập tay hoặc random
3. Chọn thuật toán từ menu (hoặc chọn 6 để chạy cả 5)

```
1-Selection  2-Insertion  3-Bubble  4-Quick  5-Heap  6-Tat ca  0-Thoat
```

## Ví dụ output

```
=== SELECTION SORT — chon truc tiep ===
Luot 1:   [  11 |  25 |  12 |  22 |  64 |  90 ]
Luot 2:   [  11 |  12 |  25 |  22 |  64 |  90 ]
...
So sanh: 15  |  Hoan vi: 3
```

Phần tử **xanh lá** = đã sắp xong, **vàng** = đang xét.

## Thuật toán

| # | Tên | Độ phức tạp |
|---|-----|------------|
| 1 | Selection Sort | O(N²) |
| 2 | Insertion Sort | O(N²) / O(N) tốt nhất |
| 3 | Bubble Sort | O(N²) / O(N) tốt nhất |
| 4 | Quick Sort | O(N logN) trung bình |
| 5 | Heap Sort | O(N logN) |

## Yêu cầu

Compiler `g++` hỗ trợ C++11 trở lên. Terminal hỗ trợ màu ANSI (Linux/macOS/Windows Terminal).

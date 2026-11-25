# Team

## Thông tin nhóm

- Tên nhóm: 25112026
- Lớp: L3B
- Repo nhóm: `K5-L3B-DAY13-25112026-LaunchEconomics` (xem [SUBMISSION.md](SUBMISSION.md))
- URL repo, nhánh nộp, commit chốt: https://github.com/huydn8816/K5-L3B-DAY13-25112026-LaunchEconomics · nhánh `main` · commit chốt: commit cuối trên `main` trước 23h59 GMT+7 ngày 25/11/2026

## Thành viên

| STT | Họ tên | MSSV | Email | GitHub | Vai trò |
| --: | ------ | ---- | ----- | ------ | ------- |
|   1 | Phạm Đức Vinh | 2A202603849     | 26ai.vinhpd@vinuni.edu.vn      |  vindpd203      | Người viết code (trước giải lao) |
|   2 | Ngô Duy Khánh | 2A202603870 | | dkhanhdev | Người kiểm số (sau giải lao nhận viết code) |
|   3 | Nguyễn Thế Bảo | 2A202603825 | 26ai.baont4@vinuni.edu.vn | NTheBao | Người gắn nhãn 1 |
|   4 | Đặng Nhật Huy | 2A202603822 | 26ai.huydn@vinuni.edu.vn |  huydn8816      | Người gắn nhãn 2, kiêm giữ hồ sơ |

Bốn vai của lab:

- **Người viết code:** viết và chạy `src/lab13.py`.
- **Người kiểm số:** tính tay một con số để đối chiếu, điền bảng.
- **Người gắn nhãn 1:** đọc đề, theo dõi điều kiện "Xong khi"; gắn nhãn 20 ca độc lập ở CP3.
- **Người gắn nhãn 2, kiêm giữ hồ sơ:** điền `report/team/ho_so_launch_v0.md` từ đầu buổi; gắn nhãn 20 ca độc lập ở CP3.

Đổi người viết code sau giờ giải lao, để ít nhất hai người trong nhóm tự tay tính được chi phí.

## Cá nhân

Mỗi thành viên đồng thời tạo một báo cáo riêng trong `report/` theo dạng:

```text
report/team/MSSV_HoTen.md
```

Ví dụ: `report/team/20241234_NguyenVanAn.md`.

Sao chép mục dưới đây cho từng thành viên.

## NgoDuyKhanh-2A202603870

### Phần việc phụ trách

- **Chính:** CP4 · Nhiệm vụ D (`report/team/pilot_plan.yaml`, code tính 5 câu cỡ mẫu D1 và tỉ lệ mở lại trong `src/lab13.py`).
- **Phụ:** CP1 (tính tay kiểm số, điền bảng A1–A4), CP2 (điền bảng độ nhạy B1–B4, tự kiểm tra quy tắc tuyến tính), CP3 (soát lại `bang_chi_phi.md`), CP5 (tính 3 chỉ số E1 trong `src/lab13.py` và điền vào `report/team/chi_so.md`).

### Đóng góp cụ thể

- Tính tay kiểm chứng số liệu chi phí và hoàn thiện toàn bộ các bảng A1–A4, B1–B4 cùng các câu trả lời ngắn gọn kèm nhãn `simulated` trong `report/team/bang_chi_phi.md`.
- Viết code giải 5 bài toán cỡ mẫu D1, tính tỉ lệ `mo_lai_trong_7_ngay` hiện tại (4,25% toàn mẫu; 3,97% trong phạm vi `noi_dia + hang_nang`) và 3 chỉ số E1 trong `src/lab13.py`.
- Chủ trì hoàn thiện `report/team/pilot_plan.yaml` (điền chú thích D1, D2, đánh đổi chấp nhận MDE 6 điểm, 3 luật dừng chuẩn `NẾU – TRONG – THÌ – KHÔNG THÌ`, xoá toàn bộ dấu `?`).
- Cập nhật kết quả tính thử 3 chỉ số E1 (82,83% · 27,12% · 4,25%) vào `report/team/chi_so.md`.

### Bằng chứng

- Code CP4 (D1) và CP5 (E1) trong [src/lab13.py](src/lab13.py).
- File [report/team/bang_chi_phi.md](report/team/bang_chi_phi.md), [report/team/pilot_plan.yaml](report/team/pilot_plan.yaml), [report/team/chi_so.md](report/team/chi_so.md) và báo cáo cá nhân [report/team/2A202603870_NgoDuyKhanh.md](report/team/2A202603870_NgoDuyKhanh.md).

## PhamDucVinh-2A202603849

### Phần việc phụ trách

- **Chính:** chuẩn bị môi trường, CP1 · Nhiệm vụ A, CP2 · Nhiệm vụ B (code trong `src/lab13.py`), đóng gói và nộp bài.
- **Phụ:** CP3 (hoàn thiện B), CP4 (soát `pilot_plan.yaml`), CP5 (chạy lại `lab13.py` trên máy khác), bàn giao code cho Người 2.

### Đóng góp cụ thể

- Viết 3 hàm A1 (ba phép thử ĐẠT: 1,20 · 1,25 · 1,25) và `mo_hinh()` A2: chi phí mỗi việc thành công 4.472 đ [simulated], gấp 16,3 lần hoá đơn chia số yêu cầu.
- Tính A3 theo loại (`quoc_te` 1,88× [simulated], chạy lại không giúp) và A4 cộng chi phí cố định (4.599 đ = 0,38× ở 45.000 yêu cầu/tháng [simulated]).
- Viết B1–B4: 9 kịch bản độ nhạy, một cặp (+46,3%), giới hạn 2 lần rẻ nhất cho công ty (6.901.220 đ [simulated]), xem lại 100% = 0,98×–1,03× [simulated].

### Bằng chứng

- Commit `b9a5f93` trên nhánh `vinh` (merge vào `main` qua pull request #1).
- Code trong [src/lab13.py](src/lab13.py), số trong [report/team/bang_chi_phi.md](report/team/bang_chi_phi.md) và báo cáo cá nhân [report/team/2A202603849_PhamDucVinh.md](report/team/2A202603849_PhamDucVinh.md).

## DangNhatHuy-2A202603822

### Phần việc phụ trách

- **Chính:** CP5 · Nhiệm vụ E (`report/team/ho_so_launch_v0.md`, chỉ số tự đề xuất và rủi ro kinh tế E2 trong `report/team/chi_so.md`) và duyệt chéo Gate 2a (`report/team/phieu_cham.md`).
- **Phụ:** CP1–CP4 (điền dần hồ sơ launch v0 sau mỗi checkpoint), CP3 (người gắn nhãn 2, gắn độc lập 20 ca lỗi), báo cáo nhóm `report/team/group_report.md`.

### Đóng góp cụ thể

- Lập danh sách đầu mục và bảng phân công 4 người theo checkpoint trong [PhanCong.md](PhanCong.md).
- Hoàn thiện hồ sơ launch v0 đủ 7 mục, mỗi mục có con số chính, trạng thái và vai trò phụ trách; đề xuất **Go có điều kiện** cho pilot `noi_dia` + `hang_nang` (4.599 đ = 0,38× [simulated]), nêu 3 con số bất lợi (xem lại 100% = 0,98× [simulated], power 0,64 ở mức 5 điểm, mở lại hiện tại 4,25%) và 5 điều kiện có người phụ trách, ngày kiểm tra.
- Đề xuất 2 chỉ số (tỉ lệ nhân viên mở gợi ý; tỉ lệ đơn hoàn sai tiền qua kiểm tra mẫu hằng tuần) và 3 dòng rủi ro kinh tế lấy số từ bảng độ nhạy.
- Gắn nhãn độc lập 20 ca lỗi (đồng thuận 20/20 với người gắn nhãn 1); hoàn thiện bảng khắc phục 5 ca và bổ sung 2 event `handoff_to_staff`, `input_validation_failed`.
- Thêm phần tính power (0,64 khi tác động thật 5 điểm, n = 859/nhóm) vào `src/lab13.py`; viết mục 1–3 báo cáo nhóm.

### Bằng chứng

- File [report/team/ho_so_launch_v0.md](report/team/ho_so_launch_v0.md), [report/team/chi_so.md](report/team/chi_so.md) (E1 hai dòng tự đề xuất, E2), [report/team/bang_loi.md](report/team/bang_loi.md) (cột nhãn người 2, bảng khắc phục), [report/team/group_report.md](report/team/group_report.md), [PhanCong.md](PhanCong.md).
- Báo cáo cá nhân [report/team/2A202603822_DangNhatHuy.md](report/team/2A202603822_DangNhatHuy.md).

## NguyenTheBao-2A202603825

### Phần việc phụ trách

- **Chính:** CP3 · Nhiệm vụ C (người gắn nhãn 1, `report/team/bang_loi.md`).
- **Phụ:** CP1 (theo dõi điều kiện "Xong khi", kiểm tra nhãn `simulated`), CP4 (phối hợp ba luật dừng, `identifiability`, `rollback`), CP5 và duyệt chéo (đối chiếu chỉ số với danh sách event có `trace_id`).

### Đóng góp cụ thể

- Gắn nhãn độc lập đủ 20/20 ca ở cột "Nhãn người 1" (Do người dùng 4 · Hệ thống 5 · Ngữ cảnh 4 · Giới hạn hệ thống 4 · Ngầm 3).
- Đối chiếu ba luật dừng với tỉ lệ mở lại hiện tại (4,25% toàn mẫu, 3,97% trong phạm vi `noi_dia` + `hang_nang`): luật an toàn so với đối chứng +2 điểm, trần 6%, cửa sổ 3 ngày; luật chi phí 8.000 đ [simulated] trong 2 tuần; luật mức dùng 40% bỏ qua gợi ý trong 1 tuần.
- Kiểm tra chéo từng chỉ số E1 với event có `trace_id` và lọc lại CSV để đối chiếu tử số, mẫu số 994/1.200, 48/177, 51/1.200.

### Bằng chứng

- Commit `86d3d06` (gán nhãn) với 20 dòng ở cột "Nhãn người 1" trong [report/team/bang_loi.md](report/team/bang_loi.md).
- [report/team/pilot_plan.yaml](report/team/pilot_plan.yaml) (luật dừng, `identifiability`, `rollback`), [report/team/chi_so.md](report/team/chi_so.md) (kiểm tra chéo chỉ số ↔ event).
- Báo cáo cá nhân [report/team/2A202603825_NguyenTheBao.md](report/team/2A202603825_NguyenTheBao.md).

## HoVaTen-MSSV

### Phần việc phụ trách

-

### Đóng góp cụ thể

-

### Bằng chứng

-

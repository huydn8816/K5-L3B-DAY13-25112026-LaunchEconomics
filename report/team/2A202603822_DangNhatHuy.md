# Báo cáo cá nhân — DangNhatHuy-2A202603822

## 1. Thông tin thành viên

- Họ tên: Đặng Nhật Huy
- MSSV: 2A202603822
- Email: 26ai.huydn@vinuni.edu.vn
- Vai trong nhóm: Người gắn nhãn 2 kiêm giữ hồ sơ (Người 4 trong [PhanCong.md](../../PhanCong.md))

## 2. Phần việc phụ trách

- **Chính:** CP5 (Nhiệm vụ E: chỉ số tự đề xuất, rủi ro kinh tế, hồ sơ launch v0) và duyệt chéo Gate 2a.
- **Phụ:** CP1–CP4: điền dần hồ sơ launch v0 sau mỗi checkpoint; CP3: gắn nhãn độc lập 20 ca lỗi (người gắn nhãn 2).
- File phụ trách: [ho_so_launch_v0.md](ho_so_launch_v0.md), [chi_so.md](chi_so.md) (phần chỉ số tự đề xuất và E2), [phieu_cham.md](phieu_cham.md), [group_report.md](group_report.md); bộ nhãn người 2 trong [bang_loi.md](bang_loi.md).

## 3. Đóng góp cụ thể

- Dựng khung hồ sơ launch v0: bảy mục, người phụ trách là vai trò, trạng thái Giả lập cho các mục dựa trên cột `_simulated`.
- Đề xuất hai chỉ số: tỉ lệ nhân viên mở gợi ý của trợ lý (dùng) và tỉ lệ đơn hoàn sai tiền qua kiểm tra mẫu hằng tuần (an toàn).
- Viết ba dòng rủi ro kinh tế (làm lại tăng, xem lại không giảm, khối lượng thấp) với dấu hiệu theo dõi, hành động, người phụ trách.
- Gắn nhãn độc lập 20 ca lỗi (cột "Nhãn người 2"), đồng thuận 20/20 với người gắn nhãn 1; hoàn thiện bảng khắc phục 5 ca và thêm 2 event `handoff_to_staff`, `input_validation_failed` vào danh sách event.
- Điền số vào hồ sơ từ `bang_chi_phi.md` và `pilot_plan.yaml` sau khi chạy lại `src/lab13.py` để đối chiếu (4.472 đ, 0,49×, 4.599 đ = 0,38× [simulated]; 82,83% · 27,12% · 4,25%; n = 859/nhóm).
- Chốt đề xuất **Go có điều kiện** cho pilot `noi_dia` + `hang_nang`, nêu 3 con số bất lợi (xem lại 100% = 0,98× [simulated], power 0,64, mở lại hiện tại 4,25%) và 5 điều kiện có người phụ trách, ngày kiểm tra.
- Thêm phần tính power vào `src/lab13.py` (0,64 khi tác động thật 5 điểm, n = 859/nhóm).
- Gộp conflict khi merge `main` (`chi_so.md`, `TEAM.md`); cập nhật `TEAM.md` và báo cáo nhóm mục 1–5, 7, 8.
- Duyệt chéo Gate 2a: chuẩn bị [DuyetCheo.md](../../DuyetCheo.md); trả lời 10 câu hỏi của nhóm 7 ([TraLoi_Nhom7.md](../../TraLoi_Nhom7.md)); đọc hồ sơ nhóm 9, soạn 10 câu hỏi ([CauHoi_Nhom9.md](../../CauHoi_Nhom9.md)) và phiếu chấm [phieu_cham.md](phieu_cham.md) (30/30, Go có điều kiện).
## 4. Bằng chứng

Commit, file, bảng hoặc con số do bạn làm.

- [ho_so_launch_v0.md](ho_so_launch_v0.md) (7 mục và đề xuất), [chi_so.md](chi_so.md) (E1 hai dòng tự đề xuất, E2, 2 event bổ sung), [bang_loi.md](bang_loi.md) (cột nhãn người 2, quy tắc phân biệt, bảng khắc phục), [group_report.md](group_report.md), [PhanCong.md](../../PhanCong.md), phần power trong [src/lab13.py](../../src/lab13.py).
- Commit `965b383` trên nhánh `huydn` ("CP3, CP5: hồ sơ launch v0, chỉ số, bảng lỗi, báo cáo nhóm và cá nhân"): toàn bộ phần việc ở trên.
- Commit `07864f7` / `0c703c9`: bảng phân công [PhanCong.md](../../PhanCong.md).

## 5. Công cụ AI đã dùng

Công cụ nào, dùng vào việc gì, bạn tự kiểm tra kết quả ra sao.

- Claude Code: đọc tài liệu đề bài để lập danh sách đầu mục và bảng phân công 4 người; soạn khung hồ sơ launch v0, hai chỉ số tự đề xuất, ba dòng rủi ro E2, bản nháp đề xuất Go có điều kiện, bảng khắc phục 5 ca và báo cáo nhóm; điền số từ `bang_chi_phi.md`, `pilot_plan.yaml` vào hồ sơ; viết hàm tính power trong `lab13.py`; gộp conflict khi merge `main`. Không dùng AI để gắn nhãn 20 ca lỗi hay tạo con số: số trong hồ sơ lấy từ `src/lab13.py` của nhóm.
- Cách tự kiểm tra:
    - Chạy lại `cd src && python lab13.py` và so từng con số trong hồ sơ, `chi_so.md` với output của code (A2, A3, A4, B1–B4, D1, E1, tỉ lệ mở lại 4,25% / 3,97%).
    - Tính tay power ở mức 5 điểm với n = 859/nhóm (0,642) trước khi đưa con số 0,64 vào hồ sơ, rồi thêm phép tính vào `lab13.py`.
    - Đếm lại trên CSV số ca làm lại trong phạm vi `noi_dia` + `hang_nang` (48/982) trước khi đặt ngưỡng 7% trong rủi ro E2.
    - Kiểm tra `pilot_plan.yaml` đọc được bằng `yaml.safe_load`, không còn dấu `?` ngoài chú thích; tìm trong `report/team` không còn từ bị cấm theo quy tắc 5 của lab; mọi số từ cột `_simulated` có nhãn `simulated`.
    - Đọc lại phần AI soạn và chỉnh những chỗ chưa đúng tình trạng thực tế (ví dụ số event 9 → 11, nhãn `simulated` còn thiếu ở một con số).

## 6. Tự đánh giá

- **Làm tốt:** hồ sơ launch v0 đủ 7 mục, mỗi mục có con số chính, trạng thái và vai trò phụ trách; đề xuất nêu thẳng 3 con số bất lợi và có điều kiện xử lý cho từng điểm; dựng khung hồ sơ từ sớm nên khi có số chỉ cần điền và đối chiếu.
- **Cần cải thiện:** nhiều phần phải chờ số của nhóm, nên lần sau cần thống nhất sớm thứ tự push để giảm conflict khi merge; cần tự tay chạy và hiểu phần code tính chi phí, cỡ mẫu chứ không chỉ đọc kết quả.
- **Điều học được:** chi phí phải tính cho mỗi việc thành công, gồm cả giờ nhân viên (92,5% tổng chi phí [simulated]), không chỉ hoá đơn token; khi chia pilot theo cụm, số cụm mới quyết định cỡ mẫu hiệu dụng (20 nhân viên tối đa 1.000 < 1.251).

# Báo cáo cá nhân — NgoDuyKhanh-2A202603870

Copy file này và đổi tên theo quy tắc `MSSV_HoTen.md`. Giữ nguyên file mẫu.

Ví dụ: `20241234_NguyenVanAn.md`.

## 1. Thông tin thành viên

- Họ tên: Ngô Duy Khánh
- MSSV: 2A202603870
- Email: 26ai.khanhnd6@vinuni.edu.vn
- Vai trong nhóm (người viết code, người kiểm số, người gắn nhãn 1, người gắn nhãn 2 kiêm giữ hồ sơ): Người kiểm số (sau giải lao nhận viết code)

## 2. Phần việc phụ trách

- **Chịu trách nhiệm chính (Chính):** CP4 · Nhiệm vụ D — Tính cỡ mẫu theo cụm và xây dựng kế hoạch pilot (`report/team/pilot_plan.yaml`, code phần D1 trong `src/lab13.py`).
- **Phối hợp thực hiện (Phụ):**
  - **CP1 (Nhiệm vụ A):** Tính tay đối chiếu số liệu chi phí, điền bảng A1, A2, A3, A4 và câu trả lời vào `report/team/bang_chi_phi.md`, gắn nhãn `simulated`.
  - **CP2 (Nhiệm vụ B):** Điền bảng độ nhạy B1–B4 vào `report/team/bang_chi_phi.md`, tự kiểm tra quy tắc tuyến tính ("giảm một nửa = nửa mức tăng của gấp đôi").
  - **CP3:** Soát lại toàn bộ số liệu trong `report/team/bang_chi_phi.md` (đảm bảo độ lệch $\le 2\%$ so với đáp án chuẩn).
  - **CP5 (Nhiệm vụ E1):** Viết code và tính thử 3 chỉ số (chỉ số chính, tỉ lệ bỏ qua gợi ý, tỉ lệ lỗi lọt đến khách) trên tập 1.200 yêu cầu, cập nhật vào `report/team/chi_so.md`.

## 3. Đóng góp cụ thể

- **Kiểm số & hoàn thiện `bang_chi_phi.md` (CP1, CP2, CP3):**
  - Tính tay đối chiếu chi phí mỗi việc thành công (`4.373.585 đ ÷ 978 = 4.472 đ [simulated]`, gấp `16,3 lần` hoá đơn token + tool `274,7 đ/yêu cầu`) và chi phí cả hệ thống khi tính cả ca chuyển nhân viên (`5.865 đ/yêu cầu = 0,49× baseline`).
  - Điền đầy đủ bảng A1–A4 và B1–B4; phân tích rõ lý do loại bỏ `quoc_te` (`22.515 đ [simulated] = 1,88×`, chạy lại 3 lần tỉ lệ thành công giảm từ `30,0%` xuống `2,2%`) và `doi_tac` (`10.215 đ [simulated] = 0,85×`).
  - Xác minh kết quả giới hạn số lần chạy ở B3 (tối đa 2 lần chạy cho tổng chi phí hệ thống thấp nhất `6.901.220 đ [simulated]`, khác với giới hạn 1 lần có CPS thấp nhất `4.111 đ [simulated]`) và điểm hoà vốn khi xem lại 100% ở B4 (`≤ 5,1 phút` nếu làm lại 9 phút; `≤ 4,8 phút` nếu làm lại 15,3 phút).
- **Viết code CP4 & chủ trì `pilot_plan.yaml`:**
  - Viết hàm `co_mau()` trong `src/lab13.py` giải 5 câu D1: chia theo yêu cầu (`1.251` yc/nhóm), theo nhân viên $m=75$ ($DE=2,48 \rightarrow 3.103$ yc/nhóm $\rightarrow$ cần 42 người/nhóm, tổng 84 > 40 người), giới hạn 20 nhân viên/nhóm (tối đa `1.000` < 1.251), 6 depot/nhóm (tối đa `300`), và mức chênh 6 điểm (`859` yc/nhóm $\rightarrow m \ge 299$ yc/người, $DE=6,96$).
  - Tính tỉ lệ `mo_lai_trong_7_ngay` hiện tại (`4,25%` toàn mẫu, `3,97%` trong phạm vi `noi_dia + hang_nang`) để thiết lập luật dừng an toàn hợp lý (cao hơn đối chứng $\ge 2$ điểm hoặc vượt trần `6%`).
  - Hoàn thiện `report/team/pilot_plan.yaml` đủ các trường, 3 luật dừng chuẩn cấu trúc `NẾU – TRONG – THÌ – KHÔNG THÌ`, xoá toàn bộ dấu `?`.
- **Tính 3 chỉ số E1 (CP5):**
  - Viết code trong `src/lab13.py` và điền vào `report/team/chi_so.md`: Chỉ số chính đạt `82,83%` (994/1.200), Tỉ lệ bỏ qua gợi ý đạt `27,12%` (48/177), Tỉ lệ lỗi lọt đến khách đạt `4,25%` (51/1.200).

## 4. Bằng chứng

- Code tính toán CP4 (D1, tỉ lệ mở lại) và CP5 (3 chỉ số E1) trong `src/lab13.py` (dòng 156–198).
- Bảng số liệu và câu trả lời hoàn chỉnh A1–A4, B1–B4 trong `report/team/bang_chi_phi.md`.
- File kế hoạch pilot hoàn chỉnh `report/team/pilot_plan.yaml` (đầy đủ chú thích D1, D2, đánh đổi, 3 luật dừng, `simulated_inputs`).
- Kết quả tính thử 3 chỉ số E1 trong bảng Đặc tả chỉ số tại `report/team/chi_so.md`.

## 5. Công cụ AI đã dùng

- **Công cụ:** Trợ lý AI (Antigravity / Gemini).
- **Mục đích sử dụng:** Hỗ trợ kiểm tra công thức tính cỡ mẫu hiệu dụng khi phân cụm ($DE = 1 + (m - 1) \times \text{ICC}$), rà soát cú pháp YAML của `pilot_plan.yaml` và kiểm tra việc tuân thủ 5 quy tắc của bài lab (nhãn `simulated`, câu trả lời $\le 3$ dòng có số liệu, chỉ giới hạn ở phạm vi kế hoạch pilot).
- **Cách tự kiểm tra kết quả:** Tự tính tay lại các phép tính trọng tâm trên máy tính bỏ túi, kiểm tra điều kiện bất biến ở bảng độ nhạy (`mức giảm khi giảm một nửa = 1/2 mức tăng khi gấp đôi`), và chạy trực tiếp `python lab13.py` để đối chiếu toàn bộ đầu ra với số liệu chuẩn của bài lab (sai số $< 2\%$).

## 6. Tự đánh giá 

- Hoàn thành đầy đủ, chính xác 100% các nhiệm vụ được phân công của Người 2 (vai trò chính ở CP4 và vai trò phụ ở CP1, CP2, CP3, CP5).
- Các file sản phẩm (`bang_chi_phi.md`, `pilot_plan.yaml`, `chi_so.md`, `lab13.py`) đều đạt chuẩn điều kiện "Xong khi" trong `CHECKPOINTS.md` và đáp ứng trọn vẹn các tiêu chí chấm điểm trong `RUBRIC.md`.

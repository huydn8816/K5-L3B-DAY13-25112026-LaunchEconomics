# Báo cáo nhóm

Báo cáo ngắn, tối đa 2 trang. Số liệu chi tiết nằm trong các file hồ sơ; ở đây chỉ dẫn lại con số chính.

## 1. Thông tin nhóm

- Tên nhóm: 25112026 (nhóm 8)
- Lớp: L3B
- Thành viên: xem `TEAM.md`

## 2. Mục tiêu và cách tiếp cận

Mục tiêu là dựng bộ hồ sơ launch v0 cho trợ lý hoàn phí của LogiX-VN để hội đồng Gate 2a duyệt kế hoạch pilot. Hồ sơ trả lời bốn câu: có đáng chạy không, nhân viên có dùng không, khi hỏng thì sao, và pilot thiết kế thế nào để ra được quyết định. Dữ liệu là mẫu giả lập 1.200 yêu cầu và 1.624 lần chạy của agent.

Cách tiếp cận:

- Mọi con số do `src/lab13.py` của nhóm tính ra. Người kiểm số tính tay ít nhất một số mỗi bảng để đối chiếu; số tính từ cột `_simulated` đều ghi nhãn `simulated`.
- Chi phí tính cho một việc thành công, không cho một lần gọi mô hình: tử số cộng mọi lần chạy kể cả lần lỗi, cộng giờ xem lại và làm lại của nhân viên; mẫu số chỉ đếm yêu cầu thành công.
- Bốn vai theo `TEAM.md`, đổi người viết code sau giờ giải lao để ít nhất hai người tự tay tính được chi phí. Phân công chi tiết: [PhanCong.md](../../PhanCong.md).
- Hai người gắn nhãn lỗi độc lập, so nhãn sau.
- Tính cỡ mẫu cho cả ba cách chia trước rồi mới chọn cách chia pilot.

## 3. Giải pháp

| Nhiệm vụ | Nhóm đã làm gì | File |
| --- | --- | --- |
| A · Mô hình chi phí | Viết ba hàm A1 và qua ba phép thử đáp án biết trước; viết `mo_hinh()` tính token, tool, xem lại, làm lại từ trace; tách theo bốn loại yêu cầu (A3); cộng chi phí cố định 40 triệu đ/tháng cho phạm vi pilot (A4) | [src/lab13.py](../../src/lab13.py), [bang_chi_phi.md](bang_chi_phi.md) |
| B · Bảng độ nhạy | Gọi lại `mo_hinh()` cho 9 kịch bản đổi từng yếu tố, một kịch bản đổi cặp, giới hạn 1/2/3 lần chạy tính cả chi phí hệ thống, và kịch bản xem lại 100% | [bang_chi_phi.md](bang_chi_phi.md) |
| C · Bảng lỗi | Hai người gắn nhãn 20 ca độc lập theo năm loại của Google PAIR, tính đồng thuận, thống nhất ca không trùng; chọn 5 ca (mỗi loại một ca) để viết cách phát hiện đo được và người phụ trách | [bang_loi.md](bang_loi.md) |
| D · Pilot plan | Tính năm câu cỡ mẫu D1, trả lời năm câu "tách được tác động" D2, tính tỉ lệ mở lại hiện tại trước khi đặt luật an toàn, viết ba luật dừng NẾU – TRONG – THÌ – KHÔNG THÌ | [pilot_plan.yaml](pilot_plan.yaml) |
| E · Chỉ số, rủi ro, hồ sơ | Tính thử ba chỉ số, đề xuất thêm một chỉ số dùng và một chỉ số an toàn, liệt kê event có `trace_id`, ghi rủi ro kinh tế lấy số từ bảng độ nhạy, ghép thành hồ sơ một trang | [chi_so.md](chi_so.md), [ho_so_launch_v0.md](ho_so_launch_v0.md) |
| Duyệt chéo | Làm hội đồng chấm nhóm n + 1 theo thang 30 điểm | [phieu_cham.md](phieu_cham.md) |

## 4. Kết quả

Con số chính (ghi nhãn `simulated` khi cần) và đề xuất cuối của `ho_so_launch_v0.md`. Kết quả duyệt chéo nhóm nhận được từ hội đồng.

**Đề xuất của nhóm: Go có điều kiện** cho pilot chỉ gồm `noi_dia` + `hang_nang`, kèm 5 điều kiện có người phụ trách và ngày kiểm tra ([ho_so_launch_v0.md](ho_so_launch_v0.md)).

| Câu hỏi | Con số chính |
| --- | --- |
| Có đáng chạy không? | 4.472 đ mỗi việc thành công, gấp 16,3× hoá đơn token + tool chia số yêu cầu (274,7 đ) [simulated]; giờ nhân viên chiếm 92,5% [simulated]. Chi phí cả hệ thống 5.865 đ/yêu cầu = 0,49× của 12.000 đ [simulated] |
| Phạm vi | `noi_dia` 0,22×, `hang_nang` 0,69×; loại `quoc_te` 1,88× (thành công 27,3%, chạy lại không giúp) và `doi_tac` 0,85× [simulated]. Phạm vi pilot cộng cố định: 4.599 đ = 0,38× [simulated] |
| Yếu tố nhạy nhất | Số ca làm lại ±51,8% · tỉ lệ xem lại ±40,7% · lương +23,1%; giá token chỉ +5,6% [simulated] |
| Nhân viên có dùng không? | Chỉ số trong đợt chạy thử: chính 82,83% · bỏ qua gợi ý 27,12% · lỗi lọt đến khách 4,25%; 11 event có `trace_id` |
| Khi hỏng thì sao? | Đồng thuận gắn nhãn 20/20; 5 cách khắc phục, mỗi loại lỗi một cách |
| Pilot | Chia theo nhân viên, 20 + 20 cụm, n = 859/nhóm, mde 0,06; 3 luật dừng; ngày quyết định 2027-01-05 |
| Con số bất lợi | Xem lại 100%: 11.743 đ = 0,98× (12.415 đ = 1,03× nếu làm lại 15,3 phút/ca) [simulated]; power 0,64 nếu tác động thật chỉ 5 điểm |

**Kết quả duyệt chéo từ hội đồng:** nhóm hội đồng: Nhóm 7 · điểm: ... / 30 · quyết định: ...

Nhóm 7 đặt 10 câu hỏi (lợi ích ròng, độ nhạy khi số giả lập lệch 15%, kịch bản hai yếu tố bất lợi cùng lúc, lỗi gây thất thoát lớn nhất, quy trình chuyển về thủ công, ngưỡng No-go…). Nhóm 8 trả lời bằng số trong [TraLoi_Nhom7.md](../../TraLoi_Nhom7.md), ví dụ: hai yếu tố bất lợi nhất cùng lúc cho 8.607 đ/việc (+92,5%) = 0,72× [simulated], vượt ngưỡng 8.000 đ nên luật dừng chi phí kích hoạt; phút giả lập lệch +15% thì chi phí trong phạm vi lên 3.889 đ, kết luận không đổi [simulated]. Ba điểm nhóm nhận còn thiếu và bổ sung trước pilot: ngưỡng phát hiện nhân viên chấp nhận bừa, diễn tập cờ tắt, tách chi phí theo depot.

**Nhóm 8 làm hội đồng cho nhóm 9:** chấm 30/30, quyết định Go có điều kiện ([phieu_cham.md](phieu_cham.md)); câu hỏi: xem lại 100% (11.743 đ) có làm luật dừng chi phí 8.000 đ kích hoạt ngay ở hai tuần đầu không.

## 5. Khó khăn và cách xử lý

| Khó khăn | Cách xử lý |
| --- | --- |
| Nhiệm vụ sau phụ thuộc số của nhiệm vụ trước (B cần `mo_hinh` của A2, phạm vi pilot cần A3, rủi ro E2 cần B) | Người giữ hồ sơ dựng khung hồ sơ và các phần không cần số trước, để chỗ chờ ghi rõ chờ bước nào; điền số ngay khi `bang_chi_phi.md` có số và đối chiếu lại bằng cách chạy `lab13.py` |
| Nhiều người cùng sửa một file (`chi_so.md`, `TEAM.md`) gây conflict khi merge | Mỗi người làm trên nhánh riêng; khi conflict, giữ phần có số do code tính và gộp ý của cả hai bên thay vì chọn một bên |
| Máy của một thành viên chưa cài `statsmodels` khi cần tính power | Viết hàm power bằng thư viện chuẩn (Cohen's h, kiểm định z hai phía), cùng cách tính với `NormalIndPower`; máy có `statsmodels` in thêm dòng đối chiếu |

## 6. Tổng hợp đóng góp

Chi tiết đóng góp của từng thành viên nằm trong `TEAM.md`.

## 7. Hạn chế và hướng cải thiện

- **Phút xem lại và làm lại là số giả lập.** Mọi chi phí dựa trên hai cột `_simulated`; trong khi đó hai khoản này chiếm 92,5% tổng chi phí. Hướng cải thiện: sau tuần 1 của pilot, thay bằng phút đo thật từ event `staff_review_decision` và `staff_rework_completed` rồi tính lại.
- **Pilot chỉ thấy được mức chênh 6 điểm.** Với 40 nhân viên, không cách chia theo cụm nào đủ mẫu cho 5 điểm; nếu tác động thật là 5 điểm thì power chỉ khoảng 0,64. Hướng cải thiện: kéo dài pilot để mỗi nhân viên xử lý nhiều yêu cầu hơn, hoặc chạy lại với nhiều nhân viên hơn.
- **ICC 0,02 là giả định của đề.** Chưa ước lượng ICC từ dữ liệu theo `staff_id`; nếu ICC thật lớn hơn thì cỡ mẫu hiệu dụng còn nhỏ hơn. Hướng cải thiện: ước lượng ICC từ dữ liệu chạy thử trước khi chốt cỡ mẫu.
- **Chi phí mỗi việc thành công chưa có khoảng tin cậy.** Hướng cải thiện: bootstrap cho 4.472 đ và cho từng loại yêu cầu.
- **Chỉ số trong đợt chạy thử không có nhóm đối chứng**, nên 82,83% chưa nói được trợ lý có cải thiện so với 0,70 hay không; đó là việc pilot phải trả lời.

## 8. Tài liệu tham khảo

- Erol và cộng sự, *Cost-of-Pass: An Economic Framework for Evaluating Language Models*, [arxiv.org/abs/2504.13359](https://arxiv.org/abs/2504.13359).
- Google PAIR, *People + AI Guidebook*, chương "Errors + Graceful Failure", [pair.withgoogle.com](https://pair.withgoogle.com).
- Tài liệu statsmodels, lớp `NormalIndPower` (mục `stats.power`).
- Tài liệu lab: [docs/du_lieu_va_cong_thuc.md](../../docs/du_lieu_va_cong_thuc.md), [docs/Lab13_Huong_dan_chi_tiet_buoi_chieu.md](../../docs/Lab13_Huong_dan_chi_tiet_buoi_chieu.md), `docs/Ngay13_Lab13_De_bai_hoc_vien.docx`, `docs/Ngay13_Slide_Launch_Economics.pdf`.

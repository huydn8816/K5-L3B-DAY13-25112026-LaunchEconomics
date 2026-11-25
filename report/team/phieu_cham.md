# Phiếu chấm hội đồng Gate 2a

Nhóm số n chấm nhóm số n + 1; nhóm cuối chấm nhóm 1. Chấm theo bằng chứng trong hồ sơ, không theo cách trình bày: một đề xuất No-go có lý do bằng số được điểm cao hơn một đề xuất Go bỏ qua con số bất lợi.

- Nhóm chấm (hội đồng): Nhóm 8 (25112026)
- Nhóm được chấm: Nhóm 9 (Hihihuhu), repo `minhh25/K5-L3B-DAY13-Hihihuhu-LaunchEconomics`, nhánh `main`

| Tiêu chí | 0 điểm | 5 điểm | 10 điểm | Điểm | Lý do (có số) |
| --- | --- | --- | --- | ---: | --- |
| Đề xuất khớp bằng chứng | Mâu thuẫn với số của chính nhóm | Khớp nhưng bỏ qua một con số bất lợi | Khớp, nêu cả con số bất lợi và cách xử lý | 10 | Go có điều kiện chỉ cho `noi_dia` + `hang_nang`, khớp A3 (loại `quoc_te` 1,88×, `doi_tac` 0,85×, simulated). Nêu cả ba con số bất lợi: xem lại 100% = 11.743–12.415 đ (simulated), power 0,64 nếu tác động thật 5 điểm, cố định 15.266 đ/việc ở bước 4 người (simulated); mỗi điểm có điều kiện, người phụ trách, ngày kiểm tra |
| Số giả lập và phạm vi | Không nhãn; phạm vi "mọi yêu cầu" | Có nhãn hoặc có thu hẹp phạm vi | Nhãn ở mọi số giả lập; phạm vi thu hẹp có lý do bằng số | 10 | Mọi chi phí ghi `simulated`, mục 1, 2, 3, 7 trạng thái Giả lập; `simulated_inputs` liệt kê 7 đầu vào giả lập. Phạm vi thu hẹp có lý do bằng số: `noi_dia` 0,22× (thành công 95,0%), `hang_nang` 0,69× (74,1%). Điểm trừ nhỏ: mục 3 chưa ghi tỉ lệ so với 12.000 đ |
| Pilot ra được quyết định | Không đối chứng hoặc thiếu cỡ mẫu | Đủ cỡ mẫu, luật dừng chung chung | Tách được tác động, đủ mẫu, luật dừng có ngưỡng, thời hạn, người có quyền dừng | 10 | Chia ngẫu nhiên theo nhân viên 20 + 20, phân tầng theo depot, đối chứng chạy cùng thời gian; mde 0,06 với n = 859/nhóm (DE 6,96, ≥ 299 yêu cầu/người, 5.980 yêu cầu thô/nhóm) có ghi đánh đổi. 5 luật dừng đủ 4 vế, có ngưỡng (6%, +2 điểm, 8.000 đ, 40%), thời hạn và người dừng; rollback 30 phút. Điểm cần làm rõ: luật mở lại 6% xét theo một lần đánh giá hằng ngày ở bước 4 người (khoảng 123 yêu cầu/ngày) dễ dừng nhầm |
| **Tổng** | | | | **30 / 30** | |

**Quyết định của hội đồng:** Go có điều kiện

**Lý do:** Đề xuất khớp số của chính nhóm 9 và nêu thẳng các con số bất lợi (xem lại 100% = 0,98×–1,03×, power 0,64, cố định 1,27× ở bước 4 người; simulated). Hội đồng thêm hai điều kiện: (1) ghi tỉ lệ xem lại ở hai bước đầu và ngưỡng giảm xem lại, vì xem lại 100% (11.743 đ) vượt ngưỡng dừng chi phí 8.000 đ; (2) làm rõ luật mở lại 6% tính trên cohort một ngày hay cộng dồn, để pilot không dừng nhầm ở bước 4 người.

**Một câu hỏi cho đội trình:** Xem lại 100% tốn 11.743 đ/việc, cao hơn ngưỡng 8.000 đ. Hai tuần đầu nhân viên xem lại bao nhiêu %, luật dừng chi phí có kích hoạt ngay không?

**Câu trả lời của đội trình (ghi lại tại buổi):** Nhóm 9 trả lời 3 câu hỏi khác trong bộ câu hỏi của nhóm 8; câu hỏi chính ở trên (xem lại 100% so với ngưỡng 8.000 đ) chưa được trả lời tại buổi.

- **Tỉ lệ so với 12.000 đ:** 4.599 đ = 0,38× và 5.784 đ = 0,48× là chi phí trong phạm vi pilot đã cộng cố định; 5.865 đ = 0,49× là toàn mẫu, chưa cộng cố định. Trong phạm vi `noi_dia` + `hang_nang`: (3.072.513 + 82 × 12.000) / 982 ≈ 4.131 đ/yêu cầu = 0,34× (simulated, chưa cộng cố định). Hội đồng đối chiếu: đúng.
- **Chỉ số "gợi ý hiển thị":** nhóm 9 đồng ý chỉ số chỉ đo mức hiển thị; trong pilot sẽ nối `agent_suggestion_shown` với `staff_review_decision` (giữ / sửa / bỏ) và `refund_ledger_write` theo `trace_id`. Trong dữ liệu, 129/177 = 72,88% ca được xem lại giữ nguyên gợi ý, không suy rộng thành tỉ lệ nhân viên dùng trợ lý. Hội đồng đối chiếu: đúng; công thức trong hồ sơ chưa sửa.
- **Thu mẫu trùng Tết Dương lịch:** kéo dài thu mẫu và lùi ngày quyết định, giữ nhân viên trong nhánh đã phân, không loại người ít đơn; điều kiện đủ 20 nhân viên/nhánh, ≥ 299 yêu cầu/người, ≥ 5.980 yêu cầu thô/nhánh, kiểm tra lại DE và đủ 7 ngày theo dõi. Không đủ mẫu thì kết luận chưa đủ bằng chứng để mở rộng.

Các câu trả lời có số đúng và nhận điểm yếu; hội đồng giữ điểm 30/30 và quyết định Go có điều kiện.

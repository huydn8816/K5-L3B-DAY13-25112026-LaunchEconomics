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

**Câu trả lời của đội trình (ghi lại tại buổi):** ...

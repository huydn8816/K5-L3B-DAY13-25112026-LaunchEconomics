# Duyệt chéo Gate 2a · Chuẩn bị của nhóm 8 (25112026)

Nhóm n chấm nhóm n + 1 (nhóm cuối chấm nhóm 1). Nhóm mình (**nhóm 8**) vừa là **đội trình** bảo vệ hồ sơ trước **nhóm 7** (hội đồng của mình), vừa là **hội đồng** chấm và đặt câu hỏi cho **nhóm 9**. Chấm theo bằng chứng, không theo cách trình bày: một đề xuất No-go có lý do bằng số được điểm cao hơn một đề xuất Go bỏ qua con số bất lợi.

| Giờ | Việc | Ai làm |
| --- | --- | --- |
| 17:00 (10 phút) | Gửi hồ sơ nhóm 8 cho nhóm 7 (hội đồng của mình); nhận hồ sơ nhóm 9 | Huy |
| 17:10 (15 phút) | Đọc hồ sơ nhóm 9, chấm theo mục 2, ghi vào [report/team/phieu_cham.md](report/team/phieu_cham.md) | Cả nhóm, Huy ghi phiếu |
| 17:25 (15 phút) | Mỗi cặp 3 phút: đội trình 1 phút · hội đồng công bố 1 phút · đội trả lời 1 phút | Huy trình (mục 4), cả nhóm trả lời |
| 17:40 (5 phút) | Giảng viên chốt quyết định nào khớp bằng chứng; ghi kết quả vào `group_report.md` mục 4 | Huy |

## 1. Gửi gì cho nhóm 7 (hội đồng của nhóm 8)

- Link repo nhánh `main`: https://github.com/huydn8816/K5-L3B-DAY13-25112026-LaunchEconomics
- File chính: [report/team/ho_so_launch_v0.md](report/team/ho_so_launch_v0.md) (một trang, bảy mục, đề xuất).
- File bằng chứng: [bang_chi_phi.md](report/team/bang_chi_phi.md) · [bang_loi.md](report/team/bang_loi.md) · [pilot_plan.yaml](report/team/pilot_plan.yaml) · [chi_so.md](report/team/chi_so.md).

Trước khi gửi: đã merge `huydn` vào `main` chưa (hội đồng đọc `main`).

## 2. Checklist chấm nhóm 9

Đánh dấu khi đọc; mỗi tiêu chí chấm 0 / 5 / 10. Số đối chiếu lấy từ dữ liệu chung, nhóm bạn lệch quá 2% thì ghi vào lý do.

### Tiêu chí 1 · Đề xuất khớp bằng chứng (0 / 5 / 10)

- [ ] Đề xuất là đúng một trong ba: Go · Go có điều kiện · No-go.
- [ ] Đề xuất không mâu thuẫn với số của chính họ (ví dụ đề xuất Go cho mọi loại trong khi bảng A3 cho `quoc_te` 1,88×) → nếu mâu thuẫn: **0**.
- [ ] Có nêu con số bất lợi không? Ba con số hay bị bỏ qua:
    - Xem lại 100% đẩy chi phí lên khoảng 11.743 đ = 0,98× (B4).
    - Chia theo nhân viên 20 + 20 chỉ đủ mẫu cho mức chênh 6 điểm; nếu tác động thật 5 điểm thì power khoảng 0,64.
    - Tỉ lệ mở lại hiện tại 4,25%.
- [ ] Có cách xử lý cho con số bất lợi (điều kiện, người phụ trách, ngày kiểm tra)?
- Khớp nhưng bỏ qua một con số bất lợi: **5** · Khớp, nêu cả con số bất lợi và cách xử lý: **10**.

### Tiêu chí 2 · Số giả lập và phạm vi (0 / 5 / 10)

- [ ] Mọi số tính từ `phut_xem_lai_simulated`, `phut_lam_lai_simulated` có nhãn `simulated` (chi phí mỗi việc thành công, độ nhạy, B3, B4, A4, rủi ro).
- [ ] Hồ sơ mục 1, 2, 3, 7 có trạng thái "Giả lập".
- [ ] Phạm vi có thu hẹp không, hay vẫn "mọi yêu cầu"?
- [ ] Lý do thu hẹp có bằng số không (ví dụ `quoc_te` 1,88× và thành công 27,3%; `doi_tac` 0,85×)?
- Không nhãn, phạm vi mọi yêu cầu: **0** · Có nhãn hoặc có thu hẹp: **5** · Nhãn ở mọi số giả lập và thu hẹp có lý do bằng số: **10**.

### Tiêu chí 3 · Pilot ra được quyết định (0 / 5 / 10)

- [ ] Có nhóm đối chứng chạy cùng thời gian, chia ngẫu nhiên.
- [ ] Cỡ mẫu khớp cách chia: theo yêu cầu 1.251/nhóm; theo nhân viên m = 75 cần 3.103/nhóm (42 người/nhóm, không đủ); 20 nhân viên/nhóm tối đa 1.000; 6 depot/nhóm tối đa 300; mức chênh 6 điểm cần m ≥ 299.
- [ ] Ít nhất 20 cụm mỗi nhóm, hoặc ghi rõ đánh đổi đã chấp nhận. Chia theo depot (6 cụm) mà không ghi đánh đổi là điểm trừ.
- [ ] Ít nhất 3 luật dừng đủ bốn vế NẾU – TRONG – THÌ – KHÔNG THÌ, có ngưỡng, thời hạn, người có quyền dừng.
- [ ] Ngưỡng an toàn có nhìn tỉ lệ mở lại hiện tại 4,25% không? Ngưỡng tuyệt đối 1–3% sẽ dừng pilot ngay tuần đầu.
- [ ] Có rollback (ai bấm, bao lâu, khách được phục vụ bằng gì) và ngày quyết định.
- Không đối chứng hoặc thiếu cỡ mẫu: **0** · Đủ mẫu, luật dừng chung chung: **5** · Tách được tác động, đủ mẫu, luật dừng có ngưỡng, thời hạn, người dừng: **10**.

### Lỗi hay gặp cần soi thêm

- [ ] Viết "trợ lý đã nâng chỉ số từ 70% lên 82,8%": đợt chạy thử không có đối chứng.
- [ ] Chi phí chia cho 1.200 thay vì số việc thành công (978), hoặc chỉ gấp 1–2 lần hoá đơn (quên giờ nhân viên).
- [ ] So với 12.000 đ mà chưa cộng ca chuyển nhân viên (đúng là 5.865 đ/yêu cầu = 0,49×).
- [ ] Người phụ trách ghi "cả đội".
- [ ] Có từ bị cấm theo quy tắc 5 của lab.

## 3. Câu hỏi để hỏi nhóm 9

Phiếu chấm chỉ ghi **một câu hỏi**. Đọc hồ sơ nhóm 9 theo checklist mục 2, tìm điểm yếu nhất, rồi chọn câu tương ứng dưới đây. Câu tốt là câu buộc đội trình trả lời bằng một con số mà hồ sơ của họ chưa có.

| Nếu thấy trong hồ sơ nhóm 9 | Hỏi | Câu trả lời đúng cần có |
| --- | --- | --- |
| Đề xuất Go nhưng không nhắc B4 | "Chi phí mỗi việc thành công là bao nhiêu nếu tuần đầu phải xem lại 100%, và khi đó trợ lý còn rẻ hơn nhân viên không?" | Khoảng 11.743 đ = 0,98× [simulated]; cần kế hoạch giảm xem lại |
| Chia theo yêu cầu | "Cùng một nhân viên vừa dùng vừa không dùng trợ lý thì nhóm đối chứng có bị ảnh hưởng không? Nhóm giảm tràn tác động thế nào?" | Tràn tác động cao; nên chia theo nhân viên |
| Chia theo depot | "Với 6 depot mỗi nhóm, cỡ mẫu hiệu dụng tối đa là bao nhiêu, có đạt 1.251 không?" | 6 ÷ 0,02 = 300, không đạt; dưới 20 cụm |
| Chia 20 + 20 nhân viên nhưng vẫn ghi mde 0,05 | "20 nhân viên mỗi nhóm thì cỡ mẫu hiệu dụng tối đa bao nhiêu? Có thấy được mức chênh 5 điểm không?" | Tối đa 20 ÷ 0,02 = 1.000 < 1.251, không bao giờ đủ |
| Chọn mde 0,06 nhưng không nói power | "Nếu tác động thật chỉ 5 điểm, pilot của nhóm còn power bao nhiêu?" | Khoảng 0,64 |
| Ngưỡng an toàn tuyệt đối thấp (1–3%) | "Tỉ lệ mở lại trong đợt chạy thử là bao nhiêu? Với ngưỡng đó pilot có dừng ngay tuần đầu không?" | 4,25% (3,97% trong phạm vi); ngưỡng thấp hơn thì dừng ngay |
| Phạm vi gồm cả `quoc_te` | "Chi phí mỗi việc thành công của `quoc_te` so với 12.000 đ là bao nhiêu? Cho chạy lại tới 3 lần có giúp không?" | 22.515 đ = 1,88× [simulated]; tỉ lệ ok 30,0% → 11,4% → 2,2%, chạy lại không giúp |
| So với 12.000 đ bằng 0,37× | "Con số so sánh đã cộng 222 ca chuyển nhân viên chưa?" | Chưa; đúng là 5.865 đ/yêu cầu = 0,49× [simulated] |
| Viết "trợ lý đã nâng chỉ số lên 82,8%" | "Đợt chạy thử có nhóm đối chứng không? Vì sao 82,8% chưa chứng minh trợ lý cải thiện?" | Không có đối chứng; chênh có thể do loại yêu cầu, mùa vụ, chọn depot |
| Luật dừng thiếu vế hoặc không có người dừng | "Ai có quyền tắt trợ lý, trong bao lâu, và nếu không làm thì việc gì bị cấm?" | Đủ 4 vế NẾU – TRONG – THÌ – KHÔNG THÌ, một vai trò cụ thể |
| Thiếu nhãn `simulated` | "Con số … tính từ cột nào? Nếu phút xem lại thật dài hơn giả lập thì kết luận có đổi không?" | Từ cột `_simulated`, phải ghi nhãn; xem lại là yếu tố nhạy thứ 2 (±40,7%) |
| Người phụ trách là "cả đội" | "Nếu luật dừng kích hoạt lúc 2 giờ sáng, cụ thể ai bấm tắt?" | Một vai trò có quyền quyết định |

**Câu hỏi dự phòng** (khi hồ sơ nhóm 9 không có lỗi rõ): "Pilot cần bao nhiêu ngày để mỗi nhân viên xử lý đủ số yêu cầu theo cỡ mẫu của nhóm, và ngày quyết định có kịp không?"

**Ghi lại khi chấm:** mỗi tiêu chí một lý do có số, ví dụ "Tiêu chí 3: 5 điểm, chia theo depot 6 cụm, tối đa 300 < 1.251, không ghi đánh đổi".

## 4. Nhóm 8 bảo vệ hồ sơ trước nhóm 7

### Trình bày 1 phút

> Nhóm đề xuất **Go có điều kiện** cho pilot chỉ gồm nội địa và hàng nặng. Chi phí thật là 4.472 đ mỗi việc thành công, gấp 16 lần hoá đơn token, vì 92,5% là giờ nhân viên [simulated]. Trong phạm vi pilot, cộng cả chi phí cố định là 4.599 đ, bằng 0,38 lần nhân viên tự làm [simulated]. Loại quốc tế bị loại vì 1,88× và chạy lại không giúp. Ba con số bất lợi nhóm không bỏ qua: xem lại 100% thì lên 0,98×; pilot 20 + 20 nhân viên chỉ thấy được mức chênh 6 điểm, power 0,64 nếu tác động thật là 5 điểm; tỉ lệ mở lại hiện tại đã 4,25% nên luật an toàn so với đối chứng. Năm điều kiện xử lý từng điểm, mỗi điều kiện có người phụ trách và ngày kiểm tra.

### Câu hỏi có thể bị hỏi và câu trả lời

| Câu hỏi | Trả lời ngắn (có số) |
| --- | --- |
| Vì sao tử số tính mọi lần chạy, mẫu số chỉ đếm việc thành công? | Lần chạy lỗi vẫn tốn token, tool và giờ nhân viên; chi phí phải tính cho một kết quả đúng, nên chia cho 978 việc thành công chứ không chia 1.200 |
| Xem lại 100% thì sao? | 11.743 đ = 0,98× (12.415 đ = 1,03× nếu làm lại 15,3 phút/ca) [simulated]; vì vậy điều kiện 5 giảm xem lại theo bậc khi sửa + bỏ dưới 15% và phút xem lại dưới 5,1 |
| Vì sao không chia theo yêu cầu cho đủ 1.251? | Cùng một nhân viên vừa dùng vừa không dùng trợ lý, tác động tràn sang nhóm đối chứng; chia theo nhân viên tách được tác động |
| Vì sao không chia theo depot? | Chỉ 6 cụm mỗi nhóm, cỡ mẫu hiệu dụng tối đa 6 ÷ 0,02 = 300, dưới mốc 20 cụm |
| Cỡ mẫu hiệu dụng khi chia theo cụm tính thế nào? | c × m ÷ (1 + (m − 1) × ICC); với 20 nhân viên, m = 299: 20 × 299 ÷ 6,96 ≈ 859; luôn nhỏ hơn c ÷ ICC = 1.000 |
| Ngưỡng an toàn có dừng pilot ngay tuần đầu không? | Không: so với đối chứng (cao hơn ≥ 2 điểm) kèm trần tuyệt đối 6%, trên mức hiện tại 4,25% |
| Giới hạn số lần chạy nào tốt nhất? | 2 lần rẻ nhất cho công ty (6.901.220 đ) [simulated]; 1 lần cho chi phí mỗi việc thấp nhất nhưng đẩy thêm 85 việc sang nhân viên |
| 82,83% có nghĩa trợ lý đã cải thiện từ 70%? | Không: đó là chỉ số trong đợt chạy thử, không có đối chứng; pilot mới trả lời được |
| Chi phí cố định có đổi kết luận không? | Không ở 45.000 yêu cầu/tháng (0,38×); khối lượng còn một nửa thì 0,48× [simulated], nên có rủi ro E2 dòng 3 |

### Câu hỏi khó nhắm vào điểm yếu của hồ sơ nhóm 8

Nhóm 7 sẽ tìm chỗ yếu nhất. Các câu dưới đây là chỗ hồ sơ mình dễ bị hỏi; trả lời thẳng, nhận điểm yếu rồi chỉ ra cách xử lý đã có trong hồ sơ.

| Câu hỏi | Trả lời ngắn (có số) |
| --- | --- |
| Xem lại 100% đã 0,98×, sao không đề xuất No-go? | Gate 2a chỉ duyệt kế hoạch pilot; pilot là để học tỉ lệ xem lại giảm được tới đâu. Nhóm không mở rộng nếu không giảm được: điều kiện 5 chặn bước 0,50 khi sửa + bỏ chưa dưới 15%, và luật dừng chi phí thu hẹp về `noi_dia` khi chi phí mỗi việc thành công trên 8.000 đ trong 2 tuần [simulated] |
| `hang_nang` chỉ thành công 74,1% và 0,69×, sao vẫn đưa vào? | Vẫn dưới 1× của 12.000 đ [simulated]; nếu chi phí vượt ngưỡng thì luật dừng thứ 2 bỏ `hang_nang`, chỉ giữ `noi_dia` (0,22×) |
| Pilot có kịp đủ mẫu trước ngày quyết định 2027-01-05 không? | Trong phạm vi có khoảng 1.500 × 982 ÷ 1.200 ≈ 1.228 yêu cầu/ngày, tức khoảng 31 yêu cầu/nhân viên/ngày; cần ≥ 299 yêu cầu mỗi nhân viên, khoảng 10 ngày làm việc sau khi lên bước 0,50. Sát nút: nếu chưa đủ 299 thì lùi ngày quyết định, không kết luận sớm |
| Dữ liệu chạy thử ở 6 depot, pilot ở 12 depot thì số có còn đúng? | Chưa chắc: đó là lý do mọi chi phí ghi `simulated` và điều kiện 4 thay phút giả lập bằng phút đo thật sau tuần 1; bốc thăm phân tầng theo depot để hai nhóm cân bằng |
| Ngưỡng 7% làm lại và 15% sửa + bỏ lấy từ đâu? | 7% ≈ 1,5 lần tỉ lệ làm lại đợt chạy thử (48/982 = 4,9%); 15% là khoảng một nửa tỉ lệ sửa + bỏ hiện tại (27,12%), mức nhóm chấp nhận để giảm xem lại. Cả hai là lựa chọn của nhóm, ghi trước khi chạy |
| Vì sao chỉ kiểm tra giữa kỳ chỉ số an toàn? | Xem chỉ số chính nhiều lần rồi dừng khi thấy tốt làm tăng sai lầm loại 1 (alpha 0,05); chỉ số an toàn thì phải xem sớm để bảo vệ khách |
| Đồng thuận 20/20 có quá đẹp không? | Hai người gắn độc lập theo nguyên nhân gốc; các ca dễ lẫn (6, 9, 13, 8, 15, 12, 18) đều có quy tắc phân biệt ghi trong `bang_loi.md`, hội đồng có thể hỏi lý do từng ca |
| Ngày kiểm tra các điều kiện dựa vào đâu? | Lấy ngày bắt đầu giả định 2026-12-08, lùi từ ngày quyết định 2027-01-05; các điều kiện kỹ thuật phải xong trước ngày bắt đầu |

## 5. Sau buổi duyệt chéo

- [ ] `phieu_cham.md`: đủ điểm 3 tiêu chí, tổng / 30, quyết định, lý do có số, một câu hỏi, câu trả lời của đội trình.
- [ ] `group_report.md` mục 4: nhóm hội đồng (nhóm 7), điểm nhận được, quyết định, câu hỏi và câu trả lời.
- [ ] Commit, push, merge vào `main` trước 23h59 GMT+7.

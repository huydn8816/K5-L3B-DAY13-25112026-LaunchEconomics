# Nhóm 8 trả lời câu hỏi của hội đồng nhóm 7 · Gate 2a

Mọi số tính từ `src/lab13.py` và hai file CSV của lab; số dựa trên phút xem lại, làm lại ghi `simulated`.

**1. 424 lần chạy lại chiếm bao nhiêu phần trăm tổng chi phí, và nhóm giảm tỷ lệ này bằng cách nào?**
424 lần chạy lại tốn 93.804 đ, chỉ **2,1%** tổng chi phí 4.373.585 đ (simulated), nhưng bằng 28,5% hoá đơn token + tool. Gần một nửa (198/424) là `quoc_te`, nên loại `quoc_te` và `doi_tac` khỏi pilot đã bỏ 258/424 lần chạy lại. Ngoài ra, luật dừng chi phí giới hạn tối đa 2 lần chạy (B3: rẻ nhất cho hệ thống, 6.901.220 đ, simulated).

**2. Những con số nào trong hồ sơ là simulated, và kết luận có đổi nếu thực tế lệch 15% không?**
Simulated là mọi số dựa trên phút xem lại và làm lại: chi phí mỗi việc thành công, bảng A3, A4, B1–B4 và 3 dòng rủi ro. Nếu phút thật cao hơn 15%, chi phí mỗi việc thành công tăng từ 4.472 đ lên **5.092 đ (+13,9%)**; trong phạm vi pilot từ 3.414 đ lên 3.889 đ, vẫn khoảng 0,3× của 12.000 đ (simulated): **kết luận không đổi**. Riêng kịch bản xem lại 100% thì lên 13.467 đ = 1,12×, nên điều kiện giảm xem lại theo bậc là bắt buộc.

**3. So với nhân viên tự làm, trợ lý tiết kiệm ròng bao nhiêu đồng/ngày trên 1.500 yêu cầu?**
Trong phạm vi pilot (khoảng 1.228 yêu cầu/ngày), chi phí cả hệ thống là 4.131 đ/yêu cầu, đã gồm ca nhân viên làm thay. So với 12.000 đ, trợ lý tiết kiệm khoảng **9,66 triệu đ/ngày**; trừ chi phí cố định 1,33 triệu đ/ngày (40 triệu/tháng) còn khoảng **8,33 triệu đ/ngày** (simulated). 272 yêu cầu `quoc_te`, `doi_tac` còn lại vẫn do nhân viên làm, không tính tiết kiệm.

**4. Nhóm dựa vào đâu để tin rằng 6 depot còn lại không có ca phức tạp hơn làm đội chi phí?**
Nhóm chưa có dữ liệu để tin như vậy: mẫu chỉ có 6 depot (D01–D06), tỉ lệ thành công dao động 77,8%–85,7%. Vì vậy pilot bốc thăm phân tầng theo depot, thay phút giả lập bằng phút đo thật sau tuần 1, và luật dừng chi phí (> 8.000 đ trong 2 tuần) chặn nếu tổng chi phí bị đội lên. Nhóm sẽ bổ sung tách chi phí theo depot để thấy depot nào kéo chi phí.

**5. Nếu hai yếu tố bất lợi nhất trong bảng độ nhạy xảy ra cùng lúc, chi phí mỗi việc thành công là bao nhiêu?**
Làm lại gấp đôi và xem lại gấp đôi cùng lúc: **8.607 đ (+92,5%)** = 0,72× của 12.000 đ (simulated), bằng tổng hai tác động riêng (+51,8% + 40,7%) vì mô hình cộng tuyến tính. Con số này vượt ngưỡng 8.000 đ, nên luật dừng chi phí sẽ kích hoạt và thu hẹp về `noi_dia`.

**6. Loại lỗi nào gây thất thoát tiền trực tiếp lớn nhất, và ai chịu trách nhiệm xử lý?**
Lỗi **Hệ thống**, ca hoàn hai lần do thiếu khoá chống trùng: mỗi ca mất trọn số tiền hoàn. Kỹ sư trưởng agent sửa khoá chống trùng trước ngày bắt đầu (điều kiện 1, kiểm tra 2026-12-04); trong pilot, chỉ 1 ca hoàn trùng là Giám đốc vận hành tắt trợ lý. Lỗi **Ngầm** (bảng giá cũ: 212 đơn × 1.000–2.000 đ) nhỏ hơn mỗi ca nhưng cộng dồn, do Kế toán trưởng kiểm tra mẫu 100 đơn/tuần.

**7. Khi trợ lý lỗi hàng loạt vào giờ cao điểm, quy trình chuyển về làm thủ công mất bao lâu?**
Giám đốc vận hành bấm cờ tắt, hiệu lực trong **30 phút**; khách được phục vụ bằng luồng nhân viên tự làm như hiện nay. Vì pilot chia theo nhân viên, chỉ 20/40 người bị ảnh hưởng, 20 người đối chứng vẫn làm thủ công bình thường. Nhóm cần diễn tập cờ tắt một lần trước ngày bắt đầu để xác nhận con số 30 phút.

**8. Thời lượng pilot hiện tại có đủ tránh nhiễu theo ngày trong tuần và mùa vụ không?**
Mỗi bước rollout kéo dài trọn 1 tuần nên mỗi bước có đủ các ngày trong tuần. Nhóm đối chứng chạy cùng thời gian nên nhiễu mùa vụ tác động cả hai nhánh như nhau và bị trừ đi khi so. Hạn chế: pilot rơi vào cuối năm (Tết Dương lịch), nên kết quả có thể chưa đại diện cho tháng bình thường.

**9. Nhóm dùng chỉ số nào để chặn việc nhân viên bấm chấp nhận bừa cho đủ KPI?**
**Tỉ lệ sai tiền trong các ca nhân viên bấm "giữ", tính theo từng `staff_id`.** Mỗi tuần, trong mẫu 100 đơn kiểm tra, Kế toán trưởng kiểm tra các ca có `staff_review_decision` = `giu` (event `audit_sample_checked`). Nhân viên nào có tỉ lệ sai cao hơn mức chung của nhóm thì đang chấp nhận mà không đọc, kể cả khi KPI tốc độ đẹp. Trưởng nhóm CSKH rà lại các ca của người đó.

**10. Chỉ số nào sau pilot chạm ngưỡng sẽ buộc nhóm phải ra quyết định No-Go ngay lập tức?**
Chỉ số an toàn: mở lại 7 ngày của nhóm trợ lý cao hơn đối chứng **≥ 2 điểm** hoặc vượt **6%**, hoặc có **≥ 1 ca hoàn trùng**, trong 3 ngày liên tiếp: Giám đốc vận hành tắt trợ lý trong 30 phút. Ở ngày quyết định 2027-01-05, nếu chỉ số chính không tăng có ý nghĩa so với đối chứng (mức chênh nhóm thiết kế để thấy là 6 điểm), nhóm đề xuất No-go.

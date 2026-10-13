# SỬA LỖI BUỔI PLANNING POKER CHO CÁC CHỨC NĂNG ĐẶT XE (RikkeiGo)

**Vai trò:** Lan (Scrum Master) rà soát biên bản Planning Poker
**Thang của đội:** 1, 2, 3, 5, 8, 13, 21 | **Reference Story:** "Xem lịch sử chuyến đi" = 3 SP

---

## Phần 1 – Phân tích

| Mã | Hợp lý / Chưa hợp lý | Quy tắc bị vi phạm | Hậu quả khi lập kế hoạch Sprint |
|----|----------------------|--------------------|----------------------------------|
| **P1** | **Chưa hợp lý** | (1) Thẻ lệch nhau là tín hiệu tìm giả định và rủi ro, không phải để lấy trung bình. (2) Kết quả chốt phải là một giá trị trên thang của đội: 4 SP không thuộc thang. | Giá trị 4 SP không tồn tại trên thang nên không so sánh được với các PBI khác và làm sai tổng SP / velocity của Sprint. Việc lệch 3 so với 5 không được thảo luận nên giả định ẩn (ví dụ cách xác thực số điện thoại) vẫn chưa lộ ra, dễ phát sinh việc ngoài dự kiến giữa Sprint. |
| **P2** | **Chưa hợp lý** | (1) Developers là người chọn thẻ; Product Owner chỉ làm rõ giá trị và phạm vi, không quyết định SP. (2) Thẻ lệch nhau (5 so với 13) phải được giải thích để tìm rủi ro, không bị bỏ qua vì lý do tiến độ. | SP bị ép theo kế hoạch thay vì theo độ lớn thực tế. Nếu thực tế gần 13 SP, đội sẽ cam kết quá sức, rủi ro tích hợp ví RikkeiPay bị bỏ sót, PBI có thể không hoàn thành trong Sprint và velocity bị méo. |
| **P3** | **Hợp lý** | Không vi phạm. | Đội làm đúng quy trình: người chọn thấp nhất (3) và cao nhất (8) giải thích, sau đó chọn lại và đạt đồng thuận 5 · 5 · 5 · 5 → 5 SP, một giá trị thuộc thang. **Không sửa.** |
| **P4** | **Chưa hợp lý** (số 13 SP đúng, ghi chú sai) | SP là độ lớn tương đối, không quy đổi cố định sang giờ hoặc ngày. | Ghi chú "13 SP = 52 giờ" dễ bị hiểu thành cam kết thời gian cố định. Khi đó có thể dùng nó để phân bổ người và deadline, sai khi năng lực đội thay đổi, và làm mất ý nghĩa ước lượng tương đối. Con số 13 SP vẫn dùng được để xếp vào Sprint. |
| **P5** | **Chưa hợp lý** | (1) PBI chưa đủ rõ thì làm rõ thêm rồi mới ước lượng. (2) Thẻ lệch nhau không được chốt theo đa số (thực tế 13 mới chỉ có 2/4 phiếu, chưa phải đa số). | 13 SP được chốt khi chưa biết mã có dùng chung với khuyến mãi khác hay không, nên con số dựa trên phỏng đoán. Khi vào Sprint, phạm vi có thể đổi, dẫn đến làm lại, trễ hoặc vượt ước lượng; cam kết Sprint thiếu tin cậy. |

---

## Phần 2 – Sửa lỗi

**P1 – Đăng nhập bằng số điện thoại**
Lan yêu cầu người chọn 3 và người chọn 5 nói rõ giả định của mình (ví dụ: có gửi OTP không, xử lý số điện thoại sai thế nào), Đức (PO) làm rõ phạm vi nếu được hỏi. Sau đó Developers chọn lại thẻ cho đến khi đồng thuận một giá trị trên thang (3 hoặc 5), không lấy trung bình.

**P2 – Thanh toán bằng ví RikkeiPay**
Bỏ kết quả 5 SP do PO chọn. Đức chỉ làm rõ giá trị và phạm vi (các trường hợp thanh toán cần hỗ trợ, thời hạn mong muốn); người chọn 5 và người chọn 13 giải thích rủi ro (ví dụ: tích hợp API ví, xử lý thanh toán lỗi / hoàn tiền) rồi Developers chọn lại. Kết quả do Developers quyết định, không điều chỉnh để khớp kế hoạch.

**P4 – Theo dõi vị trí tài xế trên bản đồ**
Giữ nguyên 13 SP nhưng xóa ghi chú "13 SP = 52 giờ" khỏi biên bản. Lan nhắc đội rằng SP là độ lớn tương đối; nếu cần dự đoán thời gian, dựa trên velocity của các Sprint trước chứ không quy đổi cố định.

**P5 – Áp mã giới thiệu bạn bè**
Hủy kết quả 13 SP và tạm hoãn ước lượng. Đức (PO) làm rõ điều chưa biết: mã có được dùng cùng khuyến mãi khác không, giới hạn số lần dùng và điều kiện áp dụng. Sau đó Developers chọn thẻ lại, người chọn thấp và cao giải thích, lặp lại đến khi đồng thuận một giá trị trên thang, không chốt theo đa số.

---

*P3 được giữ nguyên vì đã chốt đúng quy trình Planning Poker.*

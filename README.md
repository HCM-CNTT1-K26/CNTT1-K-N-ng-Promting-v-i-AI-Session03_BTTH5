# CNTT1-K-N-ng-Promting-v-i-AI-Session03_BTTH5

### Phần 1: Hai mẫu Prompt

**Prompt 1: Zero-shot**

 Cửa hàng đồ công nghệ của tôi nhận được nhiều bình luận trên Facebook và cần phân loại để ưu tiên xử lý. Hãy giúp tôi phân loại 5 phản hồi dưới đây theo quy tắc sau:
 * Tích cực: Khách khen ngợi, hài lòng.
 * Tiêu cực: Khách chê, phàn nàn, không hài lòng.
 * Yêu cầu hỗ trợ: Khách cần giải quyết một vấn đề cụ thể.
 
 
 Danh sách phản hồi:
 1. "Sản phẩm đẹp, giao hàng nhanh, rất hài lòng."
 2. "Tôi đã đặt hàng 5 ngày nhưng chưa nhận được."
 3. "Tai nghe không kết nối được Bluetooth."
 4. "Nhân viên tư vấn rất nhiệt tình."
 5. "Tôi muốn hoàn tiền vì sản phẩm bị lỗi."
 
 
 Trình bày kết quả thành bảng gồm 4 cột: STT, Phản hồi, Nhãn phân loại, Lý do.

**Prompt 2: Few-shot (3 ví dụ mẫu)**

 Cửa hàng đồ công nghệ của tôi cần phân loại bình luận khách hàng trên Facebook. Hãy dựa vào các ví dụ mẫu và quy tắc dưới đây để phân loại 5 phản hồi bên dưới.
 Quy tắc:
 * Tích cực: Khách khen ngợi, hài lòng.
 * Tiêu cực: Khách chê, phàn nàn, không hài lòng.
 * Yêu cầu hỗ trợ: Khách cần giải quyết một vấn đề cụ thể.
 
 
 Ví dụ mẫu:
 * "Loa nghe rất êm, shop đóng gói kỹ." -> Nhãn: Tích cực | Lý do: Khách khen chất lượng sản phẩm và cách đóng gói.
 * "Dây sạc mới dùng 2 ngày đã đứt, làm ăn chán quá." -> Nhãn: Tiêu cực | Lý do: Khách phàn nàn về độ bền sản phẩm.
 * "Shop hướng dẫn mình cách kết nối lại chuột không dây với." -> Nhãn: Yêu cầu hỗ trợ | Lý do: Khách cần hỗ trợ kỹ thuật cụ thể.
 
 
 Danh sách cần phân loại:
 1. "Sản phẩm đẹp, giao hàng nhanh, rất hài lòng."
 2. "Tôi đã đặt hàng 5 ngày nhưng chưa nhận được."
 3. "Tai nghe không kết nối được Bluetooth."
 4. "Nhân viên tư vấn rất nhiệt tình."
 5. "Tôi muốn hoàn tiền vì sản phẩm bị lỗi."
 
 
 Xuất kết quả ra bảng gồm các cột: STT, Phản hồi, Nhãn phân loại, Lý do.

---

### Phần 2: Bảng kết quả phân loại

| STT | Phản hồi | Nhãn phân loại | Lý do |
| --- | --- | --- | --- |
| 1 | "Sản phẩm đẹp, giao hàng nhanh, rất hài lòng." | Tích cực | Khách khen sản phẩm đẹp, giao nhanh và tỏ ra hài lòng. |
| 2 | "Tôi đã đặt hàng 5 ngày nhưng chưa nhận được." | Tiêu cực | Khách phàn nàn vì đơn hàng bị giao chậm trễ. |
| 3 | "Tai nghe không kết nối được Bluetooth." | Yêu cầu hỗ trợ | Khách báo lỗi kỹ thuật và cần được hướng dẫn cách khắc phục. |
| 4 | "Nhân viên tư vấn rất nhiệt tình." | Tích cực | Khách khen ngợi thái độ phục vụ của nhân viên. |
| 5 | "Tôi muốn hoàn tiền vì sản phẩm bị lỗi." | Yêu cầu hỗ trợ | Khách yêu cầu giải quyết thủ tục hoàn tiền cho sản phẩm hỏng. |

---

### Phần 3: So sánh kết quả Zero-shot và Few-shot

* **Độ chính xác:** Với các câu khen rõ ràng như câu 1 và 4, cả hai cách đều làm tốt. Tuy nhiên, ở các câu dễ gây nhầm lẫn như câu 3 và 5, **Few-shot** phân loại chuẩn hơn. Nhờ có ví dụ mẫu làm mốc, AI phân biệt được đâu là lời phàn nàn đơn thuần (Tiêu cực) và đâu là trường hợp khách cần shop can thiệp xử lý (Yêu cầu hỗ trợ). Zero-shot đôi khi dễ gộp nhầm câu 5 sang nhóm Tiêu cực vì có từ "lỗi".
* **Tính nhất quán:** **Few-shot** cho kết quả ổn định hơn hẳn qua nhiều lần chạy. Các ví dụ mẫu giúp AI hiểu đúng ý người hỏi về cách giải thích lý do và tiêu chuẩn gán nhãn. Ngược lại, **Zero-shot** chỉ dựa vào định nghĩa ngắn gọn nên cách diễn đạt lý do và ranh giới giữa các nhãn dễ bị thay đổi nếu chạy lại nhiều lần.

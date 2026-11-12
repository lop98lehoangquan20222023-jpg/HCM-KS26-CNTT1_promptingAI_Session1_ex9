# Phần 1:Nguyên nhân gây ảo giác
- AI không có tài liệu phải dự đoán dựa trên dữ liệu chung -> dễ bị ảo giác (Hallucination)và đưa ra con số sai.
# Phần 2:Giải pháp (dùng RAG Grounding)
- Ép AI đọc văn bản có nguồn và chỉ được trả lời dựa trên nó.
- Mẫu prompt:

[VĂN BẢN GỐC]
"Điều 8: Nhà cung cấp giao rau bị dập nát trên 10% thì bị phạt 5% giá trị lô bị dập nát và yêu cầu đổi hàng trong 24h."

[CÂU HỎI]
Theo quy định MartX, nhà cung cấp giao rau bị dập nát trên 10% thì bị phạt bao nhiêu?

[KHÓA AN TOÀN (NEGATIVE CONSTRAINT)]
TUYỆT ĐỐI KHÔNG tự suy đoán. Nếu thông tin không có trong văn bản trên, bắt buộc phải trả lời: "Không có dữ liệu trong tài liệu".
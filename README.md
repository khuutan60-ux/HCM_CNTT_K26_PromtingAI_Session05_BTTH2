
# XÂY DỰNG CHUỖI PROMPT VIẾT BÀI PR SẢN PHẨM CÔNG NGHỆ

## 1. Tổng quan quy trình Prompt Chaining

Prompt Chaining là kỹ thuật chia một nhiệm vụ phức tạp thành nhiều bước nhỏ. Kết quả đầu ra của bước trước trở thành dữ liệu đầu vào bắt buộc cho bước tiếp theo.

Trong bài tập này, quy trình gồm 3 bước:

```text
PROMPT 1: NGHIÊN CỨU KHÁCH HÀNG
        |
        v
PROMPT 2: XÂY DỰNG DÀN Ý
        |
        v
PROMPT 3: VIẾT BÀI PR VÀ TỐI ƯU SEO
        |
        v
BÀI PR HOÀN CHỈNH (1000–1500 TỪ)
```

Nguyên tắc: Không bỏ qua bước trung gian. Prompt 2 bắt buộc nhận kết quả Prompt 1; Prompt 3 bắt buộc nhận kết quả Prompt 2.

## 2. Prompt 1 – Nghiên cứu khách hàng mục tiêu

**Mục tiêu:** Xác định chân dung khách hàng, nhu cầu, khó khăn và những vấn đề mà AI Chatbot có thể giải quyết.

### Prompt sử dụng

> Bạn là chuyên gia nghiên cứu thị trường và Marketing trong lĩnh vực công nghệ.
>
> Hãy nghiên cứu đối tượng khách hàng mục tiêu cho sản phẩm AI Chatbot dành cho doanh nghiệp.
>
> Yêu cầu thực hiện:
>
> 1. Xác định 3 nhóm khách hàng mục tiêu chính.
> 2. Phân tích đặc điểm, hành vi và nhu cầu của từng nhóm.
> 3. Liệt kê ít nhất 5 Pain Points (nỗi đau) phổ biến của khách hàng.
> 4. Phân tích nguyên nhân và tác động của từng Pain Point.
> 5. Đề xuất cách AI Chatbot có thể giải quyết từng vấn đề.
> 6. Xác định lợi ích nổi bật mà sản phẩm mang lại.
>
> Định dạng đầu ra bắt buộc là JSON với cấu trúc:
>
> ```json
> {
>   "target_audience": [],
>   "customer_needs": [],
>   "pain_points": [
>     {
>       "problem": "",
>       "cause": "",
>       "impact": "",
>       "chatbot_solution": ""
>     }
>   ],
>   "product_benefits": [],
>   "key_message": ""
> }
> ```
>
> Lưu ý:
> - Không tự bịa số liệu nghiên cứu hoặc cam kết hiệu quả.
> - Nội dung phải thực tế, rõ ràng và phù hợp với thị trường doanh nghiệp.
> - Kết quả JSON sẽ được sử dụng làm đầu vào bắt buộc cho Prompt 2.
> - Không viết bài PR ở bước này.

### Kết quả đầu ra dự kiến

- **Khách hàng mục tiêu:** Doanh nghiệp vừa và nhỏ, doanh nghiệp thương mại điện tử, doanh nghiệp cung cấp dịch vụ khách hàng.
- **Pain Points:**
  - Khách hàng phải chờ lâu để được hỗ trợ.
  - Nhân viên chăm sóc khách hàng quá tải.
  - Chi phí vận hành bộ phận chăm sóc khách hàng cao.
  - Khó quản lý nhiều kênh tư vấn cùng lúc.
  - Bỏ lỡ khách hàng tiềm năng ngoài giờ làm việc.
- **Giải pháp:** AI Chatbot hỗ trợ tư vấn tự động, phản hồi nhanh và hoạt động liên tục.

## 3. Prompt 2 – Xây dựng dàn ý bài viết PR

**Mục tiêu:** Sử dụng kết quả nghiên cứu từ Prompt 1 để xây dựng dàn ý chi tiết, đảm bảo nội dung có logic và không bị trùng lặp.

### Prompt sử dụng

> Bạn là chuyên gia Content Marketing và SEO trong lĩnh vực công nghệ.
>
> Dưới đây là dữ liệu nghiên cứu khách hàng từ Prompt 1:
>
> `[DÁN TOÀN BỘ OUTPUT JSON CỦA PROMPT 1 VÀO ĐÂY]`
>
> Nhiệm vụ:
>
> Dựa trên dữ liệu đầu vào, hãy xây dựng dàn ý chi tiết cho bài PR giới thiệu sản phẩm AI Chatbot dành cho doanh nghiệp.
>
> Yêu cầu:
>
> 1. Xây dựng một tiêu đề chính (H1) thu hút và chứa từ khóa chính.
> 2. Viết định hướng đoạn mở đầu (Lead), tập trung vào Pain Points nổi bật.
> 3. Xây dựng từ 5–7 tiêu đề H2.
> 4. Mỗi H2 có từ 2–3 tiêu đề H3 phù hợp.
> 5. Sắp xếp nội dung theo trình tự:
>    - Vấn đề của doanh nghiệp.
>    - Nguyên nhân và tác động.
>    - Giới thiệu giải pháp AI Chatbot.
>    - Các tính năng nổi bật.
>    - Lợi ích thực tế.
>    - Khả năng ứng dụng.
>    - Lời kêu gọi hành động (CTA).
> 6. Đề xuất từ khóa SEO chính và ít nhất 5 từ khóa phụ.
> 7. Phân bổ số từ cho từng phần để tổng bài viết đạt 1000–1500 từ.
>
> Định dạng đầu ra JSON:
>
> ```json
> {
>   "headline": "",
>   "lead_direction": "",
>   "main_keyword": "",
>   "secondary_keywords": [],
>   "outline": [
>     {
>       "heading_h2": "",
>       "subheadings_h3": [],
>       "content_direction": "",
>       "word_count": 0,
>       "pain_point_reference": []
>     }
>   ],
>   "cta_direction": "",
>   "total_word_count": 1200,
>   "tone": "Chuyên nghiệp, tin cậy, thuyết phục"
> }
> ```
>
> Quy tắc:
> - Không được bỏ qua các Pain Points trong Prompt 1.
> - Không tự ý thay đổi thông điệp chính.
> - Không tạo nội dung trùng lặp giữa các phần.
> - Output JSON này là đầu vào bắt buộc cho Prompt 3.
> - Chưa viết nội dung bài PR hoàn chỉnh.

### Kết quả đầu ra dự kiến

Dàn ý sẽ tập trung vào những nội dung chính:

1. Doanh nghiệp đang gặp khó khăn gì trong chăm sóc khách hàng?
2. AI Chatbot là gì và hoạt động như thế nào?
3. Những tính năng nổi bật của AI Chatbot.
4. AI Chatbot giải quyết các Pain Points ra sao?
5. Lợi ích khi ứng dụng AI Chatbot vào doanh nghiệp.
6. Khả năng triển khai và tích hợp.
7. Đăng ký trải nghiệm giải pháp AI Chatbot.

## 4. Prompt 3 – Viết bài PR và tối ưu SEO

**Mục tiêu:** Triển khai bài viết hoàn chỉnh dựa trên dàn ý ở Prompt 2, đảm bảo đúng giọng văn, độ dài và cấu trúc SEO.

### Prompt sử dụng

> Bạn là chuyên gia Content Marketing, Copywriter và SEO trong lĩnh vực công nghệ.
>
> Dưới đây là dữ liệu dàn ý được tạo từ Prompt 2:
>
> `[DÁN TOÀN BỘ OUTPUT JSON CỦA PROMPT 2 VÀO ĐÂY]`
>
> Nhiệm vụ:
>
> Triển khai thành bài PR hoàn chỉnh giới thiệu giải pháp AI Chatbot dành cho doanh nghiệp.
>
> Yêu cầu nội dung:
>
> 1. Độ dài: 1000–1500 từ.
> 2. Giữ nguyên tiêu đề H1 và hệ thống H2, H3 trong dàn ý.
> 3. Đoạn Lead phải hấp dẫn, đề cập trực tiếp đến Pain Points của khách hàng.
> 4. Phân tích rõ tính năng và lợi ích của AI Chatbot.
> 5. Sử dụng từ khóa chính tự nhiên trong tiêu đề, đoạn mở đầu và nội dung.
> 6. Phân bổ từ khóa phụ hợp lý, tránh nhồi nhét từ khóa.
> 7. Có ví dụ minh họa phù hợp với môi trường doanh nghiệp.
> 8. Kết thúc bằng CTA rõ ràng, khuyến khích khách hàng tìm hiểu hoặc đăng ký trải nghiệm sản phẩm.
>
> **Quy định về giọng văn:**
>
> - Giọng văn chuyên nghiệp, tin cậy và thuyết phục.
> - Không sử dụng ngôn ngữ quảng cáo phóng đại.
> - Không thay đổi phong cách giữa các phần.
> - Không tự tạo số liệu hoặc thông tin chưa được xác thực.
>
> **Quy định đầu ra:**
>
> - H1: Tiêu đề bài viết.
> - Lead: Đoạn mở đầu.
> - H2, H3: Các tiêu đề theo dàn ý.
> - Nội dung chi tiết dưới từng tiêu đề.
> - CTA: Lời kêu gọi hành động cuối bài.
>
> Nếu bài viết vượt quá giới hạn token, hãy chia thành nhiều phần nhưng phải giữ nguyên cấu trúc và giọng văn.
>
> Không được bỏ sót hoặc viết lại những phần đã hoàn thành khi tiếp tục.

## 5. Xử lý khi AI bị ngắt quãng giữa chừng (Max Token)

Khi AI đạt giới hạn token và chưa hoàn thành bài viết, cần sử dụng câu lệnh tiếp tục để đảm bảo nội dung được nối liền mạch.

### Bước 1: Lưu trạng thái bài viết

Ghi lại các thông tin sau:

- Phần đã hoàn thành.
- Tiêu đề H2/H3 cuối cùng đã viết.
- Câu cuối cùng đã xuất hiện.
- Phần tiếp theo cần triển khai.
- Từ khóa SEO và giọng văn ban đầu.

### Bước 2: Sử dụng câu lệnh tiếp tục

> Hãy tiếp tục viết bài PR từ chính xác vị trí đã bị ngắt ở phần trước.
>
> **Trạng thái hiện tại:**
>
> - Nội dung đã hoàn thành: `[GHI CÁC PHẦN ĐÃ HOÀN THÀNH]`
> - Tiêu đề cuối cùng: `[H2/H3 CUỐI CÙNG]`
> - Câu cuối cùng đã viết: `"[DÁN NGUYÊN VĂN CÂU CUỐI]"`
> - Nội dung tiếp theo cần viết: `[TÊN PHẦN TIẾP THEO]`
>
> **Yêu cầu bắt buộc:**
>
> 1. Tiếp tục từ chính xác vị trí ngay sau câu cuối cùng, không viết lại câu đó.
> 2. Không lặp lại bất kỳ đoạn văn nào đã hoàn thành.
> 3. Giữ nguyên cấu trúc H1, H2, H3 theo Outline ban đầu.
> 4. Duy trì giọng văn chuyên nghiệp, tin cậy và thuyết phục.
> 5. Giữ nguyên từ khóa SEO chính và các từ khóa phụ.
> 6. Đảm bảo sự liên kết tự nhiên giữa phần trước và phần tiếp theo.
> 7. Không tự ý thay đổi thông điệp hoặc nội dung đã thống nhất.
>
> Chỉ viết phần nội dung tiếp theo, không giải thích quy trình.

### Bước 3: Kiểm tra sau khi tiếp tục

Sau khi AI hoàn thành, kiểm tra lại:

- Nội dung có bị trùng lặp không?
- Có thiếu tiêu đề H2/H3 nào không?
- Câu văn giữa hai phần có liên kết không?
- Giọng văn có nhất quán không?
- Tổng số từ có nằm trong khoảng 1000–1500 từ không?

## 6. Quy tắc truyền dữ liệu giữa các Prompt

| Quy trình | Dữ liệu đầu vào | Dữ liệu đầu ra |
|---|---|---|
| Prompt 1 | Bối cảnh sản phẩm AI Chatbot và yêu cầu nghiên cứu | JSON về khách hàng, nhu cầu, Pain Points và lợi ích |
| Prompt 2 | Toàn bộ JSON từ Prompt 1 | JSON về Headline, Lead, Outline và từ khóa SEO |
| Prompt 3 | Toàn bộ JSON từ Prompt 2 | Bài PR hoàn chỉnh 1000–1500 từ |

### Nguyên tắc đảm bảo tính nhất quán

1. **Không mất ngữ cảnh:** Luôn chuyển toàn bộ output của bước trước sang bước sau.
2. **Thống nhất định dạng:** Sử dụng JSON để truyền dữ liệu giữa các bước.
3. **Không tự ý thay đổi dữ liệu:** Prompt sau không được tự ý sửa Pain Points hoặc thông điệp chính đã xác định.
4. **Duy trì giọng văn:** Sử dụng thống nhất tone chuyên nghiệp, tin cậy và thuyết phục.
5. **Kiểm soát nội dung:** Đối chiếu bài viết cuối cùng với Outline ban đầu.

## 7. Kết luận

Thông qua quy trình Prompt Chaining gồm 3 bước, nhiệm vụ viết bài PR sản phẩm công nghệ được chia thành các công đoạn rõ ràng: nghiên cứu khách hàng, xây dựng dàn ý và triển khai nội dung.

Việc sử dụng JSON làm định dạng truyền dữ liệu giúp các bước liên kết chặt chẽ, hạn chế mất ngữ cảnh và duy trì tính nhất quán. Đồng thời, câu lệnh tiếp tục khi gặp giới hạn token giúp AI có thể hoàn thiện bài viết mà không lặp lại nội dung đã tạo.

Kết quả cuối cùng là một bài PR dài 1000–1500 từ, có cấu trúc chuẩn SEO, nội dung bám sát nhu cầu khách hàng, giọng văn chuyên nghiệp và CTA rõ ràng.

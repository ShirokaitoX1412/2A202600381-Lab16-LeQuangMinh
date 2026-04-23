# 2A202600280-PhanThanhSang-Track1-Lab16

## 8. Final submission — Day 16 Package

Đây là **bản nộp cuối buổi** cho assignment. Copy template dưới đây, điền đầy đủ, và submit.

---

## 1. Idea reframed

Original idea:
> Xây một chatbot AI hỗ trợ sinh viên ngành Công nghệ thông tin học tốt hơn các môn nền tảng như lập trình, giải thuật, cơ sở dữ liệu. Chatbot có thể giải thích kiến thức và trả lời câu hỏi nhanh theo ngữ cảnh môn học.

Reframed as a product opportunity:
> Khoảng trống quan sát được là sinh viên có nhiều nguồn học nhưng thiếu một "người hướng dẫn" giúp hiểu sâu theo cách Socratic (hỏi gợi mở thay vì cho đáp án ngay), đặc biệt khi tự học ngoài giờ. Founding belief của team là việc học bền vững đến từ quá trình tự suy luận, không phải sao chép lời giải. Vì vậy cơ hội sản phẩm không chỉ là "AI trả lời", mà là "AI coach" cá nhân hóa theo mức độ hiểu, phát hiện lỗ hổng kiến thức, và dẫn dắt từng bước. Nếu làm đúng, sản phẩm có thể cải thiện cả điểm số ngắn hạn lẫn năng lực tư duy dài hạn.

---

## 2. Customer / Segment Card

- **Segment name:** Sinh viên IT năm 1-3 tại đại học Việt Nam (early adopters: năm 1-2)
- **Operational context:** Học theo tín chỉ, lịch học dày, nhiều bài tập coding/quiz, thường tự học buổi tối trước deadline hoặc trước thi giữa kỳ/cuối kỳ.
- **Recurring workflow:** Xem slide/video -> đọc tài liệu -> làm bài tập -> bị kẹt ở một bước -> tìm đáp án trên Google/YouTube/ChatGPT -> làm tiếp.
- **Pain moment:** Hiểu "cách làm" nhưng không hiểu "vì sao", nên gặp biến thể đề là sai; tốn thời gian vì phải tự ghép kiến thức từ nhiều nguồn rời rạc.
- **Why now:** AI đã phổ biến trong sinh viên, nhưng trải nghiệm hiện tại thiên về cho đáp án nhanh, chưa tối ưu cho việc học tư duy.
- **Access path:** CLB học thuật IT, cộng đồng lớp trên Facebook/Zalo/Discord, giảng viên trợ giảng, các nhóm học chung theo môn.

One-sentence description:
> Đây là nhóm sinh viên IT có động lực cải thiện năng lực thật, sẵn sàng dùng AI mỗi ngày, nhưng đang thiếu một công cụ biến việc "hỏi AI" thành quá trình học có cấu trúc.

---

## 3. Need Map (2–3 needs)

### Need #1 (priority)
- **Statement (JTBD):** When em bị kẹt ở bài toán lập trình/giải thuật, em muốn được gợi ý theo từng nấc (không lộ đáp án ngay), so I can tự giải và nhớ cách tư duy cho bài tương tự.
- **Current workaround:** Hỏi bạn giỏi hơn, tìm lời giải mẫu trên mạng, hoặc prompt AI xin "full solution" rồi copy/chỉnh.
- **Pain signal:** Làm xong bài hiện tại nhưng fail ở bài tương tự trong quiz/thi; khó giải thích lại thuật toán bằng lời của mình.
- **Evidence / proxy evidence:** Quan sát phổ biến trong nhóm học: nhiều bạn có thể chạy code nhưng lúng túng khi bị hỏi "tại sao chọn approach này"; phản hồi thường gặp là "em hiểu lúc đó, sau lại quên".
- **Why underserved:** Công cụ AI phổ biến tối ưu cho tốc độ trả lời, không tối ưu cho pedagogical scaffolding và kiểm tra mức hiểu thật.

### Need #2
- **Statement (JTBD):** When em ôn thi một môn IT trong thời gian ngắn, em muốn biết lỗ hổng kiến thức cá nhân theo từng chủ đề, so I can ưu tiên học đúng phần yếu trước kỳ thi.
- **Current workaround:** Ôn theo cảm giác, làm đề ngẫu nhiên, hoặc học lại toàn bộ chương gây tốn thời gian.
- **Pain signal:** Học nhiều giờ nhưng điểm vẫn thấp ở vài dạng câu hỏi lặp lại; cảm giác "học không vào đúng chỗ".
- **Evidence / proxy evidence:** Mô hình ôn thi hiện tại của nhiều sinh viên dựa trên đề cương chung, không cá nhân hóa theo sai lầm cụ thể từng người.
- **Why underserved:** LMS và tài liệu môn học thường cung cấp nội dung tĩnh, thiếu cơ chế adaptive diagnosis theo thời gian thực.

### Need #3 (optional)
- **Statement (JTBD):** When em học kiến thức mới (ví dụ recursion, SQL join, normalization), em muốn nhận ví dụ gắn với ngữ cảnh gần gũi và được hỏi ngược để tự diễn giải lại, so I can chuyển từ "biết định nghĩa" sang "biết áp dụng".
- **Current workaround:** Xem nhiều video/đọc nhiều bài viết khác nhau rồi tự nối ý.
- **Pain signal:** Nhớ thuật ngữ nhưng áp dụng sai trong bài tập thực hành.
- **Evidence / proxy evidence:** Tình trạng "học thuộc khái niệm nhưng không làm được lab" xuất hiện thường xuyên ở môn cơ sở ngành.
- **Why underserved:** Nội dung online phong phú nhưng thiếu tính tương tác hai chiều và vòng lặp phản hồi ngay theo từng sinh viên.

---

## 4. Strategy Statement

For sinh viên IT năm 1-3 đang tự học và ôn thi,
who struggle with việc hiểu nông, lệ thuộc đáp án mẫu, và không biết mình hổng kiến thức ở đâu,
our product helps them nắm chắc kiến thức cốt lõi và tăng khả năng tự giải bài,
through AI Socratic coaching gồm hỏi gợi mở nhiều bước, chẩn đoán lỗ hổng theo chủ đề, và lộ trình ôn tập cá nhân hóa,
unlike chatbot AI trả lời trực tiếp hoặc tài liệu học tĩnh,
because we can leverage dữ liệu tương tác học tập theo workflow môn IT để tối ưu cách hỏi, mức gợi ý, và thứ tự nội dung cho từng hồ sơ người học.

---

## 5. Moat Hypothesis

**Moat mechanism:** Domain-learning flywheel theo workflow học IT + pedagogical tuning dataset

If we deploy 1,000+ phiên học trong bối cảnh sinh viên IT học các môn nền tảng (Programming, DSA, DB), the following improve:
1. Chất lượng "next best question" để gợi mở đúng mức khó cho từng người.
2. Độ chính xác của knowledge-gap graph (nhìn ra chủ đề gốc gây sai lặp).
3. Tỷ lệ chuyển đổi từ "hỏi đáp" sang "tự giải được bài tương tự".

Why competitors cannot easily replicate this:
> Dataset giá trị nằm ở chuỗi tương tác học theo thời gian (câu hỏi nào kích hoạt suy luận, ở thời điểm nào người học bứt được), không chỉ ở prompt tĩnh hay FAQ. Dữ liệu này gắn với ngữ cảnh chương trình IT địa phương và hành vi học thật, cần thời gian triển khai + phản hồi vòng lặp mới tích lũy được.

---

## 6. Initial TAM / SAM / SOM view

| Layer | Estimate | Key assumptions | Confidence |
|---|---|---|---|
| TAM | ~25-60M USD/năm (VN + SEA sinh viên IT/CS có nhu cầu edtech AI) | Tính trên số lượng sinh viên IT/CS, tỷ lệ dùng công cụ học số, ARPU gói học tập 3-8 USD/tháng | low |
| SAM | ~3-8M USD/năm (thị trường khả dụng trước mắt: sinh viên IT tại VN, học bằng tiếng Việt/Anh) | Tập trung nhóm có tần suất tự học cao và sẵn sàng trả phí cho công cụ ôn thi/lab | med |
| SOM | 200k-500k USD ARR trong 12-24 tháng | Đạt 8,000-15,000 MAU, chuyển đổi trả phí 4-7%, retention tháng 3 đủ tốt | low |

**Top 3 unknowns requiring further research:**
1. Mức willingness-to-pay thực tế của sinh viên (B2C) so với mô hình B2B2C qua trường/CLB.
2. Tác động đo được lên kết quả học tập: cải thiện điểm, tốc độ giải bài, và khả năng tự giải bài mới.
3. Chủ đề/môn học nào cho retention cao nhất để chọn beachhead segment.

**Judgment:**
- [x] Worth pursuing now
- [ ] Worth pursuing but not now (need to validate [...] first)
- [ ] Not worth pursuing as currently framed

---

## 7. Positioning Note (2 sentences)

**What we are:**
> Socratic AI là AI learning coach cho sinh viên IT, giúp học sâu qua đối thoại gợi mở và bản đồ lỗ hổng kiến thức cá nhân hóa.

**What we are not / not yet:**
> Chúng tôi không phải "máy giải bài hộ" hay nền tảng LMS đầy đủ; hiện tại chưa thay thế giảng viên mà tập trung tối ưu self-study giữa các buổi học.

---

## 8. Self-assessment before Day 17

Trong 6 mắt xích (Idea → Customer → Need → Strategy → Moat → Market Size), mắt xích nào team đang yếu nhất?

> Team đang yếu nhất ở Market Size và phần evidence định lượng cho willingness-to-pay; hiện mới ở mức giả định hợp lý, chưa có dữ liệu phỏng vấn/survey đủ mạnh.

Open questions chúng tôi muốn khám phá thêm ở Day 17:
1. MVP nên bắt đầu từ use-case nào để tạo "aha moment" nhanh nhất: giải thuật, debug code, hay ôn thi DB?
2. Thiết kế rubric đánh giá "học sâu" thế nào để không chỉ đo số câu trả lời đúng?
3. Gói giá và kênh GTM đầu tiên nào khả thi hơn: B2C sinh viên tự trả hay pilot qua khoa/CLB?

---
# 2A202600381-Lê Quang Minh-Track1-Lab16

## 8. Final submission — Day 16 Package

Đây là **bản nộp cuối buổi** cho assignment. Copy template dưới đây, điền đầy đủ, và submit.

---

## 1. Idea reframed

Original idea:
> Xây một AI assistant hỗ trợ nhân viên ngân hàng tra cứu nhanh quy định nội bộ, tiêu chuẩn KYC, SOP tín dụng và các quy trình xử lý hồ sơ. Assistant có thể trả lời câu hỏi theo ngữ cảnh từng phòng ban (giao dịch viên, back-office, compliance).

Reframed as a product opportunity:
> Khoảng trống quan sát được là nhân viên ngân hàng không thể tuân thủ 100% quy định vì quy mô tài liệu lớn, cập nhật thường xuyên, và áp lực deadline. Founding belief của team là sai sót compliance không phải do thiếu quy định mà do nhân viên không có công cụ tra cứu **nhanh, chính xác, theo ngữ cảnh công việc cụ thể** lúc đó. Cơ hội sản phẩm không chỉ là "search engine quy định", mà là "intelligent compliance assistant" biết bối cảnh (khách hàng loại nào, giai đoạn hồ sơ nào, rủi ro nào), cảnh báo áp dụng sai, và hướng dẫn quy trình từng bước với audit trail. Nếu làm đúng, sản phẩm giảm rủi ro compliance, tăng tốc độ xử lý hồ sơ, và bảo vệ dữ liệu khách hàng.

---

## 2. Customer / Segment Card

- **Segment name:** Giao dịch viên, back-office, compliance tại các ngân hàng Việt Nam (early adopters: giao dịch viên cấp teller, nhân viên kiểm soát rủi ro)
- **Operational context:** Xử lý hồ sơ khách hàng theo quy định KYC/AML, cấu trúc tín dụng theo SOP, duyệt xét approval 4 mắt. Mỗi quyết định phải tuân thủ policy nội bộ và quy định pháp luật. Áp lực deadline (khách hàng chờ), áp lực rủi ro (compliance breach = phạt, tạm dừng operation).
- **Recurring workflow:** Nhận hồ sơ khách hàng -> kiểm tra tài liệu KYC -> đối chiếu danh sách đen -> xác định loại hồ sơ (VIP, doanh nghiệp, cá nhân...) -> áp dụng quy trình tín dụng -> tra cứu SOP -> duyệt approval -> lưu trữ audit trail.
- **Pain moment:** Không chắc áp dụng policy nào, quy định này áp dụng cho loại khách hàng nào, SOP bước tiếp theo là gì, hay đã phạm violation nào. Phải gửi email hỏi leader hoặc tra cứu manual 50+ trang => tốn 30-60 phút, delay xử lý.
- **Why now:** (1) Quy định ngân hàng cập nhật liên tục (AML mới, quy định ECN...) khó cập nhật manual; (2) Penalti compliance tăng cao, tất cả phòng ban bị áp lực giảm rủi ro; (3) AI đủ tin cậy để dùng trong decision support (chưa automate quyết định).
- **Access path:** Internal tools (banking platform, intranet), training onboarding, manager recommendation, internal champion tại compliance team.

One-sentence description:
> Nhân viên ngân hàng cần tra cứu nhanh quy định compliance + hướng dẫn quy trình đúng cho từng trường hợp khách hàng, nhưng hiện phải vừa nhớ manual vừa hỏi người khác, dẫn đến delay và sai sót rủi ro.

---

## 3. Need Map (2–3 needs)

### Need #1 (priority) — Fast, contextual policy lookup
- **Statement (JTBD):** When em nhận hồ sơ khách hàng doanh nghiệp muốn vay credit line, em muốn biết liền (trong <2 phút) khách hàng loại này cần KYC nâng cao hay cơ bản, tài liệu nào là bắt buộc, và SOP bước tiếp theo là gì, so I can xác nhận hồ sơ nhanh và không phạm quy định.
- **Current workaround:** Gọi điện hỏi lead/manager (khi họ rảnh), tra cứu manual policy 50+ trang hoặc email ask intranet, tìm ví dụ case cũ tương tự.
- **Pain signal:** Hồ sơ bị delay 30-60 phút vì chờ clarify; thỉnh thoảng áp dụng quy định sai (KYC cơ bản thay vì nâng cao, hoặc bỏ qua step AML check) => sau bị compliance team phát hiện, phải redo.
- **Evidence / proxy evidence:** (1) Internal audit thường phát hiện "missing KYC documents" hoặc "unapplied risk assessment"; (2) Quản lý đơn vị báo cáo lực lượng team phải overhead 2-3 tiếng/tuần xử lý ask từ teller.
- **Why underserved:** LMS/intranet lưu policy dạng tĩnh, không search tốt; policy phát hành dạng PDF không có version control clear. Chưa có tool nào biết ngữ cảnh (loại khách hàng, giai đoạn hồ sơ) để recommend quy trình tự động.

### Need #2 — Compliance risk alert & decision support
- **Statement (JTBD):** When em đang xử lý hồ sơ khách hàng nước ngoài (foreign national hoặc corporation), em muốn assistant tự động flag các yêu cầu regulatory nặng hơn (enhanced due diligence, source of funds verification, PEP check), so I can không bỏ sót bước compliance quan trọng và không bị audit team phạt.
- **Current workaround:** Dựa vào kinh nghiệm cá nhân, hỏi bạn cũ, hoặc đợi compliance review từ bạn trong team (chậm, hay quên).
- **Pain signal:** Bỏ sót PEP check hoặc source of funds doc => sau bị phát hiện trong internal audit hoặc regulator audit => penalty, mark on appraisal.
- **Evidence / proxy evidence:** Compliance report năm ngoái liệt kê 5-7 case KYC incomplete trên khách hàng high-risk; dù có SOP nhưng áp dụng inconsistent do manual process.
- **Why underserved:** Compliance SOP tồn tại nhưng ở dạng text SOP 10-20 trang mỗi loại khách hàng, khó nhớ toàn bộ rule. Chưa có tool nào integrate SOP + khách hàng metadata để flag risk tự động.

### Need #3 (optional) — Audit trail & training support
- **Statement (JTBD):** When em xử lý hồ sơ approval phức tạp, em muốn assistant ghi lại từng bước quyết định (tại sao áp dụng rule X, tại sao yêu cầu doc Y, tại sao flag risk Z), so I can giải thích sau này cho auditor khi bị hỏi, và dễ dàng train nhân viên mới theo case thực tế.
- **Current workaround:** Ghi chú tay vào hồ sơ hoặc email, nội bộ tay chân; không có trace rõ ràng.
- **Pain signal:** External auditor hỏi "tại sao quyết định approve khách hàng này?" => không có documented trail => khó bảo vệ quyết định => ảnh hưởng audit rating.
- **Evidence / proxy evidence:** Audit finding thường liên quan đến "lack of documentation" hoặc "unclear decision rationale" hơn là quyết định sai.
- **Why underserved:** Hồ sơ xử lý hiện tại không có decision log dạng structured; chỉ có comment tự do hoặc email thread => khó trace, khó report pattern.

---

## 4. Strategy Statement

For giao dịch viên, back-office, compliance tại ngân hàng Việt Nam đang xử lý hồ sơ khách hàng hàng ngày,
who struggle with việc tuân thủ 100% policy phức tạp + cập nhật thường xuyên, không biết quy trình nào áp dụng cho loại khách hàng nào, và rủi ro bỏ sót quy định quan trọng,
our product helps them xử lý hồ sơ nhanh, chính xác, theo quy định, với trail audit rõ ràng,
through Intelligent Compliance Assistant gồm (1) quick lookup quy định theo bối cảnh khách hàng + giai đoạn hồ sơ, (2) auto-flag risk và yêu cầu quy định bổ sung, (3) structured decision log để audit trail,
unlike manual policy lookup, email ask, hoặc chỉ có SOP dạng PDF text,
because we can integrate policy database + khách hàng metadata + workflow hồ sơ để context-aware recommend quy trình, flag risk tự động, và generate audit evidence.

---

## 5. Moat Hypothesis

**Moat mechanism:** Bank-specific policy knowledge base + domain expertise in compliance + decision audit trail

If we deploy this assistant tại 1 ngân hàng tầm 3,000+ nhân viên với 500k+ hồ sơ/năm, the following become structural advantage:
1. Đạo tạo model với policy data + case history thực (hồ sơ approved, audit finding) => model hiểu "apply quy định sao cho đúng" không chỉ "quy định viết gì".
2. Tích lũy decision pattern: quy trình nào áp dụng cho loại khách hàng nào, điểm nào dễ sai => optimize workflow tuần tự.
3. Audit trail database: có thể trace từng quyết định, pattern sai lặp => improvement roadmap rõ ràng.

Why competitors cannot easily replicate this:
> Dataset giá trị nằm ở (1) policy detail + case history cụ thể của từng ngân hàng (khác quy định từng nước), (2) chuỗi quyết định approval + audit result thực tế (không phải training data generic), (3) knowledge about internal process variation. Đây là proprietary data, không thể scrape hoặc synthetic. Cần relationship + trust với bank để access, + thời gian để tuning.

---

## 6. Initial TAM / SAM / SOM view

| Layer | Estimate | Key assumptions | Confidence |
|---|---|---|---|
| TAM | ~500M-2B USD/năm (Toàn khu vực SE Asia + khu vực: bank employee compliance tool, regulatory tech) | Tính trên số lượng commercial banks, nhân viên handling compliance (30-200 người/bank), ARPU tool 50-200 USD/seat/năm | low |
| SAM | ~30-80M USD/năm (thị trường khả dụng: ngân hàng tại VN, có <50 tỷ đô tài sản, cần strengthen compliance) | Tập trung tier 2-3 bank (15-20 bank) + chi nhánh tier 1 bank, có regulatory pressure cao (central bank audit, sanction risk) | med |
| SOM | 500k-2M USD ARR trong 24-36 tháng | Đạt 3-5 ngân hàng tầm 500-2000 users/bank, adoption rate 60-70% trong compliance/teller team, churn < 5%/năm | low-med |

**Top 3 unknowns requiring further research:**
1. Willingness-to-pay của bank (enterprise license vs. per-seat vs. per-transaction): phụ thuộc vào ROI (giảm compliance cost, reduce audit finding).
2. Tác động thực tế lên compliance KPI: giảm % hồ sơ incomplete, giảm audit finding, giảm time-to-close hồ sơ.
3. Quy trình AI governance trong bank: AI trong compliance decision support được allowed khi nào, cần oversight gì, liability khi sai.

**Judgment:**
- [x] Worth pursuing now (compliance risk cao, regulatory pressure tăng, market ready)
- [ ] Worth pursuing but not now (need to validate [...] first)
- [ ] Not worth pursuing as currently framed

---

## 7. Positioning Note

**What we are:**
> Banking Compliance AI Assistant là công cụ decision support hỗ trợ nhân viên ngân hàng tra cứu policy nhanh, flag rủi ro tự động, và document audit trail dạng structured — tối ưu cho môi trường compliance-heavy, regulatory-intensive.

**What we are not / not yet:**
> Chúng tôi không phải "fully automated compliance engine" hay thay thế quyết định của con người; AI là guard rail và speed-up tool, không automate approval. Hiện tại chưa hỗ trợ lĩnh vực khác ngoài KYC/AML/credit SOP, và chưa deploy qua multiple banks.

---

## 8. Self-assessment & Unknowns

**Strongest & Weakest link trong 6 mắt xích:**
- **Strongest**: Customer segment + Pain moment → evidence rõ từ audit finding thực, regulatory feedback
- **Weakest**: Market Size (TAM/SAM/SOM) + Willingness-to-pay → mới giả định dựa trên benchmark, chưa validate qua sales conversation với bank decision maker

**Top 3 critical unknowns cần validate trước khi commit resources:**
1. **ROI tính toán từ bank side**: Giảm bao nhiêu % audit finding, hay giảm bao lâu processing time đơn vị ngân hàng sẵn sàng trả $X/seat?
2. **AI governance risk**: Bank có chấp nhận AI flag risk (non-binding) hay cần liability disclaimer? Quy trình approval AI-recommended recommendation như thế nào?
3. **Policy integration complexity**: Mỗi bank policy khác nhau → MVP nên support bao nhiêu bank-specific variation trước khi scale? (risk: scope creep)

**Recommendation cho Day 17:**
- Conduct 2-3 sales conversation với compliance manager tier 2-3 bank → estimate real WTP
- Deep-dive vào 1 bank's actual audit finding từ năm ngoái → validate pain magnitude
- Design MVP scope: KYC/AML only, 1 bank pilot, 3 tháng deployment

---
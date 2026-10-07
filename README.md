# Lab 21 — Phân tích rủi ro AI qua case study thực tế

- **Họ và tên:** Trần Thị Thuý
- **MSSV / mã học viên:** 2A202602960
- **Lớp:** K04 — Track 1
- **Ngành đã chọn:** Content creator — AI hỗ trợ tạo nội dung
- **Ngày hoàn thành:** 07/10/2026

> **Quy ước đọc bài:** “Bằng chứng” là thông tin được nguồn dẫn xác nhận. “Nhận định” là phần phân tích rủi ro của người viết; không được hiểu là kết luận pháp lý hay thiệt hại đã được chứng minh.

## 1. Industry Risk Snapshot

| Nội dung | Đánh giá của tôi và lý do |
| --- | --- |
| Những tác hại chính có thể xảy ra | **Misinformation:** nội dung sai được xuất bản như thật, làm người xem hiểu sai hoặc ra quyết định sai. **Opportunity loss:** tác giả, nhiếp ảnh gia và diễn viên lồng tiếng có thể mất việc, doanh thu hoặc quyền cấp phép khi tác phẩm/danh tính bị dùng ngoài phạm vi cho phép. **Privacy và dignity loss:** giọng nói, hình ảnh hoặc phong cách cá nhân có thể bị sao chép để tạo nội dung mà chủ thể không hề nói hoặc thực hiện. Các bên bị ảnh hưởng gồm người sáng tạo, khán giả, khách hàng, nền tảng phân phối và thương hiệu sử dụng nội dung. |
| Mức độ high-stakes | **Trung bình đến cao.** Phần lớn nội dung giải trí thông thường không trực tiếp quyết định quyền lợi thiết yếu, nhưng mức độ tăng lên **cao** khi nội dung liên quan tài chính, sức khỏe, danh tiếng, chính trị hoặc danh tính cá nhân. Một bài tài chính sai có thể ảnh hưởng quyết định của độc giả; một bản sao giọng nói có thể gây tổn hại danh tiếng và sinh kế. Đây là đánh giá định tính phục vụ bài tập, không phải phân loại pháp lý. |
| Dữ liệu nhạy cảm có thể được sử dụng | Bản ghi giọng nói; khuôn mặt, hình ảnh và đặc điểm nhận dạng; tác phẩm chưa công bố; prompt và lịch sử chỉnh sửa; thông tin tài khoản; metadata; dữ liệu bản quyền, hợp đồng và điều khoản cấp phép. Không đưa dữ liệu thật của cá nhân vào repo này. |
| Nhu cầu human review | **Cao.** Biên tập viên cần kiểm tra sự thật, phép tính, nguồn và mức độ nguyên bản trước khi xuất bản. Nhân sự pháp lý/quản trị dữ liệu cần xác minh consent, licence và provenance trước khi dùng dữ liệu để huấn luyện hoặc tạo bản sao. Với giọng nói/hình ảnh nhận dạng được, chủ thể cần có cơ chế đồng ý rõ ràng, xem trước mục đích sử dụng và thu hồi quyền. |

## 2. Case study 1 — CNET sửa hàng loạt bài tài chính do AI hỗ trợ viết

### Brief Case

- **Tổ chức / sản phẩm AI:** CNET Money và công cụ AI nội bộ của CNET.
- **Thời gian, địa điểm / bối cảnh:** Hoa Kỳ; thử nghiệm bắt đầu từ tháng 11/2022 và được công khai, kiểm tra lại vào tháng 1/2023.
- **AI được dùng để làm gì:** Hỗ trợ tạo 77 bài giải thích cơ bản về dịch vụ và kiến thức tài chính. Theo CNET, biên tập viên tạo dàn ý rồi mở rộng, bổ sung và chỉnh sửa bản nháp do AI tạo trước khi xuất bản.
- **Vấn đề hoặc sự kiện đáng chú ý:** CNET tạm dừng công cụ sau khi phát hiện lỗi và thực hiện kiểm tra toàn bộ. Một bài về lãi kép từng viết rằng gửi 10.000 USD với lãi suất 3% sẽ “kiếm được” 10.300 USD sau một năm; nội dung được sửa thành kiếm 300 USD ngoài 10.000 USD tiền gốc.
- **Số liệu có nguồn:** CNET xác nhận **77 bài**, tương đương khoảng **1%** nội dung hãng xuất bản trong cùng giai đoạn. Engadget kiểm đếm thấy **41/77 bài có correction**. Con số 41 là kiểm đếm của báo chí, không phải con số CNET công bố trong tuyên bố được CBS/CNN trích dẫn.
- **Nguồn:**
  - Igor Bonifacic, “[CNET had to correct most of its AI-written articles](https://www.engadget.com/cnet-corrected-41-of-its-77-ai-written-articles-201519489.html),” *Engadget*, 25/01/2023 — số bài có correction và vấn đề về câu chữ không hoàn toàn nguyên bản.
  - CNN/CBS San Francisco, “[CNET's decision to write stories with AI backfires](https://www.cbsnews.com/sanfrancisco/news/cnets-decision-to-write-stories-with-ai-backfires/),” cập nhật 26/01/2023 — mô tả thử nghiệm 77 bài, khoảng 1% nội dung và ví dụ lỗi lãi kép.
- **Phân biệt bằng chứng và nhận định:** **Bằng chứng:** 77 bài được xuất bản trong thử nghiệm; CNET kiểm tra lại, sửa nội dung và tạm dừng công cụ; 41 bài có correction theo kiểm đếm của Engadget. **Nhận định:** độc giả *có thể* ra quyết định tài chính sai nếu tin nội dung; các nguồn trên không chứng minh một độc giả cụ thể đã mất tiền. “Hallucination” là cách tôi phân loại hành vi tạo thông tin sai, không phải thuật ngữ CNET dùng để mô tả mọi lỗi.

### Harm Map Worksheet

| Trường | Phân tích của tôi |
| --- | --- |
| High-risk moment | Khi bài giải thích tài chính do AI hỗ trợ được biên tập và xuất bản như nội dung tư vấn đáng tin nhưng phép tính/sự kiện chưa được kiểm tra độc lập. |
| Stakeholder bị ảnh hưởng | Độc giả CNET; biên tập viên; CNET; các tổ chức hoặc chuyên gia được nhắc đến trong bài. |
| Failure mode | **Hallucination + over-reliance:** công cụ tạo chi tiết sai; quy trình con người không phát hiện hết trước khi xuất bản. |
| Layer bắt đầu lỗi | **Model:** nội dung sinh ra có phép tính/sự kiện sai. **UX/quy trình biên tập:** việc có biên tập viên nhưng lỗi vẫn qua khâu xuất bản cho thấy kiểm soát chưa đủ. Kiến trúc và dữ liệu của công cụ không được công bố nên chưa đủ bằng chứng để kết luận chi tiết về Grounding. |
| Harm xảy ra là gì? | **Đã xảy ra:** thông tin tài chính sai được công khai và CNET phải đính chính. **Nguy cơ:** độc giả hiểu sai lãi suất hoặc ra quyết định tài chính không phù hợp; chưa có bằng chứng về thiệt hại tiền bạc cụ thể. |
| Harm lens | **Misinformation**; ngoài ra có rủi ro giảm niềm tin vào nội dung và thương hiệu. |
| Severity | **High** đối với nội dung tài chính vì sai số có thể tác động quyết định; tuy nhiên không đánh giá Critical do chưa có bằng chứng về thiệt hại nghiêm trọng thực tế. |
| Scale | **Medium–High:** 77 bài được công khai; 41 bài có correction. Chưa có số liệu về lượng người đọc từng bài hoặc số người bị ảnh hưởng. |
| Probability | **Đã quan sát trong thử nghiệm:** 41/77 bài có correction. Tỷ lệ này không đồng nghĩa mọi correction đều là lỗi nghiêm trọng và không thể dùng để dự báo mọi hệ thống AI viết nội dung. |
| Frequency | **High trong phạm vi thử nghiệm:** hơn một nửa số bài có correction; CNET nói chỉ một số nhỏ cần sửa đáng kể, còn các bài khác có vấn đề nhỏ hơn. |
| Vì sao? | Case có bằng chứng về lỗi xuất bản và quy trình audit, nhưng không có bằng chứng về thiệt hại của từng độc giả. Biện pháp phù hợp là kiểm tra phép tính bằng công cụ độc lập, bắt buộc dẫn nguồn, người duyệt chịu trách nhiệm và không xuất bản tự động ở chủ đề tài chính. |

## 3. Case study 2 — Getty Images và Stability AI: tranh chấp nguồn dữ liệu huấn luyện

### Brief Case

- **Tổ chức / sản phẩm AI:** Getty Images; Stability AI; mô hình tạo ảnh Stable Diffusion.
- **Thời gian, địa điểm / bối cảnh:** Vụ tại Hoa Kỳ được nộp ngày 14/08/2025 tại Tòa án Liên bang khu vực Bắc California. Một vụ liên quan tại Anh được khởi kiện năm 2023 và có phán quyết ngày 04/11/2025.
- **AI được dùng để làm gì:** Stable Diffusion tạo hình ảnh mới từ prompt; tranh chấp tập trung vào nguồn hình ảnh, chú thích và metadata được sử dụng liên quan đến quá trình phát triển mô hình.
- **Vấn đề hoặc sự kiện đáng chú ý:** Trong hồ sơ SEC, Getty mô tả vụ kiện dựa trên **cáo buộc** Stability AI sao chép không được phép hình ảnh từ website Getty cùng caption và metadata. Tại vụ án ở Anh, tòa chỉ xử thắng Getty ở một phần khiếu nại về nhãn hiệu; yêu cầu secondary copyright infringement không thành công. Hồ sơ Getty cho biết phán quyết có nhận định thực tế rằng tác phẩm được bảo hộ của Getty đã được dùng để huấn luyện Stable Diffusion, nhưng không xác lập con số 12 triệu là số tác phẩm vi phạm đã được chứng minh.
- **Số liệu có nguồn:** Hồ sơ Form 10-K của Getty nêu con số **xấp xỉ 12,0 triệu hình ảnh** trong cáo buộc tại Mỹ. Đây là quy mô Getty cáo buộc, không phải số lượng đã được tòa xác nhận vi phạm.
- **Nguồn:**
  - Getty Images Holdings, Inc., “[Form 10-K — Stability AI Lawsuits](https://www.sec.gov/Archives/edgar/data/1898496/000162828026018160/gety-20251231.htm),” SEC, phần F-29, vụ số 3:25-CV-06891-TLT — ngày nộp vụ Mỹ, con số 12,0 triệu và tình trạng tố tụng.
  - High Court of Justice, “[Getty Images v Stability AI](https://www.judiciary.uk/judgments/getty-images-v-stability-ai/),” [2025] EWHC 2863 (Ch), 04/11/2025, case IL-2023-000007 — phán quyết chính thức tại Anh.
- **Phân biệt bằng chứng và nhận định:** **Bằng chứng:** vụ kiện tồn tại, số vụ án và ngày nộp được ghi trong hồ sơ; Getty nêu cáo buộc khoảng 12 triệu hình ảnh; phán quyết Anh được công bố chính thức. **Chưa được coi là sự kiện đã chứng minh:** toàn bộ 12 triệu hình ảnh bị sao chép trái phép hoặc mọi creator đã mất doanh thu. **Nhận định:** thiếu consent/licence và provenance rõ ràng tạo rủi ro cơ hội nghề nghiệp, bồi thường và quyền kiểm soát tác phẩm.

### Harm Map Worksheet

| Trường | Phân tích của tôi |
| --- | --- |
| High-risk moment | Khi tác phẩm, caption và metadata được đưa vào pipeline huấn luyện/ phát triển mô hình mà quyền sử dụng, phạm vi licence và khả năng phản đối của chủ sở hữu chưa được xác minh đầy đủ. |
| Stakeholder bị ảnh hưởng | Nhiếp ảnh gia, họa sĩ và chủ sở hữu quyền; Getty/iStock; Stability AI; người dùng công cụ tạo ảnh; khách hàng mua hình và nền tảng phân phối nội dung. |
| Failure mode | **Misuse** là nhãn gần nhất trong danh sách của slide: dữ liệu có thể bị dùng ngoài quyền cho phép. Case còn phản ánh rủi ro provenance/bản quyền mà taxonomy tám failure mode của bài không mô tả trọn vẹn. |
| Layer bắt đầu lỗi | **Grounding / nguồn dữ liệu:** vấn đề nằm ở nguồn, quyền và metadata của dữ liệu dùng để phát triển mô hình. Có thể liên quan Safety/data governance nếu thiếu kiểm soát licence; chưa đủ bằng chứng công khai để kết luận kiến trúc nội bộ cụ thể. |
| Harm xảy ra là gì? | **Đã xảy ra:** tranh chấp pháp lý và chi phí tố tụng giữa các tổ chức. **Được cáo buộc/nguy cơ:** creator và chủ sở hữu có thể mất quyền cấp phép, doanh thu hoặc quyền kiểm soát tác phẩm; không khẳng định các thiệt hại này đã được chứng minh cho toàn bộ 12 triệu hình ảnh. |
| Harm lens | **Opportunity loss** và **dignity loss**; có thêm rủi ro thông tin nguồn gốc bị làm mờ khi metadata không được bảo toàn. |
| Severity | **High:** nếu tác phẩm thương mại bị sử dụng ở quy mô lớn ngoài licence, ảnh hưởng có thể kéo dài tới thu nhập, quyền kiểm soát và khả năng truy xuất tác giả. Đây là đánh giá rủi ro, không phải kết luận trách nhiệm pháp lý. |
| Scale | **High theo quy mô cáo buộc:** khoảng 12,0 triệu hình ảnh. Không dùng con số này như số nạn nhân hoặc số vi phạm đã được tòa xác nhận. |
| Probability | **Chưa đủ dữ liệu để lượng hóa.** Có tranh chấp và bằng chứng tố tụng về việc tác phẩm Getty được dùng trong training, nhưng tính hợp pháp và phạm vi trách nhiệm khác nhau theo yêu cầu, lãnh thổ và phán quyết. |
| Frequency | **Chưa đủ dữ liệu để lượng hóa.** Cáo buộc liên quan nhiều phiên bản Stable Diffusion, nhưng nguồn không cung cấp số lần ingest, số lần tạo output vi phạm hay tỷ lệ tái tạo tác phẩm. |
| Vì sao? | Quy mô cáo buộc lớn làm Scale cao, nhưng Probability/Frequency không được tự suy ra từ 12 triệu. Kiểm soát phù hợp gồm inventory dữ liệu, bằng chứng licence/consent, lưu provenance, cơ chế opt-out/takedown, đánh giá khả năng memorization và review pháp lý trước khi phát hành. |

## 4. Case study 3 — Lehrman và Sage kiện LOVO về bản sao giọng nói AI

### Brief Case

- **Tổ chức / sản phẩm AI:** LOVO Inc.; nền tảng tạo giọng nói “Genny”; hai diễn viên lồng tiếng Paul Skye Lehrman và Linnea Sage.
- **Thời gian, địa điểm / bối cảnh:** Các bản ghi được đặt qua Fiverr trong năm 2019 và 2020; đơn kiện được nộp ngày 16/05/2024 tại Southern District of New York, Hoa Kỳ. Ngày 10/07/2025, tòa cho một số yêu cầu như breach of contract, bảo vệ người tiêu dùng New York và right of publicity tiếp tục, đồng thời bác các yêu cầu trademark liên bang và phần lớn copyright.
- **AI được dùng để làm gì:** Tạo voice-over từ văn bản bằng giọng tổng hợp. Đơn kiện cáo buộc bản ghi của hai nguyên đơn được dùng để tạo các giọng thương mại “Kyle Snow” và “Sally Coleman” ngoài mục đích giới hạn đã trao đổi qua Fiverr.
- **Vấn đề hoặc sự kiện đáng chú ý:** Theo đơn kiện, Lehrman được nói bản ghi chỉ dùng cho nghiên cứu học thuật và được trả 1.200 USD; Sage được nói bản ghi test quảng cáo chỉ dùng nội bộ và được trả 400 USD. Hai người cáo buộc giọng của họ sau đó được nhân bản, tiếp thị và dùng thương mại mà không được cho biết hoặc trả thêm. Việc tòa cho một số claim tiếp tục nghĩa là các cáo buộc đó đủ để được xem xét ở giai đoạn tố tụng, **không phải** phán quyết cuối cùng rằng LOVO chịu trách nhiệm.
- **Số liệu có nguồn:** Đơn kiện nêu rằng tới tháng 01/2023 LOVO đã tạo **hơn 7 triệu voice-over** và CEO nói hệ thống cần khoảng **50 câu** để nắm bắt giọng. Các số liệu này mô tả quy mô/công nghệ của sản phẩm; chúng không chứng minh 7 triệu output đều dùng giọng không được phép.
- **Nguồn:**
  - “[Class Action Complaint — Lehrman et al. v. Lovo, Inc.](https://static.pollockcohen.com/docs/2024.05.16-Lehrman-v-LOVO-complaint-Final.pdf),” Case 1:24-cv-03770, filed 16/05/2024, đặc biệt các đoạn 17–18, 28–54, 57–77 — đơn kiện và cáo buộc của nguyên đơn.
  - David Grossman & Alexander Loh, “[Lehrman v. Lovo Inc.](https://www.loeb.com/en/insights/publications/2025/07/lehrman-v-lovo-inc),” *Loeb & Loeb*, 10/07/2025 — tóm tắt lệnh của tòa về motion to dismiss và các claim được tiếp tục/bị bác.
- **Phân biệt bằng chứng và nhận định:** **Bằng chứng:** vụ kiện, nội dung đơn, khoản thanh toán được nêu, quy mô sản phẩm được viện dẫn và lệnh motion-to-dismiss. **Cáo buộc chưa có phán quyết cuối cùng:** LOVO dùng trái phép giọng của hai nguyên đơn và gây mất thu nhập. **Nhận định:** giọng nói nhận dạng được cần được quản trị như dữ liệu danh tính; nguy cơ giả mạo, mất phẩm giá và mất cơ hội tăng mạnh khi một voice clone có thể tạo nội dung không giới hạn.

### Harm Map Worksheet

| Trường | Phân tích của tôi |
| --- | --- |
| High-risk moment | Khi bản ghi được cung cấp cho mục đích giới hạn được biến thành một giọng tổng hợp tái sử dụng, đưa vào catalog và cho khách hàng tạo câu nói mới mà không có consent riêng, minh bạch và cơ chế thu hồi tương xứng. |
| Stakeholder bị ảnh hưởng | Diễn viên lồng tiếng và gia đình; khách hàng/người nghe có thể tưởng giọng là thật; LOVO và khách hàng; nền tảng phát hành podcast, quảng cáo hoặc video; cộng đồng voice actor. |
| Failure mode | **Misuse** (dùng bản ghi/voice clone ngoài mục đích được phép, theo cáo buộc) và rủi ro **privacy leak/identity misuse** vì giọng nói nhận dạng được có thể bị tái tạo. |
| Layer bắt đầu lỗi | **Grounding / nguồn dữ liệu và consent:** mục đích, quyền và provenance của bản ghi. **Safety:** cần kiểm soát ai được tạo bản sao, nội dung nào được sinh và khi nào phải chặn/takedown. Kiến trúc nội bộ không công khai nên không kết luận chi tiết hơn. |
| Harm xảy ra là gì? | **Đã xảy ra:** hai diễn viên khởi kiện; một số claim được tiếp tục ở giai đoạn motion-to-dismiss. **Theo cáo buộc:** giọng bị dùng thương mại ngoài phạm vi đồng ý và không có bồi thường bổ sung. **Nguy cơ:** giả mạo phát ngôn, tổn hại danh tiếng, mất việc/royalty và người nghe bị đánh lừa. |
| Harm lens | **Privacy loss, dignity loss và opportunity loss**; misinformation có thể phát sinh nếu output làm người nghe tin chủ thể thật đã nói câu đó. |
| Severity | **High:** giọng nói gắn với danh tính và sinh kế; một bản sao có thể tạo vô số phát ngôn mới. Không đánh giá Critical vì case chưa chứng minh tổn hại thể chất hoặc hậu quả đặc biệt nghiêm trọng. |
| Scale | **Medium–High về khả năng lan rộng:** sản phẩm được mô tả có hơn 7 triệu voice-over vào 01/2023. Tuy nhiên case chỉ nêu hai nguyên đơn cụ thể và không chứng minh mọi output đều trái phép. |
| Probability | **Không thể lượng hóa từ nguồn.** Hai cáo buộc cụ thể và việc claim được tiếp tục cho thấy rủi ro có cơ sở để điều tra, nhưng không phải xác suất áp dụng cho toàn bộ catalog. |
| Frequency | **Theo cáo buộc, việc sử dụng diễn ra lặp lại trong nhiều năm:** giọng “Kyle Snow” được nói là giọng mặc định từ 2021 đến 09/2023. Số lượt tạo nội dung bằng hai giọng và tỷ lệ không có phép chưa được công bố. |
| Vì sao? | Scale sản phẩm lớn nhưng quy mô vi phạm chưa được chứng minh, nên không suy diễn 7 triệu output thành 7 triệu hành vi gây hại. Biện pháp phù hợp gồm consent theo mục đích, hợp đồng nêu rõ quyền huấn luyện và thương mại, xác minh danh tính, watermark/provenance cho audio, log sử dụng, chia sẻ doanh thu và quy trình thu hồi/takedown nhanh. |

## 5. Kết luận và ưu tiên kiểm soát

Ba case cho thấy rủi ro của AI trong sáng tạo nội dung không chỉ nằm ở “mô hình tạo sai”. Rủi ro có thể xuất hiện ở toàn chuỗi: dữ liệu đầu vào không rõ quyền, mô hình tạo nội dung sai hoặc bắt chước danh tính, giao diện khiến người dùng quá tin và quy trình xuất bản không kiểm tra đầy đủ.

Thứ tự ưu tiên kiểm soát của tôi:

1. **Xác minh nguồn và quyền sử dụng dữ liệu trước khi huấn luyện hoặc nhân bản danh tính.**
2. **Bắt buộc human review theo mức rủi ro trước khi xuất bản**, đặc biệt với tài chính, sức khỏe, pháp lý và nội dung gắn với người thật.
3. **Giữ provenance và minh bạch nội dung AI**, gồm nguồn, licence, phiên bản, người duyệt và lịch sử chỉnh sửa.
4. **Cho creator quyền kiểm soát thực tế:** đồng ý theo mục đích, bồi thường, opt-out, thu hồi và khiếu nại/takedown.
5. **Đo counter-metrics:** tỷ lệ bài phải đính chính, khiếu nại quyền, thời gian xử lý takedown, tỷ lệ output bị chặn và số lần human review phát hiện lỗi.

## 6. Ghi chú sử dụng AI

AI được dùng để hỗ trợ tìm từ khóa, hệ thống hóa nguồn và rà soát cấu trúc theo mẫu Lab 21. Người làm bài đã đối chiếu lại các số liệu với tài liệu được dẫn, giữ nguyên trạng thái “cáo buộc” đối với các vụ kiện chưa có kết luận cuối cùng và chịu trách nhiệm về phần phân tích/rating trong Harm Map.

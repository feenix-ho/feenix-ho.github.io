---
layout: post
title: Some Thoughts on Current Large Language Models
date: 2023-04-24 15:30 +0700
tags:
  [
    natural-language-processing,
    AI-assistant,
    large-language-models,
    ChatGPT,
    BingAI
  ]
categories: [AI Tools, Chat Models]
toc: true
comments: true
math: true
mermaid: true
---

Hôm nay, nhân một ngày thứ Hai oi bức, sáng bảnh mắt ra, sau khi làm xong những việc lặt vặt cần làm, mình lao vào bàn máy tính, bóc lột mấy con large language model hiện có trên thị trường: ChatGPT, GoogleBard, và BingAI.

Ở phần này, mình sẽ chỉ nói về ChatGPT và BingAI, lý do là mình chưa có nhiều trải nghiệm với GoogleBard lắm. Mình sẽ để dành Bard cho phần sau, khi mà mình đã trải nghiệm đủ nhiều để đưa ra các đánh giá khách quan nhất.

Trước khi bước vào những thứ nó sâu xa hơn, mình xin được phép nhận xét những thứ bề mặt trước.

(Ở cuối bài có TL;DR cho bạn nào ngán chữ giống mình)

## Disclaimer

Những thứ sau đây hoàn toàn là trải nghiệm của cá nhân mình khi sử dụng cả ba tiện ích. Mình dùng bọn nó hoàn toàn bằng tiếng Anh, thế nên mình cũng không rõ là nếu hỏi tụi nó bằng tiếng Việt thì tụi nó trả lời có ổn không (mình cá là không vì dataset tiếng Việt khá hạn chế).

Bên cạnh đó, cách đặt câu hỏi của mình có thể khác với cách đặt câu hỏi của bạn, dẫn đến trải nghiệm khác nhau. Vì thế, mình mong rằng bài này sẽ chỉ là một góc nhìn để các bạn tham khảo, chứ không phải để dùng làm kim chỉ nam. Hãy trải nghiệm để mở mang tầm mắt nhé.

## Giao diện

Nhìn chung, cả ba đứa đều có giao diện dễ xài, thân thiện với người dùng (ít nhất là thân thiện với mình). Mình không có quá nhiều khó khăn khi mà dùng cả ba đứa.

Tụi nó đều có nút copy, upvote, downvote.

Với ChatGPT thì tiện hơi xíu, vì nó hiện cả 3 nút ở ngay cuối đoạn văn nó generate, mình nhìn thấy luôn, khỏi phải mò.
Với Bing và Bard thì sẽ thêm một bước nữa, tại vì chức năng copy nó nằm trong một cái button hình dấu 3 chấm. Nhưng mà nhìn chung thì cũng không quá khó để mò ra, nên ừ, dễ xài.

Riêng với code thì ChatGPT và GoogleBard có riêng nút copy cho đoạn code có trong văn bản được generate. Ở điểm này thì BingAI có hơi thiếu sót. Nếu mà hỏi một câu về code ở trên Bing thì sẽ phải dùng chuột select phần code rồi copy.

## Chức năng

Bing có chức năng <em style="color:#de6b18">share</em>. Mình chưa xài bao giờ, và mình cũng không thấy có lý do gì để xài. Nhưng mà maybe sẽ có người cảm thấy câu trả lời của Bing thú vị và share về các nền tảng xã hội. Nhưng mà hừm, với cá nhân mình thì mình thấy nó hơi vô nghĩa.

Bard và ChatGPT có chức năng <em style="color:#de6b18">re-generate</em> câu trả lời. Lỡ mà mình không thích cái câu trả lời hiện tại của tụi nó, bấm re-generate thì tụi nó sẽ cho ra câu trả lời khác. Đa số thời gian sẽ không quá khác về mặt nội dung, nhưng sẽ có sự khác biệt về mặt văn phong. Tuy nhiên cũng có lúc nó sẽ cho ra các ý nhỏ (bullet point) khác, nhờ đó mà mình có thể mở rộng lựa chọn.

Bing thì không có chức năng này. Mình chưa rõ lý do chính xác là vì sao, nhưng mình nghĩ lý do lớn nhất là vì Bing thiên về hướng một cái search engine có thêm khả năng tổng hợp hơn là một assistant. Cái này sẽ nói kỹ hơn ở phần sau.

Có một điểm mà ChatGPT hơn hẳn cả hai đứa còn lại, đó là khả năng <em style="color:#de6b18">lưu trữ</em> các cuộc hội thoại cũ theo từng chủ đề khác nhau. Với BingAI, mỗi cuộc trò chuyện sẽ bị giới hạn ở mức 20 câu hỏi. Có nghĩa là, sau 20 câu hỏi (đi kèm đó là 20 câu trả lời từ Bing), chúng ta sẽ không có cách nào tiếp tục cuộc trò chuyện với chủ đề cũ. Với Bard, dù không bị giới hạn bởi số câu hỏi, nhưng vì không có tính năng tạo cuộc trò chuyện mới, thế nên khá khó để keep track được chủ đề của cuộc trò chuyện. Điều này khiến cho người dùng sẽ khá khó để mà lục lại cuộc trò chuyện cũ.

Với ChatGPT, chúng ta có thể tạo cuộc hội thoại cho từng chủ đề, discuss với nó xoay quanh chủ đề đó, đặt tên cho cuộc hội thoại. Từ đó khiến cho việc tìm kiếm sau này cũng dễ dàng hơn. Hơn nữa, ChatGPT khá tốt trong việc tập trung vào chủ đề (này mình sẽ nói kỹ hơn ở phần sau), giúp cho việc engage vào câu chuyện cũng trở nên dễ hơn, thú vị hơn.

Chức năng <em style="color:#de6b18">Google It</em> của Bard khá tương tự với bản chất của Bing - Bing search trên các trang mạng rồi mới đưa ra kết quả. Cái này mình sẽ nói sâu hơn ở phần sau.

GoogleBard còn có một tính năng nho nhỏ, đó là thay vì chỉ generate ra 1 câu trả lời, nó sẽ cho ra <em style="color:#de6b18">nhiều câu trả lời một lúc</em> (chính xác là 4). Khi bạn bấm vào “view more drafts”, nó sẽ cho ra thêm 3 câu trả lời khác, bạn có thể chọn 1 trong 4 lựa chọn này.

## Performance

(kèm với lĩnh vực mà mình nghĩ là từng đứa sẽ phù hợp).

Đánh giá đứa nào tốt hơn, vượt trội hơn hẳn những đứa kia thì mình thấy hơi phiến diện, vì sự thật là mỗi tụi nó có một ưu điểm riêng.

Mình sẽ minh hoạ cách mình dùng ChatGPT và BingAI trong một ví dụ sau đây.

### Ví dụ

Cuối kỳ môn "Technology-based Innovation and Leadership" vừa rồi, mình được cho đề bài như sau:

Topic: "Designing an Innovative App for Social Change"

Prompt: Technology has the potential to drive creative and innovative solutions for social challenges. In your final exam, you are required to generate and develop an original idea for a technology-based innovation in the form of a mobile app that addresses a specific social challenge. You will need to demonstrate creativity, critical thinking, and problem-solving skills in ideating, conceptualizing, and designing an app that reflects your innovative idea for social change.

Khi mà phác thảo ra ý tưởng, mình có những ý chính như sau:

Vấn đề chính mà mình muốn giải quyết: Giảm thiểu carbon footprint trong thực phẩm. Với vấn đề chính này, mình định hình những yếu tố hình thành nên vấn đề.

Ngay tại chỗ này, mình muốn biết, các yếu tố nào đóng góp vào lượng khí thải của một sản phẩm. Mình sẽ dùng BingAI cho việc này. Lý do là <em style="color:#de6b18">BingAI tận dụng được sức mạnh của search engine, cho phép nó tìm kiếm thông tin trong thời gian thực</em>. Nó đồng nghĩa với việc khả năng cao là thông tin bạn kiếm được đã được kiểm chứng (hoặc ít nhất là có nguồn để bạn tự đi kiểm chứng).

Ngay tại chỗ này thì Bing có một ưu điểm: Nó sẽ <em style="color:#de6b18">dẫn nguồn</em> những thông tin nó cung cấp cho bạn ở dưới footnote. Việc này rất có lợi nếu như bạn viết các bài tập khoa học ở đại học hoặc cấp học cao hơn.

Sau đây là kết quả mình nhận được (đã lược dịch): Với thực phẩm, có khá nhiều công đoạn tạo nên carbon footprint của một sản phẩm, từ việc chặt cây tạo đất nông nghiệp, trồng trọt chăn nuôi, xử lý thực phẩm, vận chuyển, bảo quản, đóng gói, v.v.

Từ những câu đoạn đó, mình chọn ra cái dễ thay đổi nhất, ở đây là vận chuyển: Nếu như mình thúc đẩy tiêu dùng địa phương (mua nông sản từ local farmers) thì rõ ràng, mình sẽ giảm thiểu được ô nhiễm gây ra bởi việc vận chuyển quốc tế.

Sau khi định hình được mấy cái gạch đầu dòng như thế, mình ném cho ChatGPT, xem xem với hướng đi của mình thì nó phát triển được những gì. ChatGPT bị giới hạn bởi việc nó học trên một tập data có sẵn.

Tập data đó được chính ChatGPT miêu tả như sau:

> As an AI language model, I was trained on a very large dataset of text called the Common Crawl. The Common Crawl is a vast collection of web pages and documents that have been made available to the public for research purposes. The version of the Common Crawl used to train me was released in early 2020 and contained over 45 terabytes of compressed text data, which is equivalent to several trillion words. This dataset was used to train the GPT-3.5 architecture, which I am based on.

> As an AI language model, I am constantly updated with the latest information, but my knowledge is based on the cutoff date of my training data, which is September 2021. While I strive to provide the most accurate and up-to-date information possible, there may be some topics or events that have occurred after this date that I am not yet aware of. If you have any specific questions or topics that are related to events or developments that have occurred after September 2021, please let me know and I will do my best to provide you with the most up-to-date information available.

Điều đó có nghĩa là những thứ xảy ra sau tháng 9 năm 2021 sẽ không có trong kho kiến thức của ChatGPT. Song, vì tập data đồ sộ nêu trên, <em style="color:#de6b18">ChatGPT có khả năng viết ra những đoạn văn nghe siêu tự nhiên, siêu mượt mà, ngay cả khi nó đang nói phét</em>.

Đúng rồi đấy, bạn không nghe nhầm đâu, ChatGPT nói phét như thật luôn. Xin phép được dùng một ví dụ khác để minh chứng cho sự bịa như thật của ChatGPT: Đợt nọ, mình dùng ChatGPT để làm literature review cho một topic mình nghiên cứu. Lúc đó mình khá non, nên mình chỉ đưa ra các câu lệnh đơn giản như là, Ê giúp tui viết literature review về chủ đề ABC này với. Xong nó viết. Xong mình thấy nó không có để citation, thế là mình kêu, Ê dẫn cái nguồn vào bạn ơi. Xong nó dẫn nguồn, dẫn như thật luôn. Xong mình kiểu, ủa chà, mấy cái paper này mình chưa đọc, vào đọc thứ xem nào. Đoán xem chuyện gì xảy ra? Mình search trên Google Scholar, không có một cái paper nào có thật. Vấn đề là nó cite đúng format lắm. Bịa tên paper, bịa cả tên tác giả nhìn như thật luôn cơ. Thế là sau lần đấy, mình rút được kinh nghiệm xương máu. Đó là những thứ thiên về độ chính xác, tính xác thực cao (ví dụ như các con số cụ thể, các công trình nghiên cứu cụ thể) thì đừng tin ChatGPT làm gì.

Nhưng mà, nói đi vẫn phải nói lại, văn phong của ChatGPT thật sự rất tự nhiên, nhất là khi bạn làm rõ với nó là bạn muốn nó viết với tone như thế nào.

Đồng thời, nhờ vào sự đa dạng và đồ sộ của tập dữ liệu huấn luyện, ChatGPT thật sự rất tốt trong việc prompt ý tưởng.

Tiếp tục với ví dụ còn đang dang dở. Sau khi định hình được bài toán cần giải quyết, mình đề ra cách giải quyết: Tạo ra một nền tảng trực tuyến có thể kết nối trực tiếp nông dân địa phương với người tiêu dùng. Giải pháp của mình là tạo ra một ứng dụng điện thoại để cho nông dân có thể trình bày về quy trình sản xuất cũng nhưng tiêu chuẩn sản phẩn, sau đó nền tảng sẽ đem mấy cái đó đến một đơn vị thứ ba để kiểm nghiệm.

Sau khi miêu tả với ChatGPT, mình đặt câu hỏi, những rủi ro có thể xảy ra với nền tảng. Mình không dùng BingAI, vì ở phương diện này, việc browse web không có hiệu quả. Nó cần sự engage vào chủ đề hơn là sự fact check thông tin, và về phương diện này, ChatGPT làm tốt hơn rất nhiều.

### Pros and Cons

|         | Pros                                                                                                                                                        | Cons                                                                                                                                                                                 |
| ------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| ChatGPT | - Tập dữ liệu lớn, đa dạng <br>- Văn phong tự nhiên<br>- Có khả năng thảo luận tốt<br>- Có khả năng đưa ra các câu trả lời đa dạng cho cùng một câu hỏi<br> | - Tập dữ liệu không được cập nhật theo thời gian thực<br>- Không có cơ chế fact check, dẫn đến câu trả lời có thể không đúng sự thật<br>                                             |
| BingAI  | - Khả năng browse web cho phép đưa ra thông tin realtime<br>- Có trích dẫn nguồn, khiến cho việc kiểm chứng dễ dàng hơn<br>                                 | - Không linh hoạt trong việc trả lời những câu hỏi có xu hướng cá nhân<br>- Có chiều hướng phụ thuộc hơi nhiều vào search engine, dẫn đến việc câu trả lời không có tính đa dạng<br> |

## Tổng kết

ChatGPT và BingAI có điểm mạnh và điểm yếu riêng. Tuỳ thuộc vào nhu cầu sử dụng mà mọi người có thể chọn model khác nhau. Mình cảm thấy cách tốt nhất để tận dụng mấy khứa này là dùng cả hai.

**TL;DR**

- **BingAI** thiên về dạng <em style="color:#de6b18">search engine</em> có hỗ trợ tính năng của trí tuệ nhân tạo hơn là một trợ lý ảo.
  - Khả năng browse của nó cho phép đó đưa ra thông tin được cập nhật trong <em style="color:#de6b18">thời gian thực</em>.
  - Điểm cộng lớn là những thông tin này sẽ được <em style="color:#de6b18">dẫn nguồn</em>, khiến cho việc kiểm chứng dễ dàng hơn.
  - Điểm trừ là đa số thời gian nó sẽ khá <em style="color:#de6b18">cứng nhắc</em> do khi browse webs nó sẽ có xu hướng dùng những kết quả có rank cao hơn (đồng nghĩa với việc sẽ khó có sự đa dạng trong câu trả lời).
  - Nhìn chung, với vai trò là <em style="color:#de6b18">một search engine được nâng cấp với tính năng AI</em> thì nó làm khá tốt.
  - Phù hợp để hỏi những câu cần <em style="color:#de6b18">độ chính xác cao</em>, không phù hợp để bàn luận những vấn đề cần sự linh hoạt.
- **ChatGPT** có thể được xem là một <em style="color:#de6b18">large language model thuần tuý</em>.
  - Tập dữ liệu huấn luyện cũng không được cập nhật theo thời gian thực.
  - Điểm cộng là tập dữ liệu này rất lớn, giúp cho văn phong của ChatGPT siêu <em style="color:#de6b18">mượt</em>, đồng thời cũng siêu <em style="color:#de6b18">đa dạng</em>.
  - Điểm trừ là thông tin đưa ra sẽ <em style="color:#de6b18">không được kiểm chứng</em>.
  - Nhìn chung, ChatGPT là một công cụ <em style="color:#de6b18">prompt ý tưởng</em> tốt. Nó có khả năng đưa ra câu trả lời khá thú vị do sự đa dạng trong bộ dữ liệu.
  - Phù hợp để <em style="color:#de6b18">khai triển ý tưởng</em>, không phù hợp để dùng làm nguồn trích dẫn.

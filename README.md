# PHÂN TÍCH DỮ LIỆU KINH DOANH IS403.O21 - Nhóm 6
## Mở đầu
Đây là nơi chứa mã nguồn và các tài nguyên cho đồ án của nhóm 6 chúng em với chủ đề: DỰ BÁO GIÁ KHOÁNG SẢN SỬ DỤNG CÁC KỸ THUẬT PHÂN TÍCH CHUỖI THỜI GIAN

## Giới thiệu đề tài
Sự biến động của giá vàng(Au), bạc(Ag) và bạch kim(Pt) luôn là điểm nóng trong lĩnh vực đầu tư và tài chính. Việc dự đoán giá của các loại kim loại quý này không chỉ có ý nghĩa quan trọng trong việc hỗ trợ quyết định đầu tư của các nhà đầu tư và phân tích thị trường, mà còn trong việc cung cấp thông tin chi tiết và chính xác về biến động giá, giúp cải thiện đáng kể hiệu suất kinh doanh và quản lý rủi ro trong các lĩnh vực liên quan như chứng khoán và tiền tệ. Dự đoán giá kim loại quý như vàng không chỉ tập trung vào dự đoán giá toàn cầu của 1 ngày hôm sau mà còn dự đoán giá trong tương lai xa hơn như 3 đến 5 tháng sau, dự đoán khoảng biến động giá, xu hướng biến động, mối liên hệ của giá các kim loại,... Do đó, nhiều trang điện tử dự báo chuyên nghiệp đã được thiết lập như Bloomberg, Kitco, LBmMA,... Bằng cách so sánh và kiểm định nhiều phương pháp và mô hình dự báo từ kinh điển cho đến mới nhất, nhóm nghiên cứu kỳ vọng sẽ tìm ra được mô hình, thuật toán với kết quả khả quan nhất nhằm linh hoạt đáp ứng được nhu cầu ngày một cao của thị trường. Bài nghiên cứu của chúng em sử dụng bộ dữ liệu từ trang thông tin điện tử MetalPriceAPI để lấy giá vàng, bạch kim, bạc được ghi nhận trong quá khứ (lấy theo mệnh giá USD).

## Bộ dữ liệu
Bộ ba dataset thể hiện giá ba loại kim loại quý: vàng, bạc và bạch kim trong khoảng thời gian từ 1/1/2018 đến 1/6/2024 được lấy nguồn từ các API do https://metalpriceapi.com/ cung cấp. Sau khi gọi API để lấy dữ liệu, nhóm tiến hành chuyển đổi từ dạng json thành csv và thu được 3 file csv gồm:
- Giá vàng: gold_price_2018_2024.csv
- Giá bạc: silver_price_2018_2024.csv
- Giá bạch kim: platium_price_2018_2024.csv
Trong mỗi tập dữ liệu gồm hai cột:
- _Date_: ngày thu nhập dữ liệu (định dạng YYYY-MM-DD).
- _Value (USD per troy ounce)_: giá của kim loại quý tương ứng với cột _Date_ (mệnh giá USD).

## Các mô hình sử dụng
Những mô hình và thuật toán được sử dụng để thực hiện việc đánh giá trên bộ dữ liệu trong đồ án này bao gồm: 
- Linear Regression
- ARIMA
- Fast Fourier Transform Forecasting Model (FFT)
- Recurrent Neural Networks (RNN)
- Gated Recurrent Units (GRU)
- Long Short-Term Memory (LSTM)
- Simple exponential smoothing (SES)
- **T**rigonometric seasonality, **B**ox-Cox transformation, **ARMA** errors, **T**rend and **S**easonal components (TBATS)
- Neural Hierarchical Interpolation for Time Series Forecasting(N-HiTS)
- Patch Time Series Transformer(PatchTST)

## Phương pháp đánh giá
- Các mô hình được đánh giá bằng các thước đo hiệu suất khác nhau như Mean Absolute Percentage Error (MAPE), Root Mean Square Error (RMSE), Mean Average Error (MAE)
- Ba tỷ lệ được sử dụng để chia dữ liệu ban đầu huấn luyện - kiểm tra khác nhau trước khi áp dụng cho các mô hình là: 70:30, 80:20 và 90:10. Mục đích của việc phân tách với 3 tỉ lệ như vậy để có thể tiến hành so sánh được điểm mạnh, điểm yếu của các mô hình đối với từng tỉ lệ dữ liệu khác nhau như thế nào, từ đó có thể rút ra được kinh nghiệm cho nhóm trong cách sử dụng các mô hình này để thực hiện dự đoán trên dữ liệu chuỗi thời gian.

## Phân công công việc
| Thành viên | Mã số sinh viên | Công việc |
| --- | --- |--- |
| Trần Kim Thanh | 21522605 | Thực hiện mô hình GRU, PatchTST - Viết báo cáo latex|
| Võ Ngọc Lệ Xuân | 21521692 | Thực hiện mô hình SES, LSTM - Viết báo cáo latex|
| Trần Minh Hoàng | 21522101 |Thực hiện mô hình Linear Regression, TBATS - Viết báo cáo latex|
| Mai Quốc Bảo | 21521850 | Thực hiện mô hình FFT, RNN - Viết báo cáo latex|
| Bùi Hữu Bằng | 21520151 | Thực hiện mô hình ARIMA, N-HiTS - Viết báo cáo latex|


## Đóng góp
Chúng em rất sẵn sàng tiếp nhận mọi ý kiến đóng góp của thầy và sẽ sửa đổi để có thể khiến cho đồ án tốt hơn ạ.

## Lời cảm ơn
Chúng em xin gửi lời cảm ơn chân thành đến Phó Giáo sư Tiến sĩ Nguyễn Đình Thuân và Trợ giảng Nguyễn Minh Nhựt vì sự tận tâm và hướng dẫn nhiệt tình của thầy và anh. Những bài học quý báu từ thầy đã giúp chúng em hoàn thành dự án này và sẽ là nền tảng vững chắc cho những nỗ lực tương lai của chúng em. Dự án này sẽ không thể hoàn thành nếu thiếu sự giám sát và chỉ đạo của thầy. Trong suốt quá trình thực hiện dự án, chúng em đã gặp không ít khó khăn và thử thách. Nhưng nhờ có sự đoàn kết và hợp tác, chúng em đã vượt qua tất cả và hoàn thành công việc. Dự án này cũng đã mang lại cho chúng em cơ hội thực hành thực tế, giúp chúng em tích lũy được nhiều kinh nghiệm quý báu.
Chúng em cũng xin gửi lời cảm ơn đến các thành viên trong nhóm vì những đóng góp và sự hỗ trợ nhiệt tình trong suốt quá trình thực hiện dự án. Nhờ có sự hỗ trợ và cộng tác của các bạn, chúng em đã học hỏi được nhiều điều và hoàn thành công việc một cách tốt nhất.

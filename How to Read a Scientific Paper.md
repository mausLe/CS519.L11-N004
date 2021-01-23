READING - TÌM HIỂU BÀI  BÁO KHOA HỌC

1. Chọn một bài báo từ các hội nghị uy tín chuyên ngành như CVPR

2. Xác định vấn đề được bài báo giải quyết

3. Xác định giả thiết (hypothesis) của bài báo. Tại sao tác giả lại đi đến giả thiết đó (thường là trên sự phân tích của các giả thiết đã được kiểm chứng khác)

4. Xác định cách chứng minh (prove) giả thiết là đúng. Các thí nghiệm được thiết kế thế nào, kết quả thí nghiệm ra sao, các kết quả có đủ độ tin cậy để chứng minh giả thiết
_________________
1. Bài báo: PifPaf: Composite Fields for Human Pose Estimation. Tại CVPR 2019. Link PDF: https://arxiv.org/pdf/1903.06593.pdf

2. Trong bài báo, nhóm tác giả đề xuất một phương pháp để xác định dáng của nhiều người. Phương pháp này đặc biệt phù hợp cho các ứng dụng về Xe tư lái, robot vận chuyển... hoạt động trong môi trường đô thị đông đúc.
3. Trong phân tích các công trình trước đó, nhóm tác giả lựa chọn: OpenPose và Mask R-CNN, 2 SOTA papers. Tuy nhiên, dù 2 phương pháp trên cho các kết quả tốt trên ảnh có độ phân giải cao, chúng lại cho những kết quả tệ trong những ảnh có độ phân giải thấp và cả trong môi trường đô thị đông đúc. Từ đó, nhóm đã đề xuất một phương pháp tiệp cận Top-down, sử kiến trúc ResNet gồm 2 mạng NN. Part Intensity Field (PIF) dự đoán bản đồ tự tin (confidence map), vị trí chính xác của các điểm liên kết và Part Association Field (PAF) xác định mối liên kết giữa các điểm.
4. Trong phần đánh giá, nhóm tác giả đã chứng minh tính hiệu quả của phương pháp trên ảnh chất lượng thấp (321x321px), cho kết quả vượt OpenPose và Mask R-CNN trên thang đo AP và AR trên bộ dữ liệu COCO. Cụ thể, nhóm đã lựa chọn 3 baseline: ResNet50/101/152, xây dựng kiến trúc mạng và tiến hành huấn luyện trên 64115 ảnh. Quá trình đánh giá sau đó được thực hiện trên 5000 ảnh cho AP = 50 và AR=55. Để chứng minh tính ứng dụng cho Xe tự hành và robot, nhóm tác giả đưa ra một số kết quả định lượng khi thử nghiệm trên các hoạt cảnh trong đô thị - nơi có nhiều nhiễu và đối tượng cần xác định. Kết quả là OpenPifPaf có thể xác định được các đối tượng xen kẽ với các đối tượng khác (occlude) và cho ít Dương tính giả hơn OpenPose và Mask R-CNN.

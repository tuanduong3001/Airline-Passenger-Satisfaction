## Mô tả

Tập dữ liệu này chứa một cuộc khảo sát về mức độ hài lòng của hành khách hàng không. Được chia làm 2 file csv gồm: train.csv và test.csv và được chia theo phương pháp hold out theo tỉ lệ 8/2. Trong đó file train chiếm 80% (103903 thực thể) và file test chiếm 20% (25975 thực thể). Qua đó cho thấy toàn bộ dữ liệu có gần 130000 thực thể và 23 features như:

-   Gender: Giới tính của khách hàng (nam, nữ)

-   Customer Type: Loại khách hàng (khách hàng thân thiết, khách hàng không thân thiết)

-   Age: tuổi của khách hàng

-   Type of Travel: Mục đích chuyến bay của hành khách (du lịch cá nhân, đi công tác)

-   Class: Hạng du lịch trên máy bay của hành khách (Business, Eco, Eco Plus)

-   Flight distance: khoảng cách chuyến bay

-   Inflight wifi service: Mức độ hài lòng về dịch vụ wifi trên chuyến bay (0: Không áp dụng; 1-5)

-   Departure/Arrival time convenient: Mức độ hài lòng về Thời gian Đi / Đến thuận tiện

-   Ease of Online booking: Mức độ hài lòng khi đặt vé trực tuyến

-   Gate location: Mức độ hài lòng về vị trí cồng

-   Food and drink: Mức độ hài lòng về Đồ ăn và thức uống

-   Online boarding: Mức độ hài lòng của nội trú trực tuyến

-   Seat comfort: Mức độ hài lòng về sự thoải mái của chỗ ngồi

-   Inflight entertainment: Mức độ hài lòng của giải trí trên chuyến bay

-   On-board service: Mức độ hài lòng của dịch vụ trên máy bay

-   Leg room service: Mứcc độ hài lòng của dịch vụ phòng chờ

-   Baggage handling: Mức độ hài lòng của việc xếp dỡ hành lý

-   Check-in service: Mức độ hài lòng của dịch vụ check-in

-   Inflight service: Mức độ hài lòng của dịch vụ trên chuyến bay

-   Cleanliness: Mức độ hài lòng về sự Sạch sẽ

-   Departure Delay in Minutes: Bị hoãn vài phút khi khởi hành

-   Arrival Delay in Minutes: Bị Chậm Phút Khi Đến Nơi

-   Satisfaction: Mức độ hài lòng của hãng hàng không (Hài lòng, trung lập hoặc không hài lòng)

## Thư viện được sử dụng

![image](https://user-images.githubusercontent.com/56602084/172420067-db0e6c8d-c679-4501-a3b2-46daa7e27b85.png)

## Tải tập dữ liệu

![image](https://user-images.githubusercontent.com/56602084/172420306-a3b140ee-1e64-44c9-a0e1-dc86b127d65c.png)

Sau khi import datase nhóm thấy có 2 cột bị thừa ở 2 dataset đó là cột X và id nên nhóm đã quyết định loại bỏ 2 cột này

## Tổng quan về dữ liệu và tính toán giá trị NA

# Tóm tắt dữ liệu

![image](https://user-images.githubusercontent.com/56602084/172420697-97a53e79-29b2-4aff-aced-14588810711c.png)

![image](https://user-images.githubusercontent.com/56602084/172420783-75176c6f-4558-48e2-8b58-ec059ddc541b.png)

# Tính toán giá trị NA

![image](https://user-images.githubusercontent.com/56602084/172421119-aee38c2e-937b-48e7-9119-c581fcb2b784.png)

![image](https://user-images.githubusercontent.com/56602084/172421203-29c24ba3-745c-42bd-ab8d-ed4456a1e12f.png)

Qua đó ta có thể thấy được trong biến Arrival.Delay.in.Minutes có chứa N/A value và nó chỉ chiếm tỉ lệ rất thấp (trong đó ở tập train là 300 dòng có giá trị NA chiếm 0.3% còn ở tập test là 80 dòng chiếm 0.32%). Vì thế quyết định sẽ dùng hàm drop_na để loại bỏ những dòng này

## Machine Learning
# Độ tương quan

Các tham số có thể dùng để dự đoán bao gồm: Age, Customer.Type, Flight.Distance, Inflight.wifi.service, Ease.of.Online.booking, Food.and.drink, Online.boarding, Seat.comfort, Inflight.entertainment, On.board.service, Leg.room.service, Baggage.handling, Checkin.service, Inflight.service, Cleanliness

# Knn

![image](https://user-images.githubusercontent.com/56602084/172421869-df92feb2-53ce-4274-af3e-f3fbc9bb5b8f.png)

# Decision Tree

![image](https://user-images.githubusercontent.com/56602084/172422018-fcd8a21a-9892-4a3e-a1b2-29eabeb00559.png)

![image](https://user-images.githubusercontent.com/56602084/172422064-4a77f316-7027-4bc8-951f-8ac349fa2280.png)

# Random Forest

![image](https://user-images.githubusercontent.com/56602084/172422165-3d0ce0c4-66c1-4787-8e89-a80a7d91a5a9.png)





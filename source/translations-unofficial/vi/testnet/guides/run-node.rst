.. `Trang tổng quan mạng`: https://dashboard.testnet.concordium.com/
.. Discord: https://discord.gg/xWmQ5tp

.. Chạy một Node:

=============
Chạy một Node
=============

.. contents::
   :local:
   :backlinks: none

Trong hướng dẫn này, bạn học cách chạy một Node trên máy tính của mình
tham gia vào mạng Concordium. Điều này có nghĩa là bạn nhận được
khối và giao dịch từ các Node khác, cũng như lan truyền
thông tin về các khối và giao dịch tới các Node trong mạng lưới Concordium
. Sau khi làm theo hướng dẫn này, bạn sẽ có thể

- chạy một Node Concordium
- quan sát nó trên bảng điều khiển mạng và
- truy vấn trạng thái của blockchain Concordium trực tiếp từ
   máy tính.

Bạn không cần có tài khoản để chạy một Node.

Trước khi bắt đầu
=================

Trước khi chạy một Node Concordium, bạn cần phải

1. Cài đặt và chạy Docker.

   - Trên * Linux *, cho phép Docker chạy với tư cách người dùng không phải root.

2. Tải xuống và giải nén phần mềm :ref:`concordium-node-and-client-download`.

Nâng cấp từ phiên bản Open Testnet trước đó
===============================================

Để nâng cấp lên phần mềm Concordium hiện tại cho Open Testnet 4:

- Làm theo các bước trên để :ref:`download<downloads>`cập nhật phần mềm Concordium mới nhất.

- Chạy tệp ``concordium-node-reset-data'' từ tệp đã giải nén trong kho lưu trữ.

   - Đối với người dùng *Mac*: đầu tiên bạn mở công cụ, nhấp chuột phải vào
      tập tin ``concordium-node-reset-data'' và chọn **Open**. Một thông điệp
      sẽ xuất hiện rằng phần mềm đến từ một nhà phát triển không xác định.
      Chọn lại **Open**.
   - Đối với người dùng *Windows*: đầu tiên bạn mở công cụ,
      bấm đúp vào tệp ``concordium-node-reset-data''. Một thông điệp
      sẽ xuất hiện rằng phần mềm đến từ một nhà phát triển không xác định.
      Chọn **More info** → **Run anyway**.

- Công cụ sẽ hỏi:

      *Do you also want to remove saved keys?*

   Các tài khoản đã được tạo cho các phiên bản trước không còn hợp lệ vào
   Mở Testnet 3. Do đó, nếu bạn đã lưu trữ các tài khoản từ trước
   phiên bản mà chúng tôi khuyên bạn nên nhập **y** sẽ xóa tất cả tài khoản và
   khóa.

.. _running-a-node:

Chạy một Node
==============

Để bắt đầu chạy một ứng dụng khách tham gia Open Testnet, hãy làm theo các bước sau:

1. Mở tệp``concordium-node'' từ kho lưu trữ đã giải nén.

- Đối với người dùng *Mac*: đầu tiên bạn mở công cụ, nhấp chuột phải vào
   ``concordium-node'' và chọn **Open**. Một thông báo sẽ xuất hiện
   rằng phần mềm đến từ một nhà phát triển không xác định. Chọn **Open**
   lần nữa.
- Đối với người dùng *Windows*: đầu tiên bạn mở công cụ, hãy nhấp đúp vào
  ``concordium-node '. Một thông báo sẽ xuất hiện rằng
   phần mềm của một nhà phát triển không xác định. Chọn **More info** →
   **Run anyway**.
- Khi *restarting* một Node
   Tùy chọn ``--no-block-state-import''. Điều này sẽ chỉ tải xuống
   cập nhật cho chuỗi khối Concordium xảy ra trong khi Node
   không hoạt động và có thể tăng tốc quá trình khởi động.

2. Nhập tên cho Node của bạn. Tên này sẽ được hiển thị công khai trên
   bảng điều khiển.

3. Nếu công cụ đã được khởi động trước đó, nó sẽ hỏi bạn có muốn
   xóa cơ sở dữ liệu Node cục bộ trước khi bắt đầu. Nhấn **y** sẽ
   xóa và sau đó tạo lại thông tin về trạng thái của
   Chuỗi khối Concordium đã được lưu trên máy tính của bạn. **Lưu ý rằng
   xóa cơ sở dữ liệu Node cục bộ có nghĩa là sẽ mất nhiều thời gian hơn cho
   để bắt kịp với mạng Concordium.**

Công cụ bây giờ sẽ tải xuống hình ảnh Máy khách Concordium và tải nó vào
Docker. Máy khách sẽ khởi chạy và bắt đầu xuất thông tin ghi nhật ký
về hoạt động của Node.

Nhìn thấy Node của bạn trên trang tổng quan
===========================================

Sau khi chạy ``concordium-node'', bạn có thể

- xem Node của bạn trên `Trang tổng quan mạng`_
- :ref:`query<testnet-query-node>`` thông tin về các khối, giao dịch và tài khoản

Bảng điều khiển mạng
--------------------

Sẽ mất một lúc để bắt kịp với trạng thái của
Chuỗi khối Concordium. Điều này liên quan đến tải xuống
thông tin về tất cả các khối trong chuỗi.

Trong số các thông tin khác, trên ``Trang tổng quan mạng`_, bạn có thể
biết được sẽ mất bao lâu để Node của bạn bắt kịp với
chuỗi. Vì vậy, bạn có thể so sánh giá trị **Length** của Node (số
chặn Node của bạn đã nhận) với giá trị **Chain Len** (số
khối trong chuỗi dài nhất trong mạng) được hiển thị tại
đầu bảng điều khiển.


Bật các kết nối đến
===================

Nếu bạn đang chạy Node của mình sau tường lửa hoặc sau nhà của bạn
bộ định tuyến, sau đó bạn có thể sẽ chỉ có thể kết nối với các Node khác,
nhưng các Node khác sẽ không thể bắt đầu kết nối đến Node của bạn.
Điều này hoàn toàn ổn và Node của bạn sẽ tham gia đầy đủ vào
Mạng Concordium. Nó sẽ có thể gửi các giao dịch và,
:ref:`if so configured<become-a-baker>`, để nướng và hoàn thiện.

Tuy nhiên, bạn cũng có thể biến Node của mình thành người tham gia mạng tốt hơn
bằng cách cho phép các kết nối đến. Theo mặc định, ``concordium-node'' sẽ lắng nghe
trên cổng ``8888'' cho các kết nối đến. Tùy thuộc vào mạng của bạn và
cấu hình nền tảng, bạn sẽ cần chuyển tiếp một cổng bên ngoài
đến ``8888'' trên bộ định tuyến của bạn, mở nó trong tường lửa của bạn hoặc cả hai. Các
chi tiết về cách thực hiện điều này sẽ phụ thuộc vào cấu hình của bạn.

Cấu hình các cổng
-----------------

Node lắng nghe trên bốn cổng, có thể được định cấu hình bằng cách cung cấp
lệnh thích hợp khi khởi động Node. Các cổng được sử dụng bởi Node như sau:

- 8888, cổng kết nối mạng ngang hàng, có thể được thiết lập với
   ``--listen-node-port''
- 8082, cổng được sử dụng bởi phần mềm trung gian, có thể được đặt bằng ``--listen-middleware-port''
- 10000, cổng gRPC, có thể được đặt bằng ``--listen-grpc-port''

Khi thay đổi ánh xạ phía trên vùng chứa docker phải
dừng Node (:ref:`stop-a-node`), đặt lại và bắt đầu lại. Để đặt lại vùng chứa, hãy sử dụng
``concordium-node-reset-data'' hoặc chạy ``docker rm concordium-client'' trong
thiết bị đầu cuối.

Chúng tôi *thực sự khuyên bạn* rằng tường lửa của bạn chỉ nên được cấu hình
cho phép kết nối công khai trên cổng 8888 (mạng ngang hàng). Ai đó có quyền truy cập vào các cổng khác có thể lấy
,kiểm soát Node của bạn hoặc các tài khoản bạn đã lưu trên Node.

.. _stop-a-node:

Dừng Node
=========

Để dừng Node, hãy nhấn **CTRL + c** và đợi Node hoàn thành
tắt.

Nếu bạn vô tình đóng cửa sổ mà không tắt rõ ràng
ứng dụng khách, nó sẽ tiếp tục chạy nền trong Docker. Trong đó
trường hợp, sử dụng ``concordium-node-stop'' theo cách giống như cách bạn đã mở
thực thi ``concordium-node''.

Hỗ trợ và phản hồi
==================

Thông tin ghi nhật ký cho Node của bạn có thể được truy xuất bằng cách sử dụng
Công cụ ``concordium-node-retrieve-logs``. Điều này sẽ lưu nhật ký từ
đang chạy vào một tệp. Ngoài ra, nếu được cho phép, nó sẽ
truy xuất thông tin về các chương trình hiện đang chạy trên hệ thống.

Bạn có thể gửi nhật ký, thông tin hệ thống, câu hỏi và phản hồi tới
testnet@concordium.com. Bạn cũng có thể liên hệ tại `Discord` của chúng tôi hoặc
kiểm tra :ref:`troubleshooting page<troubleshooting-and-known-issues>` của chúng tôi
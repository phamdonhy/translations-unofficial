.. Discord: https://discord.gg/xWmQ5tp

.. guide-tài khoản-giao dịch:

====================================================
ID Concordium: Bắt đầu với tài khoản và giao dịch
====================================================
.. contents::
   :local:
   :backlinks: none

Trước khi thực hiện theo hướng dẫn này, bạn nên hoàn tất việc yêu cầu tài khoản và danh tính ban đầu của mình, như được mô tả trong :ref:`the previous chapter<testnet-get-started>`.

Tạo tài khoản mới
====================
Trước khi tìm hiểu cách tạo tài khoản, số dư và giao dịch của chúng hoạt động, hãy tạo tài khoản thứ hai. Bắt đầu bằng cách vào
 trang *Accounts*. Ở góc trên bên phải, bạn sẽ thấy một **plus sign**. Nhấn vào đó để tiếp tục. Trên màn hình tiếp theo
bạn sẽ được yêu cầu đặt tên cho tài khoản mới của mình. Trong ví dụ này, chúng tôi sẽ chọn tên *Example Account 2*, nhưng bạn có thể
chọn bất kỳ tên nào bạn muốn.
.. image:: Concordium/translations-unofficial/source/testnet/guides/images/concordium-id/acc1.png
      :width: 32%
.. image:: images/concordium-id/acc2.png
      :width: 32%

Khi nhấn **Next**, bạn sẽ gặp một màn hình mà trên đó bạn phải quyết định sử dụng danh tính nào để mở tài khoản mới.
Cho đến nay bạn có thể chỉ có một, nhưng nếu bạn có nhiều hơn, bạn có thể chọn bất kỳ danh tính nào bạn muốn từ danh sách. Bởi
nhấp vào danh tính, bạn sẽ được đưa đến màn hình tiếp theo. Khi tạo tài khoản không phải tài khoản ban đầu, tức là tài khoản
không được tạo khi tạo danh tính, bạn có thể chọn hiển thị một số: ref: `glossary-thuộc tính`. Điều này là không cần thiết,
và nếu bạn không có lý do cụ thể để làm như vậy, chúng tôi khuyên bạn không nên tiết lộ bất kỳ thông tin nào, vì các thuộc tính được tiết lộ sẽ diễn ra theo chuỗi và không thể xóa.

.. image:: images/concordium-id/acc3.png
      :width: 32%
.. image:: images/concordium-id/acc4.png
      :width: 32%
Nếu bạn nhấn nút **Reveal account attributes button**, bạn sẽ được đưa đến trang sau. Bạn có thể đánh dấu
tắt các thuộc tính bạn muốn tiết lộ, sau đó nhấn **Submit account**. Nhấn **Submit account** hoặc cái trước
sẽ đưa bạn đến trang tạo tài khoản cuối cùng, trang này sẽ cung cấp cho bạn tổng quan ngắn và cho bạn biết rằng tài khoản
đã được nộp.

.. image:: images/concordium-id/acc5.png
      :width: 32%
.. image:: images/concordium-id/acc6.png
      :width: 32%

Bằng cách nhấn **Ok, thanks** trên tổng quan bài nộp, bạn sẽ được đưa trở lại trang tài khoản. Bạn có thể thấy rằng cái mới của bạn
tài khoản vẫn đang chờ xử lý, vì có thể mất vài phút để hoàn tất trên chuỗi. Nếu bạn chưa cố gắng làm như vậy, bạn có thể
thử nhấn vào mũi tên hướng xuống trên một trong các thẻ tài khoản để thấy rằng nó sẽ hiện thẻ ra. Điều này tiết lộ
hai phần thông tin mới, *at disposal* và *staked*. Trường xử lý sẽ cho bạn biết số dư tài khoản là bao nhiêu
hiện có sẵn để sử dụng tại thời điểm nhất định và số tiền đặt cược bạn có thể đọc thêm trên trang :ref:`managing accounts<managing_accounts>`

.. image:: images/concordium-id/acc7.png
      :width: 32%
.. image:: images/concordium-id/acc8.png
      :width: 32%



Thực hiện một giao dịch
====================
Tiếp theo, hãy thử nhấn vào vùng  **Balance** trong tài khoản mới tạo của bạn. Về điều này
bạn có thể thấy số dư hiện tại trong tài khoản của mình và tại thời điểm này, nó cũng sẽ cho phép bạn yêu cầu 100 GTU để sử dụng
Testnet. Yêu cầu 100 GTU là một tính năng của Testnet và đối với Testnet 4, nó thực sự sẽ chuyển 2000 GTU vào tài khoản,
mặc dù nút cho biết 100. Việc giảm GTU chỉ khả dụng trên tài khoản một lần. Bằng cách nhấn nó, bạn sẽ thấy một giao dịch
xuất hiện. Điều này sẽ chờ xử lý một chút và sau một thời gian, 2000 GTU sẽ được thêm vào tài khoản của bạn.

.. image:: images/concordium-id/acc9.png
      :width: 32%
.. image:: images/concordium-id/acc10.png
      :width: 32%


Bây giờ chúng tôi có một số GTU trong tài khoản của mình, hãy thử thực hiện một giao dịch. Nhấn nút **SEND** để làm điều đó. Trên trang tiếp theo
bạn có thể nhập số tiền bạn muốn chuyển và chọn người nhận. Trong ví dụ này, chúng tôi sẽ chuyển 10 GTU.

.. image:: images/concordium-id/acc11.png
      :width: 32%
.. image:: images/concordium-id/acc12.png
      :width: 32%


Sau khi quyết định số tiền, bây giờ chúng ta sẽ chọn người nhận. Để thực hiện việc này, hãy nhấn nút Chọn **Recipient or shield amount**.
Trên trang này, bạn có thể tìm kiếm người nhận trong *address book* của mình hoặc thêm người nhận bằng cách quét mã QR của tài khoản nhận.
Như bạn có thể thấy trong ảnh chụp màn hình, chúng tôi chỉ có một người nhận được lưu, *Example Account 1*. Trên đó, chúng tôi có tùy chọn **Shield an
amount*, nhưng chúng tôi sẽ quay lại số đó sau. Chúng tôi sẽ chọn *Example Account 1* làm người nhận của chúng tôi trong ví dụ này.

.. image:: images/concordium-id/acc13.png
      :width: 32%
.. image:: images/concordium-id/acc14.png
      :width: 32%

Với số tiền và người nhận đã chọn, chúng ta có thể nhấn **Send Funds** để tiếp tục. Bằng cách này, chúng tôi sẽ gặp một màn hình xác nhận trên
mà chúng tôi có thể xác minh số tiền, người nhận và tài khoản gửi. Bằng cách nhấn **Yes, send funds**, chúng tôi sẽ xác minh
chính mình bằng cách sử dụng mật mã
hoặc sinh trắc học, và sau đó giao dịch được gửi đến chuỗi. Có thể mất một chút thời gian để giao dịch hoàn tất.

.. image:: images/concordium-id/acc15.png
      :width: 32%
.. image:: images/concordium-id/acc16.png
      :width: 32%

Bây giờ chúng ta có thể thấy rằng nhật ký *Example Account 2* là *Transfers* cho thấy rằng số tiền đã được khấu trừ, cộng với *fee*. Tất cả các giao dịch sẽ
bị tính phí và tùy thuộc vào loại giao dịch mà phí có thể khác nhau. Nhấn giao dịch sẽ cho phép bạn xem thêm chi tiết.

.. image:: images/concordium-id/acc17.png
      :width: 32%
.. image:: images/concordium-id/acc18.png
      :width: 32%
.. _move-an-amount-to-the-Shielded-balance:

Chuyển một số tiền đến số dư được bảo vệ
========================================
Nếu chúng ta quay lại màn hình *Accounts*, bây giờ chúng ta có thể thấy rằng 10 GTU đã được chuyển vào *Balance* của *Example Account 1*. Như bạn có thể
đã nhận thấy trước đây, các tài khoản cũng có :ref:`glossary-shielded-balance`. Nói tóm lại, số dư được bảo vệ là để giữ số tiền được bảo vệ (mã hóa)
trên tài khoản. Hãy thử thêm một số GTU được bảo vệ vào *Example Account 2* của chúng tôi. Bắt đầu bằng cách nhấn vào vùng **Shielded Balance** của thẻ tài khoản.

.. image:: images/concordium-id/acc19.png
      :width: 32%
.. image:: images/concordium-id/acc20.png
      :width: 32%

Tiếp theo, nhấn nút **SEND** một lần nữa và nhập một lượng GTU vào *shield*, đây là hành động thêm một số GTU vào *Shielded Balance*.
Sau khi làm điều đó, hãy nhấn lại **Select Recipient or shield amount**. Thay vì chọn người nhận, lần này chúng ta sẽ nhấn **Shield amount**.

.. image:: images/concordium-id/acc21.png
      :width: 32%
.. image:: images/concordium-id/acc22.png
      :width: 32%

Bây giờ chúng tôi có thể tiếp tục và xác nhận giao dịch, giống như chúng tôi đã làm trước đây với chuyển khoản thông thường. Giao dịch có thể mất một chút thời gian
để hoàn thiện chuỗi.

.. image:: images/concordium-id/acc23.png
      :width: 32%
.. image:: images/concordium-id/acc24.png
      :width: 32%

Bằng cách quay lại trang *Accounts*, bây giờ có thể thấy rằng có 10 GTU trên *Shielded Balance* của *Example Account 2*. Nếu *Shielded
Balance* của thẻ account được nhấn, chúng ta có thể thấy rằng có một giao dịch *Shielded amount* trong nhật ký chuyển số dư được che chắn.
Thực hiện một giao dịch che chắn cũng sẽ mất một khoản phí, nhưng khoản phí này sẽ được trừ vào số dư thông thường của tài khoản. Thử
quay lại và xem nhật ký chuyển khoản của *Balance* thông thường.

.. image:: images/concordium-id/acc25.png
      :width: 32%
.. image:: images/concordium-id/acc26.png
      :width: 32%

Thực hiện chuyển tiền được bảo vệ
=================================
Có sẵn một số GTU được bảo vệ, bây giờ chúng ta có thể thử thực hiện *Shielded transfer*, có nghĩa là chúng ta có thể thực hiện chuyển với một
lượng GTU. Bước đầu tiên là duyệt đến trang *shielded balance* của tài khoản có chứa GTU được bảo vệ, nếu bạn chưa có
ở đó. Sau đó nhấn nút **SEND**. Bây giờ bạn sẽ có thể nhập số tiền và chọn người nhận. Trong ví dụ này, chúng tôi đã chọn
chuyển 2 GTU. Khi nhấn nút **Select Recipient or unshield amount**, bạn sẽ có thể chọn người nhận. Chúng tôi sẽ chọn
*Example Account 2* trong ví dụ này.

.. image:: images/concordium-id/acc27.png
      :width: 32%
.. image:: images/concordium-id/acc28.png
      :width: 32%

Với số lượng và người nhận tại chỗ, bây giờ bạn có thể tiếp tục. Cũng giống như các giao dịch khác, bây giờ bạn sẽ thấy màn hình xác nhận,
và bằng cách tiếp tục từ đó, bạn sẽ có thể xác minh bản thân bằng mật mã hoặc sinh trắc học, sau đó gửi giao dịch được bảo vệ
vào chuỗi. Một lần nữa, giao dịch có thể mất một chút thời gian để hoàn tất trên chuỗi.

.. image:: images/concordium-id/acc29.png
      :width: 32%
.. image:: images/concordium-id/acc30.png
      :width: 32%


Bây giờ, nếu bạn quay lại màn hình *Accounts*, bạn sẽ có thể thấy rằng một chiếc khiên nhỏ đã xuất hiện bên cạnh số tiền trên
*Shielded Balance* của tài khoản nhận. Điều này cho thấy rằng có những giao dịch được che chắn mới nhận được trên số dư được che chắn.
Hãy thử nhấn số dư được che chắn và lưu ý rằng bạn phải nhập mật mã hoặc sử dụng sinh trắc học của mình để nhập.
Điều này xảy ra bởi vì bạn cần giải mã các giao dịch được bảo vệ đã nhận, trước khi bạn có thể thấy số tiền.

.. image:: images/concordium-id/acc31.png
      :width: 32%
.. image:: images/concordium-id/acc32.png
      :width: 32%

Bỏ bảo vệ một số tiền
==================
Sau khi giải mã, số tiền hiện được hiển thị trong *shielded balance* và trên thẻ tài khoản trên màn hình *Accounts*. Bây giờ, nếu chúng ta
muốn chuyển một số GTU từ số dư bị che chắn sang số dư thông thường? Hãy cố gắng chuyển 2 GTU sang số dư thông thường thông qua hành động
*Unshielding* một số tiền. Để thực hiện việc này, hãy nhấn nút **SEND** trong số dư được che chắn. Nhập 2 làm số tiền, sau đó nhấn **Select Recipient
or unshield amount**. **Choose Unshield amount**.

.. image:: images/concordium-id/acc33.png
      :width: 32%
.. image:: images/concordium-id/acc34.png
      :width: 32%

Bây giờ hãy hoàn tất giao dịch giống như bạn đã làm với những giao dịch khác và thử duyệt đến số dư thông thường của tài khoản để xem số không bị che chắn.
Nếu giao dịch đã hoàn tất theo chuỗi, bây giờ bạn sẽ có thể thấy rằng *Unshielded amount* đã được đánh dấu vào số dư thông thường.
Lưu ý rằng nó không phải là 2 GTU, mặc dù số tiền bạn vừa không được bảo vệ là 2. Điều này là do phí thực hiện bất kỳ giao dịch nào, bao gồm
không được che chắn, sẽ bị trừ vào số dư thông thường của tài khoản chịu trách nhiệm cho giao dịch.

.. image:: images/concordium-id/acc35.png
      :width: 32%
.. image:: images/concordium-id/acc36.png
      :width: 32%

Chia sẻ địa chỉ tài khoản của bạn
==================================
Nếu bạn muốn chia sẻ địa chỉ tài khoản của mình, bạn có thể dễ dàng thực hiện điều này bằng cách nhấn nút **Address**. Điều này sẽ đưa bạn đến một trang
nơi bạn có nhiều tùy chọn chia sẻ địa chỉ tài khoản. Thử nhấn nút **Share** và chia sẻ địa chỉ của bạn với ai đó.

.. image:: images/concordium-id/acc37.png
      :width: 32%
.. image:: images/concordium-id/acc38.png
      :width: 32%

Kiểm tra lịch phát hành
========================
Trên blockchain Concordium, có thể thực hiện một giao dịch giải phóng số tiền đã chuyển theo thời gian. Đây được gọi là
*transfer with a schedule*. Hiện tại, chúng tôi sẽ không trình bày về cách thực hiện chuyển như vậy vì không thể thực hiện được từ ID Concordium,
nhưng hãy cùng tìm hiểu cách kiểm tra lịch phát hành. Nếu bạn nhận được chuyển khoản có lịch phát hành, bạn có thể nhấn
**menu burger** ở góc trên bên phải của màn hình cân. Điều này sẽ cho phép bạn nhấn **Release schedule** và bằng cách làm này, bạn
sẽ được đưa đến màn hình chứa thông tin về số lượng GTU sẽ được phát hành và khi nào. Nếu bạn muốn tìm hiểu thêm về cách
thực hiện chuyển khoản với lịch phát hành, bạn có thể xem các trang :ref:`concordium_client` and :ref:`transactions`.

.. image:: images/concordium-id/rel1.png
      :width: 32%
.. image:: images/concordium-id/rel2.png
      :width: 32%
.. image:: images/concordium-id/rel3.png
      :width: 32%

Hỗ trợ và phản hồi
==================

Nếu bạn gặp bất kỳ vấn đề nào hoặc có đề xuất, hãy đăng câu hỏi của bạn hoặc
phản hồi về `Discord` hoặc liên hệ với chúng tôi tại testnet@concordium.com.

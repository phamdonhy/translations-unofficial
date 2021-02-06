.. _Discord: https://discord.gg/xWmQ5tp

.. _testnet-get-started:

=======================================
ID Concordium: Bắt đầu với ứng dụng
=======================================

.. contents::
   :local:
   :backlinks: none

Trước khi thực hiện theo hướng dẫn này, bạn nên cài đặt xong ID Concordium, như được mô tả trong :ref:`the first chapter <testnet-get-the-app>'.

Thiết lập mật mã và sinh trắc học
================================

Khi bạn mở ứng dụng ID Concordium lần đầu tiên, bạn sẽ được thông báo cài đặt
điều đó sẽ giúp bạn thiết lập mật mã và xác thực sinh trắc học, :ref: `glossary-initial-account`,
và nó cũng sẽ hướng dẫn bạn cách lấy một :ref:`glossary-Identes`. Tài khoản ban đầu là một loại tài khoản đặc biệt,
được gửi đến chuỗi bởi :ref:`glossary-Ident-provider`, khi tạo ra một danh tính. Bạn có thể làm cho
các giao dịch từ một tài khoản ban đầu giống như từ các tài khoản thông thường, nhưng chủ sở hữu của tài khoản ban đầu sẽ
được biết bởi nhà cung cấp danh tính. Sau khi danh tính của bạn được tạo, bạn sẽ có thể gửi tài khoản cho chuỗi
chính bạn và những điều này sẽ không được nhà cung cấp danh tính biết. Bạn có thể tìm hiểu thêm về các tài khoản trên trang :ref:`Identities
and accounts<reference-id-accounts>`.

Màn hình đầu tiên bạn sẽ gặp khi mở ID Concordium là màn hình này. Nó sẽ chỉ giải thích rằng
bạn phải trải qua quá trình này để bắt đầu.

Nếu bạn đã sẵn sàng tiếp tục, bạn có thể nhấn **Yes, let’s go!** Màn hình tiếp theo sẽ yêu cầu bạn nhập
mật mã sáu chữ số. Nếu bạn muốn sử dụng mật khẩu đầy đủ bao gồm các chữ cái, bạn cũng có thể chọn làm như vậy tại đây.

.. image:: images/concordium-id/int1.png
      :width: 32%
.. image:: images/concordium-id/int2.png
      :width: 32%


Sau khi chọn mật mã hoặc mật khẩu đầy đủ, bạn sẽ có tùy chọn sử dụng mật mã sinh học nếu điện thoại của bạn
hỗ trợ nó, tức là nhận dạng khuôn mặt hoặc vân tay. Chúng tôi khuyên bạn nên sử dụng sinh trắc học nếu bạn có tùy chọn đó.

.. image:: images/concordium-id/int3.png
      :width: 32%
      :align: center
Yêu cầu tài khoản ban đầu và danh tính của bạn
===============================================

Tiếp theo, bạn sẽ có được lựa chọn giữa việc tạo tài khoản ban đầu và danh tính mới hoặc nhập một tập hợp đã có sẵn.
Giả sử đây là lần đầu tiên bạn sử dụng ID Concordium, bạn có thể chọn **I want to create my initial account** để tiếp tục.

.. image:: images/concordium-id/int4.png
      :width: 32%
      :align: center


Trên màn hình tiếp theo, bạn sẽ thấy mô tả về tài khoản ban đầu là gì và ba bước bạn phải hoàn thành để có được nó,
cùng với danh tính của bạn. Nói tóm lại, tài khoản ban đầu là tài khoản do nhà cung cấp danh tính của bạn gửi đến chuỗi
lựa chọn, có nghĩa là họ sẽ biết rằng bạn là chủ sở hữu của tài khoản. Sau đó, bạn sẽ có thể gửi tài khoản đến
của chính bạn, có nghĩa là chủ sở hữu của những tài khoản này sẽ chỉ có bạn biết.

.. image:: images/concordium-id/int5.png
      :width: 32%
      :align: center

Ba bước được đề cập ở trên là:

1. Đặt tên cho tài khoản ban đầu của bạn
2. Đặt tên cho danh tính của bạn
3. Yêu cầu tài khoản ban đầu và danh tính từ một :ref:`glossary-identity-provider` mà bạn chọn

Bạn sẽ gặp bước đầu tiên trên trang tiếp theo, bước này sẽ nhắc bạn nhập tên cho tài khoản ban đầu của mình. Nhấn tiếp tục
sẽ đưa bạn đến trang tiếp theo, trên đó bạn phải đặt tên cho danh tính của mình. Cả hai cái tên này sẽ chỉ một mình bạn biết,
vì vậy bạn có thể đặt tên cho chúng nhiều hơn hoặc ít hơn bất cứ điều gì bạn muốn (Có một số ràng buộc về những chữ cái và dấu hiệu bạn có thể sử dụng).

Trong ví dụ bên dưới, chúng tôi chọn gọi tài khoản ban đầu của chúng tôi là *Example Account 1* và danh tính của chúng tôi *Example Identity*. Như
đã đề cập, bạn có thể chọn bất kỳ tên nào bạn muốn.

.. image:: images/concordium-id/int6.png
      :width: 32%
.. image:: images/concordium-id/int7.png
      :width: 32%

Bằng cách nhấn **Continue to identity providers**, bạn sẽ được đưa đến một trang mà bạn phải chọn giữa *identity providers*.
Nhà cung cấp danh tính là một thực thể bên ngoài sẽ xác minh bạn là ai, trước khi trả lại một đối tượng nhận dạng để sử dụng trên chuỗi.
Hiện tại, bạn có thể chọn giữa:

* *Notabene Development* sẽ cung cấp cho bạn danh tính thử nghiệm mà không cần xác minh danh tính ngoài đời thực.
* *Notabene* qua đó danh tính thực của bạn sẽ được xác minh.

.. image:: images/concordium-id/int8.png
      :width: 32%
      :align: center

Bằng cách chọn Notebene Development, bạn sẽ được cung cấp danh tính thử nghiệm mà không cần thêm bất kỳ điều gì. Nếu bạn chọn Notabene, bạn sẽ được đưa
đối với quy trình phát hành danh tính bên ngoài của họ, quy trình này sẽ hướng dẫn bạn qua quy trình xác minh đối tượng nhận dạng.
Sau khi kết thúc quy trình này, bạn sẽ được đưa trở lại ID Concordium.

Sau khi kết thúc một trong hai quy trình cấp danh tính, bạn sẽ gặp màn hình sau. Nó sẽ cho bạn thấy một cái nhìn tổng quan
danh tính của bạn và tài khoản ban đầu.

.. image:: images/concordium-id/int9.png
      :width: 32%
      :align: center

Tùy thuộc vào nhà cung cấp danh tính bạn đã chọn, cách bố trí của thẻ nhận dạng có thể khác một chút. Bạn có thể thấy rằng
Example Account 1 được nắm giữ bởi danh tính Example Identity. Tài khoản được tạo trong quá trình này sẽ được đánh dấu *(Initial)*
trong ứng dụng, vì vậy bạn biết tài khoản nào là tài khoản ban đầu được nhà cung cấp danh tính gửi cho chuỗi.

Bằng cách nhấn **Finish**, bạn sẽ được đưa đến màn hình *Accounts screen*. Trên màn hình này, bạn sẽ có thể thấy tên ban đầu mới tạo của mình
. Nó có thể đang hiển thị *Pending icon*, có nghĩa là nhà cung cấp danh tính vẫn đang làm việc để gửi và tạo
tài khoản ban đầu và danh tính. Bạn cũng có thể điều hướng đến *Identities screen* bằng cách nhấp vào **Identities** ở cuối
màn hình. Trên màn hình này, bạn có thể thấy danh tính mới được tạo của mình, danh tính này cũng có thể vẫn đang chờ xử lý trong trường hợp nhà cung cấp danh tính
vẫn chưa hoàn thành nó. Tất cả những gì bạn phải làm bây giờ là đợi chúng hoàn thành.

.. image:: images/concordium-id/int10.png
      :width: 32%
.. image:: images/concordium-id/int11.png
      :width: 32%


Hỗ trợ và phản hồi
==================

Nếu bạn gặp bất kỳ vấn đề nào hoặc có đề xuất, hãy đăng câu hỏi của bạn hoặc
phản hồi về `Discord`_ hoặc liên hệ với chúng tôi tại testnet@concordium.com.
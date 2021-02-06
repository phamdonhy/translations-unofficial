.. networkDashboardLink: https://dashboard.testnet.concordium.com/
.. node-dashboard: http://localhost:8099
.. Discord: https://discord.com/invite/xWmQ5tp

.. become-a-baker:

==================================
Trở thành thợ làm bánh (tạo khối)
==================================
.. contents::
   :local:
   :backlinks: none

Phần này giải thích thợ làm bánh là gì, vai trò của nó trong mạng lưới và cách trở thành
một thợ làm bánh.

Bằng cách đọc phần này, bạn sẽ biết:

- Thợ làm bánh là gì và các khái niệm liên quan đến nó.
- Cách nâng cấp Node của bạn để trở thành thợ làm bánh.

Quá trình trở thành một thợ làm bánh có thể được tóm tắt trong các bước sau:

#. Nhận một tài khoản và một số GTU.
#. Nhận một bộ chìa khóa thợ làm bánh.
#. Đăng ký chìa khóa thợ làm bánh bằng tài khoản.
#. Bắt đầu Node với khoá thợ làm bánh.

Sau khi hoàn thành các bước này, Node thợ làm bánh sẽ nướng các khối. Nếu một khối nướng
được thêm vào chuỗi, thợ làm bánh của Node sẽ nhận được phần thưởng.

.. Ghi chú::

   Trong phần này, chúng tôi sẽ sử dụng tên ``bakerAccount'' làm tên của
   tài khoản sẽ được sử dụng để đăng ký và quản lý thợ làm bánh.

Định nghĩa
===========

Thợ làm bánh
-----

Một Node là *baker* (hoặc *is baking*) khi nó tích cực tham gia vào
mạng bằng cách tạo các khối mới được thêm vào chuỗi. Một thợ làm bánh thu thập,
đặt hàng và xác thực các giao dịch được bao gồm trong một khối để duy trì
tính toàn vẹn của blockchain. Người thợ làm bánh ký tên từng khối rằng họ nướng như vậy
rằng khối có thể được kiểm tra và thực thi bởi những người tham gia còn lại của
mạng lưới.

Chìa khóa thợ làm bánh
----------------------

Mỗi thợ làm bánh có một bộ khóa mật mã được gọi là *baker keys*. Node sử dụng
các phím này để ký các khối mà nó đặt. Để nướng các khối có chữ ký của
Node thợ làm bánh cụ thể phải chạy với tập hợp các khóa thợ làm bánh được tải.

Tài khoản thợ làm bánh
----------------------

Mỗi tài khoản có thể sử dụng một bộ khóa thợ làm bánh để đăng ký thợ làm bánh.

Bất cứ khi nào thợ làm bánh đưa ra một khối hợp lệ được đưa vào chuỗi, sau một số
thời gian phần thưởng được trả cho tài khoản được liên kết.

Cổ phần và xổ số
-----------------


.. todo::

   - Link to release schedule.

Tài khoản có thể đặt một phần số dư GTU của mình vào *baker stake* và có thể
sau đó giải phóng thủ công tất cả hoặc một phần số tiền đã đặt cọc. Số tiền đặt cược
không thể được di chuyển hoặc chuyển giao cho đến khi nó được phát hành bởi thợ làm bánh.

.. Ghi chú::

   Nếu tài khoản sở hữu số tiền đã được chuyển cùng với lịch phát hành,
   số tiền có thể được đặt cược ngay cả khi chưa được phát hành.

Để được chọn nướng khối, người thợ làm bánh phải tham gia
*xổ số* trong đó xác suất nhận được vé trúng thưởng là xấp xỉ
tỷ lệ với số tiền đặt cược.

Cùng một số tiền cược được sử dụng khi tính toán xem liệu một thợ làm bánh có được đưa vào quyết toán hay không
ủy ban hay không. Xem Finalization.

.. _epochs-and-slot:

Kỷ nguyên và thời điểm
----------------------

Trong chuỗi khối Concordium, thời gian được chia thành các *slots*. Slots có một thời gian
thời lượng cố định tại khối Genesis. Trên bất kỳ nhánh nhất định nào, mỗi vị trí có thể có
hầu hết một khối, nhưng nhiều khối trên các nhánh khác nhau có thể được tạo ra trong
cùng một khe.

.. todo::

   Let's add a picture.

Khi xem xét phần thưởng và các khái niệm khác liên quan đến nướng, chúng tôi sử dụng
khái niệm về *epoch* như một đơn vị thời gian xác định khoảng thời gian trong đó tập hợp
của những người làm bánh hiện tại và cổ phần đã được cố định. Các kỷ nguyên có khoảng thời gian cố định tại
Khối khởi đầu. Trong testnet, các kỷ nguyên có thời lượng **1 giờ**.

Bắt đầu nướng
=============

Quản lý tài khoản
-----------------

Phần này cung cấp một bản tóm tắt ngắn gọn về các bước liên quan để nhập
tài khoản. Để có mô tả đầy đủ, hãy xem :ref:`managing_accounts`.

Tài khoản được tạo bằng ứng dụng :ref:`concordium_id`. Khi một tài khoản đã được
đã tạo thành công, điều hướng đến tab **More** và chọn **Export**
cho phép bạn nhận tệp JSON chứa thông tin tài khoản.

Để nhập tài khoản vào chuỗi chạy

.. code-block:: console

   $concordium-client config account import <path/to/exported/file> --name bakerAccount

``concordium-client'' sẽ yêu cầu mật khẩu để giải mã tệp đã xuất và
nhập tất cả các tài khoản. Mật khẩu tương tự sẽ được sử dụng để mã hóa
khóa ký giao dịch và khóa chuyển được mã hóa.

Tạo chìa khóa cho thợ làm bánh và đăng ký
--------------------------------------------

.. Ghi chú::

   Đối với quy trình này, tài khoản cần sở hữu một số GTU, vì vậy hãy đảm bảo yêu cầu
   100 GTU cho tài khoản trong ứng dụng di động.

Mỗi tài khoản có một ID thợ làm bánh duy nhất được sử dụng khi đăng ký thợ làm bánh của mình. Điều này
ID phải do mạng cung cấp và hiện không thể tính trước. Điều này
ID phải được cung cấp bên trong tệp khóa bánh mì cho Node để nó có thể sử dụng
phím thợ làm bánh để tạo khối. ``Concordium-client'' sẽ tự động điền
trường này khi thực hiện các thao tác sau.

Để tạo một bộ khóa mới, hãy chạy:

.. code-block:: console

   $concordium-client baker generate-keys <keys-file>.json

nơi bạn có thể chọn một tên tùy ý cho tệp khóa. Đến
đăng ký khóa trong mạng mà bạn cần phải có :ref:`running a node <running-a-node>`
và gửi giao dịch ``baker add`` vào mạng:

.. code-block:: console

   $concordium-client baker add <keys-file>.json --sender bakerAccount --stake <amountToStake> --out <concordium-data-dir>/baker-credentials.json

thay thế

- ``<amountToStake>'' bằng số GTU cược ban đầu của thợ làm bánh
- ``<concordium-data-dir>'' bằng thư mục dữ liệu sau:

  * trên Linux và MacOS:``~/.local/share/concordium''
  * trên Windows: ``%LOCALAPPDATA%\\concordium''.

(Tên tệp đầu ra phải vẫn là ``baker-credentials.json'').

Sử dụng ``--no-restake'' để tránh tự động thêm
phần thưởng cho số tiền đặt cược cho thợ làm bánh. Hành vi này được mô tả trên
phần `Restaking the earnings`

Để bắt đầu Node với thợ làm bánh này và bắt đầu sản xuất các khối,
trước tiên bạn cần tắt Node đang chạy hiện tại (bằng cách nhấn
``Ctrl + C'' trên thiết bị đầu cuối nơi Node đang chạy hoặc sử dụng
 ``concordium-node-stop'').

Sau khi đặt tệp vào thư mục thích hợp (đã được thực hiện trong
lệnh trước khi chỉ định tệp đầu ra), bắt đầu lại Node bằng cách sử dụng
``concordium-node''. Node sẽ tự động bắt đầu nướng khi thợ làm bánh
được bao gồm trong các thợ làm bánh cho thời đại hiện tại.

Thay đổi này sẽ được thực hiện
ngay lập tức và sẽ có hiệu lực khi kết thúc kỷ nguyên sau kỷ nguyên trong đó
giao dịch để thêm thợ làm bánh đã được bao gồm trong một khối.

.. table :: Dòng thời gian: thêm thợ làm bánh

   + ---------------------------------------------------+--------------------------------------------+-----------------+
   | 							| Khi giao dịch được bao gồm trong một khối  | Sau 2 kỷ nguyên |
   + =============================================================== ==================================================+
   | Thay đổi có thể nhìn thấy bằng cách truy vấn Node  |     ✓	 				     |                 |
   + ---------------------------------------------------+--------------------------------------------+-----------------+
   | Baker được thêm trong hội đồng làm bánh   		|                                            | ✓ 	       |
   + ---------------------------------------------------+--------------------------------------------+-----------------+

.. Ghi chú::

   Nếu giao dịch thêm thợ làm bánh được bao gồm trong một khối trong kỷ nguyên `E`,
   thợ làm bánh sẽ được coi là một phần của ủy ban làm bánh khi kỷ nguyên
   `E + 2` bắt đầu.

Quản lý thợ làm bánh
====================

Kiểm tra trạng thái của thợ làm bánh và sức mạnh xổ số của nó
-------------------------------------------------------------

Để xem liệu Node có đang nướng hay không, bạn có thể kiểm tra các nguồn khác nhau
cung cấp các mức độ chính xác khác nhau trong thông tin được hiển thị.

- Trong `network dashboard <http://dashboard.testnet.concordium.com>`,
  Node sẽ hiển thị ID thợ làm bánh của nó trong cột ``Baker''.
- Sử dụng ``concordium-client'', bạn có thể kiểm tra danh sách các thợ làm bánh hiện tại
  và số tiền đặt cược tương đối mà họ nắm giữ, tức là sức mạnh xổ số của họ. Các
  sức mạnh xổ số sẽ xác định khả năng một người thợ làm bánh nhất định sẽ thắng
  và nướng một khối.

    .. code-block:: console

     $concordium-client consensus show-parameters --include-bakers
     Election nonce:      07fe0e6c73d1fff4ec8ea910ffd42eb58d5a8ecd58d9f871d8f7c71e60faf0b0
     Election difficulty: 4.0e-2
     Bakers:
                                  Account                       Lottery power
             ----------------------------------------------------------------
         ...
         34: 4p2n8QQn5akq3XqAAJt2a5CsnGhDvUon6HExd2szrfkZCTD4FX   <0.0001
         ...

- Sử dụng ``concordium-client'', bạn có thể kiểm tra xem tài khoản
  đã đăng ký một thợ làm bánh và số tiền hiện tại được đặt bởi thợ làm bánh đó.

   .. code-block:: console

     $./concordium-client account show bakerAccount
     ...

     Baker: #22
      - Staked amount: 10.000000 GTU
      - Restake earnings: yes
     ...

- Nếu số tiền đặt cược đủ lớn và có một Node đang chạy với thợ làm bánh
  các phím được tải, người thợ làm bánh đó cuối cùng sẽ tạo ra các khối và bạn có thể thấy
  trong ví điện thoại di động của bạn mà tài khoản nhận được phần thưởng nướng,
  như được thấy trong hình ảnh này:

.. image:: images/bab-reward.png
     :align: center
     :width: 250px

Cập nhật số tiền đặt cược
--------------------------

Để cập nhật hoạt động đặt cược làm bánh

.. code-block:: console

   $concordium-client baker update-stake --stake <newAmount> --sender bakerAccount

Việc sửa đổi số tiền đặt cược sẽ sửa đổi xác suất người làm bánh được bầu
để nướng các khối.

Khi một thợ làm bánh ** thêm tiền đặt cược lần đầu tiên hoặc tăng tiền đặt cược của họ **, điều đó
thay đổi được thực hiện trên chuỗi và hiển thị ngay sau khi giao dịch
được bao gồm trong một khối (có thể được nhìn thấy thông qua ``concordium-client account show
bakerAccount``) và có hiệu lực sau 2 kỷ nguyên.

.. table :: Timeline: tăng tiền đặt cược

   +---------------------------------------------------+-------------------------------------------+-----------------+
   |                                                   | Khi giao dịch được bao gồm trong một khối | Sau 2 kỷ nguyên |
   +===================================================+===========================================+=================+
   | Thay đổi có thể nhìn thấy bằng cách truy vấn Node | ✓                                         |                 |
   + --------------------------------------------------+-------------------------------------------+-----------------+
   | Baker sử dụng tiền cược mới                       |                                           | ✓               |
   +---------------------------------------------------+-------------------------------------------+-----------------+

Khi thợ làm bánh ** giảm số tiền đặt cược **, thay đổi sẽ cần * 2 +
bakerCooldownEpochs* kỷ nguyên để có hiệu lực. Sự thay đổi có thể nhìn thấy trên
chuỗi ngay sau khi giao dịch được bao gồm trong một khối, nó có thể được tham khảo thông qua
``concordium-client account show bakerAccount'':

.. code-block:: console

   $concordium-client account show bakerAccount
   ...

   Baker: #22
    - Staked amount: 50.000000 GTU to be updated to 20.000000 GTU at epoch 261  (2020-12-24 12:56:26 UTC)
    - Restake earnings: yes

   ...


.. table :: Timeline: giảm tiền đặt cọc

   +---------------------------------------------------+ -------- ---------------------------------+----------------- -----------------------+
   |                                                   | Khi giao dịch được bao gồm trong một khối | Sau * 2 + bakerCooldownEpochs * epochs  |
   +===================================================+===========================================+=========================================+
   | Thay đổi có thể nhìn thấy bằng cách truy vấn Node | ✓                                         |                                         |
   +---------------------------------------------------+-------------------------------------------+-----------------------------------------+
   | Baker sử dụng tiền cược mới                       |                                           | ✓                                       |
   +---------------------------------------------------+-------------------------------------------+-----------------------------------------+
   | Cổ phần có thể được giảm một lần nữa hoặc         | ✗                                         | ✓                                       |
   | thợ làm bánh có thể được gỡ bỏ                    |                                           |                                         |
   +---------------------------------------------------+-------------------------------------------+-----------------------------------------+

.. Ghi chú::

   Trong testnet, ban đầu `` bakerCooldownEpochs '' được đặt thành 168 epochs. Điều này
   có thể được kiểm tra như sau:

  .. code-block:: console

      $concordium-client raw GetBlockSummary
      ...
              "bakerCooldownEpochs": 168
      ...

.. cảnh báo::

   Như đã lưu ý trong phần `Định nghĩa`, số tiền đặt cược bị *khóa*,
   tức là nó không thể được chuyển nhượng hoặc sử dụng để thanh toán. Bạn nên lấy cái này
   tính đến và cân nhắc đặt một số tiền sẽ không cần thiết trong
   thời gian ngắn. Đặc biệt, để hủy đăng ký một thợ làm bánh hoặc sửa đổi cổ phần
   số tiền bạn cần để sở hữu một số GTU không đặt cọc để trang trải giao dịch
   chi phí.

Khôi phục thu nhập
----------------------

Khi tham gia làm thợ làm bánh trong mạng lưới và khối nướng, tài khoản
nhận phần thưởng trên mỗi khối nướng. Những phần thưởng này sẽ tự động được thêm vào
số tiền đặt cược theo mặc định.

Bạn có thể chọn sửa đổi hành vi này và thay vào đó nhận phần thưởng trong
số dư tài khoản mà không cần đặt cược tự động. Công tắc này có thể được
đã thay đổi thông qua ``concordium-client'':

.. code-block:: console

   $concordium-client baker update-restake False --sender bakerAccount
   $concordium-client baker update-restake True --sender bakerAccount

Các thay đổi sẽ có hiệu lực ngay lập tức sau khi khởi động lại; tuy nhiên, những thay đổi
bắt đầu ảnh hưởng đến việc nướng và hoàn thành công suất trong thời gian tiếp theo. Hiện tại
giá trị của chuyển đổi có thể được nhìn thấy trong thông tin tài khoản có thể được truy vấn
sử dụng ``concordium-client'':

.. code-block:: console

   $concordium-client account show bakerAccount
   ...

   Baker: #22
    - Staked amount: 50.000000 GTU
    - Restake earnings: yes

   ...

.. table :: Dòng thời gian: cập nhật lại

   + --------------------------------------------------+ - ---------------------------------------- + --------- ----------------------+
   |                                                   | Khi giao dịch được bao gồm trong một khối  | 2 kỷ nguyên sau khi được thưởng |
   + ==================================================+==============================================================================+
   | Thay đổi có thể nhìn thấy bằng cách truy vấn Node | ✓                                          |                                 |
   + --------------------------------------------------+--------------------------------------------+ --------- ----------------------+
   | Thu nhập sẽ [không] được tính lại tự động         | ✓                                          |                                 |
   + --------------------------------------------------+--------------------------------------------+ --------- ----------------------+
   | Nếu tự động khôi phục lại, thì                    |                                            | ✓                               |
   | tiền cược ảnh hưởng đến sức mạnh xổ số            |                                            |                                 |
   + --------------------------------------------------+--------------------------------------------+---------------------------------+

Khi người thợ làm bánh được đăng ký, nó sẽ tự động chia lại tiền thu nhập, nhưng như
đã đề cập ở trên, điều này có thể được thay đổi bằng cách cung cấp ``--no-restake'' cho
lệnh ``baker add'' như được hiển thị ở đây:

.. code-block:: console

   $concordium-client baker add baker-keys.json --sender bakerAccount --stake <amountToStake> --out baker-credentials.json --no-restake

Quyết toán
------------

Quyết toán là quá trình bỏ phiếu được thực hiện bởi các Node trong *uỷ ban hoàn thiện* mà *kết thúc* một khối khi có đủ số lượng thành viên của
ủy ban đã nhận được khối và đồng ý về kết quả của nó. Các khối mới hơn
phải có khối cuối cùng làm mốc để đảm bảo tính toàn vẹn của
chuỗi. Để biết thêm thông tin về quy trình này, hãy xem
:ref:`finalization<glossary-finalization>`.

Ủy ban hoàn thiện được thành lập bởi những người thợ làm bánh có cổ phần số tiền nhất định
. Điều này đặc biệt ngụ ý rằng để tham gia vào
ủy ban quyết toán, bạn có thể sẽ phải sửa đổi số tiền đặt cược
để đạt đến ngưỡng. Trong testnet, số tiền đặt cọc cần thiết để tham gia
trong ủy ban hoàn thiện là **0,1% tổng số GTU hiện có**.

Tham gia vào ủy ban hoàn thiện sẽ tạo ra phần thưởng cho mỗi khối
được hoàn thiện. Phần thưởng được trả vào tài khoản thợ làm bánh một thời gian sau
khối được hoàn thiện.

Loại bỏ thợ làm bánh
================

Tài khoản kiểm soát có thể chọn hủy đăng ký thợ làm bánh của mình trên chuỗi. Để huỷ thợ lamg bánh sử dụng `` concordium-client '':

.. code-block:: console

   $concordium-client baker remove --sender bakerAccount

Thao tác này sẽ xóa thợ làm bánh khỏi danh sách thợ làm bánh và mở khóa số tiền đặt cược trên
thợ làm bánh để nó có thể được chuyển nhượng hoặc di chuyển tự do.

Khi loại bỏ thợ làm bánh, sự thay đổi có cùng mốc thời gian là giảm
số tiền đặt cược. Thay đổi sẽ cần các kỷ nguyên *2 + bakerCooldownEpochs* để có hiệu lực.
Thay đổi sẽ hiển thị trên chuỗi ngay sau khi giao dịch được bao gồm trong một khối và bạn
có thể kiểm tra thời điểm thay đổi này có hiệu lực bằng cách truy vấn thông tin tài khoản
với ``concordium-client'' như thường lệ:

.. code-block:: console

   $concordium-client account show bakerAccount
   ...

   Baker #22 to be removed at epoch 275 (2020-12-24 13:56:26 UTC)
    - Staked amount: 20.000000 GTU
    - Restake earnings: yes

   ...

.. table :: Dòng thời gian: xóa thợ làm bánh

   +---------------------------------------------------+-------------------------------------------+----------------------------------------+
   |                                                   | Khi giao dịch được bao gồm trong một khối | Sau * 2 + bakerCooldownEpochs * epochs |
   +===================================================+===========================================+========================================+
   | Thay đổi có thể nhìn thấy bằng cách truy vấn Node | ✓                                         |                                        |
   +---------------------------------------------------+-------------------------------------------+----------------------------------------+
   | Baker bị loại khỏi hội đồng làm bánh              |                                           | ✓                                      |
   +---------------------------------------------------+-------------------------------------------+----------------------------------------+

.. cảnh báo::

   Không thể đồng thời giảm số tiền đặt cược và loại bỏ thợ làm bánh.
   Trong thời gian phục hồi được tạo ra bằng cách giảm số lượng tiền cược
   , thợ làm bánh không thể bị loại bỏ và ngược lại.

Hỗ trợ và phản hồi
==================

Nếu bạn gặp bất kỳ vấn đề nào hoặc có đề xuất, hãy đăng câu hỏi của bạn hoặc
phản hồi về `Discord` hoặc liên hệ với chúng tôi tại testnet@concordium.com.
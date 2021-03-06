# Cách sửa lỗi "No Internet access" nhưng vẫn vào được mạng bình thường.

Ở Windows 10 20H1 đang có lỗi rất khó chịu khiến ai cũng than phiền vì nó khiến 1 số ứng dụng mặc định của Windows cũng bị ảnh hưởng theo. Không chỉ thể, nhiều người cũng không thích nhìn "quả địa cầu" ở góc dưới. Sau đây là 1 số cách có thể khắc phục được lỗi phiền phức này.

# Cách 1: Set cứng 1 DNS nào đó:
Đây là 1 cách rất đơn giản, ai cũng có thể làm được. Các bạn có thể sử dụng DNS của Google hoặc CloudFlare,.... 

Link hướng dẫn chi tiết cho ai không biết làm: [Hướng dẫn set DNS](https://www.thegioididong.com/hoi-dap/huong-dan-doi-doi-dns-tren-may-tinh-1052424)

# Cách 2: Cập nhật bản vá KB4568831 (31/7):

Theo Changelogs của Microsoft thì bản vá này đã fix được khá nhiều lỗi, bao gồm cả lỗi mạng khiến các bạn khó chịu. Các bạn hãy truy cập link dưới để tải về bản vá nhé.

Link bản vá: [KB4568831](https://www.catalog.update.microsoft.com/Search.aspx?q=KB4568831)

# Cách 3: Sử dụng công cụ bên ngoài:

Trước hết các bạn tải file theo link ở dưới và chạy với quyền Administrator

Link Tool: [Download Now](https://github.com/crazy-max/WindowsSpyBlocker/releases/tag/4.31.1)

Sau khi chạy các bạn lựa chọn theo từng hướng dẫn dưới:
* Telemetry (gõ 1 -> Enter)
* NCSI (gõ 2 -> Enter)
* Apply Debian NCSI (gõ 2 -> Enter)

Khi chạy xong, các bạn chỉ cần ngắt kết nối với mạng và kết nối lại là được.

![Image](https://scontent.fhan2-1.fna.fbcdn.net/v/t1.0-0/p600x600/117351730_2704142953134068_3213013193545685726_o.jpg?_nc_cat=102&_nc_sid=07e735&_nc_ohc=mknwVtUkKOAAX8-Uisv&_nc_ht=scontent.fhan2-1.fna&_nc_tp=6&oh=91fb18fef5571653a3207a0600511552&oe=5F51F250)
# Cách 4: Sử dụng Registry:

Đây cũng là cách có thể nói khó hơn 2 cách trên nhưng nó cũng không đến nỗi mà không làm được.

Bước 1: Các bạn mở khung tìm kiếm của Windows, tìm "Regedit"

Bước 2: Vào đường dẫn "HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\NlaSvc\Parameters\Internet"

Bước 3: Tìm "EnableActiveProbing", nháy đúp và chỉnh từ "0" thành "1" và khởi động lại máy.

Hoặc dễ hơn, bạn có thể tải file và chạy: [File reg](https://www.upload.ee/files/12103363/Fix_No_Internet_Access.reg.html)

![Regedit](https://i.imgur.com/GU6V8fZ.jpg)

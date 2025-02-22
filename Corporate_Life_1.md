<h1>Corporate Life 1</h1>

![image](https://github.com/user-attachments/assets/d8178dad-94ee-4d67-8ac2-6f9ae1aa213b)

Giao diện web chỉ có thế này 

![image](https://github.com/user-attachments/assets/d2b2d07a-363e-4958-91ae-4f9cf15808bc)

Tôi đã FUZZ qua thử nhưng không thấy gì cả, có cả api/list nhưng cũng chỉ là thông tin rõ hơn thôi 

![image](https://github.com/user-attachments/assets/7c407c97-bfc1-4c5a-b486-6f055fe5cb27)

Sau 1 lúc đi lanh quanh thì thấy cái `_buildManifest.js` và đọc trong đó có 3 cái dir lần lượt là /, /_error và /v2-testing

![image](https://github.com/user-attachments/assets/a513c61a-6e03-4916-a7c4-c75701f9c6d0)

Trong đó thì /_error chỉ là giao diện 404 chứ chả có gì, để ý đến cái /v2-testing

![image](https://github.com/user-attachments/assets/783fe3ed-3558-4e5c-a6ea-80a18fa8fbdb)

Giao diện nó như này, có vẻ là có chứa lỗi sqli, để ý sang các request ở burp

![image](https://github.com/user-attachments/assets/737699f9-2547-4f13-bc51-9428ec6ba779)

![image](https://github.com/user-attachments/assets/fc2c1f18-acb6-410a-adab-92a3f64e5148)

Trong đây gồm có 2 cái là cái name tức là ô search và cái filter tức là cái chọn thể loại, sau 1 lúc khai thác thì cái filter dính sqli. Thử cái payload `{"filter":"HR' UNION SELECT 6,5,4,3,2,1 -- -"}` là thấy được sqli rõ 

![image](https://github.com/user-attachments/assets/cdd7de2a-c5bb-4dce-b08d-288b2c0db7f1)

Nó gồm có 6 cột như ở bên response đã hiện. Sau khi xài tool để khai thác thì được 2 cái bảng là flags và requests, bảng requests thì có flag 

![image](https://github.com/user-attachments/assets/4bbdbf62-c4cb-4ebc-aa26-b78e820ee02a)

Còn bảng flags chả có gì, nó có chữ "nothing here for now"

![image](https://github.com/user-attachments/assets/d3a0aa2c-244a-4b50-abec-8a781aa4d506)


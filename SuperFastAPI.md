![image](https://github.com/user-attachments/assets/8e01f01e-2e9f-4aaa-805a-f743b270b36a)

Giao diện chỉ có thế này

![image](https://github.com/user-attachments/assets/df63e93e-097b-4840-b4f8-a5bb7b750609)

Tôi dùng `ffuf -u http://kashictf.iitbhucybersec.in:13345/FUZZ -w Filenames_or_Directories_All.txt` để FUZZ các dir có trong web này:

![image](https://github.com/user-attachments/assets/67e26416-c20e-4506-95b2-92dd411c8e8f)

Và tìm được đường dẫn là docs, đây là giao diện của nó:

![image](https://github.com/user-attachments/assets/79dda169-4bb6-4717-afa8-82957fb4c50f)

Ở chỗ lấy flag thì cần nhập tên username để lấy flag

![image](https://github.com/user-attachments/assets/53631dc0-963c-4d6f-b16c-a2fe9f999960)

Tôi vào phần create user và tạo username namdo, vào lại phần flag thì yêu cầu phải là admin 

![image](https://github.com/user-attachments/assets/1987e9cf-498b-453d-a3b1-6d2139bd855d)

Tôi sang phần update và thử thêm role admin vào:

![image](https://github.com/user-attachments/assets/fddf2b15-598f-4fd1-b9ec-c4c97e1f9e93)

Quay lại phần flag để chạy

![image](https://github.com/user-attachments/assets/bcc1dc44-2dff-44f9-a127-e2f123e26f74)


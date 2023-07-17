# Ansible
## I. Khái niệm
Ansible là một trong những công cụ quản lý cấu hình hiện đại, nó tạo điều kiện thuận lợi cho công việc cài đặt, quản lý và bảo trì các server từ xa, với thiết kế tối giản giúp người dùng cài đặt và chạy nhanh chóng.Người dùng viết các tập lệnh cấp phép Ansible trong YAML, một tiêu chuẩn tuần tự hóa dữ liệu thân thiện với người dùng, chúng không bị ràng buộc với bất kỳ ngôn ngữ lập trình nào. Chính vì vậy người dùng có thể tạo ra các tập lệnh cấp phép phức tạp một cách trực quan hơn so với các công cụ còn lại trong cùng danh mục.
## II. Ưu điểm của ansible
- Dễ sử dụng và đọc: Ansible sử dụng ngôn ngữ YAML cho việc định nghĩa cấu hình, làm cho các tệp playbook dễ đọc và hiểu. Cú pháp đơn giản và rõ ràng giúp người dùng nhanh chóng tạo và thao tác với các playbook.
- Khả năng mở rộng và linh hoạt: Ansible hỗ trợ nhiều nền tảng và hệ điều hành khác nhau, cho phép quản lý cấu hình trên nhiều môi trường và hệ thống. Nó cũng có thể kết hợp với các công cụ và công nghệ khác trong môi trường DevOps.
- Tự động hóa hoàn toàn: Ansible cho phép tự động hóa toàn bộ quy trình triển khai và quản lý cấu hình. Điều này giúp giảm thiểu sai sót do sự can thiệp của con người và tăng tính nhất quán và đáng tin cậy trong việc triển khai.
- Không yêu cầu agent: Ansible không đòi hỏi cài đặt các agent hoặc phần mềm đặc biệt trên các máy chủ mục tiêu. Nó sử dụng các giao thức mạng tiêu chuẩn như SSH và WinRM để tương tác từ xa, giảm bớt công việc cấu hình và duy trì.
- Quản lý tập trung: Ansible cho phép quản lý tập trung, giúp điều khiển và theo dõi tất cả các hệ thống và ứng dụng từ một vị trí duy nhất. Người dùng có thể quản lý hàng trăm hoặc thậm chí hàng ngàn máy chủ từ một điểm duy nhất.
- Thời gian triển khai nhanh: Ansible cho phép triển khai nhanh chóng và dễ dàng. Việc sử dụng các playbook có sẵn và các modules có thể tùy chỉnh giúp giảm thời gian triển khai và đồng thời tăng tính nhất quán giữa các môi trường triển khai.
- Cộng đồng lớn: Ansible có một cộng đồng người dùng rộng lớn và phát triển mạnh mẽ. Người dùng có thể tìm thấy nhiều tài liệu, ví dụ và hỗ trợ từ cộng đồng này, giúp giải quyết các vấn đề và mở rộng khả năng sử dụng của Ansible.
## III. Nhược điểm của ansible
- Không thích hợp cho môi trường phức tạp: Ansible thường phù hợp cho các môi trường quản lý cấu hình đơn giản và trung bình. Tuy nhiên, với các môi trường phức tạp hoặc có số lượng lớn máy chủ, Ansible có thể gặp khó khăn trong việc xử lý và quản lý một lượng lớn các tác vụ và mô-đun.
- Tốc độ thực thi: So với các công cụ khác như Chef hoặc Puppet, Ansible có thể chậm hơn trong việc thực thi các tác vụ, đặc biệt khi xử lý một lượng lớn máy chủ. Điều này có thể gây ra một số trễ trong quá trình triển khai và cấu hình.
- Khả năng xử lý lỗi: Trong một số trường hợp, việc xử lý lỗi và gỡ lỗi trong Ansible có thể khá khó khăn. Khi xảy ra lỗi trong quá trình triển khai, thông báo lỗi có thể không rõ ràng và khó hiểu, làm cho việc tìm hiểu và sửa lỗi trở nên khó khăn.
- Yêu cầu kiến thức YAML: Ansible sử dụng ngôn ngữ YAML để định nghĩa các playbook và tệp cấu hình. Điều này yêu cầu người sử dụng có kiến thức cơ bản về YAML để hiểu và viết các tệp cấu hình. Đối với những người mới bắt đầu, việc học và làm quen với YAML có thể gây khó khăn ban đầu.
- Giới hạn về việc quản lý dữ liệu: Ansible tập trung chủ yếu vào việc quản lý cấu hình và triển khai. Tuy nhiên, nó có hạn chế trong việc quản lý dữ liệu, đặc biệt là quản lý dữ liệu có tính chất thay đổi thường xuyên hoặc dữ liệu phức tạp.
## IV. Một số thuật ngữ cơ bản khi sử dụng Ansible
- Playbook: Playbook là tệp cấu hình chứa các tác vụ (tasks) và các chỉ thị (directives) để Ansible thực hiện. Nó được viết bằng ngôn ngữ YAML và mô tả các bước để đạt được trạng thái mong muốn trên các máy chủ mục tiêu.
- Task: Task là một tác vụ cụ thể mà Ansible thực hiện trong một playbook. Nó mô tả công việc cần thực hiện, bao gồm mô-đun (module) và các tham số liên quan.
- Module: Module là một phần của Ansible và cung cấp các chức năng cụ thể. Ansible đi kèm với một số module được tích hợp sẵn, nhưng bạn cũng có thể viết các module tùy chỉnh. Mỗi module có nhiệm vụ thực hiện một tác vụ cụ thể trên máy chủ mục tiêu, chẳng hạn như quản lý gói phần mềm, tạo người dùng, hoặc cài đặt ứng dụng.
- Inventory: Inventory là một danh sách các máy chủ mà Ansible sẽ tương tác và thực hiện các tác vụ trên đó. Đây có thể là một tệp cấu hình YAML hoặc có thể được định nghĩa bằng cách sử dụng các nguồn dữ liệu động như cơ sở dữ liệu hoặc các dịch vụ khác.
- Play: Play là một phần của playbook và đại diện cho một nhóm các tác vụ liên quan. Mỗi play có thể ánh xạ vào một nhóm máy chủ cụ thể từ inventory và thực hiện các tác vụ trong đó.
- Role: Role là một cách tổ chức và tái sử dụng code trong Ansible. Nó chứa một tập hợp các playbook, các biến, mô-đun và các tệp cấu hình khác liên quan. Role giúp tổ chức playbook một cách logic và cho phép tái sử dụng trong các tác vụ khác nhau.
- Variable: Variable là các giá trị có thể thay đổi trong Ansible. Các biến có thể được sử dụng để định nghĩa thông tin động như tên máy chủ, cổng kết nối, đường dẫn file, và các giá trị khác. Các biến có thể được định nghĩa trong playbook, role, hoặc inventory.
- Handler: Handler là một tác vụ được thực hiện dựa trên sự thay đổi trạng thái của máy chủ mục tiêu. Nó được sử dụng để thực hiện các hành động cần thiết sau khi tác vụ chính hoàn thành, chẳng hạn như khởi động lại dịch vụ hoặc tái khởi động máy chủ.
## V. Cài đặt
### 1. Cài đặt Ansible:
B1: Đưa PPA (kho lưu trữ gói cá nhân) của dự án chính thức vào danh sách nguồn của hệ thống:
```
sudo apt-add-repository ppa:ansible/ansible
```
Sau đó cập nhật gói hệ thống:
```
sudo apt update
```
B2: Sau khi cập nhật hệ thống xong thì cài ansible:
```
sudo apt install ansible
```
Vậy là xong bước cài Ansible

Sau khi cài đặt Ansible thì chúng ta nên thiết lập khóa SSH:
### 1. Thiết lập khóa SSH
B1: Tạo một cặp khóa:
```
ssh-keygen
```
Sau khi màn hình hiển thị ra các lệnh thì ấn nút Enter để lưu cặp khóa vào .ssh/thư mục con trong thư mục chính của mình hoặc chỉ định một đường dẫn thay thế.
Sau khi hoàn thành thì màn hình hiển thị như dưới là thành công:
```
Output
Your identification has been saved in /your_home/.ssh/id_rsa
Your public key has been saved in /your_home/.ssh/id_rsa.pub
The key fingerprint is:
SHA256:/hk7MJ5n5aiqdfTVUZr+2Qt+qCiS7BIm5Iv0dxrc3ks user@host
The key's randomart image is:
+---[RSA 3072]----+
|                .|
|               + |
|              +  |
| .           o . |
|o       S   . o  |
| + o. .oo. ..  .o|
|o = oooooEo+ ...o|
|.. o *o+=.*+o....|
|    =+=ooB=o.... |
+----[SHA256]-----+
```
B2:  Sao chép khóa công khai vào máy chủ Ubuntu

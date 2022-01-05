# NoteBasicLanguage2:
## Generic:
### Java:
-  Generic là cách để xác định kiểu dữ liệu cho phương thức hoặc biến trong 1 ngữ cảnh cụ thể.
-  Việc đặt tên quy ước là rất quan trọng,cụ thể ta đặt các tên sau: T :loại dữ liệu.E:thành phần,K :key ,V là value. N:là number.
#### Các kí hiệu đại diện trong java: 
-    "<?>  được dùng để xác định đưa vào có thể khác kiểu dữ liệu chung chung được định nghĩa."
-    "<?extends type> kiểu dữ liệu được đưa vào phải là đối tượng của lớp con."
-    "<?super type> chấp nhận kiểu dữ liệu được đưa vào phải là đối tượng cha của lớp thành phần."
#### 3 ưu điểm chính trong generic kotlin: 
- Kiểu đối tượng an toàn:
- Ko cần phải ép kiểu.
- Kiểm tra ngay lúc biên dịch.
#### Kotlin:
- Nó không có các kí hiệu đại diên wildcard mà thay vào đó nó cần declaration-site variance và thứ 2 là type projections.
##### Variance:
- Để khai báo thì ta cần dùng từ khóa in và out để giới hạn kiểu.
- Nếu chúng ta sử dụng với chú thích là out trong trong kiểu dữ liệu chung chung.Thì theo như cách gọi nó gọi là 1 convariant đối kiểu dữ liệu chung chung đó.Tức là 1 lớp hoặc 1 interface mà có cái chú thích đó nên sản xuất(producer) ra các kiểu dữ liệu chung chung.Nếu để ý rằng mọi lớp ,interface trong kotlin chỉ có out thì chắc chắn trong những cái hàm mà nó định nghĩa luôn.
luôn là những hàm trả về kiểu dữ liệu chung chung đó.///dạ còn tiếp ,tiếp tục tìm hiểu.
- Nếu chúng ta sử dụng với chú thích là in trong kiêu dữ liệu chung chung.Thì theo như cách gọi nó gọi là là 1 contravariant đối với kiểu dữ liệu  chung chung đó.Tức là 1 lớp hoăc 1 interface mà có cái chú thích đó nó nên tiêu thu(consumer).Và nếu để ý rằng thì mọi lớp,hay interface in kotlin mà có chú thích là in thì khi đó những cái hàm trong đó luôn sử dụng cái kiểu dữ liệu chung chung đó./// dạ còn tiếp ,tiếp tục tìm hiểu.
##### Type projection:

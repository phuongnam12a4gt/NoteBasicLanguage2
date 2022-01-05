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
- Nếu chúng ta sử dụng với chú thích là out trong trong kiểu dữ liệu chung chung.Thì theo như cách gọi nó gọi là 1 convariant đối kiểu dữ liệu chung chung đó.Tức là 1 lớp hoặc 1 interface mà có cái chú thích đó nên sản xuất ra các kiểu dữ liệu chung chung.
- 'Ví dụ:interface Source<out T> {
    fun nextT():T
}'

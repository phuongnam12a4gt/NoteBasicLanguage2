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
#### Collection in Kotlin:
- Có 1 cặp interface đại diện cho loại collection:1 loại chỉ để đọc ,còn 1 loại được mở rộng từ 1 loại tương ứng chỉ đọc đó và có thêm 1 số :thêm thành phần ,cập nhật thành phần và xóa thành phần.
- Loại chỉ đọc đó là convariant tất cả trong cái lớp của nó có  định danh cho kiểu dữ liệu chung chung với từ khóa là out.
##### Chúng ta cần quan tâm cái gì trong collection?:
- thì theo em ta cần quan tâm tới 3 thứ :List,Set,Map và trước khi tìm hiểu 3 thứ đó ta cần tìm hiểu về về thằng interface Collection<T> cái thằng này chính là interface mà thằng set và thằng list có kế thừa.
- Interface Collection<T> là :Nó sẽ làm gì nó sẽ truy vấn kích cỡ ,nó kiểm tra kích cở của collection này,......
- Interface Interable:Thằng này là thằng Collection nó sẽ triển khai và nó sẽ trả về 1 hàm cái hàm đó sẽ trả về 1  interface interator ,interface là convariant.Và cái thằng interator đó được trả ra để duyệt thành phần của chuổi collection được đẩy vào.Và thằng interator nó sẽ có 2 hàm ,1 hàm tên là next ,hàm này được dùng để trả về thành phần đó 
và 1 hàm tên hashNext để kiểm ra.
#### Dừng lại tại đây quay lại những bộ collection cơ bản:
##### List vs MutableList:
Để khởi tạo 1 list ta có thể dùng hàm listOf .Hàm listOf là gì thì có mấy cái code phía trong em chưa hiểu rõ ,nhưng cứ tạm hiểu tới đây là nó tạo ra List.Vậy chúng ta sẽ nhìn vào interface List thì ta thấy rằng nó hàm get để lấy thành phần tại vị trí chỉ định này.Rồi hắn có nói rằng đây là 1 bộ thành phần các chỉ mục có thứ tự.Và tóm lại nói nó chỉ đọc.Nó sẽ đi kèm với nữa là MutableList để giải quyết vấn đề chỉ đọc đó .Vậy MutableList là interface nó sẽ triển khai của thằng List thì nó còn triển khai cùa thằng MutableCollection.Mà ta biết rằng thằng MutableCollection nó triển khai từ thằng collection để giải quyết vấn đề chỉ đọc.Cụ thể trong thằng MutableCollection sẽ có thêm hàm add ,remove các thành phần.Quay lại với thằng MutableList thì chắc nó sẽ có thằng add vs thằng remove.Củng như add và remove tại các vị trí chỉ định.Nó củng là bộ sưu tập có chỉ mục
và được add ,và hổ trợ thêm các thành phần .Vì ta thấy rằng trong mọi kiểu dữ liệu chung chung mà nó có thì để tên làm kiểu dữ liệu chung chung.Vậy thằng MutableCollection là invariant.MutableList củng là invariant.
##### Set:

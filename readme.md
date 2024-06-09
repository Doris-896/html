<!-- 1. Các bước khởi tạo dự án -->
    file index.html cấu hình trang chủ
    Cấu trúc file	
        <!DOCTYPE html>                                
        <html>                                                         
            <head>    <meta charset="utf--8">    </head>            //hỗ trợ web viết tiếng việt
            <body>    Nội dung    </body>
        </html>

<!-- 2. Các thẻ html thường dùng -->
    <h1>-<h6>, <p>, <ul> - <li>, <button>, <div>
    <img src='adress' alt='chữ hiển thị nếu bị lỗi'>
    <a href='link'>Quote hiển thị<a>
    <input type=‘text/ checkbox/ radio>

    <table>  
    <thead>    <th>    </thead>
    <tbody>    <td>    </tbody>
    </table>

<!-- 3. Cách dùng CSS trong HTML -->
    Internal: viết cùng trong file code
    External: viết file code khác
    Inline: viết trong thẻ html
    
    Thứ tự ưu tiên: inline > id > class > tag
    Nếu có !important ở cuối thuộc tính thì đặc biệt ưu tiên 

<!-- 4. CSS units -->
    Absolute units: px
    Relative units: %, rem,em, vw-width, vw-height

<!-- 5. Thuộc tính -->
    box-sizing          content-box             padding-box             border-box  
    border              border-width		    border-style	        border-color		
    padding             margin                  contain                 cover        
    background-color    background-clip         background-position     
    background-image    background-origin       background-size 

<!-- 6. CSS function -->
    var()         calc()                    attr()
    rgba()        rgb(): màu cứng đơ        linear-gradient()  

<!-- 7. CSS pseudo-classes (lớp giả) -->
    pseudo-classes (lớp giả)
        :root		lớp giả tham chiếu tới cắp thẻ <html>
        :hover		các thuộc tính chỉ được thay đổi như thế khi hover chuột vào 
        :active		các thuộc tính chỉ được thay đổi như thế khi bấm chuột vào kích hoạt
        :first-child	VD như <ul> <li> thì lấy ra <li> đầu tiên
        :last-child	VD như <ul> <li> thì lấy ra <li> cuối cùng 

    pseudo-elements (phần tử giả)
        (*) Trong đó luôn có content: ‘….’
        Mỗi element chỉ tồn tại được 1 before, 1 after là max

        ::before
        ::after
        ::first-letter	kí tự đầu tiên
        ::first-line	dòng đầu tiên (cho những đoạn văn bản (h) nhiều dòng)
        ::selection	các thuộc tính thay đổi như thế khi phần nội dung được bôi đen
<!-- 8. Position -->
    Relative	Tương đối: (không phụ thuộc vào đối tượng khác, lấy vị trí đứng ban đầu là gốc tọa độ)
    Absolute	Phụ thuộc thẻ cha gần nhất có ttính position (áp dụng: bấm vào icon show thông báo)
    Fixed		Ứng dụng tạo thanh heading đầu web không thay đổi
    Sticky		Không dùng (không được hỗ trợ)%

<!-- 9. Flexbox -->
    display: flex | inline-flex
    flex-direction: row | column
    flex-wrap: nowrap | wrap | wrap-reverse (xuống dòng/ lên dòng trên)
    flex-basis: <length> (set kích thước cho main size)

    justify-content: flex-start | flex-end | center | space-between | space-around 
    Dành cho cha (in case đó thì tất cả con được mặc định là justify-self, k cần set nữa)
    justify-self: flex-start | flex-end | center

    align-content: flex-start | flex-end | center
    align-self: flex-start | flex-end | center
    
    flex-grow: <number>: thay đổi kích thước của main size (flex item)
    flex-shrink: <number>: co kích thước của main size lại

    flex-flow: = flex-wrap, flex-direction
    flex: <number> = 1 thì sẽ chiếm hết chiều rộng của hàng đó
    order : <number>: quyết định hiển thị thằng nào trước, thằng nào sau

10. BEM
Block element modifier: Tiêu chuẩn đặt tên class trong CSS
Ứng dụng
Xây dựng layout website, thành phần trên website
Dự án nhiều member/ nhiều page/ nhiều thành phần giao diện
Ưu điểm: rõ ràng, tính module, không lo CSS class này ảnh hưởng CSS class khác
Nhược điểm: tên class dài
Cú pháp
.block
.block__element
.block–modifier
.block__element–modifier

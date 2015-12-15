# Tuyển tập các câu hỏi phỏng vấn vị trí Front-end

Mục đích của trang là tổng hợp lại danh sách các câu hỏi tham khảo phỏng vấn cho vị trí lập trình viên Front-end. 

Với mong muốn mọi người cùng giúp nhau chuẩn bị tốt hơn cho cuộc phỏng vấn sắp tới của mình, đồng thời
giúp ôn lại các kỹ năng của một lập trình viên Frontend. 

Mình tha thiết mong muốn mọi người cùng đóng góp nội dung, [tại đây](#contributors).

# Table of Contents

1. [Hỏi chung](#hỏi-chung)
2. [Hỏi về HTML](#hỏi-về-html)
3. [Hỏi về CSS](#hỏi-về-css)
4. [Hỏi về Javascript](#hỏi-về-javascript)
5. [Hỏi về Testing](#hỏi-về-testing)
6. [Hỏi về Performance](#hỏi-về-performance)
7. [Hỏi về Network](#hỏi-về-network)
8. [Hỏi về Coding](#hỏi-về-coding)
9. [Hỏi chơi cho vui](#hỏi-chơi-cho-vui)

# Getting Involved

1. [Contributors](#contributors)
2. [How to Contribute](#how-to-contribute)
3. [License](https://github.com/duyetdev/phong-van-frontend-toan-tap/blob/master/LICENSE)

------------------------------------------

## Hỏi chung

* Những điểm nào mà bạn thích, hoặc không thích về lập trình?
* Khác nhau giữa UI và UX?
* Nói về môi trường làm việc mà bạn mong muốn?
* Ba cách để giảm dung lượng tải trang?
* CORS?

## Hỏi về HTML

* Tác dụng của `doctype`?
* Khác nhau giữa HTML và XHTML là gì?
* Có vấn đề gì không nếu lưu trang MIME dạng `application/xhtml+xml`?
* Điều gì mà bạn cần phải chú ý nếu xây dựng và phát triển các trang web đa ngôn ngữ?
* Thuộc tính `data-` dùng để làm gì?
* Nếu HTML5 là nguồn mở, thẻ HTML nào mà bạn sẽ phát triển thêm?
* Khác nhau giữa `cookie`, `sessionStorage` và `localStorage`.
* Khác nhau giữa `<script>`, `<script async>` và `<script defer>`.
* Tại sao nên đặt `<link>` trong thẻ `<head></head>` và đặt `<script>` sau thẻ `</body>`. Ngoại lệ khi nào?

## Hỏi về CSS
*(Coming soon)*

## Hỏi về Javascript

* Ý nghĩa của biến `this`.
* Sử dụng **AMD** và **CommonJS** có tốt hay không? Tại sao tốt hoặc không tốt?
* Nếu viết theo kiểu IIFE, tại sao đoạn mã sau bị lỗi? `function foo(){ }();`
  * Sửa lại
* Khác nhau giữa `null`, `undefined` hoặc chưa khai báo?
  * Cách kiểm tra từng trường hợp trên.
* Khác nhau giữa **host objects** và **native objects** là gì?

## Hỏi về Testing 

* Có nên sử dụng các công cụ Lint Style hay không? Tại sao?

## Hỏi về Performance

* Bạn hay xài công cụ nào để kiểm tra lỗi về hiệu suất tải trên trình duyệt? 
* Giải thích sự khác nhau giữa layout, painting và compositing.

## Hỏi về Network

* Tại sao lưu resource (js/css/...) trên nhiều domain sẽ tốt hơn? 
* Sự khác nhau giữa Long-Polling, Websockets và Server-Sent?
* Giải thích ý nghĩa của mấy cái HTTP Header sau:
  * Diff. between Expires, Date, Age and If-Modified-...
  * Do Not Track
  * Cache-Control
  * Transfer-Encoding
  * ETag
  * X-Frame-Options
* HTTP action là gì?

## Hỏi về Coding
**Hỏi:** `foo` có giá trị là bao nhiêu?
```js
var foo = 10 + '20';
```

**Hỏi:** Viết hàm `add` để thực hiện được câu lệnh sau:
```js
add(2, 5); // 7
add(2)(5); // 7
```

**Hỏi:** Kết quả trả về của hàm lệnh sau là gì?
```js
"i'm a developer".split("").reverse().join("");
```

**Hỏi:** Giá trị của `window.foo` là gì?
```js
( window.foo || ( window.foo = "bar" ) );
```

**Hỏi:** Kết quả của 2 lệnh `alert` là gì?
```js
var foo = "Hello";
(function() {
  var bar = " World";
  alert(foo + bar);
})();
alert(foo + bar);
```

**Hỏi:** Giá trị của `foo.length` trong trường hợp sau?
```js
var foo = [];
foo.push(1);
foo.push(2);
```

**Hỏi:** Giá trị của `foo.x` trong trường hợp sau?
```js
var foo = {n: 1};
var bar = foo;
foo.x = foo = {n: 2};
```

**Hỏi:** Các lệnh sau sẽ in ra console cái gì?
```js
console.log('one');
setTimeout(function() {
  console.log('two');
}, 0);
console.log('three');
```

## Hỏi chơi cho vui 

* Những dữ án nào mà bạn cho là thú vụ đã từng làm qua?
* Bạn hay sử dụng các công cụ (tools) nào? 
* Bạn thích tính năng nào của Internet Explorer nhất?
* 

------------------------------------------

# Contributors
* 15/12/2015, dự án được khởi động bởi [@duyetdev](https://github.com/duyetdev)

# How to Contribute
Trang được xây dựng bởi cộng đồng. Để đóng góp vào danh sách câu hỏi, vui lòng: 

1. Fork repo tại Github: [https://github.com/duyetdev/phong-van-frontend-toan-tap](https://github.com/duyetdev/phong-van-frontend-toan-tap)
2. Commit câu hỏi trực tiếp vào file README.md, nhánh master.
3. Tạo Pull Request.

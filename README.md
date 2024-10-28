# Tuyển tập câu hỏi phỏng vấn Front-end

Mục đích của trang là tổng hợp lại danh sách các câu hỏi tham khảo phỏng vấn cho vị trí lập trình viên Front-end. 

Với mong muốn giúp những ai đang sắp được phỏng vấn chuẩn bị tốt hơn, đồng thời
giúp ôn lại các kiến thức về front-end một cách vững chắc nhất. 

Mình tha thiết mong muốn mọi người cùng đóng góp nội dung, [tại đây](#how-to-contribute).

![](https://i.imgur.com/qJhyreL.jpg)

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
3. [License](https://github.com/duyetdev/frontend-interview-questions-vietnamese/blob/master/LICENSE)

------------------------------------------

## Hỏi chung

* Những điểm nào mà bạn thích, hoặc không thích về lập trình?
* Khác nhau giữa UI và UX?
  * UI (User Interface): Tập trung vào giao diện người dùng, cách trình bày và tương tác trực quan
  * UX (User Experience): Tập trung vào trải nghiệm tổng thể, cảm nhận và hiệu quả sử dụng
* Nói về môi trường làm việc mà bạn mong muốn?
* Ba cách để giảm dung lượng tải trang?
  * Tối ưu và nén hình ảnh
  * Minify và gộp file CSS/JS
  * Sử dụng CDN và caching hiệu quả
  * Lazy loading cho images và components
  * Tree shaking để loại bỏ code không sử dụng
* CORS là gì và cách xử lý?
  * CORS (Cross-Origin Resource Sharing) là cơ chế cho phép nhiều tài nguyên khác nhau của một trang web có thể được truy vấn từ domain khác với domain của trang đó
  * Xử lý: Cấu hình header phù hợp, sử dụng proxy, hoặc middleware trên server
* Progressive Enhancement và Graceful Degradation là gì?
* Single Page Application (SPA) vs Multi Page Application (MPA)?
* Virtual DOM là gì và tại sao nó quan trọng?

## Hỏi về HTML

* Tác dụng của `doctype`?
  * Khai báo kiểu tài liệu HTML để trình duyệt biết cách render
  * Đảm bảo trang web được hiển thị ở chế độ standards mode
* Khác nhau giữa HTML và XHTML là gì?
  * XHTML yêu cầu cú pháp nghiêm ngặt hơn (phải đóng thẻ, case sensitive)
  * XHTML tuân thủ quy tắc XML
* Có vấn đề gì không nếu lưu trang MIME dạng `application/xhtml+xml`?
* Điều gì mà bạn cần phải chú ý nếu xây dựng và phát triển các trang web đa ngôn ngữ?
  * Sử dụng thẻ lang và charset phù hợp
  * Hỗ trợ RTL (Right-to-Left) cho một số ngôn ngữ
  * Tổ chức content theo cấu trúc i18n
* Thuộc tính `data-` dùng để làm gì?
  * Lưu trữ dữ liệu tùy chỉnh trong HTML
  * Truy cập dữ liệu thông qua JavaScript Dataset API
* Nếu HTML5 là nguồn mở, thẻ HTML nào mà bạn sẽ phát triển thêm?
* Khác nhau giữa `cookie`, `sessionStorage` và `localStorage`.
  * Cookie: 4KB, gửi lên server mỗi request, có expiry
  * sessionStorage: 5MB+, chỉ tồn tại trong session, không gửi lên server
  * localStorage: 5MB+, tồn tại vĩnh viễn, không gửi lên server
* Khác nhau giữa `<script>`, `<script async>` và `<script defer>`.
  * script: Blocking, dừng parse HTML
  * async: Non-blocking, thực thi ngay khi tải xong
  * defer: Non-blocking, thực thi sau khi parse HTML
* Tại sao nên đặt `<link>` trong thẻ `<head></head>` và đặt `<script>` sau thẻ `</body>`. Ngoại lệ khi nào?
  * link trong head: Load CSS sớm tránh FOUC (Flash of Unstyled Content)
  * script cuối body: Không block render, tải sau khi có DOM
  * Ngoại lệ: Script cần thực thi sớm hoặc có async/defer
* Semantic HTML là gì và tại sao nó quan trọng?
* Web Components là gì?
* Shadow DOM dùng để làm gì?

## Hỏi về CSS

* CSS framework là gì?
  * Bootstrap, Tailwind, Material UI...
  * Ưu điểm: Phát triển nhanh, responsive sẵn
  * Nhược điểm: File size lớn, khó customize
* Có mấy cách để sử dụng CSS trên trang web?
  * Inline CSS
  * Internal CSS (style tag)
  * External CSS (link tag)
  * Import CSS (@import)
* Lợi / hại của việc sử dụng External Style Sheets?
  * Lợi: Tái sử dụng, cache, dễ maintain
  * Hại: Thêm HTTP request, có thể block rendering
* Giải thích Ruleset là gì?
  * Selector + Declaration block
  * VD: `.class-name { property: value; }`
* **Case-sensitivity** - ngôn ngữ css có phân biệt hoa thường khi nào? 
  * Selectors: Case-sensitive
  * Properties và values: Case-insensitive
* Khác nhau giữa Class selector và Id selector?
  * Class: Dùng nhiều lần, độ ưu tiên thấp hơn
  * ID: Unique, độ ưu tiên cao hơn
* Pseudo-elements là gì?
  * ::before, ::after, ::first-line, ::first-letter
  * Tạo và style element ảo
* Cách nào đổi khôi phục thuộc tính mặc định của một đối tượng? 
  * Sử dụng `initial` hoặc `unset`
  * VD: `color: initial;`
* `z-index` dùng để làm gì?
  * Kiểm soát thứ tự xếp chồng các element
  * Chỉ hoạt động với position không phải static
* Tại sao `@import` chỉ có thể sử dụng ở đầu file?
  * Đảm bảo thứ tự load CSS đúng
  * Tránh blocking render không cần thiết
* CSS Grid và Flexbox khác nhau như thế nào?
* CSS-in-JS là gì? Ưu nhược điểm?
* CSS Module là gì và khi nào nên dùng?
* BEM methodology là gì?

## Hỏi về Javascript

* Ý nghĩa của biến `this`.
  * Context của function hiện tại
  * Phụ thuộc vào cách function được gọi
* Sử dụng **AMD** và **CommonJS** có tốt hay không? Tại sao tốt hoặc không tốt?
  * AMD: Async loading, phù hợp browser
  * CommonJS: Sync loading, phù hợp Node.js
* Nếu viết theo kiểu IIFE, tại sao đoạn mã sau bị lỗi? `function foo(){ }();`
  * Sửa lại: `(function foo(){ })();`
  * Hoặc: `(function foo(){ }());`
* Khác nhau giữa `null`, `undefined` hoặc chưa khai báo?
  * undefined: Biến đã khai báo nhưng chưa gán giá trị
  * null: Giá trị rỗng được gán có chủ đích
  * Chưa khai báo: ReferenceError khi truy cập
* Khác nhau giữa **host objects** và **native objects** là gì?
  * Native: Built-in objects (Array, Date...)
  * Host: Do môi trường cung cấp (window, document...)
* Javascript closure là gì?
  * Function có thể truy cập biến ngoài scope của nó
  * Giữ reference đến biến sau khi function kết thúc
* `ES6` Yeild là gì? [giải thích](https://blog.duyetdev.com/2016/02/generator-function-javascript.html)
* `ES6` Function* là gì? [giải thích](https://blog.duyetdev.com/2016/02/generator-function-javascript.html)
* callback có phải là một phần của V8 hay không?
* Khác biệt của arrow function là gì?
* Phân biệt let,const,var khi nào thì dùng nó?
* Promise trong JS là gì?
* Có nên dùng nhiều callback lồng nhau (callback hell)?

[Rest of the original content continues unchanged...]

## Hỏi về Testing 

* Có nên sử dụng các công cụ Lint Style hay không? Tại sao?
* Có nên áp dụng unit test hay không ? 
* Bạn có biết về TDD không ? nêu thử 1 vài framework ?

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
* Phân biệt các method HTTP(khi nào thì dùng nó).

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

**Hỏi:** Các lệnh sau sẽ in ra console cái gì?
```js
baz = function() {
 return "some thing cool";
}
foo = false;
console.log (foo && baz());
console.log (foo || baz());
```

**Hỏi:** Cho `var string = ['1','3','4','10','2','5','9','7','8','6']` in ra kết quả sau
```js
10 9 8 7
6 5 4 
3 2 
1
```

## Hỏi chơi cho vui 

* Những dự án nào mà bạn cho là thú vị đã từng làm qua?
* Bạn hay sử dụng các công cụ (tools) nào? 
* Bạn thích tính năng nào của Internet Explorer nhất?
* Bạn cho biết cách để đo thời gian chạy của một đoạn code javascript, chính xác tới ms?
* Cho 8 viên bi trong đó có 7 viên cùng khối lượng và 1 viên còn lại nặng hơn ? 
* Cho 1 cái cân -|- (kiểu vậy). Làm sao để tìm viên bi nặng hơn nhanh nhất ?
* Cho 2 sợi dây. Đốt 2 sợi dây đó thì mất 1 tiếng. Hỏi trong 45 phút thì làm sao có thể đốt được 2 sợi dây đó.

------------------------------------------

# Contributors

* 24/06/2016, pull request [#1](https://github.com/duyetdev/vietnamese-frontend-interview-questions/pull/1) - [@dannyphung](https://github.com/dannyphung)
* 15/12/2015, dự án được khởi động bởi [@duyetdev](https://github.com/duyetdev)

# How to Contribute
Trang được xây dựng bởi cộng đồng. Để đóng góp vào danh sách câu hỏi, vui lòng: 

1. Fork repo tại Github: [https://github.com/duyetdev/frontend-interview-questions-vietnamese](https://github.com/duyetdev/frontend-interview-questions-vietnamese)
2. Commit câu hỏi trực tiếp vào file README.md, nhánh master.
3. Tạo Pull Request.

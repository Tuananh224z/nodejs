# NodeJS

# I. JavaScript
# 1. ECMAScript 6+
## A. Let, const

Trước ES6, JS chỉ có var → rất nhiều lỗi khó chịu:
- Không kiểm soát được phạm vi (scope)
- Dễ ghi đè biến
- Bug ngầm rất khó debug

_Ví dụ_: var bị “lọt” ra ngoài if

```js
if (true) {
  var x = 10;
}

console.log(x); // 👉 10 😱 (lẽ ra không được phép)
```
let => Biến có thể thay đổi giá trị
biến có thể thay đổi được nhưng không khai báo lại đc
const =>Biến ko thay đổi đc
có thể khai báo lại đc nhưng biến ko thay đổi được
var  Ko hỗ trợ trong phạm vi  Block Scope
Vì var chỉ có Function Scope, KHÔNG có Block Scope

{} --> đây chính block
scope --> Phạm vi



## B. Template Literals
Là cách viết kiểu chuỗi ( string ) trong ES6
`Hello world` => cái này đc gọi là ` (backtick)
${} dùng để nhúng biến hoặc biểu thức vào chuỗi
Nó giúp:
Nhúng biến vào chuỗi
Viết chuỗi nhiều dòng
Code gọn, dễ đọc
VD:
const name = "An";
const age = 20;

const message = `Tên: ${name}, Tuổi: ${age}`;
console.log(message);


## C. Multi-line String
Multi-line String (viết chuỗi nhiều dòng) – phần này đi liền với Template Literals.
VD :
const text = `
Dòng 1
Dòng 2
Dòng 3
`;

console.log(text);


## D. Arrow function
Arrow Function là cách viết hàm ngắn gọn hơn trong ES6
Cú pháp cơ bản
const tenHam = (thamSo) => {
  // code
};


## E. Classes
Class là khuôn mẫu (template) để tạo ra object


## F. Default parameter values
## G. Destructuring
## H. Rest parameters
// Quan trọng
Rest parameters dùng để:
Gộp nhiều tham số thành một mảng
VD :
function sum(...numbers) {
  return numbers.reduce((total, n) => total + n, 0);
}

sum(1, 2, 3, 4); // 10

## J. Spread
// Quan trọng
Spread dùng để:
Tách mảng / object thành từng phần
Dùng khi gán, copy, merge
VD :
Spread với Array
Copy mảng (RẤT QUAN TRỌNG)
const a = [1, 2, 3];
const b = [...a]; // 1,2,3

b.push(4); thêm vào mảng 

console.log(a); // [1, 2, 3]
console.log(b); // [1, 2, 3, 4]
## K. Enhanced object literals
## L. Tagged template literal
## M. Modules
// Quan trọng
Chia code thành nhiều file nhỏ và import/export qua lại
Giải quyết vấn đề:
Code dài, khó quản lý
Dùng lại code
Làm project lớn (NodeJS, React)
export và import khác nhau ở đâu?
export
Dùng để CHIA SẺ (xuất) code ra ngoài file
File cho đi
import
Dùng để NHẬN (nhập) code từ file khác
File nhận về dùng
## N. Optional chaining
// Quan trọng
dùng để:
Truy cập thuộc tính an toàn khi object có thể null hoặc undefined
const response = {
  data: {
    user: {
      name: "Tuấn Anh"
    }
  }
};
const name = response?.data?.user?.name; // kiểu check xem thuộc tính có an toàn ko 
console.log(name); // Tuấn Anh



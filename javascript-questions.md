# Câu hỏi JavaScript

Dưới đây là các câu hỏi cơ bản về **JavaScript**, kèm theo câu trả lời ngắn gọn và dễ hiểu. Những câu hỏi này bao quát các kiến thức cơ bản mà bạn cần nắm vững:

---

### **1. JavaScript là gì?**
**Câu hỏi**: JavaScript là gì và được sử dụng để làm gì?  
**Câu trả lời**:  
JavaScript là ngôn ngữ lập trình phổ biến dùng để tạo ra các tính năng tương tác trên trang web, như xử lý sự kiện, thay đổi giao diện động, xác thực biểu mẫu, hoặc gọi API.

---

### **2. Biến trong JavaScript**
**Câu hỏi**: Làm thế nào để khai báo biến trong JavaScript?  
**Câu trả lời**:  
Có ba cách khai báo biến:  
- `var`: Có phạm vi function hoặc global.  
- `let`: Có phạm vi block, thay thế `var` trong hầu hết trường hợp.  
- `const`: Có phạm vi block và không thể tái gán giá trị.  

**Ví dụ**:
\`\`\`javascript
var x = 5;       // Global scope
let y = 10;      // Block scope
const z = 15;    // Không thể thay đổi giá trị
\`\`\`

---

### **3. Kiểu dữ liệu**
**Câu hỏi**: Các kiểu dữ liệu cơ bản trong JavaScript là gì?  
**Câu trả lời**:  
JavaScript có các kiểu dữ liệu sau:  
1. **Primitive types**:  
   - `string`, `number`, `boolean`, `null`, `undefined`, `symbol`, `bigint`.  
2. **Non-primitive type**:  
   - `object` (bao gồm array, function, object).

---

### **4. Toán tử**
**Câu hỏi**: Sự khác nhau giữa `==` và `===` là gì?  
**Câu trả lời**:  
- `==` so sánh giá trị, không xét kiểu dữ liệu (loose equality).  
- `===` so sánh cả giá trị và kiểu dữ liệu (strict equality).  

**Ví dụ**:
\`\`\`javascript
console.log(5 == "5");  // true (chỉ so sánh giá trị)
console.log(5 === "5"); // false (so sánh cả kiểu)
\`\`\`

---

### **5. Vòng lặp**
**Câu hỏi**: Các loại vòng lặp trong JavaScript là gì?  
**Câu trả lời**:  
- `for`: Lặp qua số lần cố định.  
- `while`: Lặp khi điều kiện là true.  
- `do...while`: Lặp ít nhất một lần, sau đó kiểm tra điều kiện.  
- `for...in`: Lặp qua các thuộc tính của object.  
- `for...of`: Lặp qua các giá trị trong iterable (mảng, chuỗi,...).

**Ví dụ**:
\`\`\`javascript
for (let i = 0; i < 5; i++) {
  console.log(i); // In ra 0, 1, 2, 3, 4
}
\`\`\`

---

### **6. Hàm**
**Câu hỏi**: Làm thế nào để định nghĩa một hàm trong JavaScript?  
**Câu trả lời**:  
Có 3 cách định nghĩa hàm:  
1. **Function Declaration**:  
   \`\`\`javascript
   function sayHello() {
     console.log("Hello!");
   }
   \`\`\`
2. **Function Expression**:  
   \`\`\`javascript
   const sayHello = function() {
     console.log("Hello!");
   }
   \`\`\`
3. **Arrow Function**:  
   \`\`\`javascript
   const sayHello = () => {
     console.log("Hello!");
   }
   \`\`\`

---

### **7. DOM (Document Object Model)**
**Câu hỏi**: Làm thế nào để lấy một phần tử HTML bằng JavaScript?  
**Câu trả lời**:  
Có thể dùng các phương thức sau:  
- `document.getElementById("id")`: Lấy phần tử theo `id`.  
- `document.querySelector("selector")`: Lấy phần tử đầu tiên theo CSS selector.  
- `document.querySelectorAll("selector")`: Lấy tất cả phần tử theo CSS selector.  

**Ví dụ**:
\`\`\`javascript
const element = document.getElementById("myDiv");
const button = document.querySelector(".btn");
\`\`\`

---

### **8. Xử lý sự kiện**
**Câu hỏi**: Làm thế nào để xử lý sự kiện click trong JavaScript?  
**Câu trả lời**:  
Dùng phương thức `addEventListener`.  
**Ví dụ**:
\`\`\`javascript
const button = document.querySelector("button");
button.addEventListener("click", function() {
  alert("Button clicked!");
});
\`\`\`

---

### **9. Mảng**
**Câu hỏi**: Làm thế nào để thêm hoặc xóa phần tử trong mảng?  
**Câu trả lời**:  
- Thêm phần tử: Dùng `push` (cuối mảng) hoặc `unshift` (đầu mảng).  
- Xóa phần tử: Dùng `pop` (cuối mảng) hoặc `shift` (đầu mảng).  

**Ví dụ**:
\`\`\`javascript
const arr = [1, 2, 3];
arr.push(4);      // [1, 2, 3, 4]
arr.pop();        // [1, 2, 3]
\`\`\`

---

### **10. Object**
**Câu hỏi**: Làm thế nào để truy cập vào thuộc tính của một object?  
**Câu trả lời**:  
Dùng dấu chấm (`.`) hoặc dấu ngoặc vuông (`[]`).  
**Ví dụ**:
\`\`\`javascript
const person = { name: "John", age: 30 };
console.log(person.name);     // John
console.log(person["age"]);   // 30
\`\`\`

---

### **11. JSON**
**Câu hỏi**: JSON là gì? Làm thế nào để chuyển đổi giữa object và JSON?  
**Câu trả lời**:  
- **JSON (JavaScript Object Notation)** là định dạng dữ liệu nhẹ để trao đổi thông tin.  
- Chuyển từ object sang JSON: `JSON.stringify()`.  
- Chuyển từ JSON sang object: `JSON.parse()`.  

**Ví dụ**:
\`\`\`javascript
const obj = { name: "John", age: 30 };
const json = JSON.stringify(obj); // '{"name":"John","age":30}'
const parsedObj = JSON.parse(json); // { name: "John", age: 30 }
\`\`\`

---

### **12. Promise**
**Câu hỏi**: Promise trong JavaScript là gì?  
**Câu trả lời**: Promise là một cách xử lý bất đồng bộ, đại diện cho một giá trị sẽ được trả về trong tương lai (thành công hoặc thất bại).  

**Ví dụ**:
\`\`\`javascript
const promise = new Promise((resolve, reject) => {
  let success = true;
  if (success) resolve("Success!");
  else reject("Error!");
});

promise
  .then((result) => console.log(result))  // Output: Success!
  .catch((error) => console.log(error));
\`\`\`

---

### **13. Async/Await**
**Câu hỏi**: Async/Await là gì?  
**Câu trả lời**: Async/Await là cú pháp mới của JavaScript để xử lý bất đồng bộ, giúp code dễ đọc hơn.  

**Ví dụ**:
\`\`\`javascript
async function fetchData() {
  const response = await fetch("https://api.example.com/data");
  const data = await response.json();
  console.log(data);
}
fetchData();
\`\`\`

---

### **14. Vòng lặp trong mảng**
**Câu hỏi**: Làm thế nào để duyệt qua các phần tử của một mảng?  
**Câu trả lời**: Dùng các phương thức như `forEach`, `map`, hoặc `for...of`.  
**Ví dụ**:
\`\`\`javascript
const arr = [1, 2, 3];
arr.forEach(num => console.log(num)); // 1, 2, 3
\`\`\`

---



Dưới đây là các câu hỏi cơ bản về **ReactJS**, kèm theo câu trả lời ngắn gọn và dễ hiểu. Các câu hỏi này giúp bạn chuẩn bị tốt cho buổi phỏng vấn:

---

### **1. ReactJS là gì?**
**Câu hỏi**: ReactJS là gì?  
**Câu trả lời**:  
ReactJS là một thư viện JavaScript mã nguồn mở do Facebook phát triển, được sử dụng để xây dựng giao diện người dùng (UI) dựa trên các thành phần (components). Nó giúp tạo ra các ứng dụng web đơn trang (SPA) với hiệu suất cao.

---

### **2. Component trong React là gì?**
**Câu hỏi**: Component trong React là gì?  
**Câu trả lời**:  
Component là khối xây dựng cơ bản của React. Một component là một đoạn mã độc lập, tái sử dụng được, có thể trả về giao diện (HTML) bằng cách sử dụng JavaScript.

---

### **3. State trong React là gì?**
**Câu hỏi**: State trong React là gì?  
**Câu trả lời**:  
State là một đối tượng lưu trữ dữ liệu động của một component. Khi `state` thay đổi, React sẽ tự động re-render lại giao diện.  

**Ví dụ**:
```javascript
import React, { useState } from "react";

function Counter() {
  const [count, setCount] = useState(0);

  return (
    <div>
      <p>Count: {count}</p>
      <button onClick={() => setCount(count + 1)}>Increase</button>
    </div>
  );
}
```

---

### **4. Props là gì?**
**Câu hỏi**: Props trong React là gì?  
**Câu trả lời**:  
Props (properties) là dữ liệu được truyền từ component cha đến component con. Props không thể thay đổi bên trong component nhận chúng.  

**Ví dụ**:
```javascript
function Greeting(props) {
  return <h1>Hello, {props.name}!</h1>;
}

function App() {
  return <Greeting name="John" />;
}
```

---

### **5. Sự khác nhau giữa state và props là gì?**
**Câu hỏi**: Sự khác nhau giữa state và props là gì?  
**Câu trả lời**:  
- **State**: Thuộc sở hữu của component, có thể thay đổi được bằng cách dùng `setState` hoặc `useState`.  
- **Props**: Được truyền từ component cha, chỉ đọc (read-only), không thể thay đổi.

---

### **6. JSX là gì?**
**Câu hỏi**: JSX trong React là gì?  
**Câu trả lời**:  
JSX (JavaScript XML) là cú pháp mở rộng của JavaScript, cho phép viết HTML trực tiếp trong JavaScript. JSX giúp mã React dễ đọc và viết hơn.

**Ví dụ**:
```javascript
const element = <h1>Hello, world!</h1>;
```

---

### **7. Lifecycle methods là gì?**
**Câu hỏi**: Lifecycle methods trong React là gì?  
**Câu trả lời**:  
Lifecycle methods là các phương thức được gọi trong các giai đoạn khác nhau của vòng đời component. Có 3 giai đoạn chính:  
1. **Mounting**: Khi component được tạo và thêm vào DOM.  
2. **Updating**: Khi `props` hoặc `state` thay đổi.  
3. **Unmounting**: Khi component bị xóa khỏi DOM.

---

### **8. useEffect Hook là gì?**
**Câu hỏi**: useEffect Hook trong React là gì?  
**Câu trả lời**:  
`useEffect` là một Hook được dùng để xử lý các tác vụ phụ (side effects) như gọi API, đăng ký sự kiện, hoặc thao tác với DOM.  

**Ví dụ**:
```javascript
import React, { useState, useEffect } from "react";

function Timer() {
  const [seconds, setSeconds] = useState(0);

  useEffect(() => {
    const interval = setInterval(() => setSeconds(seconds + 1), 1000);
    return () => clearInterval(interval); // Cleanup
  }, [seconds]);

  return <p>Seconds: {seconds}</p>;
}
```

---

### **9. useState Hook là gì?**
**Câu hỏi**: useState Hook trong React là gì?  
**Câu trả lời**:  
`useState` là một Hook được sử dụng để khai báo state trong functional components. Nó trả về một mảng gồm giá trị hiện tại của state và hàm để thay đổi state.

**Ví dụ**:
```javascript
const [count, setCount] = useState(0);
```

---

### **10. Virtual DOM là gì?**
**Câu hỏi**: Virtual DOM là gì?  
**Câu trả lời**:  
Virtual DOM là bản sao nhẹ của DOM thật, giúp React so sánh và cập nhật giao diện một cách hiệu quả. Khi state hoặc props thay đổi, React chỉ cập nhật các phần tử bị thay đổi trong DOM thật.

---

### **11. Event Handling trong React**
**Câu hỏi**: Làm thế nào để xử lý sự kiện trong React?  
**Câu trả lời**:  
React sử dụng các thuộc tính camelCase để xử lý sự kiện. Bạn có thể truyền một hàm xử lý sự kiện vào thuộc tính đó.

**Ví dụ**:
```javascript
function handleClick() {
  alert("Button clicked!");
}

function App() {
  return <button onClick={handleClick}>Click me</button>;
}
```

---

### **12. Key trong React là gì?**
**Câu hỏi**: Key trong React là gì?  
**Câu trả lời**:  
Key là thuộc tính đặc biệt được sử dụng trong React để xác định duy nhất các phần tử trong danh sách. Điều này giúp React tối ưu hóa quá trình re-render.

**Ví dụ**:
```javascript
const items = ["Apple", "Banana", "Cherry"];
const listItems = items.map((item, index) => <li key={index}>{item}</li>);
```

---

### **13. Fragment trong React là gì?**
**Câu hỏi**: React.Fragment là gì?  
**Câu trả lời**:  
React.Fragment được sử dụng để nhóm nhiều phần tử lại với nhau mà không thêm thẻ DOM thừa vào.  

**Ví dụ**:
```javascript
function App() {
  return (
    <>
      <h1>Hello</h1>
      <p>Welcome to React!</p>
    </>
  );
}
```

---

### **14. Controlled Component là gì?**
**Câu hỏi**: Controlled Component trong React là gì?  
**Câu trả lời**:  
Controlled Component là component mà dữ liệu đầu vào của nó được quản lý bởi state của React.

**Ví dụ**:
```javascript
function App() {
  const [value, setValue] = useState("");

  return (
    <input
      type="text"
      value={value}
      onChange={(e) => setValue(e.target.value)}
    />
  );
}
```

---

### **15. Cách gọi API trong React**
**Câu hỏi**: Làm thế nào để gọi API trong React?  
**Câu trả lời**:  
Sử dụng `fetch` hoặc thư viện như `axios` để gọi API.  

**Ví dụ**:
```javascript
import React, { useState, useEffect } from "react";

function App() {
  const [data, setData] = useState([]);

  useEffect(() => {
    fetch("https://api.example.com/items")
      .then((response) => response.json())
      .then((data) => setData(data));
  }, []);

  return (
    <ul>
      {data.map((item) => (
        <li key={item.id}>{item.name}</li>
      ))}
    </ul>
  );
}
```

---

### **16. Sự khác nhau giữa Class Component và Functional Component**
**Câu hỏi**: Sự khác nhau giữa Class Component và Functional Component là gì?  
**Câu trả lời**:  
- **Class Component**: Được viết dưới dạng ES6 class, có thể sử dụng state và lifecycle methods.  
- **Functional Component**: Là hàm JavaScript đơn giản, sử dụng Hook (như `useState`, `useEffect`) để quản lý state và lifecycle.

---

### **17. Higher-Order Component (HOC) là gì?**
**Câu hỏi**: HOC trong React là gì?  
**Câu trả lời**:  
HOC là một hàm nhận một component và trả về một component mới, giúp tái sử dụng logic.  

**Ví dụ**:
```javascript
function withLogger(WrappedComponent) {
  return function Logger(props) {
    console.log("Props: ", props);
    return <WrappedComponent {...props} />;
  };
}
```

---

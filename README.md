# HOW TO HERO REACT

#### 1. React là một library, chứ không phải là một framework. Đây là một điều mà rất nhiều người hiểu sai.
- Library là một trong những module của framework, một mình nó không thể build ra một project được mà cần phải rất nhiều library khác kết hợp với nhau nữa.
- Framework là tập hợp những library, một mình nó có thể build ra một project hoàn chỉnh.

#### 2. React căn bản cũng là HTML/CSS/JS. Nhưng nó hỗ trợ những thứ chúng ta thường sử dụng và nâng cao performance ứng dụng.

#### 3. React hoạt động theo template JSX. Nhưng 'JSX' thằng trình duyệt nó không hiểu được nên cần phải nhờ thằng Babel compile code cho trình duyệt hiểu.

#### 4. Bình thường khi code react thì phải setup rất nhiều thứ liên quan ví dụ JSX, Babel,.. nhưng rất may mắn nay đã có CRA (npx create-react-app app-name) nó hỗ trợ setup project cho chúng ta.

#### 5. Component là trái tim của react. Component có 2 loại là Container và Pure Component.
- Pure Component nó chỉ biết nhận dữ liệu và render ra giao diện. 
- Container là nơi chứa dữ liệu, chịu trách nhiệm xử lý logic và truyền dữ liệu xuống thằng Component Pure.

#### 6. Life Circle của một Component có 3 trạng thái: Mounting - Updating - Unmounting.

#### 7. Có 3 Life Cirle chúng ta hay sử dụng nhất đó là: ComponentDidMount - ComponentDidUpdate - ComponentWillUnmount.
- ComponentDidMount sẽ thực thi ngay sau khi component mount vào DOM.
- ComponentDidUpdate sẽ thực thi ngay sau khi component đã update.
- ComponentWillUnmount sẽ thực thi trước khi component unmount ra khỏi cây DOM.

#### 8. Mỗi khi props hoặc state của component thay đổi thì nó sẽ update lại.
- Ví dụ khi state của component A thay đổi thì component A sẽ update lại.  
- Ví dụ ta có một component ListTodo truyền props xuống component Todo. Mỗi khi props của component ListTodo truyền xuống thay đổi thì component Todo sẽ update lại, chứ không phải toàn bộ component Todo xóa đi và mount những component Todo mới.

#### 9. Truyền biến vào props thông qua HOC hoặc children.

#### 10. Những thằng padding, margin, width, height mà đơn vị phần trăm thì nó lấy tỉ lệ phần trăm của thằng cha, chỉ có thằng translate là lấy tỉ lệ của thằng element hiện tại.
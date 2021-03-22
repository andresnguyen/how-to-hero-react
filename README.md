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

#### 11. classnames 

#### 12. Trong hàm JSX thì không thể sử dụng hàm for, if.. Khi sử dụng Conditinal Rendering thì sử dụng toán tử 2 ngôi hoặc &&. Nhưng sử dụng if bên để xét điều kiện nó được render hay không. 

#### 13. Những cái component bọc bên ngoài thì ta css không được, truyền className cũng không được luôn. Nếu ra muốn css hoặc className thì ta phải xử lý bên trong component truyền vào nữa. Căn bản cái component bọc bên ngoài đó nó chỉ là một cái vỏ bọc thôi, giúp ta truyền props.

#### 14. props.children. 
- Nếu không có thì giá trị sẽ là undefined.
- Nếu có một giá tị thì sẽ là giá trị đó. 
- Nếu có nhiều hơn một giá trị thì sẽ là mảng.

- Nếu trong props là một comonent thì ta có thể truyền props và nhận props ở component đó như thường.

#### 15. useRef(null)
- Được dùng khi ta muốn chọc vào cây DOM.
- Được dùng khi ta muốn lưu giá trị trước đó của component sau khi render lại.

#### 16. react-router-dom

#### 17. async setState
- Trong class component có thể dùng setState truyền vào một callback nhưng trong function component thì không được, có thể dùng async await hoặc sử dụng một useEffect().

#### 18. Higher Order Component
- Higher Order Function là những function nhận vào một function hoặc return về một function.
- Muốn truyền props phải nhận thông qua thằng bọc rồi truyền xuống thằng con. Chứ không truyền trực tiếp như thằng props children được.

#### 19. Render props
- Sử dụng kỹ thuật higher order function hoặc props.children.
- Dữ liệu thuộc về thằng component cha chứ nó, nhưng render dữ liệu đó như thế nào thì thằng con sẽ quyết đinh.
- Đôi khi cùng một loại dữ liệu đó, nhưng ta muốn render nhiều chỗ và render nhiều cách khác nhau thì ta áp dụng kỹ thuật này. 

#### 20. useState()
- Nó là REPLACING chứ không phải MEARGING chứ class component.
- Cũng là async. Mỗi lần state thay đổi thì nó không vội render lại mà đưa setState vào một queue và chạy xuống dưới nếu có hàm setState nữa thì mới tính toán giá trị mới và render ra một lần.
- Lần đầu mouting sẽ chạy giá trị mặc định, những lần sau sẽ không lấy giá trị mặc định nữa, cho nên là nếu ta lấy giá trị từ local storage. Thì mỗi lần updating nó đều phải chạy lại hàm lấy giá trị từ local storage. Nếu muốn nó chỉ chạy một lần thì ta đưa nó vô callback.


#### 21. useEffect()
- Có 2 phần: effect và clear.
- Mặc định effect luôn chạy khi khi component mouting vào DOM còn clear chạy khi component chuẩn bị unmouting khỏi cây DOM.
- Có 3 loại: có tham số truyền vào, tham số truyền vào là rỗng, tham số truyền vào là một biến
    - Mỗi lần update luôn luôn sẽ chạy clear sau đó effect
    - Giống componentDidMount và componentWilUnmount. Effect chỉ chạy lần đầu sau khi mounting và chạy Clear trước khi mounting ra khỏi cây DOM. Mỗi lần update thì nó sẽ không chạy.
    - Mỗi khi update thì nó sẽ kiểm tra điều kiện, nếu biến trong điều kiện thay đổi thì nó sẽ chạy Clear sau đó là Effect
- Nếu dùng hàm async thì viết riêng một hàm async sau dó gọi hàm đó thôi.
#### Custom hooks
- Dùng khi component dùng chung một dữ liệu nhưng render khác nhau.
- Custom hook khác với component là nó return ra data còn component return một JSX
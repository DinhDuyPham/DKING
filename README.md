components/: Chứa các thành phần giao diện như đăng nhập, đăng ký, dashboard, danh sách dự án, bảng Kanban.
context/: Quản lý trạng thái ứng dụng (ví dụ: trạng thái đăng nhập, dữ liệu người dùng).
services/: Chứa các hàm gọi API đến backend (đăng nhập, lấy danh sách dự án, task).
hooks/: Các custom hooks để tái sử dụng logic (ví dụ: useAuth để kiểm tra trạng thái đăng nhập).
pages/: Chứa các trang của ứng dụng (trang chủ, trang đăng nhập, trang đăng ký).

DKING/          # Thư mục gốc của frontend (ReactJS)
│
├── public/          # Thư mục chứa các tài nguyên tĩnh như favicon, index.html
│   └── index.html
│
├── src/             # Thư mục chứa mã nguồn chính của ứng dụng React
│   ├── assets/      # Chứa các file hình ảnh, biểu tượng
│   │   └── logo.png
│   │
│   ├── components/  # Chứa các component UI của ứng dụng
│   │   ├── Auth/    # Chứa các component liên quan đến Authentication
│   │   │   ├── LoginPage.js
│   │   │   ├── RegisterPage.js
│   │   │   └── ProtectedRoute.js  # Route bảo vệ cho các trang chỉ có quyền đăng nhập mới truy cập được
│   │   │
│   │   ├── Dashboard/  # Chứa giao diện dashboard của người dùng
│   │   │   ├── Dashboard.js
│   │   │   ├── ProjectList.js  # Hiển thị danh sách các dự án
│   │   │   └── TaskBoard.js    # Hiển thị bảng Kanban với các task
│   │   │
│   │   ├── Project/   # Giao diện liên quan đến project
│   │   │   ├── ProjectDetail.js
│   │   │   └── ProjectCard.js
│   │   │
│   │   ├── Task/      # Giao diện liên quan đến task
│   │   │   ├── TaskCard.js
│   │   │   └── TaskDetail.js
│   │
│   ├── context/      # Context API để quản lý trạng thái chung như User Context, Project Context
│   │   └── AuthContext.js
│   │
│   ├── hooks/        # Custom hooks cho ứng dụng
│   │   └── useAuth.js  # Hook để quản lý trạng thái người dùng đăng nhập
│   │
│   ├── pages/        # Các trang chính của ứng dụng
│   │   ├── HomePage.js
│   │   ├── LoginPage.js
│   │   └── RegisterPage.js
│   │
│   ├── services/     # Chứa các hàm gọi API qua Axios
│   │   ├── authService.js
│   │   ├── projectService.js
│   │   └── taskService.js
│   │
│   ├── App.js        # Component gốc của ứng dụng React
│   ├── index.js      # Điểm vào chính của ứng dụng React
│   ├── routes.js     # Cấu hình các route
│   └── App.css       # CSS chính của ứng dụng
│
├── package.json      # File cấu hình của npm
└── .env              # File cấu hình biến môi trường (nếu cần)
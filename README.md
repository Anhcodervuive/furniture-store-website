# Website Kinh Doanh Nội Thất

> Niên luận CT271 - Đại học Cần Thơ

**MSSV**: B2111834  
**Họ và tên**: Đỗ Thanh Dũ

## Giới thiệu

Website thương mại điện tử chuyên kinh doanh các sản phẩm nội thất, cho phép khách hàng duyệt sản phẩm, thêm vào giỏ hàng và đặt hàng trực tuyến. Hệ thống có trang quản trị dành cho admin để quản lý toàn bộ hoạt động kinh doanh.

## Chức năng chính

### Khách hàng
- Xem danh sách sản phẩm theo danh mục
- Xem chi tiết sản phẩm
- Xem sản phẩm đang giảm giá
- Tìm kiếm sản phẩm
- Quản lý giỏ hàng
- Đặt hàng và theo dõi đơn hàng
- Đăng ký, đăng nhập, quên mật khẩu
- Quản lý thông tin cá nhân

### Quản trị viên
- Dashboard thống kê
- Quản lý sản phẩm (CRUD)
- Quản lý danh mục sản phẩm
- Quản lý nhà cung cấp
- Quản lý phiếu nhập hàng
- Quản lý đơn hàng và trạng thái đơn hàng
- Quản lý chương trình giảm giá
- Quản lý mã giảm giá (coupon)
- Phân quyền người dùng (Role & Permission)

## Công nghệ sử dụng

### Backend
- PHP >= 8.2
- Laravel 11
- SQLite (có thể đổi sang MySQL/PostgreSQL)
- Spatie Laravel Permission (phân quyền)
- Intervention Image (xử lý ảnh)

### Frontend
- Blade Template
- Tailwind CSS 3
- Vite 5
- Axios

### Công cụ
- Composer
- NPM
- Laravel Artisan

## Cài đặt

### Yêu cầu
- PHP >= 8.2
- Composer >= 2.7
- Node.js & NPM

### Các bước cài đặt

```bash
# Clone project
git clone https://github.com/DoThanhDuB2111834/CT271_Project.git
cd CT271_Project

# Cài đặt dependencies
composer install
npm install

# Cấu hình môi trường
cp .env.example .env
php artisan key:generate

# Tạo database và seed dữ liệu mẫu
php artisan migrate
php artisan db:seed

# Chạy ứng dụng
php artisan serve
npm run dev
```

Truy cập: http://localhost:8000

## Cấu trúc thư mục chính

```
├── app/
│   ├── Http/Controllers/   # Controllers
│   ├── Models/             # Eloquent Models
│   └── Traits/             # Traits
├── database/
│   ├── migrations/         # Database migrations
│   └── seeders/            # Database seeders
├── resources/
│   └── views/              # Blade templates
├── routes/
│   ├── web.php             # Routes khách hàng
│   ├── admin.php           # Routes admin
│   └── auth.php            # Routes xác thực
└── public/                 # Assets công khai
```

## License

MIT License

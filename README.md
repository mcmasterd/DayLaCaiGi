# DayLaCaiGi
- Thêm Razor View (tên _AdminLayout) vào Shared để tạo phần FrontEnd cho Admin + Bỏ tick phần Use a Layout Page
- Tự dán code FrontEnd vào
- @RenderBody()  vào cuối body nhưng trong div (Div bên trên Script)
- Tự add AdminController (chọn MVC Controller- Emty)
- Vào phần View ở public IActionResult -> Chuột phải rồi chọn Razor View -> Chọn Layout Page là cái _AdminLayout        (Trong Layout tổng thì Admin-Index)

  Tạo  CSDL trên VS
- Thêm class(User) vào Model
- Khai báo trong class các thuộc tính của bảng:
  
    [Key]                                            //Set khoá chính
    public int UserId { get; set; }                  
    [Required]                                       //NotNull
    public string? UserName { get; set; }            //? Để cho String có thể có sẵn hay ko
    [Required]
    public string? UserEmail { get; set; }
    [Required]
    public string? Password { get; set; }
    [Required]
    public string? UserRole { get; set; }
  -Thêm Controller vào phần Controller (chọn MVC Controller with views, using Entity Framework)
    Model class: Chọn class User
    Data context class thêm bên dấu + (Không sửa j)
    Layout page như trên(_AdminLayout)
    Sửa tên Controller
    Tick 1+3
  --> Chạy lên web sẽ lỗi sql

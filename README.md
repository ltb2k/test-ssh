@startuml
!theme plain
skinparam shadowing false
skinparam defaultTextAlignment center
skinparam actor {
    borderColor black
    backgroundColor white
}
skinparam rectangle {
    borderColor black
    backgroundColor white
}

rectangle "Hệ thống\nEatToday" as System

actor Guest as "Khách vãng lai"
actor User as "Người dùng/\nThành viên gia đình"
actor Planner as "Người lập\nkế hoạch"
actor Expert as "Chuyên gia\n dinh dưỡng"
actor Admin as "Quản trị viên"

Guest --> System : xem giới thiệu,\nxem mẫu công thức
User --> System : quản lý nguyên liệu,\nquản lý công thức,\nlập kế hoạch bữa ăn
Planner --> System : lập kế hoạch bữa ăn,\ntạo danh sách mua sắm,\nxem thống kê dinh dưỡng
Expert --> System : cung cấp dữ liệu\ndinh dưỡng,\nkhuyến nghị chế độ ăn
Admin --> System : quản lý tài khoản,\nquản lý công thức,\nquản lý hệ thống

' Quan hệ kế thừa
User --|> Guest
Planner --|> User

@enduml

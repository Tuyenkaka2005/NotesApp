<img width="200"  alt="b4a85e7e-af5e-4bd9-8168-c1a2e8c7c17c" src="https://github.com/user-attachments/assets/770f7015-eee2-4c87-ba8d-d1c36364ccb2" />
<img width="200"  alt="e090c55d-f1a1-42ad-9c69-64003d9655c8" src="https://github.com/user-attachments/assets/167730df-2a48-491c-9ff1-7e59cb1cde47" />
<img width="200"  alt="f0fff670-4629-4427-a984-e546518dc389" src="https://github.com/user-attachments/assets/3e84a892-14c6-4fd3-8dd4-a0ed27955b82" />
<img width="200"  alt="cb6bb29e-350b-48b1-9e88-236cdb8d40f6" src="https://github.com/user-attachments/assets/eb621d35-d7a9-4153-bcb0-f39eed7ef4d7" />
<img width="200"  alt="bf44ec5c-efa5-45a3-bbd3-be36b1d21bd0" src="https://github.com/user-attachments/assets/fe771cb0-5612-44c6-9bd3-53374dd1cd7e" />

# 📝 Notes App - iOS Local Storage Foundation

Một ứng dụng ghi chú iOS hiện đại được xây dựng bằng SwiftUI, áp dụng kiến trúc MVVM và lưu trữ dữ liệu nội bộ (Local Storage) thông qua `FileManager`. 

Dự án này là kết quả của bài thực hành Lab 9 - Notes App, tập trung vào tư duy phát triển ứng dụng "Offline-first", quản lý state và tối ưu hoá hiệu năng.

## ✨ Tính năng nổi bật (Features)

*   **Quản lý ghi chú (CRUD):** Tạo mới, xem chi tiết, chỉnh sửa và xoá ghi chú.
*   **Ghim ghi chú (Pin):** Ưu tiên hiển thị các ghi chú quan trọng lên đầu danh sách.
*   **Tìm kiếm (Search):** Bộ lọc tìm kiếm theo thời gian thực (Real-time search) trên cả tiêu đề và nội dung.
*   **Tự động lưu (Auto-save):** Tự động lưu nội dung trong quá trình chỉnh sửa, mang lại trải nghiệm liền mạch.
*   **Lưu trữ Offline:** Dữ liệu được mã hoá (`Codable`) và lưu trữ an toàn dưới dạng JSON trong thư mục Document của thiết bị.
*   **Giao diện hiện đại (Clean UI):** Hỗ trợ toàn diện Dark Mode/Light Mode, tích hợp Empty States, Swipe Actions, và thiết kế dạng thẻ (Card-based UI).

## 🛠 Công nghệ & Kiến trúc (Tech Stack)

*   **Ngôn ngữ:** Swift
*   **UI Framework:** SwiftUI
*   **Kiến trúc:** MVVM (Model - View - ViewModel)
*   **Lưu trữ (Persistence):** `FileManager` (Foundation), `JSONEncoder` / `JSONDecoder`, `UserDefaults`

## 📁 Cấu trúc thư mục (Folder Structure)

Dự án được tổ chức theo chuẩn Clean Architecture nhằm đảm bảo khả năng mở rộng và dễ dàng bảo trì:

```text
NotesApp/
│
├── Models/
│   └── Note.swift                 # Data model (Codable, Identifiable)
│
├── Services/
│   └── NoteStorageService.swift   # Xử lý logic đọc/ghi file JSON
│
├── ViewModels/
│   └── NoteViewModel.swift        # Quản lý state, filter, sort và điều phối data
│
├── Views/
│   ├── NoteListView.swift         # Màn hình chính (Danh sách)
│   ├── NoteEditorView.swift       # Màn hình tạo mới ghi chú
│   └── NoteDetailView.swift       # Màn hình xem/sửa chi tiết
│
├── Components/
│   ├── NoteCardView.swift         # UI Thẻ ghi chú
│   ├── SearchBar.swift            # Component thanh tìm kiếm custom
│   ├── PinBadge.swift             # Component icon ghim
│   └── EmptyStateView.swift       # Component trạng thái trống
│
└── NotesApp.swift                 # App Entry Point
```
🚀 Hướng dẫn cài đặt (Installation)
Yêu cầu môi trường:

macOS (phiên bản hỗ trợ Xcode mới nhất)

Xcode 15.0 trở lên

iOS Target: 17.0+ (hoặc tuỳ chỉnh lại UI API nếu build cho iOS thấp hơn)

Khởi chạy dự án:

Clone repository này về máy.

Mở file project NotesApp.xcodeproj bằng Xcode.

Cấu hình Signing & Capabilities: Chọn Team của bạn. Nếu gặp lỗi "Maximum App ID limit has been reached", hãy đổi Bundle Identifier sang một ID cũ mà bạn đã chạy thành công trong 7 ngày qua.

Nhấn Cmd + R để chạy ứng dụng trên Simulator hoặc thiết bị thật.

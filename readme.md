# 🚀 Landing Page Template – Quick Start

Template dựng landing page bằng **HTML + SCSS + JS thuần**, tối ưu cho **build production cực gọn – cực nhanh**.

---

# ⚡ Khởi tạo project mới chỉ với 1 lệnh

Sau khi đã setup alias `newlp`, bạn chỉ cần chạy:

```bash
newlp sun-landingpage
```

---

# 🧠 Lệnh `newlp` làm gì?

Chỉ với **1 lệnh**, script sẽ tự động:

- Clone source template
- Đổi tên thư mục project → `sun-landingpage`
- Đổi tên project trong `package.json`
- Xóa git history cũ
- Khởi tạo git repository mới

👉 Tạo **1 project landing page hoàn toàn mới trong 5 giây** 🚀

---

# 📦 Cài đặt alias `newlp` (chỉ làm 1 lần)

## 🖥 macOS (zsh – mặc định)

### Mở file cấu hình:

```bash
open ~/.zshrc
```

### Thêm alias:

```bash
alias newlp='git clone https://github.com/USERNAME/landing-core.git $1 && cd $1 && npm pkg set name="$1" && rm -rf .git && git init'
```

> ⚠️ Thay `USERNAME` bằng username github của bạn.

### Reload terminal:

```bash
source ~/.zshrc
```

---

## 🪟 Windows – Git Bash

### Mở file cấu hình:

```bash
nano ~/.bashrc
```

### Thêm alias:

```bash
alias newlp='git clone https://github.com/USERNAME/landing-core.git $1 && cd $1 && npm pkg set name="$1" && rm -rf .git && git init'
```

### Reload terminal:

```bash
source ~/.bashrc
```

---

## 🪟 Windows – PowerShell (khuyến nghị)

### Mở profile:

```powershell
notepad $PROFILE
```

Nếu file chưa tồn tại:

```powershell
New-Item -Path $PROFILE -Type File -Force
notepad $PROFILE
```

### Thêm function:

```powershell
function newlp($name) {
  git clone https://github.com/USERNAME/landing-core.git $name
  cd $name
  npm pkg set name="$name"
  Remove-Item -Recurse -Force .git
  git init
}
```

---

# 🛠 Sau khi tạo project

```bash
cd sun-landingpage
npm install
npm run dev
```

---

# 🏗 Build production

```bash
npm run build
```

Output:

```text
build/
 ├─ index.html
 ├─ css/main.min.css
 └─ js/
```

Upload toàn bộ thư mục `build/` lên hosting.

---

# 📁 Cấu trúc dự án

```text
project/
 ├─ scss/        # SCSS source
 ├─ js/          # Javascript
 ├─ index.html
 ├─ build/       # Output production
 └─ package.json
```

---

# 🎯 Workflow chuẩn

```text
Code → npm run dev → Build → npm run build → Deploy build/
```

---

Happy coding 🚀

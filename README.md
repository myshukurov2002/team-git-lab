# 🚀 Advanced Git & GitHub

Bu kurs orqali siz Git va GitHub'ni professional darajada o'rganasiz va real proyektlarda ishlay olasiz.

---

## 📚 7kunlik Dars Reja

### 📅 1-DARS: Git Asoslari (Chuqur Nazariya)

#### 🎯 O'rganadigan Mavzular
- **Git nima va nima uchun ishlatiladi**
- **Local va Remote repository farqi**
- **3 ta asosiy zona tushunchasi:**
    - 📁 Working Directory
    - 🎭 Staging Area
    - 📦 Repository
- **HEAD pointer va commit navigation**
- **SHA-1 hash algoritmi va commit identifikatsiya**
- **.git papkasi ichki tuzilishi**

#### 💻 Amaliy Mashqlar

```bash
# Git repository yaratish
mkdir git-lab && cd git-lab
git init

# Fayl yaratish va o'zgartirish
touch hello.txt
echo "Hello Git" > hello.txt

# Git status va staging
git status
git add hello.txt
git commit -m "feat: add hello.txt file"

# Tarixni ko'rish
git log --oneline --graph --all
```

#### ⭐ Professional Tips
- **Conventional Commits** formatidan foydalaning: `feat:`, `fix:`, `docs:`, `refactor:`, `chore:`
- Har bir commit bitta mantiqiy o'zgarishni ifodalashi kerak
- Commit message'lar aniq va tushunarli bo'lishi shart

#### ⚠️ Keng Tarqalgan Xatolar
- `.git` papkasini tasodifan o'chirish - butun tarix yo'qoladi
- Barcha o'zgarishlarni bitta katta commit'ga birlashtirish
- Commit message'larni noaniq yozish

#### 🤖 ChatGPT bilan Mashq Promptlari

**Asosiy tushunchalar uchun:**
```
Sen Git bo'yicha o'qituvchisan. Menga Git'ning 3 ta asosiy zonasi (Working Directory, Staging Area, Repository) haqida savollar ber va javoblarimni baholab, xatolarimni tuzat. Har bir savol uchun real misol keltir.
```

**Commit yozish praktikasi:**
```
Menga har xil kod o'zgarishlarini taqdim et va men ular uchun Conventional Commits formatida commit message yozaman. Keyin sen mening yozganimni baholab, yaxshilash bo'yicha tavsiyalar ber.
```

**Tushunchalarni sinash:**
```
Git terminologiyasi bo'yicha menga 10 ta savol ber. Masalan: "HEAD nima?", "SHA-1 hash qanday ishlaydi?" kabi. Javoblarimni baholab, qo'shimcha tushuntirishlar ber.
```

### 📅 2-DARS: Branch'lar va Boshqarish Strategiyalari

#### 🎯 O'rganadigan Mavzular
- **Branch - bu faqat commit'ga pointer**
- **Merge vs Rebase fundamentallari**
- **Fast-forward va Non-fast-forward merge**
- **Branch naming conventions:**
    - `feature/user-authentication`
    - `fix/login-bug`
    - `release/v2.1.0`
- **Detached HEAD holati va echimi**

#### 💻 Amaliy Mashqlar

```bash
# Yangi branch yaratish va o'tish
git branch feature/login
git checkout feature/login
# yoki qisqa usul: 
git checkout -b feature/login

# O'zgarishlar kiritish
echo "Login Page Content" > login.txt
git add login.txt
git commit -m "feat: implement user login functionality"

# Main branch'ga qaytish va merge
git checkout main
git merge --no-ff feature/login

# Branch'ni tozalash
git branch -d feature/login
```

#### ⭐ Professional Tips
- **Merge** - tarixni saqlab qoladi, hamkorlikda ishlash uchun ideal
- **Rebase** - tarixni chiroyli va linear qiladi, shaxsiy branch'lar uchun
- Har doim `--no-ff` flag'ini ishlating team'da ishlashda

#### ⚠️ Keng Tarqalgan Xatolar
- Public branch'larda rebase ishlatish - tarixni buzadi
- Branch nomlarini noaniq qo'yish: `test1`, `branch2`
- Merge conflict'larni noto'g'ri hal qilish

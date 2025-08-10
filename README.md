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

#### 🤖 ChatGPT bilan Mashq Promptlari

**Branch strategiyalarini o'rganish:**
```
Sen Git workflow bo'yicha mentor bo'lib, menga turli xil loyiha senariylari taqdim et. Masalan: "E-commerce saytiga yangi to'lov tizimi qo'shish kerak" - va men qaysi branch strategiyasini tanlashim kerakligini so'ra. Javobimni baholab, alternativ yechimlar taklif et.
```

**Merge vs Rebase praktikasi:**
```
Menga Git tarixining turli holatlarini tasvirlab ber va men merge yoki rebase'dan qaysi birini tanlashim kerakligini so'ra. Har bir tanlash uchun sabab-natijalarni tushuntirib ber va xatolarimni to'g'irla.
```

**Conflict resolution simulyatsiya:**
```
Tasavvuriy merge conflict holatlarini yaratib ber va men ularni qanday hal qilishimni so'ra. Masalan, ikkita dasturchi bir xil faylning bir xil joyini o'zgartirgan holatlar. Mening yechimlarimni baholab, eng yaxshi amaliyotlarni ko'rsat.
```

### 📅 3-DARS: Remote Repository va GitHub Integration

#### 🎯 O'rganadigan Mavzular
- **Remote repository tushunchasi**
- **Origin nima va qanday ishlaydi**
- **Push, Pull, Fetch o'rtasidagi farqlar**
- **Remote tracking branch'lar**
- **Repository documentation:**
    - `.gitignore` optimizatsiyasi
    - `README.md` professional yozish
    - `LICENSE` tanlash

#### 💻 Amaliy Mashqlar

```bash
# Remote repository qo'shish
git remote add origin https://github.com/username/awesome-project.git

# Branch'ni track qilish bilan push
git push -u origin main

# Remote o'zgarishlarni olish
git pull origin main
# yoki
git fetch origin
git merge origin/main
```

#### ⭐ Professional Tips
- `.gitignore` faylini loyihaning boshidaoq sozlang
- README.md'da installation, usage, contributing guide bo'lishi shart
- Large file'lar uchun Git LFS dan foydalaning

#### ⚠️ Keng Tarqalgan Xatolar
- Katta binary file'larni repository'ga qo'shish
- .env va sensitive data'larni commit qilish
- Remote branch nomlarini local bilan chalkashtirib yuborish

#### 🤖 ChatGPT bilan Mashq Promptlari

**Remote repository tushuntiruv:**
```
Sen Git instructor bo'lib, menga remote repository ishlash jarayonini step-by-step tushuntir. Har bir qadamda (git remote add, git push, git pull, git fetch) nima sodir bo'layotganini batafsil so'zlab ber va amaliy misollar keltir.
```

**.gitignore optimizatsiya:**
```
Menga turli xil loyihalar (Node.js, Python, React, etc.) uchun .gitignore faylini qanday sozlashni o'rgat. Men loyiha turini aytsam, sen optimal .gitignore konfiguratsiyasini taklif et va har bir qatorni nima uchun qo'shganimizni tushuntir.
```

**Remote vs local farqlar:**
```
Git'da local va remote branch'lar o'rtasidagi farqlarni simulation qilib ko'rsat. Masalan, boshqalar origin/main'ga push qilgan, men esa local'da ishlayapman - bu holatda qanday sync qilishni o'rgat.
```

### 📅 4-DARS: Teamwork - Pull Request va Code Review

#### 🎯 O'rganadigan Mavzular
- **Pull Request lifecycle**
- **Code Review best practices:**
    - Comment va suggestion berish
    - Request changes vs Approve
- **Merge strategiyalari:**
    - Squash and Merge
    - Rebase and Merge
    - Create Merge Commit
- **Fork workflow va upstream management**
- **Protected branches va status checks**

#### 💻 Amaliy Mashqlar

```bash
# Repository'ni fork qilish va clone
git clone https://github.com/your-username/forked-repo.git
cd forked-repo

# Upstream qo'shish
git remote add upstream https://github.com/original-owner/repo.git

# Feature branch yaratish
git checkout -b feature/awesome-feature

# O'zgarishlar va commit
git add .
git commit -m "feat: add awesome new feature with tests"

# Fork'ga push
git push origin feature/awesome-feature

# GitHub'da Pull Request ochish
```

#### ⭐ Professional Tips
- PR description'da **nima** va **nega** o'zgarganini tushuntiring
- Small PR'lar (300 line'dan kam) tez review bo'ladi
- Draft PR'dan foydalaning WIP uchun

#### ⚠️ Keng Tarqalgan Xatolar
- 1000+ line'li katta PR ochish
- Review olmagan PR'ni merge qilish
- Conflicts'ni noto'g'ri resolve qilish

#### 🤖 ChatGPT bilan Mashq Promptlari

**Pull Request Review praktikasi:**
```
Sen senior developer bo'lib, menga Pull Request review jarayonini o'rgat. Turli xil kod o'zgarishlarini taqdim et va men ular uchun review comment'lari yozaman. Mening comment'larimni baholab, konstruktiv feedback berishni o'rgat.
```

**Team workflow simulyatsiya:**
```
4 nafar dasturchi jamoasi bilan ishlayotgan loyihani tasavvur et. Har birining turli feature'lari bor. Menga bu holatda qanday branch strategy, PR workflow va conflict resolution qilishni step-by-step ko'rsat.
```

**Code review etikasi:**
```
Menga yomon yozilgan Pull Request'larni ko'rsat va men ular uchun yaxshi review comment'lari yozishni mashq qilaman. Qanday qilib konstruktiv, yordam beruvchi va professional review yozishni o'rgat.
```

### 📅 5-DARS: Conflict Resolution va Advanced Operations

#### 🎯 O'rganadigan Mavzular
- **Merge conflict'lar va resolution strategies**
- **Git status, diff, mergetool usage**
- **Git stash - vaqtinchalik saqlash:**
    - `stash push`, `stash pop`, `stash list`
- **Git reset turlari:**
    - `--soft` - faqat HEAD'ni move qiladi
    - `--mixed` - staging area'ni tozalaydi
    - `--hard` - barcha o'zgarishlarni yo'q qiladi
- **Git revert vs cherry-pick**

#### 💻 Amaliy Mashqlar

```bash
# Stash bilan ishlash
git stash push -m "WIP: working on user profile"
git checkout main
# boshqa ishlar...
git checkout feature/profile
git stash pop

# Conflict'ni simulate qilish
git checkout -b conflict-test
echo "Version A" > conflict.txt
git add . && git commit -m "Version A"

git checkout main
echo "Version B" > conflict.txt  
git add . && git commit -m "Version B"

git merge conflict-test
# Manual resolution
git add conflict.txt
git commit -m "resolve: merge conflict in conflict.txt"
```

#### ⭐ Professional Tips
- `git reflog` - yo'qolgan commit'larni tiklash uchun
- Reset `--hard`'ni faqat local commit'larda ishlating
- Conflict resolution'da har ikki tomonni ham ko'rib chiqing

#### ⚠️ Keng Tarqalgan Xatolar
- Automatic merge qilishda logic'ni buzish
- Stash'ni pop qilishni unutish
- Reset --hard'ni public commit'larda ishlatish

#### 🤖 ChatGPT bilan Mashq Promptlari

**Advanced Git commands mashqi:**
```
Sen Git expert bo'lib, menga murakkab Git holatlarini berasan (masalan: "Commit qildim lekin noto'g'ri branch'da", "Fayl o'chirildi lekin kerak", "History'ni tozalamoqchiman"). Men ularni Git commands bilan hal qilishga harakat qilaman, sen yechimlarimni baholab, optimal yechimlarni ko'rsat.
```

**Conflict resolution master class:**
```
Turli xil merge conflict holatlarini yaratib ber: simple text conflicts, binary file conflicts, rename conflicts va boshqalar. Men ularni qanday hal qilishimni so'ra va har bir holatda eng yaxshi amaliyotni o'rgat.
```

**Git stash va reset strategiyalari:**
```
Menga Git stash va reset commandlarining turli use case'larini keltir. Qachon stash, qachon reset --soft/mixed/hard ishlatishni, real loyiha misollarida ko'rsat va mening qarorlarimni baholab takomillashtir.
```

### 📅 6-DARS: Team Workflow Strategiyalari

#### 🎯 O'rganadigan Mavzular
- **Git Flow** - traditional, feature-rich projects uchun
- **GitHub Flow** - continuous deployment uchun
- **Trunk-Based Development** - large teams uchun
- **Sprint-based branching strategy**
- **Release management va versioning**

#### 💻 Workflow Examples

**GitHub Flow Example:**
```bash
git checkout main
git pull origin main
git checkout -b feature/payment-integration
# development...
git push origin feature/payment-integration
# Create PR → Review → Merge → Deploy
```

**Git Flow Example:**
```bash
git checkout develop
git checkout -b feature/shopping-cart
# development...
git checkout develop
git merge --no-ff feature/shopping-cart
# Create release branch
git checkout -b release/v2.0.0
# Bug fixes only
git checkout main
git merge --no-ff release/v2.0.0
git tag v2.0.0
```

#### ⭐ Professional Tips
- Startup'lar uchun GitHub Flow tezroq va sodda
- Enterprise'da Git Flow stability beradi
- Release branch'da faqat bugfix va documentation

#### ⚠️ Keng Tarqalgan Xatolar
- Workflow'ni team'ga tushuntirmaslik
- Bir nechta strategiyani aralashtirib yuborish
- Hotfix'larni noto'g'ri branch'ga qilish

#### 🤖 ChatGPT bilan Mashq Promptlari

**Workflow decision making:**
```
Sen technical lead bo'lib, menga turli xil loyihalar taqdim et (startup, enterprise, open-source) va men har biri uchun Git workflow strategiyasini tanlashim kerak. Tanlashlarimni baholab, har bir loyiha turiga mos workflow'ni o'rgat.
```

**Team scenario simulation:**
```
10 nafar dasturchi, 3 ta product manager va 2 ta QA engineer bilan katta loyihani boshqarishni tasavvur et. Menga bu holatda Git Flow, GitHub Flow yoki boshqa strategiyalardan qaysi birini tanlashni so'ra va qarorimni substantiation qilishni o'rgat.
```

**Release management praktikasi:**
```
Menga turli xil release holatlarini taqdim et: hotfix kerak, feature freeze, parallel development va boshqalar. Men ular uchun Git strategy yozaman va sen optimal yechimlarni ko'rsatib, xatolarimni to'g'irlaysan.
```

### 📅 7-DARS: Automation - Hooks, Tags, CI/CD

#### 🎯 O'rganadigan Mavzular
- **Git tagging:**
    - Lightweight tags
    - Annotated tags
- **Git hooks automation:**
    - pre-commit - code quality check
    - pre-push - test running
- **GitHub Actions basics**
- **Semantic versioning (SemVer)**
- **Automated changelog generation**

#### 💻 Amaliy Mashqlar

```bash
# Tag yaratish va push
git tag -a v1.0.0 -m "🎉 First stable release"
git push origin v1.0.0

# Lightweight tag
git tag v1.0.1
git push origin v1.0.1

# Version ma'lumotini olish
git describe --tags --abbrev=0
```

**Pre-commit Hook Example:**
```bash
#!/bin/sh
# .git/hooks/pre-commit
npm run lint
if [ $? -ne 0 ]; then
  echo "❌ Linting failed. Fix errors before committing."
  exit 1
fi
echo "✅ Pre-commit checks passed!"
```

**GitHub Actions Workflow:**
```yaml
name: CI/CD Pipeline
on: [push, pull_request]
jobs:
  test:
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@v3
    - name: Run Tests
      run: npm test
```

#### ⭐ Professional Tips
- Annotated tag'lar release history uchun muhim
- Semantic versioning'dan foydalaning: MAJOR.MINOR.PATCH
- Automated testing CI/CD'da shart

#### ⚠️ Keng Tarqalgan Xatolar
- Tag yaratib remote'ga push qilmaslik
- Hook'larni noto'g'ri konfiguratsiya qilib workflow'ni buzish
- Version numbering'da consistency yo'q

#### 🤖 ChatGPT bilan Mashq Promptlari

**CI/CD pipeline design:**
```
Sen DevOps mentor bo'lib, menga turli xil loyihalar uchun (web app, mobile app, microservices) CI/CD pipeline'larni GitHub Actions orqali qanday sozlashni o'rgat. Men pipeline konfiguratsiyasini yozaman, sen optimize qilishga yordam ber.
```

**Git hooks automation:**
```
Menga turli xil loyiha holatlarini ber va men ular uchun kerakli Git hooks'larni yozishim kerak. Masalan: code quality check, test running, commit message validation. Mening hook'larimni baholab, xavfsizlik va samaradorlik bo'yicha tavsiyalar ber.
```

**Versioning va tagging strategiyasi:**
```
Turli xil loyihalar uchun (library, web app, API) semantic versioning va tagging strategiyasini qanday qo'llashni o'rgat. Men version numbering qarorlarini qabul qilaman, sen ularni baholab industry best practice'lar bilan taqqosla.
```

## 🎁 Bonus Materiallar

### 📦 Essential Templates

#### **Professional .gitignore**
```gitignore
# Dependencies
node_modules/
npm-debug.log*
yarn-debug.log*
yarn-error.log*

# Production builds
/dist
/build

# Environment variables  
.env
.env.local
.env.*.local

# IDE files
.vscode/
.idea/
*.swp
*.swo
*~

# OS files
.DS_Store
Thumbs.db

# Logs
*.log
logs/

# Database
*.db
*.sqlite
```

#### **README.md Template**
```markdown
# Project Name

Brief description of your project.

## 🚀 Installation

```bash
git clone https://github.com/username/project.git
cd project
npm install
```

## 📖 Usage

```bash
npm start
```

## 🧪 Testing

```bash
npm test
```
```
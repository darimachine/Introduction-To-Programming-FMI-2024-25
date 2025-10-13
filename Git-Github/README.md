# Въведение в Git и GitHub

Когато работите по проекти (дори сами), е важно да можете:
- да **запазвате история на промените**;
- да **се връщате назад** при грешки;
- да **работите в екип**, без да си пречите;
- да **тествате нови идеи**, без да “чупите” основния код;
- да **имате backup** на проекта

📝 Пример:  
Без Git — имате `main_v3_final_really_final.cpp`.  
С Git — имате чист `main.cpp`, а историята на промените е в репото.

---

## Основни понятия

| Термин | Обяснение |
|--------|-----------|
| **Git** | Система за контрол на версиите (version control), която работи локално на вашия компютър. |
| **GitHub** | Онлайн платформа за споделяне и съвместна работа върху Git проекти. |
| **Repository (репо)** | “Папка с памет” — съдържа кода и историята му. |
| **Staging area** | Буфер, в който добавяте промени, преди да ги запишете като commit. |
| **Commit** | “Snapshot” на промените по проекта в определен момент, с описание (commit message). |
| **Branch** | Паралелна версия на проекта ("разклонение") — позволява да работите по нови неща, без да пипате основния код (в main бранча). |
| **Merge** | Сливане на промени от един branch в друг. |
| **Remote** | Онлайн версия на вашето репо (например в GitHub). |
| **Push** | Изпращане на локалните промени към remote репото (GitHub). |
| **Pull** | Изтегляне на промени от remote репото към локалното. (обратната посока на Push) |
| **Fork** | Копие на чуждо репо във вашия GitHub акаунт. |
| **Pull Request (PR)** | Предложение за сливане на промени — често се ползва при екипна работа. |
| **Clone** | Изтегляне (клониране) на съществуващо репо, локално на вашия компютър. |
| **HEAD** | Показва към кой commit/branch в момента сте позиционирани. |

---

![Git diagram](https://assets.bytebytego.com/diagrams/0202-git-commands.png)

## 🧪 Основен workflow (примерен сценарий)

```bash
# 1. Създаваме ново локално репо
mkdir demo-git # Създаваме директория (или проект през някое IDE)
cd demo-git # Влизаме в директорията / проекта
git init # Създаваме локално git repository 

# 2. Добавяме някакъв файл и го комитваме
git status             # проверяваме състоянието на локалното git репозитори
git add main.cpp       # добавяме файла в staging area
git commit -m "Initial commit" # Правим commit

# 3. Правим промени във файла
git diff               # виждаме какво е променено
git add main.cpp
git commit -m "Added print message"

# 5. Качваме в GitHub
git remote add origin <URL на репото> # показваме на локалното репо към кое remote репозитори да сочи в GitHub
git push -u origin main # пращаме промените в GitHub
```

---

## Работа в екип (Fork + Pull Request)
1. Fork-нете чуждо репо в GitHub.  
2. Клонирайте fork-а локално:
   ```bash
   git clone https://github.com/<your-username>/<repo>.git
   ```
3. Създайте нов branch, направете промени и ги commit-нете.
4. Push-нете в GitHub:
   ```bash
   git push origin <branch-name>
   ```
5. В GitHub → “Compare & pull request” → създавате PR.

---

## 💬 Полезни команди

| Команда | Обяснение |
|---------|-----------|
| `git init` | Създава ново локално Git репо |
| `git clone <url>` | Клонира съществуващо репо |
| `git status` | Показва текущото състояние |
| `git add <file>` | Добавя файл към staging |
| `git add .` | Добавя всички промени |
| `git commit -m "..."` | Прави commit |
| `git log` | Показва историята на комитите |
| `git log --oneline --graph` | Историята в кратък и визуален вид |
| `git diff` | Показва разлики преди commit |
| `git branch` | Списък с branch-ове |
| `git checkout <branch>` | Превключва към branch |
| `git checkout -b <branch>` | Създава и превключва към нов branch |
| `git merge <branch>` | Слива друг branch в текущия |
| `git push` | Качва промените в remote |
| `git pull` | Изтегля промени от remote |
| `git fetch` | Изтегля промените от remote, без да ги слива |
| `git remote -v` | Показва remote URL-ите |
| `git reset --hard <commit>` | Връща проекта към даден commit (⚠️ внимателно) |
| `git stash` | Скрива текущите промени временно |
| `git stash pop` | Възстановява скритите промени |
| `git rebase` | Подрежда историята (по-напреднала команда) |

---

## 📚 Ресурси
- [Install Git](https://git-scm.com/downloads)
- [Install GitHub Desktop](https://desktop.github.com/download/) (цъкалка)
- [GitHub Docs](https://docs.github.com/en/get-started)  
- [Learn Git Branching (интерактивно)](https://learngitbranching.js.org/)  
- [Git Cheat Sheet](https://education.github.com/git-cheat-sheet-education.pdf)  
- [Git - Understandng the basics](https://medium.com/@onejohi/git-understanding-the-basics-ba004a20dacc)
---

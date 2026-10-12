# GitHub Branch және Pull Request практикалық жұмысы

Бұл — VS Code-та ашып, браузерде іске қосуға болатын дайын портфолио үлгісі. Файлдар: `index.html`, `style.css`, `script.js`.

## 1. VS Code-та ашу
1. ZIP файлын шығарып алыңыз.
2. VS Code → **File → Open Folder** → `github_branch_pr_practice` бумасын таңдаңыз.
3. `index.html` файлын браузерде ашыңыз. Қаласаңыз, VS Code-та Live Server кеңейтімін қолданыңыз.

## 2. GitHub репозиторийімен байланыстыру
Егер бұл буманы жаңа репозиторий ретінде жіберсеңіз, алдымен GitHub-та бос репозиторий құрыңыз. Содан кейін терминалда:

```bash
git init
git add .
git commit -m "Create portfolio website"
git branch -M main
git remote add origin https://github.com/USERNAME/REPOSITORY.git
git push -u origin main
```

`USERNAME/REPOSITORY` орнына өз репозиторийіңіздің мекенжайын қойыңыз. Егер жобаңызда Git бұрыннан қосылған болса, `git init` және `git remote add origin` командаларын қайта орындамаңыз.

## 3. Тақырып 3.1.30 — тармақ құру
```bash
git switch main
git pull origin main
git switch -c feature-contact
```

`index.html` файлына `id="contact"` бар байланыс бөлімін қосыңыз. Содан кейін:

```bash
git status
git add .
git commit -m "Add contact section"
git push -u origin feature-contact
```

Галерея тармағын тексеру:
```bash
git switch main
git switch -c feature-gallery
git add .
git commit -m "Add gallery section"
git push -u origin feature-gallery
```

Ескерту: екінші тармақты нақты орындау үшін `index.html` немесе `style.css` файлына жаңа өзгеріс енгізіңіз.

## 4. Тақырып 3.1.31 — Pull Request
1. GitHub-та репозиторийді ашыңыз.
2. **Pull requests → New pull request** таңдаңыз.
3. **Base: main**, **Compare: feature-contact** деп қойыңыз.
4. Тақырып: `Add contact section`.
5. Сипаттама: `Портфолиоға байланыс бөлімі қосылды. HTML құрылымы тексерілді.`
6. **Create pull request** басыңыз.
7. Өзгерістерді тексеріп, тапсырма талап етсе, **Merge pull request** таңдаңыз.
8. Соңында жергілікті негізгі тармақты жаңартыңыз:

```bash
git switch main
git pull origin main
```

## 5. Merge Conflict мысалы
Егер екі тармақта бір жол әртүрлі өзгертілсе, Git конфликт көрсетуі мүмкін. Файл ішінен `<<<<<<<`, `=======`, `>>>>>>>` белгілерін тауып, дұрыс HTML нұсқасын қалдырыңыз. Содан кейін:

```bash
git add index.html
git commit -m "Resolve merge conflict"
git push
```

## Есепке арналған қорытынды
Git тармақтары функцияларды бөлек әзірлеуге мүмкіндік береді. Pull Request кодты тексеріп, өзгерістерді негізгі тармаққа біріктіруге арналған. Конфликт пайда болса, қайшылықты қолмен шешіп, өзгерісті қайта тексеру қажет.

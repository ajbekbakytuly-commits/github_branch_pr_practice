# GitHub Branch және Pull Request практикалық жұмысы

Бұл — VS Code-та ашып, браузерде іске қосуға болатын дайын портфолио үлгісі.

## 1. Жоба файлдары

- `index.html` — сайттың HTML құрылымы
- `style.css` — сайттың стилі мен дизайны
- `script.js` — JavaScript функционалдығы

## 2. VS Code-та ашу

1. VS Code бағдарламасын ашыңыз.
2. **File → Open Folder** арқылы `github_branch_pr_practice` бумасын таңдаңыз.
3. `index.html` файлын браузерде ашыңыз немесе Live Server кеңейтімін пайдаланыңыз.

## 3. Git тармақтарын құру

Негізгі тармақты жаңартып, байланыс бөліміне арналған жаңа тармақ жасаңыз:

```bash
git switch main
git pull origin main
git switch -c feature-contact
```

Өзгерістерді сақтап, GitHub-қа жіберіңіз:

```bash
git add .
git commit -m "Add contact section"
git push -u origin feature-contact
```

## 4. Pull Request құру

1. GitHub-та репозиторийді ашыңыз.
2. **Pull requests → New pull request** бөліміне кіріңіз.
3. Base ретінде `main`, Compare ретінде `feature-contact` таңдаңыз.
4. **Create pull request** батырмасын басыңыз.
5. Өзгерістерді тексеріп, қажет болса, негізгі тармаққа біріктіріңіз.

## 5. Merge Conflict шешу

Егер конфликт пайда болса, файлдағы `<<<<<<<`, `=======`, `>>>>>>>` белгілерін алып тастап, дұрыс нұсқаны қалдырыңыз.

Содан кейін:

```bash
git add .
git commit -m "Resolve merge conflict"
git push
```

## Қорытынды

Git тармақтары жобаның әртүрлі функцияларын бөлек әзірлеуге мүмкіндік береді. Pull Request өзгерістерді тексеріп, негізгі тармаққа біріктіруге көмектеседі. Merge Conflict пайда болған жағдайда, қайшылықтарды қолмен шешіп, өзгерістерді қайта сақтау қажет.
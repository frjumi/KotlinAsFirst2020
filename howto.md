#Часть 1. Работа с моим репозиторием
1. Клонировала репозиторий https://github.com/frjumi/KotlinAsFirst2020 (git clone https://github.com/frjumi/KotlinAsFirst2020.git)
2. Открыла папку KotlinAsFirst2020 (cd KotlinAsFirst2020).
3. Указала в качестве upstream-my свой форк KotlinAsFirst2021 (git remote add upstream-my https://github.com/frjumi/KotlinAsFirst2021.git).
4. Проверила, всё ли добавилось (git remote -v).
5. Создала ветку backport (git branch backport).
6. С помощью fetch загрузила репозиторий локально (git fetch upstream-my).
7. Перешла в созданную ранее ветку (git checkout backport).
8. Перенесла коммиты с решениями (git cherry-pick d535f3592006b8f2593c9f881d72c05164aadc13...FETCH_HEAD).
9. Перешла в ветку master (git checkout master).

#Часть 2. Работа с репозиторием напарника

1. Указала в качестве upstream-their форк напарника (git remote add upstream-theirs https://github.com/Qustarnick/KotlinAsFirst2021.git).
2. git branch backport1.
3. git fetch upstream-theirs.
4. git checkout backport1.
5. git cherry-pick d535f3592006b8f2593c9f881d72c05164aadc13...FETCH_HEAD.
6. git checkout master.

#Часть 3. Слияние веток
1. git merge backport.
2. git merge backport1 -Xtheirs.

#Часть 4. добавление новых файлов
1. В IDE создаю файлы remotes.txt и howto.md.
2. В командной строке пишу команду (git remote -v), копирую информацию и добавляю в файл remotes.txt.
3. Заполняю файл howto.md.
4. Делаю коммит и пуш.
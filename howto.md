git clone https://github.com/ChaVi6/KotlinAsFirst2020.git cd KotlinAsFirst2020  
  
git remote add upstream-my https://github.com/ChaVi6/KotlinAsFirst2021.git  
git fetch upstream-my  
(добавляем upstream)  

git checkout -b backport  
(создаём и переходим в ветку backport)  

git cherry-pick d535f3592006b8f2593c9f881d72c05164aadc13...FETCH_HEAD  
(переносим все коммиты в эту ветку)  

git remote add upstream-theirs https://github.com/vloadka/KotlinAsFirst2021.git  
git fetch upstream-theirs  
(добавляем upstream партнёра)  

git checkout master  
git merge backport upstream-theirs/master  
(переходим в ветку master и мёрджим)  

(вручную исправляем все конфликты)  

git commit -m "go"  
git push  

git remote -v > remotes  
(создаём файл remotes и переносим туда всё, что выдаёт git remote -v)  

(создаём файл howto.md и записываем в него процесс работы)  
  
git add remotes  
git add howto.md  
(добавляем remotes и howto.md)  
  
git commit -m "win"
git push

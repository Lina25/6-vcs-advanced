1. Робота з бренчами
 -  створити бренчу "architecture" з "master",      переключитися в неї
  create new repository on GitHub - "6-vcs- advanced"
  
   git clone https://github.com/Lina25/6-vcs-advanced.git
   cd 6-vcs-advanced
   git branch architecture
   git checkout architecture
   (git checkout -b architecture - to create and switch to)
-  створити структуру в файловій системі
   mkdir assets
   mkdir uploads 
   echo "hello" > index.html  
   git status
   git add .
   git status
   git commit -m "add file structure"
   cd assets
   echo "" > all.js
   echo "" > css.js
   git status
   git add .
   git status
   git commit -m "add js files"
   git push origin architecture   

 зробити щоб ігнорилися всі файли з папки uploads/ (сама папка має бути в репозиторії)
   cd uploads
   echo '' > .keep
   git add .
   git commit -m "ignore"
   git push origin architecture
   echo "uploads/*\n !.keep" > .gitignore
   git add .
   git commit -m "gitignore file"
   git push origin architecture
   touch uploads/some.txt
   git add .
   git commit -m "file to be ignored"
   git push origin architecture
   git checkout master
   git merge architecture
   git branch -d architecture

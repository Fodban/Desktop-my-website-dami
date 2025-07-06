java -jar bfg.jar --delete-files '*' --no-blob-protection
git reflog expire --expire=now --all && git gc --prune=now --aggressive
rm -rf *
git add .
git commit -m "Remove all files and history"
git push --force --all

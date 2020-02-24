# Git Commands

migrating a directory into a new repository with history
http://blakesmith.me/2009/10/06/git-migrating-a-directory-into-a-new-repository-with-history.html

git clone --no-hardlinks b
git filter-branch --subdirectory-filter src/mylib HEAD
git reset --hard
git gc --aggressive
git prune
git filter-branch --tree-filter "rm -rf src/mylib" --prune-empty HEAD

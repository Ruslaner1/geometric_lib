git clone https://github.com/smartiqaorg/geometric_lib
cd geometric_lib
git checkout feature
git checkout develop
git checkout main
git merge develop --no --ff
git reset --hard HEAD^
git merge develop
git checkout release
git rebase -i main
gid add docs/README.md
git rebase --continue
git checkout main
git merge release
git remote remove origin
git remote add origin git@github.com:Ruslaner1/geometric_lib.git
git push origin --all 

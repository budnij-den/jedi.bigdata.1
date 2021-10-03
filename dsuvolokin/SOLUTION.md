git checkout -b airflow
git remote add https://github.com/apache/airflow.git

#here was a kind of mental eclipse and i didnt log my commands

git checkout -b fix
git revert 95f5b80542fc6259f333a426c13f1652fa5631b4
git revert ca97ca752bad4b793c24d574a2f434bb561e84cd

git remote rm airflow
git branch -d airflow
git checkout main && git push --force
git push --set-upstream origin fix
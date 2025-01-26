![image](https://github.com/user-attachments/assets/fcc8cbe4-20e1-4e8f-a88c-14385fb9b1f2)

```
$ git clone https://github.com/juintination/conflict-scenario.git
$ cd conflict-scenario/
$ touch resume.txt
$ touch personal_statement.txt
$ git add resume.txt
$ git commit -m "feat: add resume.txt"
$ git add personal_statement.txt
$ git commit -m "feat: add personal_statement.txt"

$ git branch sub1
$ git checkout sub1
$ vi resume.txt
$ git add resume.txt
$ git commit -m "chore: update resume.txt"

$ git checkout main
$ git branch sub2
$ vi personal_statement.txt
$ git add personal_statement.txt
$ git commit -m "chore: update personal_statement.txt"

$ git checkout main
$ vi resume.txt
$ git add resume.txt
$ git commit -m "chore: update resume.txt"
$ vi personal_statement.txt
$ git add personal_statement.txt
$ git commit -m "chore: update personal_statement.txt"

$ git merge sub1 # CONFLICT (content): Merge conflict in resume.txt
$ vi resume.txt
$ git commit -m "chore: merge resume.txt"
$ git merge sub1

$ git merge sub2 # CONFLICT (content): Merge conflict in personal_statement.txt
$ vi personal_statement.txt
$ git commit -m "chore: merge personal_statement.txt"
$ git merge sub2

$ git push
```

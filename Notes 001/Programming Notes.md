#### Useful Javascript / Js Libraries
Lodash: https://lodash.com/
D3: https://d3js.org/

#### Useful Python Libraries
pydash: https://pypi.org/project/pydash/ --- https://pydash.readthedocs.io/en/latest/
Pandas: https://pypi.org/project/pandas/ --- https://pandas.pydata.org/
matplotlib: https://pypi.org/project/matplotlib/ --- https://matplotlib.org/
seaborn: https://pypi.org/project/seaborn/ --- https://seaborn.pydata.org/
scikit-learn: https://pypi.org/project/scikit-learn/ --- https://scikit-learn.org/stable/
TensorFlow: https://pypi.org/project/tensorflow/ --- https://www.tensorflow.org/
PyTorch: https://pypi.org/project/torch/ --- https://pytorch.org/ (pip install torch torchvision torchaudio / pip3 install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cpu)
django: https://www.djangoproject.com/
flask: https://flask.palletsprojects.com/en/stable/
FastAPI: https://fastapi.tiangolo.com/

#### Express Js Security Best Practices
https://expressjs.com/en/advanced/best-practice-security.html

#### Creating Random Token Secret Key In Node Repl
```
require('crypto').randomBytes(64).toString('hex');
.exit
```

Hash / Cryptographic Algorithms:
- MD5: least secure, ultra fast, 32-bit, fast tagging
- SHA-256: secure, ultra fast, 64-bit, data integrity check
- bcrypt: password security, slow, low memory usage, web app passwords
- Argon2 (id): maximum security, slow, high memory usage, ultra secure app passwords

#### Nodemon Hot Reload
https://stackoverflow.com/questions/37979489/how-to-watch-and-reload-ts-node-when-typescript-files-change

#### Dataset: Databases For Lazy People (Python)
https://dataset.readthedocs.io/en/latest/

#### Creating A New Branch
```
git branch <new-branch>
```

#### Git Gui
lazygit (terminal)
SourceTree
GitKraken Desktop
SmartGit
GitHub Desktop
Git Cola
Gitg
Sublime Merge

#### Creating And Switching To The New Branch
```
git switch -c <new-branch>
git checkout -b <new-branch>
```

#### Switching To Another Branch
```
git switch <branch-name>
git checkout <branch-name>
```

#### Checkout To Origin Branch (Detached Head)
```
git checkout origin/develop
git switch -
```

#### Checkout To Certain Commit (Detached Head)
```
git checkout 2a4a4d7
```

#### Adding Changes
```
git add .
git add src/py/main.py
```

#### Committing Changes
```
git commit -m "<comment>"
```

#### Reverting Commit
```
git revert HEAD
git revert <commit_hash>
```

#### Change Local Commit
```
git commit --amend --no-edit
git push -f
git push origin <branch-name>
```

#### Change Local Commit Comment
```
git commit --amend
```

#### Git Undo Local Commit
```
git reset HEAD~
```
[ edit files as necessary ]
```
git add .
git commit -c ORIG_HEAD   (to reuse the old commit message)
```

#### Git Remove Untracked Files
```
git clean -xdf
```

#### Pushing Commit To Remote
```
git push origin <branch-name>
```

#### Rebase / Rebasing
```
git switch <parent-branch>
git pull origin <parent-branch>
git switch <child-branch>
git rebase origin/<parent-branch>
git push --force origin <child-branch> OR git push --force-with-lease origin <child-branch>
```

#### Pull Another Branch Without Switching:
```
git fetch origin <branch-name>:<branch-name>
git fetch origin rel_2_0:rel_2_0
```

#### Hint When Pulling A Branch
```
hint: You have divergent branches and need to specify how to reconcile them.
hint: You can do so by running one of the following commands sometime before
hint: your next pull:
hint:
hint:   git config pull.rebase false  # merge
hint:   git config pull.rebase true   # rebase
hint:   git config pull.ff only   	# fast-forward only
hint:
`hint: You can replace "git config" with "git config --global" to set a default`
`hint: preference for all repositories. You can also pass --rebase, --no-rebase,`
`hint: or --ff-only on the command line to override the configured default per`
hint: invocation.
```

#### Fetch And Merge Merge Pulled Branch
```
git fetch origin develop
git checkout origin/develop
git checkout develop
git merge develop origin/develop
```

#### Fetch Remote Branch Into New Local Branch
```
git fetch origin <remote_branch_name>
git checkout -b <local_branch_name> origin/<remote_branch_name>
```

#### List All Remote Branches
```
git branch -r
git branch -r -v
git ls-remote
git remote -v
git remote show [remote_name]
git branch -a. Shows all the local and remote branches.
```

#### Git Update/Change Remote Git Repository Url
```
git remote set-url origin https://github.com/your-username/repo-name.git
git remote set-url origin git@github.com:your-username/repo-name.git
```

#### Rename A Local Branch
```
git branch -m <new-branch-name>
git branch -m <current-branch-name> <new-branch-name>
```

#### Delete A Local Branch
```
git branch -D <target_branch_name>
```

#### Rename A Remote Branch
```
git push origin --delete <old-branch-name>
git push origin <new-branch-name>
git push origin -u <new-branch-name>
```

#### Init And Update Submodule
```
git submodule init
git submodule update
```

#### Using Git Diff
```
git diff develop..feature-branch -- src/py/app.py
git diff 5ee19847..89f6af10
git diff develop..origin/develop
git diff --cached
git diff --staged
```

#### Stash Changes, Drop Stash And Pop/Apply Stash
```
git stash
git stash list
git stash drop 0
git stash pop
git stash apply
git stash --patch   OR   git stash -p
```
It will prompt with this: (1/2) Stash this hunk [y,n,q,a,d,j,J,g,/,e,?]?
y: Stash the current hunk.
n: Don't stash the current hunk.
q: Quit the patch selection interface and discard all staged changes.
a: Stash all remaining hunks without further prompting.
d: Delete the current hunk from the staging area.
j: Move down to the next hunk.
J: Move down to the next hunk, skipping hunks that would be deleted.
g: Go to the hunk at the top of the patch.
/: Search for a specific pattern within the staged changes.
e: Edit the current hunk.
?: Print a help message summarizing the available options.

#### Git Tagging
```
git tag
git tag -l
git tag -l *-rc*
git tag -a v1.4
git tag -f v0.0.1
git tag -f v5.4.3+21 <commit-hash>
git log --pretty=oneline
git tag -a v1.2 15027957951b64cf874c3557a0f3547bd83b3ff6
git tag -a v1.4 -m "my version 1.4"
git push origin v1.4
git checkout v1.4
git push --tags
git tag -d v1.4
git fetch --tags
```

#### Git Other Commands
```
git config pull.rebase false  # merge
git config pull.rebase true   # rebase
git config pull.ff only   	# fast-forward only
git rm -r --cached package-lock.json    # remove from git repository
git add .
git commit -m 'Removing ignored files'
```

`You can replace "git config" with "git config --global" to set a default preference for all repositories. You can also pass --rebase, --no-rebase, or --ff-only on the command line to override the configured default per invocation.`

```
git merge --no-ff
git rebase
git rebase --reapply-cherry-picks  # to include skipped commits
```

```
git config advice.skippedCherryPicks false
git config --list
git config --list --show-origin
```

```
git reset --merge  // cancels the merge after conflicts have been resolved and staged
git merge --abort  // best used when you haven't yet resolved and staged the conflicts
git commit  // once all conflicts are resolved and staged
```


#### Compact/Vacuum Sqlite3 Database
```
sqlite3 /path/to/db/mydb.sqlite3 'VACUUM'
VACUUM table_name;
```
#### Vacuum;
```
PRAGMA auto_vacuum = FULL;
PRAGMA auto_vacuum = INCREMENTAL;  -- Set to auto compact database, but must be manually activated
VACUUM table_name INTO file_name
```
https://sqlite.org/lang_vacuum.html
```
for f in *.db; do sqlite3 $f 'VACUUM'; done
```

#### Sqlite3 Query/Queries
```
.table  -- show table names
PRAGMA table_info(<table_name);  -- show column names and types
```
`ctrl + D  -- exit`
```
.quit  --  exit
```

#### Save Sqlite Query Results To A Text File
If you only want to save a single query to a file, use the .once command.
The .once command specifies that the next query will be sent to the specified file. Any further queries will revert to the standard output (the console).

```
.headers on
.mode column
.once query_results.txt
SELECT * FROM Products;
```

#### Postgresql Auto Grant Select Privileges
```
ALTER DEFAULT PRIVILEGES IN SCHEMA public GRANT SELECT ON TABLES TO "task-ro";
```

#### Postgresql Docker Dump And Load Table
```
docker exec -t my-postgres-container pg_dump -U <your_pg_username> -d <your_pg_database_name> -t <table_name> > file.sql
cat file.sql | docker exec -i my-postgres-container psql -U <your_pg_username> -d <your_pg_database_name>
docker exec -i my-postgres-container psql -U <your_pg_username> -d <your_pg_database_name> < file.sql
```

#### Postgresql Docker Dump All Tables In Public Schema
```
for table in $(docker exec <container_name> psql -U <user_name>-d <database_name> -Atc "SELECT tablename FROM pg_tables WHERE schemaname='public'"); do
docker exec -t <container_name> pg_dump -U <user_name> -d <database_name> -t "$table" > "${table}.sql"
```
done

#### Mysql Docker Dump And Load Table
```
docker exec -t [project_name]-mysql-1 mysqldump -u [user_name] -p[password] [database_name] > [project_name]_20250804.sql
docker exec -t [project_name]-mysql-1 mysql -u [user_name] -p[password] [database_name] < [project_name]_20250804.sql
```

#### Self Contained Database Engines
SQLite3
DuckDB - For OLAP
LevelDB - Key-value storage
LiteDB - NoSQL (document-based)
H2 Database - Embedded database for Java
Firebird Embedded - Advanced SQL features
Berkeley DB - Embedded key-value

#### A Complete Guide To Css Grid
https://css-tricks.com/snippets/css/complete-guide-grid/
#### A Complete Guide To Flexbox
https://css-tricks.com/snippets/css/a-guide-to-flexbox/
#### Css Snippets
https://css-tricks.com/snippets/

#### Inspect Parquet Files In Command Line
https://pypi.org/project/parquet-tools/
`parquet-tools cat --json  hdfs://localhost/tmp/save/part-r-00000-6a3ccfae-5eb9-4a88-8ce8-b11b2644d5de.gz.parquet`

#### Scrcpy (Phone Screen Copy)
https://github.com/Genymobile/scrcpy

#### Node Js Related
https://github.com/nvm-sh/nvm
https://classic.yarnpkg.com/lang/en/docs/install/
#### Nvm Default / Node Js Default Version
```
nvm alias default 20.16.0
```

NODE JS ERROR: node is running secure mode, SSL connection required
```
set rejectUnauthorized to false
```
const pool = new Pool({ connectionString: databaseUrl, ssl: { rejectUnauthorized: false } })

#### To Generate A Random String For Secret Key, Run This Code In The Node Repl
```
require('crypto').randomBytes(64).toString('hex');
.exit
```

#### Install Latest Version Library
```
npm install typescript@latest ts-node@latest @types/node@latest --save-dev
```

#### Pnpm Store Libraries
pnpm store path
pnpm store prune

#### Pyenv Commands
pyenv install -l | grep 3.12
`pyenv shell <version> – modifies python for the current shell session`
`pyenv local <version> – modifies the python used in the current directory (or subdirectories)`
`pyenv global <version> – modifies the python used for your user account`

#### Python Create Virtual Environment
```
python -m venv my_env
```

#### Python Pip Remove All Packages
```
pip freeze | xargs pip uninstall -y
```

#### Python Code Style And Format
```
pip install flake8
```
flake8 main.py
```
pip install autopep8
```
autopep8 main.py
`autopep8 --in-place --aggressive main.py`

#### Flutter Commands
```
flutter emulators
flutter clean
flutter pub get
flutter pub add toastification
flutter pub remove toastification
flutter devices
flutter emulators
flutter emulators --launch <emulator id>
flutter emulators --create [--name xyz]
flutter run -d <emulator_id>
flutter config --jdk-dir "/Library/Java/JavaVirtualMachines/jdk-17.jdk/Contents/Home"
flutter config --jdk-dir ~/Apps/jdk-17.0.2.jdk/Contents/Home
flutter build apk --debug
flutter build apk --split-per-abi
flutter build apk
```

#### Flutter Change Application Id
```
flutter pub global activate rename
```
`rename setBundleId --value "com.kane.dealdiligence"`
```
flutter pub add dev:change_app_package_name
flutter pub run change_app_package_name:main com.kane.dealdiligence
```
Find for leftovers, search "com.example" in the project folder and replace manually, if any.

#### Flutter Repair Cached Packages
```
flutter pub cache repair
flutter pub cache remove <package_name>
```
Delete all cache:  flutter pub cache clear

#### Flutter Upgrade Packages
```
flutter pub upgrade
flutter pub upgrade --major-versions
```

#### Flutter Android Default Configuration File
/Users/user/Apps/flutter/packages/flutter_tools/gradle/src/main/groovy/flutter.groovy

#### Learn Cpp/C++
https://www.learncpp.com

#### Configuring Your Compiler
https://www.learncpp.com/cpp-tutorial/configuring-your-compiler-build-configurations/
https://www.learncpp.com/cpp-tutorial/configuring-your-compiler-choosing-a-language-standard/
https://www.learncpp.com/cpp-tutorial/configuring-your-compiler-warning-and-error-levels/
https://www.learncpp.com/cpp-tutorial/configuring-your-compiler-choosing-a-language-standard/

```
alias g++='g++ -ggdb -pedantic-errors -Wall -Weffc++ -Wextra -Wconversion -Wsign-conversion -std=c++17'
alias ge++='g++ -ggdb -pedantic-errors -Wall -Weffc++ -Wextra -Wconversion -Wsign-conversion -std=c++17 -Werror'
alias gcc='gcc -ggdb -pedantic-errors -Wall -Weffc++ -Wextra -Wconversion -Wsign-conversion -std=c++17'
alias gecc='gcc -ggdb -pedantic-errors -Wall -Weffc++ -Wextra -Wconversion -Wsign-conversion -std=c++17 -Werror'
```

g++ -c -I./source/includes main.cpp -o build/main.o
g++ -c -I./source/includes source/includes/add.cpp -o build/add.o
cd build
g++ -o main main.o add.o

#### Learn Assembly
https://github.com/0xAX/asm

#### Learn How To Use Neovim As An Ide
https://programmingpercy.tech/blog/learn-how-to-use-neovim-as-ide/

#### Neovim As Ide
https://www.lazyvim.org/

#### Vim Adjust Tab Size
:set tabstop=4
:set shiftwidth=4
:set expandtab

#### Android Studio Asset Studio Path
Android Studio.app/Contents/plugins/android/resources/images/asset_studio

OPEN API by SANTRIKODING
https://open-api.my.id/

#### Creating React App That Uses Javascript
https://github.com/remix-run/react-router-templates
`npx create-react-router@latest --template remix-run/react-router-templates/javascript my-react-router-app`

#### Setting Up A Php Development Environment With Docker
https://medium.com/@etearner/setting-up-a-php-development-environment-with-docker-06cc7396a858

Running Selenium Firefox Webdriver on WSL2
https://blog.henrypoon.com/blog/2020/09/27/running-selenium-webdriver-on-wsl2/
- Setup WSL2
- Install VcXsrv (https://sourceforge.net/projects/vcxsrv/)
Start it up with the the command line parameter “-ac”
- Install Firefox (https://support.mozilla.org/en-US/kb/install-firefox-linux)

```
sudo install -d -m 0755 /etc/apt/keyrings
```

```
wget -q https://packages.mozilla.org/apt/repo-signing-key.gpg -O- | sudo tee /etc/apt/keyrings/packages.mozilla.org.asc > /dev/null
```

`gpg -n -q --import --import-options import-show /etc/apt/keyrings/packages.mozilla.org.asc | awk '/pub/{getline; gsub(/^ +| +$/,""); if($0 == "35BAA0B33E9EB396F59CA838C0BA5CE6DC6315A3") print "\nThe key fingerprint matches ("$0").\n"; else print "\nVerification failed: the fingerprint ("$0") does not match the expected one.\n"}'`

```
echo "deb [signed-by=/etc/apt/keyrings/packages.mozilla.org.asc] https://packages.mozilla.org/apt mozilla main" | sudo tee -a /etc/apt/sources.list.d/mozilla.list > /dev/null
```

```
echo "deb [signed-by=/etc/apt/keyrings/packages.mozilla.org.asc] https://packages.mozilla.org/apt mozilla main" | sudo tee -a /etc/apt/sources.list.d/mozilla.list > /dev/null
```

```
sudo apt-get update && sudo apt-get install firefox
```

- Add this line to ashrc
```
export DISPLAY=$(ip route | awk '{print $3; exit}'):0
```

`- Download geckodriver (https://github.com/mozilla/geckodriver/releases) -- (make sure to get the Linux one and not the Windows one.`
- Put it in /usr/bin (or alternatively some other folder in your PATH)

Node PM2
```
npm install pm2@latest -g
pm2 start --name <app_name> app.js
pm2 list
pm2 logs app.js
pm2 info app.js
```

Regular Expression (Regex)
- Search the beginning of string: use caret ^
```
echo "hello something\!" | rg "^he"
```
- Search the end of string: use dollar sign $
```
echo "hello something\!" | rg "ing\!$"
```
- A dot represents one character:
```
echo "cat hat cat" | rg "c.t"
```
- A set of optional characters: use square brackets
```
echo "A B C D" | rg "[A-C]"
```
- Search all words with "at" that don't start with "c"
```
echo "cat bat mat" | rg "[^c]at"
```
- Parentheses are used to find a scope and a precedence of operators:
```
echo "gray graay groy grey" | rg "gr(a|e)y"
```
- Curly brackets are mainly for count
```
echo "AAAAA" | rg "A{3}"
echo "AAAAA" | rg "A{3,5}"
```
- Zero or one occurrences: use question mark
```
echo "color colour" | rg "colou?r"
```
- One or more occurrences: use plus sign
```
echo "color colour colouuur" | rg "colou+r"
echo "aaaaaaa ab a" | rg "a+"
```
- Wildcard, zero or more occurrences: use star sign
```
echo "color colour colouuur" | rg "colou*r"
echo "aaaaaaa ab a cc bbb" | rg "a*b"
```
- Search digits: use \d+
```
echo "Order 65764564 was shipped" | rg "\d+"
```
- Search words: use \w+
```
echo "hell\!o_world42\!....." | rg "\w+"
```
- For space: use \s
```
echo "hello  world" | rg "hello\s+world"
```
- Or operator: |
```
echo "cat dog mouse" | rg "cat|dog"
echo "gray grey" | rg "gr(a|e)y"
echo "color colour" | rg "col(o|ou)r"
```
- Find email addresses
```
echo "Contact us: omer@dotb.sh or admin@test.org" | rg -o '[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-z]{2,}'
```
- Enforce strong password
```
echo "thisisMYSUUPERSTRONGP@@@SSWORD123" | rg –pcre2 '^(?=.*[a-z])(?=.*[A-Z])(?=.*\d)(?=.*[@$!%*?&])[A-Za-z\d@$!%*?&]{8,}$'
```
- sed -E ‘s/pattern/replacement/flags’
```
echo "hello world\nnot hello\n" | sed -E 's/^hello/hi/'
```
- Masking numbers
```
echo "user123" | sed -E 's/[0-9]/#/g'
echo "a123 b9 c" | sed -E 's/[0-9]+/<NUM>/g'
```
- Replacing file extension
```
echo "/src/assets/logo.png" | sed -E 's#/src/assets/(.*)\.png#/assets/\1.webp#'
```

My VSCode Intalled Extensions
C/C++
C/C++ Extension
C/C++ Extension Pack
C/C++ Themes
C#
C# Dev Kit
CMake
CMake Tools
Dart
EditorConfig for VS Code
ESLint
Flutter
GitLens
JSON Formatter
Jupyter
Jupyter Cell Tags
Jupyter Keymap
Jupyter Notebook Renderers
Jupyter Slide Show
Markdown All in One
Parquet Explorer
Partial Diff
Pylance
Python
Python Debugger
Python Environments
Rainbow CSV
Remote - SSH
Remote - SSH: Editing Configuration Files
Remote Explorer
Tailwind CSS IntelliSense
Fitten Code: Faster and Better AI Assistant
Gemini Code Assist
GitHub Copilot
GitHub Copilot Chat

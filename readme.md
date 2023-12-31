# GIT TUTORIAL

1. Configure Git
   - git config --global user.name "tridotrong"
   - git config --global user.email "tri.dotrong@ncc.asia"
2. Initialize Git
   - git init -> Khởi tạo file .git
3. Git Adding New Files
   - git status -> Kiểm tra trạng thái file đã add hay chưa
4. Git Staging Environment
   - git add readme.md -> add file readme.md hoặc git add . -> để add all file
5. Git Commit
   - git commit -m "git-training" -> thêm các thông báo rõ ràng vào mỗi lần xác nhận để dễ dàng nhận biết
   - git log để xem lịch sử commit của mình
6. Git Push
   - git push -u origin dev -> push lên repository trên branch dev
7. Git Branch
   - git branch -> xem các branch đang có
   - git branch git-branch-test -> create branch git-branch-test
   - git checkout git-branch-test -> chuyển sang branch git-branch-test
8. Git Merge
   - git checkout <span style="color:red;">dev</span> -> chuyển sang nhánh chính cần merge
   - git git merge git-branch-test -> merge nhánh git-branch-test vào nhánh <span style="color:red;">dev</span>
   - git branch -d git-branch-test -> deleted branch git-branch-test
   - git push origin --delete git-branch-test -> delete branch git-branch-test trên origin
9. Merge Conflict
   - mở file và edit lại file

# GIT AND GITHUB

1. Git clone
   - git clone https://github.com/tridotrong/git-training -> clone 1 repository vào new directory
2. Git Pull from GitHub
   - // chỉnh sửa trên giao diện
   - // chỉnh sửa trên giao diện lần 2 -> test lại git fetch
   - // chỉnh sửa trên giao diện lần 3 -> test lại git fetch
   - git fetch origin - theo dõi những thông tin thay đổi mới từ branch của Remote repository về máy tính của bạn không hợp nhất với local repository
   - ### Với git fetch, bạn có thể theo dõi các commit người khác đã cập nhật lên server, đồng thời nắm bắt được những thông tin khác nhau giữa remote và local
   - git log origin/dev -> kiểm tra bằng cách xem lại log
   - git diff origin/dev -> xem những thay đổi 1 cách rõ ràng
   - ### git fetch origin + git merge origin/dev = git pull origin

# GIT ADVANCED

1. Git Ignore and .gitignore -> sử dụng khi bạn push code nhưng có những file không muốn push
   - git sẽ theo dõi các file được chỉ định trong .gitignore , tuy nhiên bản thân tệp .gitignore bị git theo dõi

# GIT UNDO

1. Git Revert -> là lệnh chúng tôi sử dụng khi chúng tôi muốn thực hiện một previous commit và thêm nó dưới dạng new commit, giữ nguyên log
   - Step 1: Find the previous commit:
     ![git revert step 1](https://www.w3schools.com/git/img_revert_part1.gif)
   - Step 2: Use it to make a new commit:
     ![git revert step 2](https://www.w3schools.com/git/img_revert_part2.gif)
   - git revert <commit-id>
2. Git reset -> là lệnh chúng ta sử dụng khi muốn di chuyển kho lưu trữ về previous commit , loại bỏ mọi thay đổi được thực hiện sau lần commit đó
   - Step 1: Find the previous commit:
     ![git reset step 1](https://www.w3schools.com/git/img_reset_part1.gif)
   - Step 2: Step 2: Move the repository back to that step:
     ![git reset step 2](https://www.w3schools.com/git/img_reset_part2.gif)
3. Git Amend -> sửa đổi commit gần đây nhất \
4. Git stash
   - stash all change : git stash
   - get the last change has been stashed : git pop

# rename branch đã push

- test

1. Rename branch
   - git checkout Task-46052
   - git branch -m Bug-46052
   - git push origin -u Bug-46052
   - git push origin --delete Task-460522
2. Git conflict
   - chưa tạo pull-request
     - git stash
     - git stash drop
     - git pull
   - đã tạo pull-request
     - git pull origin dev
     - edit file

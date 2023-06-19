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
9. Merge Conflict
   - mở file và edit lại file

# GIT AND GITHUB

1. Git clone
   - git clone https://github.com/tridotrong/git-training -> clone 1 repository vào new directory
2. Git Pull from GitHub
   - // chỉnh sửa trên giao diện
   - // chỉnh sửa trên giao diện lần 2 -> test lại git fetch
   - // chỉnh sửa trên giao diện lần 3 -> test lại git fetch
   - git fetch 

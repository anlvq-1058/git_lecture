- local 
  + working 
  + staging 
- remote
  + my 
  + root
- commit
  đưa code staging -> .git 
  + -m
    => tạo commit mới
  + --amend
    => không thêm commit - sử dụng commit hiện tại
  (*) 1 pull request / 1 commit 
  + git log --oneline
- Nguyên nhân
  + Vô ý: không biết
  + Cố ý: sử dụng commit -m nhiều lần
    .) create user
       tạo form - lưu kq vào db - viết validate 
          ok            ok            X
          C1            C2            X
  + checkout từ nhánh khác
    branch: master
      .) co chapter 3: done -> reviewing
          => chapter 4: có toàn bộ commit từ chapter 3 + chapter 4
      .) co chapter 4:
          code lại chapter 3
          làm chapter 4
- rebase gộp commit/code
  + git rebase -i HEAD~n (n=2)
  chapter 3 thay đổi code
  chưa cần cập nhập luôn ở chapter 4
  chapter 3 đc merged 
  + git pull origin master 
  + checkout chapter 4 
  + rebase master
  + có conflict
  + git add .
  + rebase --continue 
    rebase --abort
    rebase --skip

# Git Branch & Merge Strategy

## 📚 Directory
```
- jh_profile.md
- sh_profile.md
- README.md
```

## 📚 Branch Structure
```
main
├── seunghui
│   ├── try/fast-forward-merge
│   ├── try/squash-and-merge
├── try/3-way-merge
    └── try/rebase-merge
```

## 🛠 Merge Types & Usage
### ✅ Fast-forward merge
+ 사용 조건: `main`에 다른 변화가 없을 때
+ 특징: 브랜치가 main으로 단순히 이어 붙여짐
+ <b>적용 방법: 초기세팅 내용을 pull 해와서 처음 박승희 프로필 작성 후 try/fast-forward-merge -> seunghui로 merge함.</b>

### ✅ 3-way merge
+ 사용 조건: main에 이미 다른 커밋들이 존재하여 충돌 가능성이 있을 때
+ 특징: 공통 조상(commit)을 기준으로 3-way로 병합
+ <b>적용 방법: 박승희 프로필 변경 완료 & 박지환 프로필 변경 완료 이후 main에 머지할때 사용함 try/3-way-merge -> main으로 merge함.</b>

### ✅ Rebase merge
+ 사용 조건: main에 변화가 있지만 충돌 가능성이 없을 때
+ 특징: 커밋 내역이 깔끔하게 정리됨 (linear history)
+ <b>적용 방법: 박승희가 프로필 수정 이후 main에 merge했으나, 작업한 파일이 다르기에 박지환 브랜치를 머지할때 사용함 try/rebase-merge -> try/3-way-merge 으로 merge함.</b>

### ✅ Squash merge
+ 사용 조건: 커밋 내에 오류 수정, Fix 커밋 등이 많아 정리가 필요할 때
+ 특징: 여러 커밋을 하나의 커밋으로 합쳐서 머지
+ <b>적용 방법: 박승희 프로필 내에서 소개글 오타 수정이 빈번하게 일어나 커밋 내역이 많을 때 사용함</b>
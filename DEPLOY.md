# Deploy ขึ้น github.com/raisemfu-adt

## ครั้งแรก (สร้าง repo + เปิด Pages)

```bash
cd "/Users/prasarajakkaew/Desktop/My-Document/wiki/my-wiki/raw/02_NewGen/Batch_2_Planning/student-handbook"

git init
git add index.html README.md DEPLOY.md .gitignore
git commit -m "Add Batch 2 student handbook for GitHub Pages"

# สร้าง repo ภายใต้ org (ต้อง login gh และมีสิทธิ์ใน raisemfu-adt)
gh repo create raisemfu-adt/batch2-student-handbook --public --source=. --remote=origin --push
```

## เปิด GitHub Pages

1. ไปที่ **Settings → Pages** ของ repo `batch2-student-handbook`
2. Source: **Deploy from a branch**
3. Branch: **main** · Folder: **/ (root)**
4. Save

URL ที่ได้: `https://raisemfu-adt.github.io/batch2-student-handbook/`

## อัปเดตครั้งถัดไป

```bash
cd ".../student-handbook"
git add index.html
git commit -m "Update student handbook schedule"
git push
```

## ใส่ลิงก์ในอีเมลประกาศผล

```
คู่มือผู้เรียน: https://raisemfu-adt.github.io/batch2-student-handbook/
```

## หมายเหตุ

- **อย่า** push ไฟล์จาก `รายชื่อผู้สมัคร/` (ข้อมูลส่วนตัว)
- repo นี้มีเฉพาะ `index.html` + README — public ได้

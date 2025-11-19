
-[طراحی سیستم](https://www.mermaidchart.com/app/projects/54601f72-1cc0-4013-8064-c5c665071c8a/diagrams/67b5d5e6-5a78-4a3a-969e-7489b7c6ca66/share/invite/eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkb2N1bWVudElEIjoiNjdiNWQ1ZTYtNWE3OC00YTNhLTk2OWUtNzQ4OWI3YzZjYTY2IiwiYWNjZXNzIjoiRWRpdCIsImlhdCI6MTc2MzU2MjkzM30.K5Ba32ZzufEu2yVTgcL941pKDJ8uxPmkCQHSxQlmq70)


---
config:
  theme: redux
---
flowchart TB
    A(["ورود ب سیستم"]) --> B["نام کاربری"] & n27["خروج از سیستم"]
    B --> D["رمز عبور"]
    n1["ثبت نام کاربر"] --> n2["اطلاعات وارد کنید"] & n5["ثبت"] & n27
    n2 --> n4(["حساب کاربری جدید"]) & n5
    n4 --> n5
    D --> n6["ثبت"] & n7["فراموشی رمز"]
    n7 --> n6
    n8["مشاهده محصولات"] --> n9["جست وجو محصولات"] & n27
    n9 --> n10["دسته بندی محصولات"] & n11["قیمت"]
    n10 --> n11
    n11 --> n12["ثبت"]
    n13["ایجاد تسک"] --> n14["درخواست فروش"] & n15["درخواست خرید"] & n17["مشاهده تسک"] & n18["تعیین وضعیت تسک"] & n27
    n15 --> n16["ثبت"]
    n14 --> n16
    n18 --> n16
    n19["نظرات و امتیاز دهی"] --> n20["ایجاد نظر"] & n21["امتیاز دهی"] & n27
    n21 --> n22["ثبت"]
    n20 --> n22
    n23["مدیریت پروفایل"] --> n24["تغییر پروفایل"] & n25["ویرایش نام"] & n27
    n24 --> n26["ثبت"]
    n25 --> n26
    B@{ shape: rounded}
    n27@{ shape: rounded}
    D@{ shape: rounded}
    n1@{ shape: rounded}
    n2@{ shape: rounded}
    n5@{ shape: rounded}
    n6@{ shape: rounded}
    n7@{ shape: rounded}
    n8@{ shape: rounded}
    n9@{ shape: rounded}
    n10@{ shape: rounded}
    n11@{ shape: rounded}
    n12@{ shape: rounded}
    n13@{ shape: rounded}
    n14@{ shape: rounded}
    n15@{ shape: rounded}
    n17@{ shape: rounded}
    n18@{ shape: rounded}
    n16@{ shape: rounded}
    n19@{ shape: rounded}
    n20@{ shape: rounded}
    n21@{ shape: rounded}
    n22@{ shape: rounded}
    n23@{ shape: rounded}
    n24@{ shape: rounded}
    n25@{ shape: rounded}
    n26@{ shape: rounded}
    style A color:#000000
    style n27 stroke:#FFCDD2

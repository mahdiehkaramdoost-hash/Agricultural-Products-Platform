
-[طراحی سیستم](https://www.mermaidchart.com/app/projects/54601f72-1cc0-4013-8064-c5c665071c8a/diagrams/67b5d5e6-5a78-4a3a-969e-7489b7c6ca66/share/invite/eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkb2N1bWVudElEIjoiNjdiNWQ1ZTYtNWE3OC00YTNhLTk2OWUtNzQ4OWI3YzZjYTY2IiwiYWNjZXNzIjoiRWRpdCIsImlhdCI6MTc2MzU2MjkzM30.K5Ba32ZzufEu2yVTgcL941pKDJ8uxPmkCQHSxQlmq70)









``` mermaid



---
config:
  theme: redux
  layout: elk
---
flowchart TB
    A(["ورود ب سیستم"]) --> B["نام کاربری"]
    B --> D["رمز عبور"]
    n1["ثبت نام کاربر"] --> n2["اطلاعات وارد کنید"] & n5["ثبت کردن"]
    n2 --> n4(["حساب کاربری جدید"]) & n5
    n4 --> n5
    D --> n6["ثبت کردن"] & n7["فراموشی رمز"]
    n7 --> n6
    n8["مشاهده محصولات"] --> n9["جست وجو محصولات"]
    n9 --> n10["دسته بندی محصولات"] & n11["قیمت محصولات"]
    n10 --> n11
    n11 --> n12["ثبت کردن"]
    n13["ایجاد تسک"] --> n14["درخواست فروش"] & n15["درخواست خرید"]
    n15 --> n16["ثبت کردن"]
    n14 --> n16
    n19["نظرات و امتیاز دهی"] --> n20["ایجاد نظر"] & n21["امتیاز دهی"]
    n21 --> n22["ثبت کردن"]
    n20 --> n22
    n23["مدیریت پروفایل"] --> n24["تغییر پروفایل"] & n25["ویرایش نام"]
    n24 --> n26["ثبت کردن"]
    n25 --> n26
    n29(("خریدار")) --> n19 & n8 & A & n13
    n30(("فروشنده")) --> n1 & n23 & n13
    n28(("مدیر")) --> n30

    B@{ shape: rounded}
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
    n16@{ shape: rounded}
    n19@{ shape: rounded}
    n20@{ shape: rounded}
    n21@{ shape: rounded}
    n22@{ shape: rounded}
    n23@{ shape: rounded}
    n24@{ shape: rounded}
    n25@{ shape: rounded}
    n26@{ shape: rounded}
     A:::Sky
     B:::Sky
     D:::Sky
     n1:::Aqua
     n2:::Aqua
     n5:::Aqua
     n4:::Aqua
     n6:::Sky
     n7:::Sky
     n8:::Sky
     n9:::Sky
     n10:::Sky
     n11:::Sky
     n12:::Sky
     n13:::Aqua
     n14:::Aqua
     n15:::Aqua
     n16:::Aqua
     n19:::Sky
     n20:::Sky
     n21:::Sky
     n22:::Sky
     n23:::Aqua
     n24:::Aqua
     n25:::Aqua
     n26:::Aqua
     n29:::Sky
     n30:::Aqua
     n28:::Pine
    classDef Peach stroke-width:1px, stroke-dasharray:none, stroke:#FBB35A, fill:#FFEFDB, color:#8F632D
    classDef Ash stroke-width:1px, stroke-dasharray:none, stroke:#999999, fill:#EEEEEE, color:#000000
    classDef Rose stroke-width:1px, stroke-dasharray:none, stroke:#FF5978, fill:#FFDFE5, color:#8E2236
    classDef Pine stroke-width:1px, stroke-dasharray:none, stroke:#254336, fill:#27654A, color:#FFFFFF
    classDef Aqua stroke-width:1px, stroke-dasharray:none, stroke:#46EDC8, fill:#DEFFF8, color:#378E7A
    classDef Sky stroke-width:1px, stroke-dasharray:none, stroke:#374D7C, fill:#E2EBFF, color:#374D7C
    style A color:#000000

    
    
    ```
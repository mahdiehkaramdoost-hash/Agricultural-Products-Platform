




``` mermaid



sequenceDiagram
    participant Admin as مدیر سیستم
    participant Farmer as کشاورز
    participant Customer as خریدار

    %% فرایندهای کشاورز
    Farmer->>Admin: درخواست عضویت/ورود به سیستم
    Admin-->>Farmer: تایید/رد حساب کاربری
    Farmer->>Admin: ثبت اطلاعات محصول برای فروش
    Admin-->>Farmer: تایید/رد محصول (بررسی و مدیریت)
    Farmer->>Admin: دسته‌بندی و مدیریت محصولات
    Farmer->>Admin: مشاهده سفارشات ثبت‌شده

    %% فرایندهای خریدار
    Customer->>Admin: ثبت‌نام/ورود به سیستم
    Admin-->>Customer: تایید ورود
    Customer->>Admin: جستجو و مشاهده محصولات تایید شده
    Admin-->>Customer: نمایش لیست محصولات کشاورزی
    Customer->>Farmer: ارسال درخواست خرید محصول
    Farmer-->>Customer: تایید دریافت سفارش
    Customer->>Admin: پرداخت آنلاین سفارش
    Admin-->>Customer: تایید پرداخت و ثبت سفارش نهایی

    %% نظارت و گزارش‌دهی مدیر سیستم
    Admin->>Admin: نظارت بر تراکنش‌ها و گزارشات
    Customer->>Farmer: ثبت نظر و امتیازدهی بعد از خرید
    Farmer-->>Customer: مشاهده امتیاز و نظر خریدار

    %% سفارش و ارسال
    Admin-->>Farmer: اطلاع‌رسانی سفارش جدید و تایید پرداخت
    Farmer-->>Admin: تایید آماده‌سازی و ارسال محصول
    Admin-->>Customer: اطلاع‌رسانی وضعیت سفارش و ارسال
    
    ```
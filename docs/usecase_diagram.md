




``` 



``` sequenceDiagram

    participant Admin as مدیر سیستم
    participant Farmer as کشاورز
    participant Customer as خریدار

    %% فرآیندهای کشاورز
    Farmer->>Admin: درخواست عضویت/ورود به سیستم
    Admin-->>Farmer: تایید حساب کاربری
    Farmer->>Admin: ثبت محصول جدید (درخواست فروش)
    Admin-->>Farmer: تایید محصول و انتشار در لیست
    Farmer->>Admin: مدیریت و دسته‌بندی محصولات خود
    Farmer->>Admin: مشاهده سفارش‌های دریافتی

    %% فرآیندهای خریدار
    Customer->>Admin: ثبت‌نام/ورود به سیستم
    Admin-->>Customer: تایید ورود
    Customer->>Admin: جستجوی محصولات موجود
    Admin-->>Customer: نمایش لیست محصولات مورد تایید
    Customer->>Farmer: ثبت سفارش محصول
    Farmer-->>Customer: تایید دریافت سفارش
    Customer->>Admin: پرداخت آنلاین هزینه سفارش
    Admin-->>Customer: تایید پرداخت و نهایی‌سازی سفارش

    %% امتیاز و نظر
    Customer->>Farmer: ثبت امتیاز و نظر درباره محصول/فرایند خرید
    Farmer-->>Customer: مشاهده بازخورد مشتری

    %% عملکرد مدیر سیستم
    Admin->>Admin: نظارت بر تراکنش‌ها و کلیه سفارشات
    Admin->>Admin: تهیه و مشاهده گزارشات سیستمی

    ```
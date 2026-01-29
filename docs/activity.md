
``` mermaid



flowchart TD
    start@{shape: sm-circ, label: "شروع"} --> role{نقش کاربر؟}

    %% مسیر خریدار
    role -- "خریدار" --> CLogin["ورود/ثبت نام خریدار"]
    CLogin --> CPanel["ورود به پنل خریدار"]
    CPanel --> Search@{shape: lean-r, label: "جستجوی محصولات"}
    Search --> ViewProduct["مشاهده محصول"]
    ViewProduct --> PlaceOrder["ثبت سفارش خرید"]
    PlaceOrder --> PayOnline@{shape: lean-r, label:"پرداخت آنلاین"}
    PayOnline --> Rate["ثبت امتیاز و نظر"]
    Rate --> fin@{shape: dbl-circ, label: "پایان"}

    %% مسیر کشاورز
    role -- "کشاورز" --> FLogin["ورود/ثبت نام کشاورز"]
    FLogin --> FPanel["ورود به پنل کشاورز"]
    FPanel --> ProductManage["مدیریت محصولات"]
    ProductManage --> AddProduct["افزودن/دسته‌بندی محصول"]
    AddProduct --> SaleReq["ثبت درخواست فروش"]
    SaleReq --> FarmerOrders["مشاهده سفارشات"]
    FarmerOrders --> fin

    %% مسیر مدیر
    role -- "مدیر سیستم" --> LoginAdmin["ورود مدیر"]
    LoginAdmin --> AdminPanel["پنل مدیریت"]
    AdminPanel --> ViewReports@{shape: doc, label:"مشاهده گزارشات"}
    ViewReports --> MonitorTrans@{shape: cyl, label:"نظارت بر تراکنش‌ها"}
    MonitorTrans --> fin

    %% استایل‌ها (رنگ و پس‌زمینه)
    style start fill:#ecf6fb,stroke:#4682b4,stroke-width:3px
    style fin fill:#f9e79f,stroke:#b7950b,stroke-width:3px
    style role fill:#dfe3e6,stroke:#566573,stroke-width:2px
    style PlaceOrder fill:#d5f5e3,stroke:#145a32
    style Rate fill:#fdebd0,stroke:#b9770e

    %% توضیح برای مسیرها
    subgraph توضیحات [ ]
      direction TB
      شرح1["☑️ مسیر سبز: فرایند خریدار"]
      شرح2["☑️ مسیر آبی: فرایند کشاورز"]
      شرح3["☑️ مسیر زرد: مدیریت سیستم"]
    end



     ```
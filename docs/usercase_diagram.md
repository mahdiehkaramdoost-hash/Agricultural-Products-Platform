



``` mermaid



flowchart TB
    %% نقش‌ها با رنگ مجزا
    Farmer@{ icon: "fa:tractor", shape: "circle", label: "کشاورز" }
    Customer@{ icon: "fa:user", shape: "circle", label: "خریدار" }
    Admin@{ icon: "fa:user-shield", shape: "circle", label: "مدیر سیستم" }

    %% یوزکیس‌های کشاورز
    subgraph بخش_کشاورز[" "]
    F1[مدیریت محصولات]
    F2[ثبت فروش محصول]
    F3[مشاهده سفارشات]
    end

    %% یوزکیس‌های خریدار
    subgraph بخش_خریدار[" "]
    C1[جستجوی محصول]
    C2[ثبت سفارش]
    C3[پرداخت آنلاین]
    C4[ثبت امتیاز و نظر]
    end

    %% یوزکیس‌های مدیر
    subgraph بخش_مدیر[" "]
    A1[نظارت بر تراکنش‌ها]
    A2[بررسی گزارشات]
    A3[مدیریت کاربران]
    end

    %% یوزکیس مشترک
    Register[ورود/ثبت‌نام]

    %% ارتباط نقش‌ها به یوزکیس‌ها
    Farmer --> Register
    Farmer --> F1
    Farmer --> F2
    Farmer --> F3

    Customer --> Register
    Customer --> C1
    Customer --> C2
    Customer --> C4

    Admin --> A1
    Admin --> A2
    Admin --> A3

    %% روابط include و extend
    C2 -->|include| C3
    C2 -.->|extend| C4

    %% موقعیت و چینش
    Register -.-> F1
    Register -.-> C1

    %% رنگ‌بندی کلاس‌ها
    classDef farmer fill:#eafbea,stroke:#27ae60,stroke-width:2px,color:#145a32;
    classDef customer fill:#e8f6ff,stroke:#2980b9,stroke-width:2px,color:#154360;
    classDef admin fill:#fbeee6,stroke:#e37e18,stroke-width:2px,color:#633700;
    classDef usecaseFarmer fill:#dcffe4,stroke:#16a34a;
    classDef usecaseCustomer fill:#e8fafe,stroke:#249aca;
    classDef usecaseAdmin fill:#fff0d6,stroke:#e67e22;
    classDef joincase fill:#f5f5f5,stroke:#434343;

    class Farmer farmer;
    class F1,F2,F3 usecaseFarmer;

    class Customer customer;
    class C1,C2,C3,C4 usecaseCustomer;

    class Admin admin;
    class A1,A2,A3 usecaseAdmin;

    class Register joincase;

    ```
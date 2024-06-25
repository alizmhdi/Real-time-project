### گزارش شبیه‌سازی پروتکل‌های اشتراک منابع

#### مقدمه
در این گزارش، ما دو پروتکل مهم اشتراک منابع در سیستم‌های چندپردازشی، یعنی MSRP (Multiprocessor Stack Resource Policy) و MrsP (Multiprocessor Resource Sharing Protocol) را مورد بررسی قرار داده و شبیه‌سازی انجام شده برای ارزیابی این پروتکل‌ها را ارائه می‌دهیم. این شبیه‌سازی‌ها شامل تولید وظایف مصنوعی، تخصیص منابع به وظایف و ارزیابی زمان‌بندی وظایف با استفاده از الگوریتم EDF (Earliest Deadline First) می‌باشد. همچنین برای نگاشت وظایف به پردازنده‌ها از الگوریتم WFD (Worst Fit Decreasing) استفاده شده است.

#### پروتکل‌های اشتراک منابع

##### پروتکل MSRP
پروتکل MSRP برای مدیریت انسداد وظایف در سیستم‌های چندپردازشی طراحی شده است. در این پروتکل، زمانی که یک وظیفه به دلیل دسترسی به یک منبع دچار انسداد می‌شود، سایر وظایف در همان پردازنده نیز متوقف می‌شوند. این امر باعث می‌شود که وظیفه انسداد شده بدون هیچ‌گونه تداخل زمانی که منبع مورد نیازش آزاد شد، به اجرای خود ادامه دهد.

##### پروتکل MrsP
پروتکل MrsP برای بهبود عملکرد پروتکل MSRP طراحی شده است. در این پروتکل، زمانی که یک وظیفه به دلیل دسترسی به یک منبع دچار انسداد می‌شود، سایر وظایف در همان پردازنده می‌توانند به اجرای خود ادامه دهند. این امر باعث افزایش بهره‌وری پردازنده‌ها می‌شود.

#### الگوریتم‌های زمان‌بندی و نگاشت وظایف

##### الگوریتم EDF
الگوریتم EDF یکی از معروف‌ترین الگوریتم‌های زمان‌بندی در سیستم‌های بلادرنگ است. در این الگوریتم، وظیفه‌ای که نزدیک‌ترین مهلت (deadline) را دارد، برای اجرا انتخاب می‌شود. این الگوریتم سعی می‌کند وظایف را به گونه‌ای زمان‌بندی کند که هیچ وظیفه‌ای مهلت خود را از دست ندهد.

##### الگوریتم WFD
الگوریتم WFD برای نگاشت وظایف به پردازنده‌ها استفاده می‌شود. در این الگوریتم، وظایف براساس زمان اجرای بدترین حالت (WCET) مرتب شده و سپس به پردازنده‌ای تخصیص داده می‌شوند که کمترین استفاده را دارد. این الگوریتم سعی می‌کند بار پردازنده‌ها را به طور یکنواخت توزیع کند.

#### شبیه‌سازی

##### تولید وظایف مصنوعی با الگوریتم Uunifast
برای تولید وظایف مصنوعی، از الگوریتم Uunifast استفاده می‌کنیم که نرخ استفاده (utilization) وظایف را به طور تصادفی تولید می‌کند. سپس براساس این نرخ استفاده، دوره‌های زمانی (period) و زمان اجرای بدترین حالت (WCET) وظایف تعیین می‌شوند.

##### تولید منابع و تخصیص به وظایف
منابع به طور تصادفی تولید شده و به وظایف تخصیص داده می‌شوند. هر وظیفه به یک منبع تخصیص داده می‌شود که باید برای اجرای وظیفه مورد استفاده قرار گیرد.

### نتایج
در این شبیه‌سازی، پروتکل‌های MSRP و MrsP با استفاده از مجموعه وظایف مصنوعی و منابع تخصیص داده شده به آن‌ها مورد ارزیابی قرار گرفتند. نتایج این ارزیابی نشان داد که پروتکل MrsP با اجازه دادن به وظایف دیگر برای اجرا در زمان انتظار مشغول، بهره‌وری پردازنده‌ها را افزایش می‌دهد.

### نتیجه‌گیری
پروتکل‌های اشتراک منابع در سیستم‌های چندپردازشی نقش حیاتی در بهبود عملکرد و بهره‌وری این سیستم‌ها دارند

. پروتکل MrsP با مدیریت بهینه‌تر زمان انتظار مشغول، می‌تواند عملکرد بهتری نسبت به پروتکل MSRP ارائه دهد. این شبیه‌سازی نشان داد که استفاده از پروتکل MrsP می‌تواند منجر به افزایش بهره‌وری پردازنده‌ها و کاهش زمان انتظار وظایف شود.

### کارهای آینده

در ادامه‌ی کار باید نکات دقیق‌تر زمان‌بندی‌ها را پیاده‌سازی کرد و همچنین نمودارهای زمان‌بند‌پذیری را اضافه کرد تا بتوانیم به مقایسه کامل این دو پروتکل بپردازیم.
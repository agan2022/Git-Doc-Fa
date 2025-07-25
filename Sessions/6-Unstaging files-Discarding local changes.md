## خارج کردن فایل‌ها از حالت Stage (Unstaging files)

```bash
$ git reset -- file.txt
```

گاهی ممکن است در کد خود مشکلی داشته باشیم و بخواهیم فایل‌ها را از staging area خارج کنیم؛ به عبارت دیگر می‌خواهیم تغییرات را بازگردانیم.
برای این کار می‌توانیم از دستور زیر استفاده کنیم:

```bash
$ git restore --staged file.txt
```
اکنون اگر بررسی کنید، فایل `file.txt` از staging area خارج شده است.

## بازگرداندن تغییرات محلی (Discarding local changes)

```bash
$ git restore file.txt
```

اما برای فایل‌هایی که هنوز ردیابی نشده‌اند (untracked files) باید به شکل زیر عمل کنیم:

```bash
$ git clean -fd
```

- `-f` : اجرا با اجبار (force)
- `-d` : حذف کل پوشه‌ها (remove whole
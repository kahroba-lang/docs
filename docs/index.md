
## گرفتن ورودی
به وسیله دستور input میتوان یک رشته را از کاربر به عنوان ورودی دریافت کرد:
```rust
name = input("What is your name:")
print("Hello, ",name)
```
## تعریف فانکشن
فانکشن ها در زبان کهربا به وسیله کلمه کلیدی fn تعریف میشوند.
فانکشن های میتوانند مقداری باز گردانند یا باز نگردانند.
بصورت پیش فرض آخرین دستور یک فانکشن برگردانده میشود و استفاده از کلمه return اختیاری است

```rust
fn sum(a,b) {
    a+b
}
```
توابع میتوانند بصورت بازگشتی فراخوانی شوند. پیاده سازی مثال کلاسیک فاکتوریل:
```rust
fn f(n) {
    if n <= 1 { 1 }
    n * f(n-1)
}

println(f(5)) // 120
```
ورودی فانکشن میتواند از هر نوعی باشد حتی یک فانکشن دیگر:

    fn getName() {
        "Kahroba"
    }
    fn hello(name) {
        println("Hello ",name)
    }
    hello(getName())

خروجی:

    Hello Kahroba

## swap
توسط این فانکشن میتوانید مقدار دو متغیر را باهم عوض کنید
```rust
a = 5
b = 10
println(a,b)
swap(a,b)
println(a,b)
```
خروجی
```bash
5 10
10 5
```
# کنترل جریان برنامه
## دستورات شرطی
به وسیله دستور if میتوان از دستورات شرطی استفاده کرد
```rust
if a + b > c {
    print("OK")
}
```

همچین میتوان از دستور else برای زمان عدم صحت شرط استفاده کرد
```rust
if a + b > c {
    print("OK")
} else {
    print("Not OK")
}
```

## حلقه تکرار
برای استفاده از حلقه در زبان کهربا از دستور for به شکل زیر استفاده میشود
```rust
for i in 1..5 {
    println(i)
}
```
خروجی:

    1
    2
    3
    4
    5

میتوانید تعداد گام های حلقه را به این شکل مشخص کنید:
```rust
for i in 1..5:2 {
    println(i)
}
```
خروجی:

    1
    3
    5

به وسیله حلقه for میتوانید به روی رشته ها، آرایه ها و مپ ها پیمایش انجام دهید
### پیمایش رشته
```rust
for s in "Hello World" {
    print(s," ")
}
```
خروجی
```bash
H e l l o  W o r l d
```
### پیمایش آرایه
```rust
arr = ["Kahroba","version",0.1]
for v in arr {
    print(v)
}

for i,v in arr {
    println(i,":",v)
}
```

خروجی
```bash
Kahroba version 0.1

0:Kahroba
1:version
2:0.1
```
### پیمایش مپ
```rust
data = {"name":"Kahroba","version":0.1}
for v in data {
    println(v)
}

for k,v in data {
    println(k,":",v)
}
```
خروجی
```bash
Kahroba
0.1

name : Kahroba
version : 0.1
```

### فراخوانی فایل های کهربا خارجی
با استفاده از زبان کهربا همچنین می توانید از سایر فایل های .krb که به زبان کهربا نوشته شده است استفاده کنید. 

```rust 
import("helper.krb")
```

تمامی فانکشن ها و متغیرهای تعریف شده در فایل helper.krb در اسکوپ جاری برنامه قابل دسترس خواند بود.


## پیاده سازی الگوریتم quicksort توسط کهربا
```rust
fn qsort(arr) {
    sort(arr,0,len(arr)-1)
}

fn sort(arr,l,r) {
    if l < r {
        q = partition(arr,l,r)
        sort(arr,l,q-1)
        sort(arr,q+1,r)
    }
}

fn partition(arr,l,r)  {
    i = l
    for j in l..r {
        if a[j] < a[r] {
            swap(a[i],a[j])
            i = i + 1
        }
    }
    swap(a[i],a[r])
    i
}


a = [5,1,2,4,3,9,8,7,6,0]

println(a)
qsort(a)
println(a)
```
خروجی

```bash
[5 1 2 4 3 9 8 7 6 0]
[0 1 2 3 4 5 6 7 8 9]
```
> [مثال های بیشتر](/examples/)

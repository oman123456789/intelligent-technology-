# ⚡ PowerGuard Pro

تطبيق مراقبة كهربائية يعمل مع Arduino + PZEM-004T + HC-05/06

## كيفية الاستخدام

### رفع الموقع على GitHub Pages
1. ارفع جميع الملفات على GitHub repository
2. فعّل GitHub Pages من Settings
3. افتح الرابط من أي جهاز

### كود الأردوينو - إضافة إرسال البيانات
أضف هذا في نهاية processPZEM() بعد نجاح القراءة:

```cpp
Serial.print(F("{\"V\":"));  Serial.print(rawV,1);
Serial.print(F(",\"A\":"));  Serial.print(rawA,2);
Serial.print(F(",\"W\":"));  Serial.print(rawW,0);
Serial.print(F(",\"F\":"));  Serial.print(rawFreq,1);
Serial.print(F(",\"PF\":")); Serial.print(rawPF,2);
Serial.print(F(",\"E\":"));  Serial.print(rawEnergy,3);
Serial.println(F("}"));
```

### التثبيت كتطبيق
- **Android**: Chrome ← ⋮ ← إضافة إلى الشاشة الرئيسية
- **iPhone**: Safari ← مشاركة ← إضافة إلى الشاشة الرئيسية  
- **PC**: Chrome ← أيقونة التثبيت في شريط العنوان

### ملاحظة iPhone
استخدم تطبيق Bluefy من App Store بدل Safari لدعم البلوتوث

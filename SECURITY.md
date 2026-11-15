# سياسة الأمان / Security Policy

> الحالة: مرحلة الوثائق — لا كود يعمل بعد. هذه السياسة مسودة تُفعَّل مع أول نشر.

## الإبلاغ عن ثغرة
- استخدم **Private vulnerability reporting** في تبويب Security بمستودع GitHub (يُفعَّل من إعدادات المستودع). **لا تفتح Issue عامًا** لثغرة.
- اذكر: الوصف، خطوات إعادة الإنتاج، الأثر المتوقع. لا ترسل بيانات حقيقية لزبائن.
- نردّ على أمل خلال أيام قليلة؛ لا نلتزم بمهلة رسمية بعد (لم يُحدَّد).

## القواعد الداخلية
انظر `AGENTS.md` §3: لا أسرار في الكود، تحقق على الخادم، RBAC على الخادم، توقيع Webhooks، لا بيانات شخصية في السجلات. اكتشاف سرّ مسرَّب ⇒ **أوقف وأبلغ المالك فورًا ودوّر السر**.

## ما لا يغطيه هذا المستودع
بيانات الإنتاج لا تدخل المستودع أبدًا.

---
**English:** Please report vulnerabilities privately via GitHub's "Report a vulnerability" (Security tab). Do not open a public issue. This project is pre-code; no supported versions yet.

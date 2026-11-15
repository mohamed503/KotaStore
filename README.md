# KotaStore

> **الحالة: 🚧 قيد البناء — مرحلة الأساس (وثائق فقط، v5). لا يوجد كود تطبيق بعد، ولا شيء مُختبر.**

**KotaStore** متجر إلكتروني عربي أولًا، مربوط بمنظومة مبيعات ومحاسبة متكاملة: أصناف بمتغيراتها (مقاس/لون)، أسعار شراء وبيع، مخزون، نظام محاسبي بقيد مزدوج، مناديب توصيل بشاشة خاصة (مسح باركود الطلب بكاميرا الهاتف أو إدخال الكود)، وتأكيد الطلبات عبر واتساب (يدويًا أو تلقائيًا عبر WhatsApp API)، ونقطة بيع، ومخازن وفروع متعددة، وتتبع GPS للمناديب، وداشبورد وتقارير مفصلة، ونسخ احتياطي، وبوت ردود، مع إدخال مصاريف الإعلانات الممولة (فيسبوك/إنستغرام) في الدورة المحاسبية.

## الهدف
تشغيل المتجر كله من نظام واحد: من الإعلان، إلى الطلب، إلى التأكيد، إلى التوصيل، إلى القيد المحاسبي، إلى تقرير الربح الحقيقي لكل منتج وحملة.

## الفكرة في سطرين
1. الزبون يجمع سلته ويقدّم الطلب → **يُحجز المخزون له فورًا** حتى لا يُباع لغيره → تصله رسالة واتساب للتأكيد.
2. بعد التأكيد يُجهَّز الطلب ويستلمه المندوب بمسح باركوده → عند التسليم وتحصيل المبلغ تُسجَّل القيود المحاسبية تلقائيًا.

## التقنيات (مقترحة، بانتظار الموافقة — انظر `docs/adr/`)
**أول عمل: تجربة جدوى المكدس المجاني (المرحلة 1A) قبل اعتماد أي قرار تقني.**

Next.js · TypeScript (strict) · Tailwind CSS · shadcn/ui · PostgreSQL (Neon) · استضافة سحابية مجانية (Cloudflare) · العملة: دينار ليبي + دولار بسعر صرف متغير · واجهة RTL أولًا (عربي) مع الإنجليزية بضغطة زر · متجاوب بالكامل مع الجوال.

## خريطة الوثائق
| الملف | المحتوى |
|---|---|
| [`docs/PRD.md`](docs/PRD.md) | المتطلبات: من المستخدم، ماذا يفعل المشروع وما لا يفعله |
| [`docs/ARCHITECTURE.md`](docs/ARCHITECTURE.md) | أجزاء المشروع وكيف تتصل |
| [`docs/adr/`](docs/adr/) | قرار معماري لكل خيار كبير: الخيارات والسبب |
| [`docs/ROADMAP.md`](docs/ROADMAP.md) | المراحل وشروط النجاح |
| [`docs/TESTING.md`](docs/TESTING.md) | الاختبار الآلي + الاختبار اليدوي للمالك |
| [`docs/DATA-MODEL.md`](docs/DATA-MODEL.md) | مسودة نموذج البيانات (للمراجعة قبل المرحلة 2) |
| [`docs/ACCOUNTING-CHART.md`](docs/ACCOUNTING-CHART.md) | دليل الحسابات وقواعد الترحيل المقترحة (لمراجعة محاسب) |
| [`docs/UX-FLOWS.md`](docs/UX-FLOWS.md) | تدفقات المستخدم وهياكل الشاشات الأولية |
| [`docs/SEO.md`](docs/SEO.md) | خطة SEO والمشاركة الاجتماعية |
| [`docs/SEED-DATA.md`](docs/SEED-DATA.md) | مواصفات البيانات التجريبية |
| [`docs/REVIEW-2026-11-15.md`](docs/REVIEW-2026-11-15.md) | مراجعة الأساس: ما وُجد وما عُدِّل وما ينتظر قرارك (ملحق v5: مراجعة المبيعات والتكامل) |
| [`docs/adr/0032-sales-accounting-operations-integration.md`](docs/adr/0032-sales-accounting-operations-integration.md) | **v5:** تكامل المبيعات والمحاسبة والتشغيل |
| [`SECURITY.md`](SECURITY.md) | الإبلاغ عن الثغرات |
| [`AGENTS.md`](AGENTS.md) | قواعد العمل لأي وكيل/مطوّر يبني المشروع |

## الرخصة
**مقترحة: AGPL-3.0-or-later (بانتظار الموافقة)** — انظر `docs/adr/0013-license.md`. لن يُضاف ملف `LICENSE` قبل موافقتك.

---

### English summary
KotaStore is an Arabic-first (RTL), fully responsive e-commerce store tied to a professional sales & double-entry accounting system, with variant-aware inventory, delivery-courier PWA (barcode scan / code entry), WhatsApp order confirmation (manual + WhatsApp Cloud API), and ad-spend accounting. Status: **under construction — documentation phase only; nothing is tested yet.**

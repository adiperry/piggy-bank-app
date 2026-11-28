# 🐷 קופת חיסכון לילדים — Piggy Bank for Kids

אפליקציית קופת חיסכון בעברית (RTL) לילדים — גרסה עצמאית שעובדת כולה בדפדפן,
בלי שרת, בלי חשבון ובלי התקנה. פותחים את `index.html` ומתחילים לחסוך.

A Hebrew (RTL) piggy-bank app for kids — a standalone single-file app that
runs entirely in the browser. No server, no account, no install. Just open
`index.html` and start saving.

---

## מה יש כאן? / Features

- 💰 **יתרה** — כמה כסף יש בקופה עכשיו, עם סך הכנסות והוצאות
- 🧾 **היסטוריה** — הוספה, עריכה ומחיקה של הכנסות והוצאות עם סיבה ותאריך
- 📅 **פעולות מתוכננות** — תאריך עתידי נשמר כמתוכנן ונכנס ליתרה כשהתאריך מגיע
- 📈 **גרף יתרה** — איך היתרה השתנתה לאורך הזמן
- 🛍️ **מה אפשר לקנות** — הצעות קנייה לפי היתרה, והדבר הבא שחוסכים אליו
- ✅ **משימות** — משימה שהושלמה מוסיפה את הפרס אוטומטית כהכנסה
- 🗓️ **דמי כיס אוטומטיים** — סכום קבוע כל שבוע או כל חודש, נכנס לבד
- 💰 **חיסכון קבוע** — סכום קבוע או אחוז קבוע מהיתרה, שנכנס אוטומטית כהכנסה ליתרה כל שבוע או כל חודש (כל תשלום נרשם בהיסטוריה; לא קשור ליעד החיסכון)
- 🎯 **יעד חיסכון** — יעד אחד עם התקדמות (אופציונלי)
- 💭 **כסף דמיוני** — מכניסים סכום דמיוני (עד ₪1,000,000) ורואים מה אפשר היה
  לקנות איתו — כולל החלום הבא וכמה חסר. לא משנה את היתרה האמיתית
- 🧒 **מצב ילד** — צפייה בלבד, בלי אפשרות לערוך
- 👨‍👩‍👧‍👦 **כמה קופות (פרופילים)** — קופה נפרדת לכל ילד, עם מעבר מהיר
  ביניהן; הקופה האחרונה שנבחרה נשארת ברירת המחדל. לכל קופה יתרה, היסטוריה,
  משימות, דמי כיס, חיסכון קבוע ויעד משלה. אפשר ליצור, לשנות שם ולמחוק
  (אי אפשר למחוק את הקופה האחרונה). נתונים ישנים מהגרסה של קופה אחת
  עוברים אוטומטית לקופה הראשונה.
- ☁️ **סנכרון Google Drive (אופציונלי)** — מתחברים עם חשבון גוגל והקופות
  נשמרות גם בדרייב של אותו חשבון (קובץ JSON נסתר בתיקיית האפליקציה,
  appDataFolder), כך שהן עוברות בין מכשירים. בלי חיבור, הכל נשמר בדפדפן
  בלבד. דורש Client ID של גוגל — ראו "הפעלת סנכרון Google Drive" למטה.
- 🔗 **שיתוף לצפייה** — יוצר קישור עם הנתונים מקודדים בו; מי שפותח אותו רואה
  את הקופה (יתרה, היסטוריה, יעד, גרף) אבל לא יכול לערוך

## איך משתמשים? / How to use

1. פותחים את `index.html` בדפדפן — ישירות מהמחשב, או מהקישור החי למטה.
   Open `index.html` in a browser — straight from disk, or via the live link below.
2. בהפעלה הראשונה מזינים את שם הילד/ה ויתרת פתיחה (אופציונלי).
   On first run, enter the child's name and an optional starting balance.
3. מוסיפים פעולות, משימות, דמי כיס ויעד — הכל נשמר אוטומטית בדפדפן.
   Add transactions, tasks, allowance and a goal — everything is saved
   automatically in the browser.
4. לשיתוף לצפייה: לשונית ⚙️ הגדרות → "יצירת קישור לשיתוף לצפייה" → שולחים
   את הקישור. הקישור הוא צילום־מצב: אחרי שינויים צריך ליצור קישור חדש.
   To share a read-only view: Settings → "Create a view-only share link" →
   send the link. The link is a snapshot: after changes, create a new one.
5. לא בטוחים איך זה נראה? כפתור "🎲 טען נתוני הדגמה" ממלא נתוני דוגמה
   (הילד "דני", נתונים מומצאים לחלוטין).
   Not sure how it looks? The "Load demo data" button fills in sample data
   (a fictional kid, "דני", with made-up transactions).

## קישור חי / Live link

לאחר הפעלת GitHub Pages (ראו למטה) האפליקציה תהיה זמינה כאן:
Once GitHub Pages is enabled (see below), the app will be live here:

**https://adiperry.github.io/piggy-bank-app/**

## הפעלת סנכרון Google Drive / Enabling Google Drive sync

סנכרון הדרייב אופציונלי ודורש מזהה לקוח של גוגל (OAuth Client ID):

1. נכנסים ל־[Google Cloud Console](https://console.cloud.google.com/) עם
   חשבון הגוגל שרוצים לסנכרן אליו, ויוצרים פרויקט (אפשר להשתמש בפרויקט קיים).
2. מפעילים את **Google Drive API** לפרויקט (APIs & Services → Library).
3. יוצרים **OAuth client ID** מסוג Web application (APIs & Services →
   Credentials → Create Credentials → OAuth client ID). אם זו הפעם הראשונה,
   צריך קודם להגדיר את מסך ההסכמה (OAuth consent screen) — מספיק למלא שם
   אפליקציה, לבחור External ולשמור.
4. מוסיפים את `https://adiperry.github.io` לרשימת **Authorized JavaScript
   origins** (אין צורך ב־Authorized redirect URIs — האפליקציה משתמשת ב־GIS
   token client, בלי redirect).
5. מדביקים את ה־Client ID במשתנה `GOOGLE_CLIENT_ID` בראש הקובץ `index.html`
   (במקום `"PASTE_YOUR_CLIENT_ID_HERE"`) ומעלים שוב לגיטהאב.
6. פותחים את האפליקציה, נכנסים להגדרות → "☁️ סנכרון Google Drive" →
   "התחבר עם Google" ובוחרים את אותו חשבון גוגל.

הקופות נשמרות בקובץ `piggy-bank-profiles.json` בתיקיית האפליקציה הנסתרת של
הדרייב (appDataFolder) — הוא לא מופיע בדרייב הרגיל ושייך רק לחשבון המחובר.
הסנכרון הוא local-first: הדפדפן הוא מקור האמת, והדרייב הוא עותק מסונכרן;
בכניסה, העותק החדש יותר (לפי חותמת זמן) מנצח.

## פרטיות / Privacy

- כל הנתונים נשמרים ב־`localStorage` של הדפדפן — אצל המשתמש, על המכשיר שלו.
  All data is stored in the browser's `localStorage` — on the user's own device.
- אין שרת, אין חשבון, אין שליחת נתונים לשום מקום, אין מעקב.
  No server, no account, no data sent anywhere, no tracking.
- סנכרון Google Drive (אופציונלי) שולח את הנתונים רק לדרייב של החשבון
  שהמשתמש התחבר איתו — קובץ JSON נסתר בתיקיית האפליקציה (appDataFolder).
  הטוקן נשמר בזיכרון בלבד, לא ב־localStorage.
  Optional Google Drive sync sends the data only to the signed-in account's
  Drive — a hidden JSON file in the appDataFolder. The token lives in memory
  only, never in localStorage.
- קישור השיתוף מכיל את הנתונים בתוכו (מקודד ודחוס) — מי שמקבל אותו רואה רק
  את מה שהיוצר בחר לשתף, ואי אפשר לערוך דרכו.
  The share link carries the data inside it (encoded and compressed) — whoever
  opens it sees only what the creator chose to share, and cannot edit through it.

## פרסום ל־GitHub Pages / Publish to GitHub Pages

```bash
# 1. יצירת ריפו ציבורי / Create a public repo
gh repo create piggy-bank-app --public --source=. --remote=origin --push

# 2. הפעלת GitHub Pages / Enable GitHub Pages
gh api repos/{owner}/piggy-bank-app/pages -X POST \
  -f source[branch]=main -f source[path]=/

# 3. הקישור החי יופיע תוך דקה־שתיים / Live link appears in a minute or two
# https://{owner}.github.io/piggy-bank-app/
```

אפשר גם דרך האתר: Settings → Pages → Deploy from a branch → `main` / `(root)`.
Or via the website: Settings → Pages → Deploy from a branch → `main` / `(root)`.

## פיתוח / Development

- קובץ אחד: `index.html` — בלי build, בלי תלויות, בלי CDN. עובד גם מ־`file://`.
  A single file: `index.html` — no build step, no dependencies, no CDN.
  Works from `file://` too.
- סכומים נשמרים באגורות (מספרים שלמים) כדי להימנע משגיאות עיגול.
  Amounts are stored in agorot (integers) to avoid floating-point errors.
- בדיקות: `node` + headless Chromium דרך `puppeteer-core` (ראו `/tmp/piggy-test`
  — לא חלק מהריפו): מעבר בין פרופילים, הגירה מהפורמט הישן, דמי כיס וחיסכון
  קבוע לכל פרופיל, מחיקה ושינוי שם, מצב ילד, קישור שיתוף, ונתיבי ה־Drive
  (עם fetch מדומה — סבב חי מול גוגל דורש Client ID אמיתי).
  Tests: `node` + headless Chromium via `puppeteer-core` (see `/tmp/piggy-test`
  — not part of the repo): profile switching, migration from the old format,
  per-profile allowance and recurring savings, rename/delete, kid mode, share
  links, and the Drive code paths (with a mocked fetch — a live Google
  round-trip needs a real Client ID).

## רישיון / License

MIT — ראו `LICENSE`.

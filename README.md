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
- ☁️ **סנכרון Firebase (אופציונלי)** — נרשמים עם מייל וסיסמה והקופות
  נשמרות בענן (Firestore), כך שהן עוברות בין מכשירים. בלי חיבור, הכל נשמר
  בדפדפן בלבד. דורש פרויקט Firebase — ראו "הפעלת סנכרון Firebase" למטה.
  חובה: התוכנית החינמית Spark בלבד — בלי כרטיס אשראי ובלי שדרוג ל־Blaze.
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

## הפעלת סנכרון Firebase / Enabling Firebase sync

סנכרון Firebase אופציונלי. ההגדרה חד־פעמית, בפרויקט Firebase **בחינם**:

⚠️ **חובה — לא לשלם שום דבר:** הפרויקט חייב להישאר בתוכנית החינמית
**Spark** בלבד — **לא לחבר כרטיס אשראי / לא לשדרג ל־Blaze**. אם המכסה
החינמית נגמרת הסנכרון פשוט מפסיק והאפליקציה ממשיכה לעבוד לוקאלית.
המכסה החינמית (50 אלף קריאות ו־20 אלף כתיבות ביום, גיגה אחסון) גדולה
בהרבה ממה שקופה משפחתית צריכה.

**No payment, ever:** the project must stay on the free **Spark** plan —
**do not attach a billing account / do not upgrade to Blaze**. If the free
quota runs out, sync simply stops and the app keeps working locally.

1. נכנסים ל־[Firebase Console](https://console.firebase.google.com/) עם
   חשבון הגוגל שרוצים לסנכרן אליו, ויוצרים פרויקט (אפשר להשתמש בפרויקט
   קיים). **לא מפעילים שדרוג ל־Blaze ולא מחברים אמצעי תשלום.**
2. מפעילים התחברות במייל וסיסמה: Build → Authentication → Sign-in method
   → Email/Password → Enable → Save.
3. יוצרים מסד נתונים: Build → Firestore Database → Create database →
   Start in **production mode** (לא test mode) ובוחרים אזור.
4. מגדירים את חוקי הגישה (Firestore Database → Rules) — רק המשתמש עצמו
   יכול לקרוא ולכתוב את המסמך שלו:
   Set the access rules (Firestore Database → Rules) — each user can only
   read and write their own document:
   ```javascript
   rules_version = '2';
   service cloud.firestore {
     match /databases/{database}/documents {
       match /users/{userId} {
         allow read, write: if request.auth != null && request.auth.uid == userId;
       }
     }
   }
   ```
   ולוחצים Publish.
5. רושמים אפליקציית Web: Project settings → Your apps → Web app (`</>`)
   → נותנים שם (למשל piggy-bank) → Register app — ומעתיקים את אובייקט
   ה־`firebaseConfig` שמוצג.
6. מדביקים את הערכים במשתנה `FIREBASE_CONFIG` בראש הקובץ `index.html`
   (במקום מחרוזות ה־`"PASTE_YOUR_*_HERE"`) ומעלים שוב לגיטהאב.
7. פותחים את האפליקציה, נכנסים להגדרות → "☁️ סנכרון Firebase" →
   ממלאים מייל וסיסמה (לפחות 6 תווים) ולוחצים "📝 הרשמה" (בפעם הראשונה)
   או "🔑 התחברות". יש גם "✉️ שכחתי סיסמה" לאיפוס במייל.

כל משתמש רואה רק את הקופות של עצמו — המסמך ב־Firestore הוא
`users/{uid}` ומכיל את כל הפרופילים של אותו חשבון. הסנכרון הוא
local-first: הדפדפן הוא מקור האמת, והענן הוא עותק מסונכרן; בכניסה,
העותק החדש יותר (לפי חותמת זמן) מנצח. אם הסנכרון נכשל — למשל בגלל
סיום המכסה החינמית — האפליקציה מציגה הודעה בעברית בכרטיס הסנכרון
וממשיכה לעבוד לוקאלית, בלי לאבד נתונים.

## פרטיות / Privacy

- כל הנתונים נשמרים ב־`localStorage` של הדפדפן — אצל המשתמש, על המכשיר שלו.
  All data is stored in the browser's `localStorage` — on the user's own device.
- אין שרת, אין חשבון, אין שליחת נתונים לשום מקום, אין מעקב.
  No server, no account, no data sent anywhere, no tracking.
- סנכרון Firebase (אופציונלי) שולח את הנתונים למסמך פרטי ב־Firestore
  (`users/{uid}`) ששייך רק לחשבון המחובר — חוקי הגישה חוסמים כל חשבון
  אחר. בלי חיבור, שום דבר לא יוצא מהדפדפן.
  Optional Firebase sync sends the data to a private Firestore document
  (`users/{uid}`) owned by the signed-in account only — the security rules
  block every other account. Without signing in, nothing leaves the browser.
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

- קובץ אחד: `index.html` — בלי build, בלי תלויות, בלי CDN (ה־SDK של Firebase
  נטען מה־CDN של גוגל רק כשהסנכרון מוגדר; בלי תצורה האפליקציה לא פונה לרשת
  בכלל). עובד גם מ־`file://`.
  A single file: `index.html` — no build step, no dependencies, no CDN (the
  Firebase SDK is loaded from Google's CDN only when sync is configured;
  without config the app makes no network requests at all). Works from
  `file://` too.
- סכומים נשמרים באגורות (מספרים שלמים) כדי להימנע משגיאות עיגול.
  Amounts are stored in agorot (integers) to avoid floating-point errors.
- בדיקות: `node` + headless Chromium דרך `puppeteer-core` (ראו `/tmp/piggy-test`
  — לא חלק מהריפו): מעבר בין פרופילים, הגירה מהפורמט הישן, דמי כיס וחיסכון
  קבוע לכל פרופיל, מחיקה ושינוי שם, מצב ילד, קישור שיתוף, ונתיבי ה־Firebase
  (עם Firebase SDK מדומה — סבב חי מול Firebase דורש תצורה אמיתית; כולל
  בדיקת שגיאת מכסה resource-exhausted — הסטטוס מציג הודעה בעברית והנתונים
  המקומיים נשארים שלמים).
  Tests: `node` + headless Chromium via `puppeteer-core` (see `/tmp/piggy-test`
  — not part of the repo): profile switching, migration from the old format,
  per-profile allowance and recurring savings, rename/delete, kid mode, share
  links, and the Firebase code paths (with a mocked Firebase SDK — a live
  Firebase round-trip needs a real config; including a resource-exhausted
  quota-error check — the status shows a Hebrew message and local data stays
  intact).

## רישיון / License

MIT — ראו `LICENSE`.

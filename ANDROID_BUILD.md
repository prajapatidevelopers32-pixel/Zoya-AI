# 📱 Zoya AI - Android APK & AAB Build Guide 🚀

Aapki application me Android package setup pehle se done hai. Is guide ki help se aap apne local computer par **APK (Installable App)** aur **AAB (Play Store Release)** bana sakte hain easily.

---

## 🛠️ Step 1: Pre-requisites (Samaan Jo Chahiye)
Apne computer par ye tools install rakhein:
1. **Node.js** (LTS version)
2. **Android Studio** (Koala or latest version)
3. **Java JDK 17** (Android Studio setup me built-in mil jata hai)

---

## 💻 Step 2: Dependencies Install Karein
Apne project folder ko terminal/cmd me kholiye aur run karein:
```bash
npm install
```

---

## 🚀 Step 3: Web Code Build & Capacitor Sync (Sabse Important!)
Hamein React web application ko build karke static code Android project me copy karna hai. Iske liye humne custom script banayi hai:

Sirf ye single command run karein:
```bash
npm run build:android
```
*(Ye command `npm run build` karegi aur automatic saara code `dist` se uthakar `android/app/src/main/assets/public/` folder me copy/sync kar degi!)*

---

## 🎨 Step 4: Android Studio Me Project Open Karein
Project ko Android Studio me open karne ke liye:
```bash
npm run cap:open
```
*(Ya fir aap manual **Android Studio** open karke **"Open Project"** select karein aur apne main project ke andar waale `android/` folder ko choose karein.)*

---

## 📦 Step 5: APK aur AAB Generate Karein (Android Studio Ke Andar)

### 1️⃣ APK Kaise Banayein (Direct Phone Me Install Karne Ke Liye):
1. Android Studio me project fully load hone ka wait karein (niche progress bar complete hone dein).
2. Top Menu bar me jayein: **Build** ➜ **Build Bundle(s) / APK(s)** ➜ **Build APK(s)**.
3. Gradle build complete hone par, right corner me **"APK(s) generated successfully"** ka pop-up aayega.
4. **"Locate"** par click karein. Aapko aapki installable **`app-debug.apk`** mil jayegi! Isko direct phone me bhejkar install kar sakte hain.

### 2️⃣ AAB (Android App Bundle) Kaise Banayein (Google Play Store Par Upload Karne Ke Liye):
1. Top Menu bar me jayein: **Build** ➜ **Generate Signed Bundle / APK...**
2. **Android App Bundle** select karein aur **Next** karein.
3. **Keystore details** banayein ya select karein (Sign karne ke liye key).
4. Build variant me **`release`** select karein.
5. **Finish** par click karein. Aapki **`app-release.aab`** taiyaar ho jayegi jo Google Play Console par upload ho sakegi!

---

## ⚠️ Important Tips & Troubleshooting

- **Internet Error inside Android Studio:** Pehli baar build me Gradle libraries download karta hai, isliye active internet connection zaroori hai.
- **Gradle Sync Failed:** Agar Android Gradle plugin error de, to project ko clean karein: **Build** ➜ **Clean Project** aur fir **File** ➜ **Sync Project with Gradle Files** par click karein.
- **Port Warning:** Dev server 3000 port use karta hai. Physical app build release configuration use karegi, jisme local server ki zaroorat nahi padti aur app offline fast chalegi!

---

**✨ Zoya Studio (Pro) aur Image Generation ke sath ab aapki App ready hai build hone ke liye! Best of luck!**

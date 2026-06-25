# 🛠️ Morphe Patched Builds (Automated Builder)

**Automated cloud builder for patched YouTube & YT Music using GitHub Actions.**

Ye repository **GitHub Actions** ka use karke automatically YouTube aur YouTube Music ke patched versions build karti hai. Is project me **Morphe Patches** (jo ki ReVanced ka ek behtareen alternative/variant hai) ka use kiya gaya hai.

Is builder ki khaasiyat ye hai ki ye aapko cloud me automatically apps build karke seedha **Releases** section me de deta hai. Ab aapko apne phone ya PC par manual patching karne ki koi zarurat nahi!

## ✨ Key Features

* ☁️ **100% Fully Automated:** Daily subah (IST 4:00 AM) automatically check karta hai ki koi naya Morphe patch aaya hai ya nahi. Agar naya patch milta hai, tabhi naya build banata hai.

* 📱 **Dual Architecture (Non-Root):** `arm64-v8a` (modern phones) aur `armeabi-v7a` (older phones) dono ke liye alag-alag optimized APKs banata hai.

* ⚡ **Root / Magisk Support:** Root users ke liye seedha flashable `.zip` (Magisk Modules) banata hai.

* 📥 **Smart Downloader:** Archive.org se hamesha officially untouched (nodpi) APKs fetch karta hai, jisse build kabhi fail nahi hota.

* 🧹 **Clean File Naming:** Output files ka naam directly app version ke hisaab se hota hai (e.g., `YouTube-v19.xx.xx-NonRoot.apk`).

## 🚀 Kaise Use Karein (Setup Guide)

Apne khud ke account par is automatic builder ko set up karne ke liye in simple steps ko follow karein:

### Step 1: Fork ya Clone

Sabse pehle is repository ko apne GitHub account par **Fork** kar lein.

> 💡 **Tip:** DMCA copyright issues se bachne ke liye apni forked repository ko **Private** rakhna sabse safe option hota hai.

### Step 2: Permissions Set Karein

GitHub Actions ko automatically "Release" create karne ki permission dena zaruri hai:

1. Apni Repo ki **Settings ⚙️** me jayein.
2. Left sidebar se **Actions** > **General** par click karein.
3. Scroll karke sabse niche **Workflow permissions** section me aayein.
4. **`Read and write permissions`** select karein aur Save par click kar dein.

### Step 3: Action Enable aur Run Karein

1. Repo ke **Actions** tab me jayein.
2. Agar koi warning dikhe, toh **"I understand my workflows, go ahead and enable them"** par click karein.
3. Left side se **`Build Morphe APKs and Magisk Modules`** par click karein.
4. Right side me **`Run workflow`** ka button aayega, us par click karke process start karein.
5. 5-10 minute wait karein. Build complete hone ke baad, aapke repo ke **Releases** section me latest files aa jayengi! 🎉

## 📦 Output Files

Build complete hone ke baad aapke Releases page me ye 6 files generate hongi:

| **File Name** | **Type** | **Architecture** | **Description** | 
| ----- | ----- | ----- | ----- | 
| `YouTube-vX.XX.XX-arm64-v8a-NonRoot.apk` | **APK** | ARM64 | Normal install ke liye (Modern devices) | 
| `YouTube-vX.XX.XX-armeabi-v7a-NonRoot.apk` | **APK** | ARMv7 | Normal install ke liye (Older devices) | 
| `YouTube-vX.XX.XX.zip` | **ZIP** | Universal | Root users ke liye (Magisk Module) | 
| `YTMusic-vX.XX.XX-arm64-v8a-NonRoot.apk` | **APK** | ARM64 | Normal install ke liye (Modern devices) | 
| `YTMusic-vX.XX.XX-armeabi-v7a-NonRoot.apk` | **APK** | ARMv7 | Normal install ke liye (Older devices) | 
| `YTMusic-vX.XX.XX.zip` | **ZIP** | Universal | Root users ke liye (Magisk Module) | 

## 📌 Required Add-ons (Install karne se pehle zaroori)

* 🧩 **For Non-Root Users:** Aapko Google account login karne ke liye **MicroG** install karna hoga.
  👉 [Download MicroG-RE Here](https://github.com/morpheapp/MicroG-RE/releases)

* 🛡️ **For Root Users:** Magisk module flash karne ke baad, app ko Play Store se update hone se rokne ke liye Zygisk-Detach ka use karein.
  👉 [Download Zygisk-Detach Here](https://github.com/j-hc/zygisk-detach)

## ⚠️ Disclaimer

> * Ye repository sirf **educational aur personal testing purposes** ke liye banayi gayi hai.
> * Original apps ke copyrights aur trademarks unke respective owners (Google LLC) ke paas hain.
> * Is repository ka app piracy ya kisi copyright violation se koi lena-dena nahi hai. Hum sirf open-source patching tools (Morphe) ko run karne ke liye ek cloud environment provide kar rahe hain. Kripya iska public distribution avoid karein.

## 💖 Credits & Acknowledgements

Ye project community ke inn behtareen open-source developers aur unke tools ke bina mumkin nahi tha:

* [**MorpheApp**](https://github.com/MorpheApp) - Morphe CLI, Patches aur Integrations ke liye jiske bina ye patched apps ban hi nahi sakti.
* [**j-hc**](https://github.com/j-hc) - Original unpatched APKs ko regularly `jhc-apks` archive par update rakhne ke liye aur Zygisk-Detach module ke liye.
* [**MicroG-RE**](https://github.com/WSTxda/MicroG-RE) - Non-root devices me seamlessly Google account login bypass aur background services provide karne ke liye.
* [**topjohnwu**](https://github.com/topjohnwu) - **Magisk** banane ke liye jisse hum in apps ko systemless tarike se root devices me flash kar paate hain.

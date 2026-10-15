# Muhammad Khizar — Video Portfolio

Website files for GitHub Pages.

## Website online karna (GitHub Pages)
1. GitHub pe naya **public** repository banayein (jaise `khizar-portfolio`).
2. Is folder ki saari files upload karein (`index.html`, `videos.html`, `style.css`, `videos.js`, `app.js`, CV pdf, aur `img` + `media` folders).
3. Repository ki **Settings → Pages** mein Branch: `main`, folder `/ (root)` select karke **Save** karein.
4. 1–2 minute baad link milega: `https://USERNAME.github.io/khizar-portfolio/`

## Nayi video add karna
Sirf `videos.js` file edit karni hai:
1. Video Google Drive pe upload karein aur sharing **"Anyone with the link"** rakhein.
2. Drive link mein se ID copy karein: `drive.google.com/file/d/`**`YEH_ID`**`/view`
3. `videos.js` mein kisi bhi video ka block copy karke list mein paste karein aur values badal dein:

```js
{
  title: "Video ka naam",
  category: "Product Ads",        // Brand & Corporate / Product Ads / AI Explainers / Motion & Logo
  format: "9:16",                 // vertical = "9:16", landscape = "16:9"
  duration: "0:30",
  about: "Ek line mein kya banaya.",
  drive: "YEH_ID"
},
```

Bas. Video khud "All videos" page pe aa jayegi, thumbnail Drive se aa jayega, aur video Drive se chalegi.
Home page pe bhi dikhani ho to `featured: true` add kar dein.

## Automatic mode: Drive ki har video khud website pe (optional, ek dafa ka kaam)
Is ke baad aap sirf Drive folder mein video daalein, website pe khud aa jayegi. Kuch edit nahi karna padega.
1. https://console.cloud.google.com pe Gmail se login karein aur ek naya project banayein.
2. **APIs & Services → Library** mein "Google Drive API" search karke **Enable** karein.
3. **APIs & Services → Credentials → Create credentials → API key**. Key copy kar lein.
4. Key ko secure karne ke liye "Website restrictions" mein apni GitHub site ka address daal dein (jaise `https://USERNAME.github.io/*`), aur "API restrictions" mein sirf Google Drive API select karein.
5. `videos.js` mein sab se upar `window.DRIVE_API_KEY = "";` ke quotes ke andar key paste karke file save/upload kar dein.

Tips:
- Drive folder ki sharing "Anyone with the link" honi chahiye.
- Drive mein file ka naam hi website pe title banega, isliye files ke achay naam rakhein (jaise `Nike Shoes Ad.mp4`).
- Kisi video ki category ya description chahiye ho to uska block `videos.js` mein bhi add kar dein; baaki khud "More Work" mein aa jayengi.

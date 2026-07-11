# Kamin Duangmala — Project Bug Tracker

---

## Overview
This document tracks all identified issues in the `cv-template.html` file and the overall project structure. Each issue is categorized by severity and tracked with fix status.

---

## ✅ Fix Status Summary

| # | Issue | Status |
|---|-------|--------|
| 1 | CSS `@keyframes glowPulse` syntax error (`- que50%` → `-50%`) | ✅ Fixed |
| 2 | Page never shows without user interaction (no fallback) | ✅ Fixed |
| 3 | No localStorage language persistence | ✅ Fixed |
| 4 | Missing IT logo for college entry | ✅ Fixed |
| 5 | Education section missing full structured details | ✅ Fixed |
| 6 | `profile.md` was outdated (now clean tracker) | ✅ Fixed |
| 7 | Section nav mobile feedback | ✅ Fixed |
| 8 | Education section visual dividers between entries | ✅ Fixed |
| 9 | Contact row missing second email | ✅ Fixed |
| 10 | Experience section logo mismatch (college logo on ROTC) | ✅ Fixed |
| 11 | Custom font files not linked (`Font English.otf`, `Font Thai.ttf`) | ✅ Fixed |
| 12 | Inline JS not modular (kept as-is for simplicity) | 🔵 Note |
| 13 | Print styles not hiding animations | ✅ Fixed |
| 14 | Fragile image paths with spaces | 🟡 Noted |
| 15 | Custom font applied only to name heading (not whole page) | ✅ Fixed |
| 16 | Name now dynamic — switches between "Kamin Duangmala" (EN) and "คามิน ดวงมาลา" (TH) on language toggle | ✅ Fixed |
| 17 | 4 Thai school name keys (`edu_school_1-4`) missing from `i18n.th` — showed "undefined" in education section | ✅ Fixed |
| 18 | "Udon Thani, Thailand" → "Thailand" in contact row; "Thailand" date removed from Photographer entry | ✅ Fixed |
| 19 | Removed non-existent "Grade certificates/ได้รับเกียรติบัตร" from Photographer experience | ✅ Fixed |
| 20 | Added new experience: โครงการจิตอาสาจราจรและความปลอดภัย at Udon Thani Technical College | ✅ Fixed |
| 21 | Added new experience: ฝึกงาน at Central Advertising (with logo `Central Advertising.png`) | ✅ Fixed |
| 22 | Added date "2025" to Photographer experience entry | ✅ Fixed |
| 23 | Added date "2024-2025" to Traffic Volunteer experience entry | ✅ Fixed |
| 24 | Added date "3 months" + bullet "Vinyl banner" to Central Advertising Intern entry | ✅ Fixed |
| 25 | Replaced Central Advertising bullet with 3 detailed points about print production, Photoshop skills, and production process | ✅ Fixed |
| 26 | Added 2 bullet points to Traffic Volunteer: patience/sacrifice and safety awareness | ✅ Fixed |
| 27 | Changed Photographer company label from "ROTC / Student" to "2 years / 2 ปี" | ✅ Fixed |
| 28 | Changed Traffic Volunteer company label from "Udon Thani Technical College" to "2 years / 2 ปี" | ✅ Fixed |
| 29 | Date column → Duration: Photographer "2025" → "2 years / 2 ปี", Traffic Volunteer "2024-2025" → "2 years / 2 ปี"; removed redundant company text | ✅ Fixed |
| 30 | New experience: Dog2boy Kennel — added with 2 bullets (Client Relations + Ultimate Responsibility), duration 10 years, logo `Dog2boy Kennel.png` | ✅ Fixed |
| 31 | Changed Central Advertising bullet 1 title: "Real-world vs digital" → "Real-world vs game" | ✅ Fixed |
| 32 | Dog2boy Kennel: changed role to "Assistant / ผู้ช่วย", added company "Dog2boy Kennel (Home Business) / Dog2boy Kennel (ธุรกิจบ้านส่วนตัว)" | ✅ Fixed |
| 33 | Dog2boy Kennel duration changed from "10 years" to "10 years - Present / 10 ปี - ปัจจุบัน" | ✅ Fixed |
| 34 | New experience: นักเรียน อวท เลขา (Student, AVT Secretary) — with 3 bullets, logo `อวท..jpg`, duration Present | ✅ Fixed |
| 35 | Reordered Experience section: AVT Secretary → Dog2boy Kennel → Intern → Photographer → Traffic Volunteer | ✅ Fixed |
| 36 | Added address to About Me (Dog2boy Kennel with new i18n key `about_address`) | ✅ Fixed |
| 37 | Changed contact row "Thailand" → "Thailand, Udon Thani" | ✅ Fixed |
| 38 | Added 4 social links with SVG icons: FB Kamin Sunta, FB Legacy Saga, YT Kazamakaden, YT EXE Legacy Saga | ✅ Fixed |
| 39 | Added MBTI + mindset to About Me: "INTP 9w8 — Born Gen Z with Gen X mindset, shaped by my father" | ✅ Fixed |
| 40 | Replaced Skills section with Hard Skills (11 items) + Soft Skills (10 items) with knowledge note | ✅ Fixed |
| 41 | Added "Photo / รูปภาพ" link in left nav linking to Facebook photo album | ✅ Fixed |
| 42 | Increased font sizes across all text elements for better readability; polished EN/TH copy | ✅ Fixed |
| 43 | Humanized all EN experience bullet points & About Me — rewrote from formal/robotic to personal, humble, natural voice | ✅ Fixed |
| 44 | Extracted inline styles to CSS classes + mobile nav horizontal scrollable + font-display:swap for FOUT prevention | ✅ Fixed |
| 45 | Added logo images to Hard Skills section + new skills: Adobe Premiere Pro, AI - Ollama, AI - Gemini, AI Coding | ✅ Fixed |

---

## 📝 Changes Applied to `cv-template.html`

### 🔴 Critical
1. **glowPulse CSS** — Changed `- que50%` to `-50%` so the animation works
2. **Page fallback** — Added `localStorage` check on load + `setTimeout(showPage, 8000)` safety net
3. **Language persistence** — `setLanguage()` now saves to `localStorage`, and on page load it checks for a saved language

### 🟡 Content
4. **IT logo** — Added second logo image for the IT program alongside college logo
5. **Education details** — Expanded to show full structured details per user request
6. **profile.md** — Now this clean bug tracker document
9. **Second email** — Added `legacysaga000@gmail.com` to contact row
10. **Experience logo** — Removed college logo from ROTC Photographer entry

### 🟠 Visual
7. **Mobile feedback** — Added tap highlight color and improved active states
8. **Dividers** — Added bottom border separators between education entries

### 🆕 Latest (2026-07-09)
15. **Name font only** — `@font-face` rules added; `font-family: 'CustomEnglish', 'CustomThai', var(--font)` applied only to `.name-block h1`, not whole page
16. **Dynamic name i18n** — Name now has `data-i18n="name"`; switches between English "Kamin Duangmala" and Thai "คามิน ดวงมาลา" when user selects language
17. **Missing Thai school names** — Added `edu_school_1` through `edu_school_4` to `i18n.th` (were present in `en` but absent in `th`, causing "undefined")
18. **Location cleanup** — Changed "Udon Thani, Thailand" to just "Thailand" in contact row; removed "Thailand" date label from Photographer experience entry
19. **Removed fake experience bullet** — Deleted "Grade certificates and professional photography training" from EN and "ได้รับเกียรติบัตรและผ่านการอบรมด้านการถ่ายภาพระดับมืออาชีพ" from TH exp_list
20. **New experience: Traffic Volunteer** — Added `โครงการจิตอาสาจราจรและความปลอดภัย` with Udon Thani Technical College logo
21. **New experience: Internship** — Added `ฝึกงาน` at Central Advertising with `Central Advertising.png` logo
22. **Photographer date** — Added `<span class="date">2025</span>` to Photographer entry with i18n keys `exp_date`
23. **Traffic Volunteer date** — Added `<span class="date">2024-2025</span>` to Traffic Volunteer entry with i18n keys `exp2_date`
24. **Intern details** — Added date "3 months" and bullet "Vinyl banner" to Central Advertising entry with i18n keys `exp3_date`, `exp3_list`
25. **Central Advertising detailed bullets** — Replaced single "Vinyl banner" with 3 detailed bullets: (1) real-world print vs digital design/CMYK/resolution, (2) Adobe Photoshop skills with deadlines/bleed/layout, (3) production process — inkjet printing, vinyl folding, eyelet punching, vinyl type selection
26. **Traffic Volunteer bullets** — Added 2 detailed bullets with new i18n key `exp2_list`: (1) ความอดทนและเสียสละ (patience & sacrifice) — waking up early, standing in sun/wind during rush hour, cultivating public safety awareness, (2) การสร้างความตระหนักรู้ (safety awareness) — 100% helmet campaign, pedestrian crossings, traffic rules in school
27. **Photographer duration** — Changed `exp_comp` from " — ROTC / Student" to " — 2 years" (EN) / " — 2 ปี" (TH)
28. **Traffic Volunteer duration** — Changed `exp2_comp` from " — Udon Thani Technical College" to " — 2 years" (EN) / " — 2 ปี" (TH)
29. **Duration column** — Replaced date values with duration: Photographer `exp_date` "2025" → "2 years / 2 ปี", Traffic Volunteer `exp2_date` "2024-2025" → "2 years / 2 ปี"; removed `exp_comp` and `exp2_comp` company labels as redundant
30. **New experience: Dog2boy Kennel** — Added as first entry with `Dog2boy Kennel.png` logo, 10 years duration, and 2 bullets: (1) Client Relations — updating photos/videos/reports for dog owners with sincerity and care, (2) Ultimate Responsibility — 24/7 dog care shaping high responsibility, punctuality, and gentle but strong problem-solving mindset
31. **Central Advertising title fix** — Changed first bullet title from "Real-world vs digital" to "Real-world vs game"
32. **Dog2boy Kennel role** — Changed role from "Dog2boy Kennel" to "Assistant" (EN) / "ผู้ช่วย" (TH); added company label `exp4_comp`: " — Dog2boy Kennel (Home Business)" (EN) / " — Dog2boy Kennel (ธุรกิจบ้านส่วนตัว)" (TH)
33. **Dog2boy Kennel duration** — Changed from "10 years" to "10 years - Present" (EN) / "10 ปี - ปัจจุบัน" (TH) to indicate ongoing
34. **New experience: AVT Secretary** — Added as 5th entry with `อวท..jpg` logo, role "Student, AVT Secretary" (EN) / "นักเรียน อวท เลขา" (TH), duration Present, and 3 bullets: (1) meeting preparation & agenda notification, (2) meeting minutes & resolution summaries, (3) document management — official correspondence, project proposals
35. **Experience reorder** — Moved entries into final order: (1) Student AVT Secretary, (2) Dog2boy Kennel Assistant, (3) Intern Central Advertising, (4) Photographer, (5) Traffic Volunteer
36. **About Me address** — Added address paragraph with new i18n key `about_address` — Dog2boy Kennel address in both EN and TH
37. **Contact location** — Changed "Thailand" to "Thailand, Udon Thani" in contact row
38. **Social media links** — Added 4 social links below contact row with inline SVG icons: YT Kazamakaden El KA, FB Kamin Sunta, YT EXE Legacy Saga, FB Legacy Saga
39. **About Me MBTI** — Added `about_mbti`: "INTP 9w8 — Born Gen Z with Gen X mindset, shaped by my father" (EN) / "MBTI: INTP 9w8 — เกิด Gen Z แต่มีความคิดแบบ Gen X ที่พ่อปลูกฝัง" (TH)
40. **Skills section redesign** — Replaced old 5 tags with Hard Skills (11 items) and Soft Skills (10 items) with knowledge note
41. **Photo link** — Added "Photo" (EN) / "รูปภาพ" (TH) as left nav link to Facebook photo album https://www.facebook.com/media/set/?set=a.2204627816772101&type=3

### 🔧 Technical
11. **Fonts** — Added `@font-face` rules linking to `Font/` directory files
13. **Print** — Added styles to hide canvas, glow, overlay during printing

---

## File Structure

```
📁 Project Root
├── cv-template.html          ✅ Fixed — Main CV page
├── profile.md                ✅ Fixed — Bug tracker (this file)
├── file read.txt             📄 User instructions
├── Font/
│   ├── Font English.otf      🔗 Now linked
│   └── Font Thai.ttf          🔗 Now linked
└── Picture logo/
    ├── วิทยาลัยเทคนิคอุดรธานี.png
    ├── โรงเรียนเทศบาล 6 อุดรธานี.png
    ├── โรงเรียนอุดรคริสเตียนวิทยา.png
    └── โรงเรียน กระจ่างวิทย์.jpg
```

---

*All fixes applied. Open `cv-template.html` in a browser to view the updated CV.*
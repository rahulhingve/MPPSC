# 🎯 Universal Video Transcript → Revision HTML Converter Prompt

> **Copy-paste this entire prompt to any AI (ChatGPT / Claude / Gemini) along with your video transcript text file.**

---

## PROMPT START — COPY EVERYTHING BELOW THIS LINE

---

You are an expert **Exam Revision Page Builder**. I will give you a **video transcript** (lecture/class). Your job is to:

1. **Read the ENTIRE transcript** — do NOT skip or miss any topic, sub-topic, fact, name, date, full-form, definition, example, or exam tip mentioned.
2. **Create a single HTML revision file** for exam revision that covers 100% of the content taught in the video and uses verified online images wherever they improve learning.

---

## 📋 CONTENT EXTRACTION RULES

- Extract **every single topic and sub-topic** discussed in the video.
- Extract **every fact, date, year, name, inventor, full-form, definition, comparison, and example**.
- Extract **every exam-oriented tip** the teacher gives (e.g., "यह पूछा जाता है", "याद रखिए", "इंपोर्टेंट है").
- Extract **all previous year question patterns** mentioned.
- If the teacher says "यह पूछा गया है" or "एग्जाम में आता है" — mark that point as 🔥 **Exam Hot**.
- Do NOT add content that was NOT in the video. Stay faithful to the transcript.
- If the teacher mentions something will be covered in a future class, note it as "📌 Upcoming Topic" at the end.

---

## 🌐 LANGUAGE — HINGLISH (Hindi + English Mix)

- Use **Hinglish** throughout — the way Indian students naturally speak and study.
- Technical terms in **English** (e.g., CPU, RAM, Operating System, Microprocessor).
- Explanations and descriptions in **Hindi** (e.g., "यह एक स्वचालित मशीन है").
- Full forms: Show **English full form** + **Hindi meaning** side by side.
- Example: `RAM — Random Access Memory (अस्थायी मेमोरी — बंद करो तो डाटा उड़ जाता है)`

---

## 🧠 LEARNING SCIENCE TECHNIQUES — MANDATORY

Apply these **cognitive science methods** to help students remember longer:

### 1. Chunking (टुकड़ों में बाँटो)
- Break large topics into small digestible cards/sections.
- Max 5-7 points per card. No walls of text.
- Use collapsible sections for detailed content.

### 2. Dual Coding (Visual + Text)
- Pair every major concept with a **visual element** (icon, emoji, table, diagram, or color-coded box).
- Use relevant **emojis** as visual anchors: 💻 🖥️ 🧠 ⚡ 📱 🔧 📊 🗂️ 🔑 🎯 🔥
- Use **Mermaid diagrams** or simple ASCII art for hierarchies and flowcharts where applicable.
- For every major topic, **must use real, topic-relevant online `<img>` tags** with descriptive `alt` text. **Do NOT use random placeholder images** from picsum.photos, via.placeholder.com, dummyimage.com, etc.
- Use only **free-to-use / openly licensed images** from reliable sources such as:
  - **Wikimedia Commons** / Wikipedia media files (prefer Public Domain, CC0, CC BY, CC BY-SA)
  - **Openverse** results (verify the original source page and license)
  - **Unsplash** photos when a real-world conceptual photo is useful
  - Official public-domain/open government or institution media when relevant
- Every external image must include a small visible caption with: **Image source + creator if available + license**. Example: `Image: Wikimedia Commons, Creator Name, CC BY-SA 4.0`.
- Prefer images that directly explain the concept, not decorative stock photos. Use diagrams/screenshots/real device photos where they improve memory.
- If a verified free image URL is hard to find, still try reliable open sources first; use HTML/CSS diagrams, Mermaid diagrams, tables, or icon-based visuals only as supplements, not as the main visual for major topics.
- Use images generously but intelligently: add **at least 1 visual/image block for every major topic** and **additional images for hardware, network, maps, diagrams, historical devices, and confusing comparisons**.
- For computer/internet classes like this transcript, strongly consider free images or diagrams for: computer system, CPU/RAM/storage, internet network, WWW/webpage, browser, search engine, URL/domain name, IP address, email, server-client model, modem/router, printer/print buffer, virus/malware, emoji vs emoticon, and web surfing.
- For Madhya Pradesh geography/map-heavy classes, use this MP map image where needed: `https://www.slbcmadhyapradesh.in/images/MP-NewMap-55.gif` (540 × 387). If the whole class repeatedly needs the MP map (districts, borders, divisions, Kark Rekha, location/extent), place it as a static/sticky side reference visible while scrolling on desktop. If only one topic needs it, place it only in that topic section with descriptive `alt` text.

### 3. Spaced Repetition Hooks
- Add a **"Quick Recall" quiz section** at the end of each major topic — simple Q&A format.
- Add a **Master Revision Checklist** at the very end with all key facts as checkboxes.

### 4. Mnemonics & Memory Tricks (याद रखने की ट्रिक)
- Create **mnemonics** for lists (e.g., computer generations, input devices).
- If the teacher gives any trick, include it prominently.
- Create your own Hindi/English mnemonics where helpful.

### 5. Comparison Tables
- Whenever two or more things are compared (e.g., RAM vs ROM, Analog vs Digital), use a **comparison table**.
- Tables are easier to scan than paragraphs.

### 6. Timeline / Flow for Historical Topics
- For any historical evolution (e.g., history of computers), use a **visual timeline** format.
- Show: Year → Invention → Inventor → Key Fact

---

## 🎨 UI/UX DESIGN RULES — STUDENT-FRIENDLY

### Color & Theme
- Use a **Dark Mode** theme — dark background (#0f0f1a or similar), light text.
- Add a clearly visible **Dark/Light Theme Toggle** button. The selected theme must persist using `localStorage`.
- Accent colors: Use a **vibrant but harmonious palette** — cyan (#00d4ff), orange (#ff6b35), green (#00ff88), purple (#b388ff).
- Each major topic section should have its own **subtle accent color** for visual separation.

### Typography & Readability — NO SQUINTING!
- Import **Google Font: "Inter"** or **"Outfit"** — clean, modern, highly readable.
- Base font size: **17px minimum** for body text.
- Headings: Large and bold, with emoji prefix for quick scanning.
- Line height: **1.7** minimum — give text room to breathe.
- Letter spacing: slightly increased for Hindi text readability.
- **Never use light gray text on dark background** — minimum contrast ratio 7:1.

### Layout
- **Mobile-first responsive** — most students study on phones.
- Max content width: **800px**, centered.
- Generous padding and margins — content should feel spacious, not cramped.
- Use **cards with rounded corners** and subtle borders for each sub-topic.
- Sticky/fixed **Table of Contents** navigation sidebar or top nav for quick jumping.
- Add a **sticky quick navigation control** that is always visible while scrolling: use a compact dropdown/select or jump menu so students can instantly jump to any major topic on mobile and desktop.
- If a map is used as a class-wide reference, keep it in a separate sticky side panel on desktop and make it non-sticky/responsive on mobile so content remains readable.

### Interactive Elements
- **Collapsible/Accordion sections** for detailed content — keeps page clean.
- **Click-to-reveal answers** for quiz questions.
- **Checkboxes** in the master checklist that persist (use localStorage).
- Smooth scroll to sections when clicking TOC links.
- Theme toggle must switch between dark and light mode without page reload and must persist after refresh using `localStorage`.
- **Progress indicator** showing how much revision is done.

---

## 📄 HTML FILE STRUCTURE

```
1. HEADER
   - Topic title (from video)
   - Subject & Unit info
   - Total topics count badge
   - Progress bar

2. TABLE OF CONTENTS (Sticky)
   - Clickable list of all major topics
   - Visual indicator for completed sections
   - Sticky quick-jump dropdown/menu for instant navigation to any major topic
   - Dark/Light theme toggle button

3. TOPIC SECTIONS (Repeat for each topic in video)
   For each topic:
   a. Section Header with emoji + topic name (Hindi & English)
   b. Key Concept Cards (chunked, max 5-7 points each)
   c. Important Definitions (highlighted box)
   d. Full Forms Table (if any)
   e. Comparison Tables (if applicable)
   f. Timeline (if historical content)
   g. Exam Hot Points 🔥 (things teacher said are asked in exams)
   h. Quick Recall Quiz (3-5 questions with hidden answers)
   i. Online Free/Open Image Block with caption, source, creator/license, and useful alt text

4. MASTER SECTION — FULL FORMS
   - Alphabetical table of ALL full forms mentioned in video

5. MASTER SECTION — EXAM HOT FACTS 🔥
   - All "previously asked" and "important for exam" points in one place

6. MASTER REVISION CHECKLIST
   - Every key fact as a checkbox
   - localStorage persistence
   - Progress counter

7. FOOTER
   - "Upcoming Topics" (mentioned but not covered in this video)
   - Revision tips
```

---

## 🔧 TECHNICAL REQUIREMENTS

- **Single HTML file** with inline CSS and JS. External dependencies are allowed for Google Fonts CDN and verified free/open online images.
- External `<img>` URLs **must be used** for every major topic when verified free/open sources are available. Do not hotlink random copyrighted images.
- Exception: if the class needs the official/reference MP map, the image URL `https://www.slbcmadhyapradesh.in/images/MP-NewMap-55.gif` may be used as an external `<img>` source.
- All images must use a **robust loading strategy**: `decoding="async"`, responsive CSS (`max-width: 100%; height: auto;`), useful `alt` text, and a visible attribution caption. For revision pages, prefer `loading="eager"` + `fetchpriority="high"` for important concept images, or include inline JS that force-preloads all images so students do not see blank image blocks while studying.
- Add an inline **image reliability script**: preload every `<img>` URL, retry failed Wikimedia/Commons images through an alternate stable URL such as `Special:Redirect/file/...`, and show a visible fallback link if an image still cannot load. Do not leave broken-image icons silently on the page.
- Avoid huge image files. Prefer thumbnails or reasonably sized image URLs so the HTML page remains fast on mobile.
- All CSS **inline in `<style>` tag** inside the HTML.
- All JS **inline in `<script>` tag** inside the HTML.
- Internet-connected study is assumed. Prioritize useful online images over offline-only diagrams; the page may rely on the network for fonts/images.
- Use **semantic HTML5** elements.
- Smooth **CSS animations** for card reveals and hover effects.
- **Print-friendly** — add `@media print` styles that show all content expanded in clean black/white format.
- File size should be reasonable — don't add unnecessary bloat.

---

## ⚠️ IMPORTANT WARNINGS

1. **DO NOT MISS ANY CONTENT** from the transcript. If it was taught, it must be in the revision page.
2. **DO NOT ADD FAKE CONTENT** — only include what was actually discussed in the video.
3. **DO NOT make it text-heavy** — use visual elements, tables, cards. Student should be able to scan quickly.
4. **DO NOT use tiny fonts** — readability is #1 priority.
5. **DO NOT skip full forms** — they are the most asked questions in exams.
6. **DO NOT forget the quiz sections** — active recall is the #1 study technique.
7. **Every section must be bilingual** — Hindi + English terms side by side.
8. **DO NOT use unverified copyrighted images** — must use free/open online images with caption attribution for major topics; HTML/CSS/Mermaid diagrams can supplement them.
9. If the HTML is too large for one response, **split into parts** and clearly label them for concatenation.

---

## 📎 INPUT FORMAT

The video transcript will be provided as plain text. It may:
- Be in Hindi/Hinglish
- Contain speech-to-text errors — interpret intelligently
- Have informal language — extract the educational content
- Include promotional content (ads for apps/courses) — SKIP those parts entirely
- Be very long — process ALL of it

---

## ✅ FINAL CHECKLIST BEFORE OUTPUTTING

Before giving the HTML, verify:
- [ ] Every topic from transcript is covered
- [ ] Every full form is included
- [ ] Every inventor/year/fact is included
- [ ] Every exam tip is marked with 🔥
- [ ] Quiz sections are present for each topic
- [ ] Free/open online images are added for every major topic
- [ ] Each image has descriptive alt text, responsive sizing, robust preload/retry loading, source, creator if available, and license caption
- [ ] No random placeholder or unverified copyrighted image is used
- [ ] Master checklist is at the end
- [ ] Mobile responsive
- [ ] Dark mode with readable fonts
- [ ] Dark/Light theme toggle is present and persists with localStorage
- [ ] Sticky quick navigation/dropdown is present and can jump instantly to all major topics
- [ ] Hinglish language throughout
- [ ] All interactive features work (collapsible, quiz reveal, checkboxes)
- [ ] No promotional content from transcript is included

---

## 🚀 NOW CREATE THE REVISION HTML

Here is the video transcript. Read it completely, extract all educational content, and generate the revision HTML file:

**[PASTE YOUR VIDEO TRANSCRIPT TEXT BELOW THIS LINE]**

---

## PROMPT END

---

# 📖 HOW TO USE THIS PROMPT

1. **Copy** everything between "PROMPT START" and "PROMPT END" above.
2. **Open** any AI tool — ChatGPT (GPT-4), Claude, Gemini, etc.
3. **Paste** the prompt first.
4. **Then paste** your video transcript text at the end where it says "[PASTE YOUR VIDEO TRANSCRIPT TEXT BELOW THIS LINE]".
5. **Send** the message.
6. If the AI says the output is too large, tell it: *"Give me the HTML in parts. Part 1 first."*
7. **Save** the output as a `.html` file and open in any browser.
8. **Study & Revise!** 🎯

### Tips for Best Results:
- **Longer transcripts**: If your transcript is very long (500KB+), split it into 2-3 parts and generate separate HTML files for each part.
- **Better AI**: Use GPT-4, Claude Opus, or Gemini Pro for best quality output.
- **Iterate**: If the AI misses something, tell it: *"You missed the section about [topic]. Add it."*
- **Customize**: Add your exam name (MPPSC/UPSC/SSC/Patwari) in the prompt for targeted content.

# Privacy Policy for ChatArchive Pro
**Last Updated:** June 17, 2026
ChatArchive Pro ("we," "us," or "our") develops the **ChatArchive Pro - AI Chat Exporter** browser extension (the "Extension"). We are committed to protecting your privacy. This Privacy Policy explains our practices regarding data collection, processing, and storage. 
Our core privacy philosophy is simple: **Your data belongs to you.** The Extension is designed to operate entirely locally on your machine, with zero remote server transmissions, zero telemetry, and zero tracking.
---
## 1. Executive Summary (Zero-Data Promise)
* **No Data Collection:** We do not collect, monitor, store, scrape, or transmit any personal information, browsing history, or chat transcripts.
* **Local Processing Only:** All chat extraction, parsing, image encoding, formatting, and file downloads are performed locally inside your browser sandbox on your device.
* **No Network Transmissions:** The Extension does not communicate with external servers. It has no server backend.
* **No Third-Party Sharing:** Since we do not collect any data, we cannot and do not share, sell, or trade your data with any third parties, advertisers, or AI training groups.
---
## 2. Information Handled by the Extension
While ChatArchive Pro handles sensitive information (your AI chat transcripts and images), it does so strictly on your device. Here is how different types of information are processed:
### A. AI Chat Transcripts & Text Content
* **What is handled:** The conversation messages (prompts and assistant responses) from ChatGPT, Claude, and Gemini.
* **How it is processed:** When you click the Extension icon, the content script reads the active tab's DOM (document structure) to extract the chat transcript.
* **Where it is stored:** The parsed transcript is temporarily written to Chrome's local extension storage (`chrome.storage.local`) to allow the popup to open the Advanced Studio Dashboard (`viewer.html`). Closing the tab or clearing the browser storage completely deletes this data.
### B. Image Attachments
* **What is handled:** User-uploaded images and AI-generated inline images within the chat tabs.
* **How it is processed:** The Extension extracts images and encodes them into Base64 format locally in your browser. This enables offline-ready rendering when exporting as Markdown or HTML.
* **Where it is stored:** These Base64 encoded strings are stored temporarily in `chrome.storage.local` alongside the text transcripts. No remote image storage or uploading occurs.
### C. Extension Settings & Configurations
* **What is handled:** Your export preferences, including your selected visual theme (e.g., Indigo Nocturne, Emerald Glass), formatting options (include metadata, auto-censor options), and filters.
* **How it is processed:** Saved locally to preserve your preferences across launches.
* **Where it is stored:** Stored on your local device in `chrome.storage.local`.
---
## 3. Chrome Web Store Permissions Justification
We request minimal Chrome extension permissions, strictly scoped to enabling local functionality. Below is a detailed breakdown of each permission requested:
* **`activeTab`**
  * *Purpose:* Grants the Extension temporary permission to interact with the currently active browser tab.
  * *Justification:* Used solely to access the DOM structure of ChatGPT, Claude, or Gemini when you explicitly click the Extension popup icon.
* **`scripting`**
  * *Purpose:* Allows the Extension to inject the document-level parsing engine (`parser.js`) into the active tab.
  * *Justification:* Required to read and extract the chat transcript from the webpage's DOM.
* **`storage`**
  * *Purpose:* Accesses Chrome's local storage APIs.
  * *Justification:* Used to temporarily store the extracted chat data and transfer it safely to the advanced studio dashboard (`viewer.html`), as well as to save your theme preferences and metadata settings.
* **`tabs`**
  * *Purpose:* Accesses the active tab's URL and title.
  * *Justification:* Used to populate export metadata header fields (e.g., source URL, platform, and date) and set the default export file name.
* **Host Permissions (`https://chatgpt.com/*`, `https://*.chatgpt.com/*`, `https://claude.ai/*`, `https://*.claude.ai/*`, `https://gemini.google.com/*`, `https://*.gemini.google.com/*`)**
  * *Purpose:* Grants permission to execute content scripts on these specific domains.
  * *Justification:* Restricts script injection capabilities exclusively to official ChatGPT, Claude, and Gemini URLs. The Extension cannot run or access data on any other websites.
---
## 4. Third-Party Services & Integrations
* **No Analytics/Telemetry:** The Extension does not integrate Google Analytics, Mixpanel, Sentry, or any other tracking, crash reporting, or telemetry SDKs.
* **No Ads or Tracker Scripts:** The Extension is entirely ad-free and tracker-free.
* **Platform Interaction:** The Extension interacts with ChatGPT (OpenAI), Claude (Anthropic), and Gemini (Google). These third-party websites have their own privacy policies. We encourage you to review their policies to understand how they process your data on their platforms.
---
## 5. Security & Browser Sandbox Boundaries
All operations are executed within the sandboxed environment provided by Google Chrome's Extension APIs. This ensures that:
* The parsed chat data cannot be accessed by other websites or extensions.
* No data is transmitted in transit over the internet, mitigating any risks of man-in-the-middle (MITM) attacks or data breaches.
* You can audit the network traffic of the Extension via Chrome DevTools to verify that no HTTP/HTTPS network requests are made by the Extension background or viewer pages.
---
## 6. GDPR and CCPA/CPRA Compliance
* **General Data Protection Regulation (GDPR):** Since we do not collect, process, or transmit personal data to any server, we do not transfer personal data outside the European Economic Area (EEA). The user remains in full custody and control of their data.
* **California Consumer Privacy Act (CCPA/CPRA):** We do not collect "Personal Information" as defined under California law. We do not "sell" or "share" personal information.
* **Data Erasure & Portability:** You can delete all data associated with the Extension at any time by right-clicking the Extension icon and selecting "Remove from Chrome," or by clearing your browser's site data/cookies.
---
## 7. Children's Privacy
Because the Extension collects zero information from users, it does not knowingly or unknowingly collect personal data from children under the age of 13 (in compliance with COPPA) or under the age of 16 (in compliance with GDPR).
---
## 8. Changes to this Privacy Policy
We may update this Privacy Policy from time to time to reflect changes in our Extension or Google Chrome developer policies. Any updates will be posted on this page with an updated "Last Updated" date. Because the Extension does not communicate with external servers, we cannot push notifications directly to you; we encourage you to review this policy periodically.
---
## 9. Contact Information
If you have any questions or concerns regarding this Privacy Policy or the security of the Extension, please contact us at:
* **Email:** support@chatarchivepro.example.com
* **GitHub Repository:** [Insert public repository link here if applicable]

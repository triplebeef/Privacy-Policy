# Reelo Privacy Statement

**Last updated:** 16 October 2026  
**Effective date:** 16 October 2026  
**Operator:** triplebeef  
**Privacy contact:** ReeloRecorder@gmail.com  
**Project:** [Reelo on GitHub](https://github.com/triplebeef)


This statement explains how Reelo handles information when you use the Windows desktop application, contact its operator, or use its diagnostic reporting features. “We”, “us” and “our” mean the operator named above.


## 1. Information Reelo handles on your device

### Recordings and related content

Depending on the features you select, Reelo can process screen or window images, system audio, microphone audio and webcam video. It can also process existing media for playback, editing, subtitle generation and summaries.

Reelo saves recordings and related files to the folder you select. Related files can include screenshots, subtitles, generated summaries and exported or edited media. You control which content you record and what you do with those files.

Your recordings and related content never leave your device.

### Settings, library state and local logs

Reelo stores application data locally, this can include:

- `settings.ini`: preferences, output locations, device selections, schedules and custom text used in editing features.
- `seen.txt`: file paths used to remember which library items have been marked as seen.
- `reelo.log`: local troubleshooting information, which can contain file paths, device names, licence information and error details.
- Downloaded AI models and local licence activation records.

These local files are **not automatically uploaded** as diagnostic reports.

### AI processing and models

Reelo's subtitle and summary features run on your device. Reelo does not send your recordings, audio, video frames, transcripts or generated summaries to a hosted AI inference service for these features.

When a required model is not installed, downloading it contacts the service that hosts the model and its delivery infrastructure. Downloading a model does not require uploading the media you want to process.

### Licensing

Reelo verifies signed licences locally and creates a device-bound activation record. A licence can contain the licence holder's name, an email address, a licence identifier and entitlement information.

The current activation process does not contact an activation server. Licence keys, licence holder details and licensing device identifiers will not be included in automatic diagnostic reports. Information you separately provide to request a licence or obtain support is covered by Section 6.

## 2. Planned diagnostic summaries

### Default setting and purpose

In the diagnostics-enabled release, basic diagnostic reporting will be **enabled by default**.

We will use these summaries to understand reliability, investigate compatibility problems, compare releases and improve Reelo's features and defaults. We will not use Reelo diagnostic reports for targeted advertising, cross-application tracking or decisions that produce legal or similarly significant effects about individuals. We will not sell or rent these reports.

### Information included

Reports will use a defined set of fields, rather than uploading arbitrary settings or free-form log messages.

| Category | Included information |
| --- | --- |
| Software environment | Reelo version, diagnostic format version and Windows version or version category. |
| Graphics environment | GPU vendor or broad graphics category, without hardware serial numbers or a hardware fingerprint. |
| Recording reliability | Counts of recording attempts, completed recordings, start failures, encoding failures and finalisation failures. |
| Capture and encoding | Capture methods, encoder categories, predefined error categories or codes, fallback attempts and recovery results. |
| Usage totals | Counts of feature use, such as screenshots, pausing, microphone or webcam use, subtitles, summaries, editing, exporting and scheduled recording. |
| Duration information | Recording-duration ranges or totals, without a timeline of individual recording sessions. |
| Selected preferences | Frame rate, quality, capture and encoder preferences, image or audio format, and whether relevant features are enabled. Custom text and paths are excluded. |
| Report administration | A reporting-period date, a random report identifier and delivery or receipt information needed to process the report and prevent duplicate counting. |

A random report identifier will identify a report for delivery and duplicate prevention. It will not be a persistent installation identifier, account identifier or licensing device identifier. Retries of the same report will use the same report identifier.

We will collect per-report summaries and combine them into aggregate statistics. We do not describe these reports as completely anonymous: connection metadata and combinations of technical information may still relate to an individual.

### Information excluded

Automatic diagnostic reports will **not** include:

- Recordings, screenshots, screen images, audio or webcam footage.
- Transcripts, subtitle text, AI prompts or generated summaries.
- Filenames, file paths, recording titles, window titles or browsing URLs.
- The contents of `reelo.log`, `settings.ini` or `seen.txt`.
- Custom watermark text, title-card text or other user-written content.
- Licence keys, licence holder names or emails, licensing device IDs, machine GUIDs, hardware serial numbers or a persistent installation ID.
- Exact recording schedules, precise recording-session start times or saved screen-region coordinates.

The diagnostic integration will not enable PostHog Session Replay, automatic click capture, heatmaps or behavioural advertising.

### Sending reports

Reelo will prepare summaries locally and ordinarily send them approximately once per day while the application is running and reporting is enabled. Offline reports may be queued and retried. The queue will have a size and age limit; unsuccessful delivery will not prevent normal recording.

The planned delivery path is:

**Reelo → Cloudflare Worker → PostHog EU → private aggregate dashboards**

## 3. Cloudflare, PostHog and network information

### Cloudflare

Cloudflare will host the diagnostic upload endpoint and process incoming requests before forwarding accepted summaries to PostHog. Handling an internet connection necessarily exposes network information to Cloudflare, such as the source IP address, request time and connection or security metadata.

We will not intentionally include client IP addresses in diagnostic report fields or forward the original client IP as an analytics property. Cloudflare may separately process or retain operational and security information under its applicable service terms and privacy documentation.

### PostHog EU

We have selected **PostHog EU** for diagnostic analytics storage. PostHog states that its EU-hosted customer-user data is stored and processed on servers in Germany. Provider support, subprocessors and other operational processing may involve other countries.

Our integration will be configured to discard client IP data from stored analytics events, disable IP-based location enrichment and avoid creating individual person profiles. These settings do not mean that the network connection is invisible to the service providers.

### International processing

Using PostHog EU does not mean every request or every item of provider operational information is processed exclusively in the European Union. Cloudflare operates a global network, and our providers and their subprocessors may process information in Germany, the United States and other countries described in their documentation. Applicable contractual safeguards will be used where required.

| Provider | Purpose | Privacy information |
| --- | --- | --- |
| Cloudflare | Diagnostic request handling, delivery and service security | [Cloudflare Privacy Policy](https://www.cloudflare.com/privacypolicy/) |
| PostHog | Diagnostic event storage and aggregate analytics, using our EU project | [PostHog Privacy Policy](https://posthog.com/privacy) |
| Hugging Face | Delivery of downloadable local AI model files | [Hugging Face Privacy Policy](https://huggingface.co/privacy) |
| GitHub | Hosting project information and this privacy statement; any support information you choose to post there | [GitHub General Privacy Statement](https://docs.github.com/en/site-policy/privacy-policies/github-general-privacy-statement) |


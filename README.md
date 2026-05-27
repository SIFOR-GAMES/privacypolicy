# CatVerse — Privacy Policy

**Effective date:** 2026-05-15
**Application:** com.sifor.catgame
**Vendor:** CatVerse

---

## TL;DR

**CatVerse does not collect, transmit, or share any personal
information about you, your TV, your viewing habits, or your
cat.** The app makes no requests to CatVerse-owned servers, has
no analytics, and never accesses the camera or microphone on LG
webOS TVs.

The app ships with one third-party SDK — **BrightSDK** by
Bright Data Ltd. — which keeps CatVerse free for everyone. It
is **opt-in** and described in full below. You can disable it
at any time from **Settings → Web Indexing**.

---

## 1. Data we do **not** collect

- We do **not** collect names, email addresses, phone numbers, or any
  other personally identifiable information (PII).
- We do **not** collect device identifiers (LG account ID, MAC
  address, etc.) for CatVerse's own use.
- We do **not** collect viewing history, voice samples, or pet data.
- We do **not** integrate any analytics, advertising, social, or
  crash-reporting SDKs other than the BrightSDK runtime described
  below.

## 2. Data stored on your device

The app stores **only** the following data in the browser's
`localStorage`. This data never leaves your TV and is removed
when the app is uninstalled:

| Key | Purpose | Example |
|---|---|---|
| `cv.settings.v1` | Your chosen play speed, volume, auto-pause minutes, protect-mode flag, and per-prey enable toggles | `{ "speed": 1.0, ... }` |

You can clear this at any time by uninstalling CatVerse from the
LG Content Store.

## 3. Third-party SDK: BrightSDK (Bright Data Ltd.)

CatVerse is free for cats around the world because we share a
small amount of your TV's **unused internet bandwidth** while you
are running the app. This is delivered by the BrightSDK runtime,
which ships as a peer service inside the IPK
(`com.sifor.catgame.brd_sdk`).

### What BrightSDK does
- Routes anonymous web requests (commercial-grade web data
  collection - SEO checks, price comparison, brand protection)
  through your TV's idle internet connection while the app is
  open.
- Communicates only with the BrightSDK peer service and the
  Bright Data network. Bright Data publishes its own policy at
  <https://bright-sdk.com/terms> and <https://bright-sdk.com/privacy>.

### What BrightSDK does **not** do
- It does **not** access your TV's screen, files, viewing
  history, or any LG account information.
- It does **not** transmit any personally identifiable
  information about you. Bright Data treats your TV as an
  anonymous peer and does not link traffic to any user identity.
- It does **not** stream other users' content through your TV;
  the traffic is short-lived API/web-fetch requests, not video.

### Consent and control
- On first launch CatVerse displays the BrightSDK consent dialog
  before any bandwidth sharing begins. You may **opt in** to
  keep the app free, or decline.
- If you decline, CatVerse continues to work normally without
  any bandwidth sharing.
- You can change your decision at any time from
  **Settings → Web Indexing**.

### Why this design
- It allows the app to remain **free and ad-free**, which is
  better for both you and your cat than advertising.
- The TV's actual capacity used is tiny (typically a few KB/s
  while idle); LG TVs report no measurable effect on streaming
  performance during testing.

## 4. Bright SDK Terms of Service

In return for premium features of CatVerse, you may choose to be
a peer on the Bright Data network. By doing so, you agree to have
read and accepted the
[Bright SDK EULA](https://bright-sdk.com/eula) and
[Bright Data's Privacy Policy](https://bright-sdk.com/privacy-policy).

You may opt out of the Bright Data network at any time by opening
**Settings → Web Indexing** and selecting **Opt out**.

## 5. Permissions

- **Camera:** never requested.
- **Microphone:** never requested on webOS TVs. (A
  `MicAdapter` interface exists in source for forward
  compatibility, but the TV build does not call `getUserMedia`.)
- **Location:** never requested.
- **Storage:** browser `localStorage`, as listed in section 2.

## 6. Network use

- **CatVerse itself** is fully offline. The gameplay does not
  make any HTTP or WebSocket requests during normal use.
- **BrightSDK** (if you opted in) communicates with the Bright
  Data network in the background. See section 3.
- App **updates** are delivered solely through the LG Content
  Store.

## 7. Children

CatVerse is suitable for all ages. The app does not contain
advertising, in-app purchases, or any user-generated content.

## 8. Contact

For privacy questions, contact: **privacy@catverse.example**
(replace with your verified seller contact before submission).

For questions specific to BrightSDK bandwidth sharing, see
<https://bright-sdk.com/contact>.

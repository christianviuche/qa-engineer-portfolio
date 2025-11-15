
# 12: Mobile Automation

This section covers **Mobile Automation**, the process of testing applications that run on mobile devices like phones and tablets (iOS and Android).

This is distinct from Frontend testing because it usually involves testing **Native Apps** (apps downloaded from the App Store / Play Store), not just websites in a mobile browser.

---

## Native vs. Hybrid vs. Web

A key concept in mobile testing is the *type* of app:

* **Native App:** Built specifically for one OS (iOS or Android) using native code (Swift/Kotlin). They are fast and have access to all device hardware (camera, GPS). **(e.g., WhatsApp, Instagram)**.
* **Hybrid App:** One "web" app (built with HTML, CSS, JS) that is wrapped in a native "shell." It *looks* like a native app but is actually a website inside. **(e.g., many banking apps)**.
* **Mobile Web App:** Just a regular website (like your portfolio) accessed through a mobile browser (Chrome, Safari).

---

## Key Tools & Frameworks

The tool you choose depends *entirely* on the type of app you are testing.

### 1. Cross-Platform Frameworks (Nativo & Híbrido)

* **Appium:**
    * **What:** The **industry standard** for mobile automation. It's an open-source, "cross-platform" tool.
    * **Pros:** You can write *one* test script (in Java, Python, JS, etc.) and run it on *both* iOS and Android. It works for Native, Hybrid, and Mobile Web apps. It is the "Selenium for Mobile."
    * **Cons:** Can be complex and slow to set up.

* **Detox (by Wix):**
    * **What:** A modern, "gray box" automation framework for **React Native** apps.
    * **Pros:** Extremely fast and much more reliable (less flaky) than Appium, *if* your app is built with React Native. It runs tests from the "inside" of the app.

### 2. Native Frameworks (Nativo Puro)

These tools are provided by Google and Apple. They are extremely fast and reliable but **only work for their own platform** (you cannot test an iOS app with Espresso).

* **Espresso (by Google):**
    * **What:** The native, "white box" testing framework for **Android**.
    * **Use:** Used by developers and SDETs to write fast, reliable tests. It has direct access to the app's code.

* **SwiftTesting / XCUITest (by Apple):**
    * **What:** The native framework for **iOS**. (XCUITest is the UI testing part, and SwiftTesting is the newer framework).
    * **Use:** The official way to write fast, reliable UI tests for iOS apps, written in Swift.

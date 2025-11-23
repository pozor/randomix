# Frequently Asked Questions (FAQ)

Common questions about Randomix and their answers.

---

## General

### What is Randomix?
Randomix is a free, ad-free iOS app for generating random numbers and phrases with advanced features like weighted probabilities, statistical distributions, and complete history tracking.

### Is Randomix really free?
Yes! Randomix is 100% free with no ads, no in-app purchases, and no subscriptions.

### Does Randomix work offline?
Yes. Randomix works completely offline and never requires an internet connection.

### What devices are supported?
- **iPhone:** iOS 13.4 or later (iPhone 6s and newer)
- **iPad:** iPadOS 13.4 or later (all models)
- **iPod touch:** 7th generation or later

**Not supported:** Apple Watch, Apple TV, Mac (Catalyst)

---

## Privacy & Data

### Is my data private?
Absolutely. Randomix collects **zero data**. Everything stays on your device. See the [Privacy Policy](PRIVACY_POLICY.md) for details.

### Where is my data stored?
All data (phrases, history, settings) is stored locally on your device using iOS secure storage. Nothing is sent to external servers.

### Can I sync data between devices?
Not currently. Since Randomix is fully offline with no cloud backend, data stays on each device. I may add iCloud sync in a future update if requested.

### What happens to my data if I uninstall the app?
All data is permanently deleted when you uninstall. There's no way to recover it since nothing is backed up externally.

---

## Number Generator

### How does the Number Generator work?
It generates cryptographically secure random integers within your specified min/max range using iOS's `SecRandomCopyBytes`.

### What's the maximum range I can use?
You can generate numbers from -2,147,483,648 to 2,147,483,647 (32-bit integer range).

### What does "Allow repetitions" mean?
- **ON** (default): The same number can be generated multiple times
- **OFF**: Each number can only appear once until all unique numbers are exhausted

**Example:** Range 1-10, repetitions OFF
- You can generate exactly 10 unique numbers (1, 2, 3... 10)
- After 10 generations, an alert appears: "All unique numbers used. Reset to continue."

### How do I clear the history?
Open the History modal (📋 button) and tap the "Clear History" button. This only clears history, not your settings.

### How do I sort the history?
Use the 4 sorting buttons in the History modal:
- **Recent:** Newest first (default)
- **↓:** Oldest first
- **↑ 1→9:** Smallest to largest
- **↓ 9→1:** Largest to smallest

### Why does history show "100 of 1000 items"?
The modal displays the first 100 items of the sorted history, but sorting is done on **all** saved items (up to 1000 for distributions). This keeps the UI fast while preserving complete data.

---

## Phrase Generator

### How do I add phrases?
Tap the "Add Phrase" button (+ icon), enter your text and weight (1-10), then tap "Save".

### What are weights and how do they work?
Weights determine probability. Higher weight = more likely to be selected.

**Formula:** P(phrase) = weight / total_weights

**Example:**
- Phrase A: weight 5
- Phrase B: weight 2
- Phrase C: weight 3
- **Total:** 5 + 2 + 3 = 10

**Probabilities:**
- A: 5/10 = 50%
- B: 2/10 = 20%
- C: 3/10 = 30%

### Can I use equal probability?
Yes! If you don't specify weights (or use weight=1 for all), phrases are selected with equal probability.

### How do I edit or delete phrases?
- **Edit:** Tap the phrase to open the edit modal
- **Delete:** Swipe left on the phrase and tap "Delete"

### What does "Allow repetitions" mean for phrases?
- **ON** (default): The same phrase can be selected multiple times
- **OFF**: Each phrase can only appear once until all phrases are selected (then resets)

### How many phrases can I add?
There's no hard limit, but performance is optimized for up to ~500 phrases. The UI remains smooth with thousands of phrases.

---

## Statistical Distributions

### What are statistical distributions?
Mathematical models that describe how random values are distributed. Randomix includes 7 types:
- **Uniform (Discrete):** Equal probability for all values
- **Normal (Gaussian):** Bell curve, common in nature (heights, test scores)
- **Exponential:** Time between events (customer arrivals, radioactive decay)
- **Poisson:** Count of events (emails per hour, defects per batch)
- **Binomial:** Success/failure trials (coin flips, A/B tests)
- **Weibull:** Reliability analysis and failure rates
- **Triangular:** Three-point estimation (min, mode, max)

### How do I use distributions?
1. Go to the **Distributions** tab (3rd tab)
2. Tap **"Select Distribution"** to choose a type
3. Configure parameters (μ, σ, λ, etc.) based on the distribution
4. Tap **"Generate"** to create a random value

### Do distributions have visualizations?
Yes! Each distribution includes:
- Interactive histogram showing your generated values
- Reference curve (blue) from 1,000 theoretical samples
- Real-time statistics (min, max, mean, median)
- Comparison overlay (visible after 20+ generations)

### How do I interpret the distribution chart?
- **Blue curve:** Theoretical reference (what the distribution should look like)
- **Red curve:** Your actual generated values (appears after 20+ samples)
- **Closer match:** Your values converge to theory as you generate more

### Can I use distributions for scientific research?
Randomix uses cryptographically secure randomness (iOS `SecRandomCopyBytes`), which is statistically rigorous for most purposes. However, it's not certified for formal peer-reviewed research. For academic studies, use dedicated software (R, Python SciPy, MATLAB).

---

## Advanced Features

### What is "Shake-to-Generate"?
Shake your device to generate a result instead of tapping the button. Works on all three tabs (Numbers, Phrases, Distributions).

### How do I enable Shake-to-Generate?
Settings tab → Toggle **"Shake to Generate"** ON. Shake your device to test it!

### How hard do I need to shake?
The threshold is calibrated to **2.5g acceleration** (moderate shake). Normal walking or light movement won't trigger it.

### Why doesn't shake work immediately after?
There's a **1-second cooldown** (debounce) to prevent multiple triggers from a single shake.

### Does shake work with VoiceOver?
Yes! Shake-to-generate is **WCAG 2.5.4 compliant**:
- It's **opt-in** (OFF by default)
- The generate button is always available as an alternative
- It respects "Reduce Motion" (disabled if enabled)

### What is the Christmas Theme?
A festive theme with red/green colors and **animated falling snow** (30 particles). Perfect for the holiday season!

### Does the snow animation affect battery?
No. The animation is **GPU-accelerated** and optimized for 60fps with negligible battery impact. If you enable "Reduce Motion" in iOS settings, the snow disappears automatically.

---

## Settings

### How do I change the theme?
Settings tab → Tap a theme card (White, Dark, Modern, or Christmas). Changes apply instantly.

### How do I change the language?
Settings tab → Language → Select from 6 languages. The app automatically uses your system language on first launch.

### What languages are supported?
- 🇬🇧 English
- 🇮🇹 Italian (Italiano)
- 🇫🇷 French (Français)
- 🇩🇪 German (Deutsch)
- 🇪🇸 Spanish (Español)
- 🇵🇹 Portuguese (Português)

**Want another language?** [Request it here!](https://github.com/pozor/randomix/issues/new?template=feature_request.md)

### Do settings persist after closing the app?
Yes. All settings (theme, language, ranges, phrases) are saved and restored when you reopen the app.

### How do I reset to defaults?
Currently, you must manually change each setting.

---

## Accessibility

### Is Randomix accessible?
Yes! Randomix is **WCAG 2.1 Level AA Compliant** with a perfect 10/10 accessibility score.

### What screen readers are supported?
- **iOS:** VoiceOver

All buttons, inputs, and content have proper labels and semantic roles.

### Does Randomix support Dynamic Type (larger text)?
Yes. All text respects iOS Dynamic Type settings (Settings → Accessibility → Display & Text Size → Larger Text).

### What about color blindness?
All themes have been tested for:
- Deuteranopia (red-green)
- Protanopia (red-green)
- Tritanopia (blue-yellow)

The app uses high-contrast colors and never relies solely on color to convey information.

### Does Randomix respect "Reduce Motion"?
Yes. If you enable "Reduce Motion" (Settings → Accessibility → Motion), animations are minimized or removed.

### Found an accessibility issue?
Please [report it immediately](https://github.com/pozor/randomix/issues/new?template=bug_report.md). I prioritize accessibility fixes.

---

## Technical

### What technology is Randomix built with?
- **Framework:** React Native with Expo
- **Language:** TypeScript
- **Navigation:** React Navigation (Bottom Tabs)
- **Storage:** AsyncStorage (local, secure)
- **Internationalization:** i18next
- **Charts:** react-native-chart-kit

### Does Randomix use third-party services?
**No.** Randomix uses zero third-party services:
- ❌ No analytics (Google Analytics, Firebase, etc.)
- ❌ No crash reporting (Sentry, Crashlytics)
- ❌ No ad networks
- ❌ No social media SDKs
- ❌ No payment processors

### How is randomness generated?
Randomix uses iOS's `SecRandomCopyBytes` (cryptographically secure random number generator) combined with algorithm-specific transformations for distributions (e.g., Box-Muller for Normal, Knuth for Poisson).

### Is the randomness "truly random"?
It's cryptographically secure pseudorandom (CSPRNG), which is indistinguishable from true randomness for all practical purposes. Suitable for games, simulations, and non-cryptographic use cases.

For quantum randomness or cryptographic key generation, use dedicated hardware random number generators.

---

## Troubleshooting

### App crashes on launch
1. **Force quit** the app: Swipe up from Home and flick Randomix away
2. **Restart your device**
3. **Update iOS** (Settings → General → Software Update)
4. **Reinstall the app** (⚠️ deletes data)
5. If still crashing, [report a bug](https://github.com/pozor/randomix/issues/new?template=bug_report.md)

### History is empty after update
This should never happen. If it does:
1. **Don't uninstall** (will permanently delete data)
2. [Report an urgent bug](https://github.com/pozor/randomix/issues/new?template=bug_report.md) with your iOS version and app version
3. Check if data is in another tab's history (unlikely, but worth checking)

### Phrases disappeared
1. Check if you're on the correct device (data doesn't sync between devices)
2. Check if you accidentally cleared them (History → Clear All)
3. If truly gone without action, [report a critical bug](https://github.com/pozor/randomix/issues/new?template=bug_report.md)

### VoiceOver not announcing correctly
1. **Update iOS** (Apple improves VoiceOver with each release)
2. **Toggle VoiceOver off/on** (Settings → Accessibility → VoiceOver)
3. If specific element is broken, [report an accessibility bug](https://github.com/pozor/randomix/issues/new?template=bug_report.md) with:
   - Which element (e.g., "History button in Number Generator")
   - What it says (incorrect announcement)
   - What it should say (expected announcement)

### Theme changes don't save
1. **Close the app completely** (swipe up from Home) and reopen
2. If still not saving, [report a bug](https://github.com/pozor/randomix/issues/new?template=bug_report.md)

### How do I report other issues?
See [SUPPORT.md](SUPPORT.md) for all support channels.

---

## App Store

### When will Randomix be available?
**Coming soon!** Submission to the App Store is pending completion of the Distributions feature.

### How much does it cost?
**Free.** No ads, no in-app purchases, no subscriptions.

### Will there be a paid version?
Not currently planned. If I add premium features in the future, the core functionality (numbers, phrases, distributions) will always remain free.

### Is there an Android version?
Randomix is currently iOS-only. An Android version is under consideration based on demand.

---

## Feature Requests

### How do I suggest a feature?
[Open a feature request!](https://github.com/pozor/randomix/issues/new?template=feature_request.md)

---

## Still Have Questions?

- 📖 **Read the docs:** [README.md](README.md) | [SUPPORT.md](SUPPORT.md) | [PRIVACY_POLICY.md](PRIVACY_POLICY.md)
- ❓ **Ask a question:** [Open an issue](https://github.com/pozor/randomix/issues/new?template=question.md)
- 🐛 **Report a bug:** [Bug report](https://github.com/pozor/randomix/issues/new?template=bug_report.md)
- 💡 **Suggest a feature:** [Feature request](https://github.com/pozor/randomix/issues/new?template=feature_request.md)

---

**Last Updated:** November 20, 2025

© 2025 Randomix. All rights reserved.

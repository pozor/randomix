# Contributing to Randomix

Thank you for your interest in making Randomix better! 🎉

---

## 📌 Important Note

**Randomix is a proprietary app.** The source code is not open source and is not available in this repository.

However, **I warmly welcome contributions in the form of:**
- 🐛 Bug reports
- 💡 Feature requests
- 📖 Documentation improvements
- 🌍 Translation corrections
- ❓ Questions and discussions

This repository is specifically for **public support and issue tracking**.

---

## 🐛 Reporting Bugs

Found a bug? Help me squash it!

### Before Reporting
1. **Search existing issues** to avoid duplicates
2. **Update to the latest version** from the App Store
3. **Restart your device** to rule out temporary glitches
4. **Check [FAQ.md](FAQ.md)** - it might be a known issue

### How to Report

**[Create a Bug Report →](https://github.com/pozor/randomix/issues/new?template=bug_report.md)**

A great bug report includes:

#### Required Information
- **iOS Version** (Settings → General → About → Software Version)
- **Randomix Version** (visible in Settings tab of the app)
- **Device Model** (iPhone 12, iPad Pro, etc.)
- **Clear description** of the problem

#### Steps to Reproduce
Provide step-by-step instructions:
```
1. Open Number Generator tab
2. Set min=100, max=50 (invalid range)
3. Tap "Generate Number"
4. Observe: App crashes instead of showing error
```

#### Expected vs Actual Behavior
- **Expected:** Error message "Max must be greater than min"
- **Actual:** App crashes with white screen

#### Supporting Materials
- **Screenshots** - Show the issue visually
- **Screen recordings** - For complex interactions
- **Console logs** - If you're technical (Settings → Privacy & Security → Analytics)

### Bug Report Template
The template will guide you through the process. Just fill in the blanks!

---

## 💡 Suggesting Features

Have an idea? I'd love to hear it!

### Before Suggesting
1. **Search existing feature requests** - it might already be proposed
2. **Consider if it fits Randomix's scope** - random generation and statistics

### How to Suggest

**[Create a Feature Request →](https://github.com/pozor/randomix/issues/new?template=feature_request.md)**

A great feature request includes:

#### Problem Statement
What problem are you trying to solve?
```
"I often need to generate lottery numbers (e.g., 6 numbers from 1-49 without repetitions).
Currently, I have to generate 6 times and manually check for duplicates."
```

#### Proposed Solution
How would you solve it?
```
"Add a 'Batch Generate' mode that generates N unique numbers at once and displays
them as a list."
```

#### Alternatives Considered
What other approaches did you think about?
```
"I considered using the 'Allow repetitions OFF' feature, but it doesn't show
all generated numbers together."
```

#### Use Cases
How would you (and others) use this?
```
"Useful for:
- Lottery number selection
- Random team assignments
- Raffle ticket generation
- Bingo card creation"
```

### What Happens Next?
1. I'll review your suggestion (usually within 7 days)
2. I'll label it (e.g., `enhancement`, `needs discussion`)
3. Community members can vote with 👍 reactions
4. Popular features may be prioritized for future releases

**Note:** I can't implement every request, but I value all feedback!

---

## 📖 Improving Documentation

Documentation lives in this repository and is open to contributions!

### What You Can Improve
- **Fix typos** in README, SUPPORT, FAQ, etc.
- **Clarify confusing sections**
- **Add missing information** (e.g., new FAQ entries)
- **Improve translations** (non-English documentation)

### How to Contribute Docs

**Option 1: Simple Edits (GitHub Web)**
1. Navigate to the file (e.g., `FAQ.md`)
2. Click the pencil icon (Edit this file)
3. Make your changes
4. Scroll down and click "Propose changes"
5. Create a Pull Request

**Option 2: Formal Pull Request**
```bash
# Fork the repository on GitHub
git clone https://github.com/pozor/randomix.git
cd randomix

# Create a branch
git checkout -b docs/fix-faq-typo

# Make your changes
# Edit FAQ.md, README.md, etc.

# Commit
git add .
git commit -m "docs: fix typo in FAQ question 5"

# Push and create PR
git push origin docs/fix-faq-typo
# Then open a Pull Request on GitHub
```

### Documentation Style Guide
- Use **clear, concise language**
- **Avoid jargon** (or explain it)
- Use **examples** when possible
- Use **emoji sparingly** (only for visual hierarchy)
- Use **relative links** for internal docs (`[FAQ](FAQ.md)` not full URLs)
- Follow **Markdown best practices**

---

## 🌍 Translation Contributions

Randomix supports 6 languages. Found an error in a translation?

### Supported Languages
- 🇬🇧 English (primary)
- 🇮🇹 Italian (Italiano)
- 🇫🇷 French (Français)
- 🇩🇪 German (Deutsch)
- 🇪🇸 Spanish (Español)
- 🇵🇹 Portuguese (Português)

### How to Report Translation Issues

**[Open a Bug Report →](https://github.com/pozor/randomix/issues/new?template=bug_report.md)**

Include:
- **Language** affected (e.g., German)
- **Current (incorrect) text** - exact wording and screenshot
- **Location** - which screen/button/message (screenshot helps!)
- **Suggested correction** - your proposed translation
- **Context** - explain nuance if needed

**Example:**
```
Language: French
Screen: Number Generator → History
Current text: "Valeurs précédentes" (Previous values)
Suggested: "Historique des résultats" (History of results)
Reason: "Historique" is more common for "History" in UI contexts
```

**Note:** Translations are managed in the private codebase, so I'll apply your corrections in the next update.

---

## ❓ Asking Questions

Not sure how something works? Just ask!

**[Ask a Question →](https://github.com/pozor/randomix/issues/new?template=question.md)**

### Good Questions
- "How does weighted probability work in the Phrase Generator?"
- "What's the difference between Normal and Exponential distributions?"
- "Can I export my phrase lists to another device?"
- "Does Randomix support Apple Watch?"

### Questions Best Answered Elsewhere
- **"How do I download the app?"** → See [README.md](README.md#-download)
- **"Is my data private?"** → See [PRIVACY_POLICY.md](PRIVACY_POLICY.md)
- **"How do I report a bug?"** → See [SUPPORT.md](SUPPORT.md#-report-a-bug)
- **App Store reviews** → Not monitored, use GitHub Issues instead

---

## 🎨 Design Feedback

Have thoughts on the UI/UX?

### What I Welcome
- **Accessibility issues** (e.g., "Low contrast on Dark theme")
- **Usability problems** (e.g., "Hard to find the History button")
- **Design inconsistencies** (e.g., "Settings icon differs across tabs")

### How to Provide Feedback
1. [Open a Feature Request](https://github.com/pozor/randomix/issues/new?template=feature_request.md)
2. Use label `design` or `ui/ux` (I'll add it)
3. Include screenshots or mockups if possible
4. Explain the problem before suggesting solutions

**Example:**
```
Problem: The "Generate" button blends in with the background on Modern theme
Impact: Users with low vision may struggle to find it
Suggestion: Increase contrast or add a border
Screenshot: [attached]
```

---

## 🏷️ Issue Labels

I use labels to organize issues:

### Type Labels
- `bug` - Something isn't working
- `enhancement` - New feature or improvement
- `question` - Need clarification or help
- `documentation` - Improvements to docs

### Priority Labels
- `critical` - Crashes, data loss (handled ASAP)
- `high` - Major issues affecting many users
- `medium` - Moderate issues
- `low` - Minor issues or nice-to-haves

### Status Labels
- `needs reproduction` - Cannot reproduce, need more info
- `confirmed` - Issue verified by maintainers
- `in progress` - Actively being worked on
- `blocked` - Waiting on something else
- `wontfix` - Won't be addressed (with explanation)

### Special Labels
- `good first issue` - Easy tasks for newcomers
- `help wanted` - Community input needed
- `duplicate` - Already reported elsewhere
- `accessibility` - Related to accessibility features
- `translation` - Related to language/i18n

---

## 📋 Issue Etiquette

### Do's ✅
- **Be respectful and constructive**
- **Provide complete information** (versions, steps, screenshots)
- **Stay on topic** (one issue per report)
- **Search before posting** (avoid duplicates)
- **Follow up** if I request more info
- **React with 👍** to issues you also experience (helps me prioritize)

### Don'ts ❌
- **Don't bump issues** with "+1" comments (use 👍 reactions)
- **Don't demand features** ("You MUST add this!")
- **Don't report multiple bugs** in one issue (split them up)
- **Don't post personal/sensitive info** (email, phone, etc.)
- **Don't use issues for support questions** (unless it's about the docs)

---

## 🚀 Release Process

### How Features Get Added
1. Feature request opened
2. Community discussion and voting
3. I evaluate feasibility
4. Feature added to roadmap (if approved)
5. Implementation (timeline varies)
6. Testing and review
7. Release in next app update

### Release Schedule
Updates will be released as needed based on bug fixes and new features.

---

## 🔒 Security Issues

**Found a security vulnerability?**

**DO NOT** open a public issue. Instead:

**Email:** security@randomix.app *(placeholder - update with real email)*

Include:
- Vulnerability description
- Steps to reproduce
- Potential impact
- Suggested fix (if you have one)

I'll respond within 24 hours.

---

## 📜 Code of Conduct

### My Pledge
I'm committed to providing a welcoming, inclusive, harassment-free experience for everyone, regardless of age, body size, disability, ethnicity, gender identity, experience level, nationality, personal appearance, race, religion, or sexual identity.

### Standards
**Positive behaviors:**
- Using welcoming and inclusive language
- Being respectful of differing viewpoints
- Gracefully accepting constructive criticism
- Focusing on what's best for the community

**Unacceptable behaviors:**
- Harassment, insults, or derogatory comments
- Public or private harassment
- Publishing others' private information
- Trolling or sustained disruption

### Enforcement
Violations should be reported to: conduct@randomix.app *(placeholder - update with real email)*

I may remove, edit, or reject contributions that violate this Code of Conduct.

---

## 🙏 Recognition

### Contributors
Contributors who help improve Randomix will be recognized in:
- **GitHub Contributors** - Appears on the repo
- **Special thanks** - Major contributors may get a shout-out

### What Counts as a Contribution?
- Reporting a critical bug
- Suggesting an implemented feature
- Improving documentation
- Helping other users in issues

---

## 📞 Questions About Contributing?

**[Open a Question Issue →](https://github.com/pozor/randomix/issues/new?template=question.md)**

I'm happy to help you get started!

---

## 📚 Additional Resources

- **[README.md](README.md)** - Project overview
- **[SUPPORT.md](SUPPORT.md)** - Getting help
- **[FAQ.md](FAQ.md)** - Common questions
- **[PRIVACY_POLICY.md](PRIVACY_POLICY.md)** - Privacy information

---

**Thank you for contributing to Randomix!** 🎉

Your feedback and suggestions make the app better for everyone.

---

© 2025 Randomix. All rights reserved.

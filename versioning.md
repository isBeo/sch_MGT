# Semantic Versioning (SemVer)
---
***🔢 What does 1.0.1 mean?***

follows this structure:
***MAJOR.MINOR.PATCH***

**Breakdown:**
- MAJOR (1) → Big changes, breaking stuff
- MINOR (0) → New features, but still compatible
- PATCH (1) → Small fixes (bugs, improvements)
---

📦 Real Meaning of 1.0.1
- 1 → First stable release (big milestone)
- 0 → No new features added since 1.0.0
- 1 → One bug fix applied

***👉 So 1.0.1 = “Same app, just fixed something small”***

---

## 🔄 How versioning works on GitHub

On Git / GitHub, versioning is usually done with:
- Tags

You mark a specific commit as a version:


```bash
git tag v1.0.0
git push origin v1.0.0
```

- Commit Flow Example

Let’s say you’re building a project:

Step | Change | Version
-----|--------|---------
First working app |	Initial release | 1.0.0
Fix login bug | Small fix | 1.0.1
Add new feature (e.g dashboard) | Feature |	1.1.0
Rewrite backend (breaking change) |	Major change | 2.0.0

---

### 🚨 When to increase each number

🔴 **MAJOR → 2.0.0**
* You break existing code
* API changes
* Old users must update things

🟡 **MINOR → 1.1.0**
* Add new features
* Backward compatible

🟢 **PATCH → 1.0.1**

* Fix bugs
* Improve performance

---

## ⚡ Real-world example

A project could go like:

```
    0.1.0 → first prototype
    0.2.0 → added login
    0.2.1 → fixed login bug
    1.0.0 → stable release
    1.1.0 → added dashboard
    1.1.1 → fixed dashboard bug
```

---

## Writting a [CHANGELOG](https://chatgpt.com/c/69dc5a11-bbb4-83ea-9ce4-bddfe9b52c16#:~:text=Or-,how%20to%20write%20a%20clean%20CHANGELOG.md%20like%20professionals,-You%20said%3A) like professionals


A CHANGELOG [markdown] is a file where you clearly document what changed in each version of your project.

**Professionals usually follow a standard called**:
*👉 Keep a Changelog*

``` 
markdown:

# Changelog

All notable changes to this project will be documented in this file.

The format is based on Keep a Changelog
and this project adheres to Semantic Versioning.

---

## [1.0.1] - 2026-04-13
### Fixed
- Fixed login bug where users could not authenticate

---

## [1.0.0] - 2026-04-10
### Added
- Initial release
- User authentication system
- Basic dashboard

---

## [0.1.0] - 2026-04-05
### Added
- Project setup
```

---

#### 🧠 Sections you should use

Each version can have these categories:

* ✨ Added
* New features
* 🔧 Changed
* Updates to existing features
* ❌ Fixed
* Bug fixes
* 🗑️ Removed
* Deleted features
* 🔒 Security
* Vulnerability fixes

#### 🧱 Real Example (More Professional)

```
# Changelog

## [1.1.0] - 2026-04-15
### Added
- Dashboard analytics page
- User profile editing

### Changed
- Improved API response time

---

## [1.0.1] - 2026-04-13
### Fixed
- Fixed crash when login fields are empty
- Resolved token expiration issue

---

## [1.0.0] - 2026-04-10
### Added
- Full authentication system
- REST API endpoints for users
```

### 🔥 Pro Tips (this is where pros differ)
1. Use dates

Always include:
```
YYYY-MM-DD
```
---
2. Write for humans, not machines

❌ Bad:
```
- fix bug

```

✅ Good:

```
- Fixed issue where login fails when password is empty
```

3. Group changes

```

Don’t mix everything:

❌ Messy:

- Added login
- Fixed bug
- Changed UI

✅ Clean:

### Added
- Login system

### Fixed
- Login validation bug

### Changed
- Updated UI styling
```
---
4. Keep newest version at the top

Always reverse order:
```
Latest
↓
Oldest

```
---

### ⚙️ How it connects to GitHub workflow

When you:

1. Make changes
2. Commit code
3. Tag version (v1.0.1)
Update CHANGELOG.md

👉 Then push to GitHub
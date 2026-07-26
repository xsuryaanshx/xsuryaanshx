# Palette's Journal

This journal documents critical UX and accessibility learnings while improving projects in this repository.

## 2025-01-23 - GitHub Profile README Alt Text
**Learning:** Dynamic badges and widgets (like GitHub Stats, Streak, Top Languages, and Trophies) are widely used in profile READMEs to showcase developer achievements, but they are almost always added without alt text. This makes them completely invisible/meaningless to screen readers, which is a major accessibility issue for developer portfolios.
**Action:** Always provide descriptive alt text for SVGs, stats cards, trophies, and visit counter widgets in Markdown files.

## 2025-01-23 - GitHub Profile Case-Sensitivity and Active Mirrors
**Learning:**
1. GitHub is strictly case-sensitive for profile repository README matching. A lowercase file named `readme.md` will fail to display in the profile section, whereas renaming it to uppercase `README.md` immediately makes it visible on the profile.
2. The default hosted public deployment of `github-readme-stats` on Vercel is currently paused (`DEPLOYMENT_PAUSED` 503 error), breaking stats on thousands of developer profiles. Pointing to the active community mirror `github-readme-stats-fast.vercel.app` is an excellent, drop-in solution to restore user statistics.
**Action:** Always ensure the profile README is named uppercase `README.md` and use the active community mirror `github-readme-stats-fast.vercel.app` for reliable stats loading.

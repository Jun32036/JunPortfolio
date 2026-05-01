# Repository Audit Tasks

## 1) Fix a spelling/wording issue
- **Task:** Standardize mixed-language spacing in skill labels by changing `ERP系統操作` to `ERP 系統操作` for readability and consistency with other labels such as `Power BI`.
- **Why:** The current token is visually cramped and inconsistent with neighboring terminology.
- **Reference:** `skills.html` line 171.

## 2) Fix a functional bug
- **Task:** Prevent runtime errors in `script.js` by guarding `nav` before calling `nav.classList.toggle(...)`.
- **Why:** If `script.js` executes on a page without `id="nav"`, it will throw `Cannot read properties of null` and break other JS behavior.
- **Reference:** `script.js` lines 1-5.

## 3) Fix code-comment / documentation drift
- **Task:** Align timeline labels with actual dates by replacing `3 年+` with a computed or currently accurate value based on start date (`2023.06`).
- **Why:** As of 2026-05-01, `2023.06` to now is under 3 years; the displayed metric overstates tenure and drifts from source timeline data.
- **Reference:** `experience.html` lines 188 and 195.

## 4) Improve testing
- **Task:** Add a lightweight UI smoke test (e.g., Playwright) that validates: navigation links render on every page, active-link highlighting works, and mobile menu toggle adds/removes `.open`.
- **Why:** The site currently has no automated tests, so regressions in shared navigation and JS interactions are likely to slip in.
- **Reference:** shared nav markup in all HTML pages and behavior in `script.js` lines 15-18.

# TESTING.md
**GGC Maps – Team Lost**  
**Lead Tester: Karen Armendariz**  
**Fall 2025 – Software Development II**

---

# 1. Overview

This testing document summarizes all Quality Assurance activities completed for the GGC Maps project.  
The information in this file directly corresponds to the test evidence recorded in the project’s Excel workbook:

📄 GGC_Maps_Test_Log_11.16.2025.xlsx, which includes:

1. Test Log – detailed test cases  
2. Prefix Table – explanation of test ID categories  
3. Pass/Fail Trends Over Time – automated chart of test progress  

This TESTING.md mirrors the content of the spreadsheet so instructors and reviewers can track exactly what was tested, when, and with what results.

---

# 2. Test ID Prefix Table

| Prefix | Feature / Component | Description |
|--------|----------------------|-------------|
| **T-CAMP** | Campus Map (ZoomPan.js, CampusMapView.js) | Used for map zoom, pan, and building marker tests |
| **T-FLOOR** | Floor Viewer Page | Used for building floor display and SVG floor loading |
| **T-LEG** | Legend (legend.jsx) | Used for legend toggles, colors, and translations |
| **T-FIND** | Find Component | Used for search and navigation tests |
| **T-SIDE** | Sidebar | Used for sidebar information and display logic |
| **T-HDR** | Header | Used for header navigation and logo behavior |
| **T-LNK** | Links Panel | Used for external links and resource verification |

---

# 3. Detailed Test Log (Mirroring Spreadsheet)

Below is a restructured version of the “Test Log” worksheet. All tests, dates, results, and notes are preserved exactly as recorded.

---

## ✔ T-FLOOR-01 – Floor Viewer Page
- **Test Description:** Select Building → Choose Floor 2  
- **Expected Result:** Correct floor plan displays  
- **Actual Result:** Floor 1 stays loaded  
- **Status:** Pass (after fix)  
- **Notes:** Needs event fix — event fixed / passes successfully  
- **Date:** 9/23/2025  

## ✔ T-LEG-02 – Legend Language Toggle
- **Action:** Switch to Spanish  
- **Expected:** All labels appear in Spanish  
- **Actual:** Works correctly  
- **Status:** Pass  
- **Notes:** Tested on both languages  
- **Date:** 9/27/2025  

## ✔ T-LEG-01 – Legend Panel
- **Action:** Click “Hide Legend”  
- **Expected:** Panel collapses  
- **Actual:** Works correctly  
- **Status:** Pass  
- **Date:** 9/30/2025  

## ✔ T-FIND-01 – Find Component
- **Action:** Search “AEC”  
- **Expected:** Map centers on A-Building and highlights  
- **Actual:** Error displayed (initial), then fixed  
- **Status:** Pass  
- **Date:** 10/7/2025  

## ✔ T-SIDE-01 – Sidebar
- **Action:** Open building info panel  
- **Expected:** Displays room list and hours  
- **Actual:** Works correctly  
- **Status:** Pass  
- **Date:** 10/20/2025  

## ✔ T-CAMP-01 – Campus Map Zoom (ZoomPan.js)
- **Action:** Load map and zoom in/out  
- **Expected:** Smooth zoom that stays centered  
- **Actual:** Initial failure due to pathname null in OverlayHUD; fixed later  
- **Status:** Pass  
- **Date:** 10/21/2025  
- **Notes:** Summary: 3 tests failed → later all fixed  

## ✔ T-CAMP-02 – Campus Map Panning
- **Action:** Pan by dragging  
- **Expected:** Smooth movement  
- **Actual:** Works correctly  
- **Status:** Pass  
- **Date:** 10/25/2025  

## ✔ T-HDR-01 – Header Logo
- **Action:** Click GGC Logo  
- **Expected:** Redirects to ggc.edu  
- **Actual:** Works correctly  
- **Status:** Pass  
- **Date:** 11/5/2025  

## ✔ T-LNK-01 – Helpful Links Panel
- **Action:** Click “Original Map”  
- **Expected:** Opens ggcmaps.com  
- **Actual:** Works correctly  
- **Status:** Pass  
- **Date:** 11/8/2025  

## ✔ T-FLOOR-02 – Floor Viewer Test
- **Action:** Select Building → Floor 2  
- **Expected:** Correct floor loads  
- **Actual:** Floor 2 displays  
- **Status:** Pass  
- **Date:** 11/11/2025  

## ✔ T-CAMP Re-Test – Zoom
- **Actual:** Works correctly  
- **Status:** Pass  
- **Date:** 11/16/2025  

## ✔ T-CAMP-02 Re-Test – Housing Click
- **Expected:** Show “housing not available”  
- **Actual:** Runtime error (startsWith null) → fixed  
- **Status:** Pass  
- **Date:** 11/16/2025  

## ✔ T-CAMP-03 – Building Navigation
- **Expected:** Navigate correctly  
- **Actual:** Same pathname error → fixed  
- **Status:** Pass  
- **Date:** 11/16/2025  

## ✔ T-SIDE-02 – Sidebar Error Fix
- **Expected:** Navigate to Building E  
- **Actual:** Runtime error → fixed  
- **Status:** Pass  
- **Date:** 11/16/2025  

## ✔ T-LNK-02 – Links Panel Second Test
- **Action:** Click Virtual Tour, GGC Website, Original Map  
- **Expected:** All open correct links  
- **Actual:** Pass  
- **Date:** 11/16/2025  

---

# 4. Pass/Fail Trends (from Spreadsheet)

Summary of the “Pass/Fail Trends Over Time” worksheet:

| Date | Passed | Failed | Blocked |
|------|--------|--------|---------|
| 9/23 | 2 | 0 | 0 |
| 9/27 | 1 | 0 | 0 |
| 9/30 | 1 | 0 | 0 |
| 10/7 | 0 | 1 | 0 |
| 10/20 | 1 | 0 | 0 |
| 10/21 | 1 | 0 | 0 |
| 10/25 | 0 | 1 | 0 |
| 11/1 | 1 | 0 | 0 |
| 11/5 | 1 | 0 | 0 |
| 11/8 | 1 | 0 | 0 |
| 11/11 | 1 | 0 | 0 |
| 11/16 (AM) | 0 | 3 | 0 |
| 11/16 (PM) | 3 | 0 | 0 |

### Trend Observations
- Several early failures occurred due to overlay routing issues.
- Mid-cycle alternated between pass/fail as features matured.
- Final iteration (11/16 PM) achieved **100% passing** after fixing the OverlayHUD pathname bug.

---

# 5. Final QA Conclusion

All components passed final testing.  
All major bugs were resolved.  
Final pass rate: **100% after fixes**.  
The application is stable, responsive, and meets all acceptance criteria.

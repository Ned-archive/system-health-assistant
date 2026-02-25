# System Health Assistant – MAP

## Core diagnostics
- [x] Disk health  
- [x] CPU health  
- [x] RAM health  
- [ ] Uptime check  
- [ ] Battery health (laptops only)  
- [ ] Temperature monitoring (if safely accessible)  
- [ ] Startup load indicator (light version)  

---

## Architecture & Structure
- [x] Refactor diagnostics into functions  
- [x] Separate diagnostics into modules  
- [ ] Create unified diagnostic return model  
- [ ] Standardize severity levels (`ok`, `notice`, `warning`, `critical`)  
- [ ] Remove printing from diagnostic modules completely  
- [ ] Implement CPU smoothing (multi-sample averaging)  
- [ ] Centralize issue aggregation logic  
- [ ] Refactor into `/checks` folder structure  

---

## Advisory Layer
- [x] Basic human-readable explanations  
- [x] Overall system health summary  
- [ ] Severity-based prioritization  
- [ ] Explanation level toggle (short vs detailed)  
- [ ] Health score (only if mathematically justified)  
- [ ] Suggested safe next steps (never automated)  

---

## Safety & Constraints
- [ ] Explicit read-only guarantee message (printed once per session)  
- [ ] Defensive error handling  
- [ ] Exclude removable drives safely  
- [ ] Validate false positive thresholds  
- [ ] Performance impact testing on low-end hardware  

---

## UX Philosophy Refinement
- [ ] Reduce false positives (especially CPU spikes)  
- [ ] Limit analogies to prevent over-explaining  
- [ ] Ensure warnings are calm, not alarming  
- [ ] Keep Quick Scan minimal and non-overwhelming  

---

## Stability & Reliability
- [ ] Graceful handling of permission errors  
- [ ] Prevent duplicate warnings across modes  
- [ ] Ensure consistent data structure across checks  

---

## Future Expansion (Not Now)
- [ ] GUI  
- [ ] Logging system  
- [ ] Snapshot comparison over time  
- [ ] Guided troubleshooting (text-only, no automation)  
- [ ] Vendor/support suggestion system  
- [ ] Voice interaction  

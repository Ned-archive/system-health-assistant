# Internal Notes — System Health Assistant


---

##1 Core Philosophy (Locked)

Strictly read-only.

Zero automatic fixes.

Clear language for non-technical users.

Modular, scalable architecture.

Low system impact.

Trust-first design.

##2 Architectural Improvements Required
A. Unified Diagnostic Model (Next Major Refactor)

All checks should return:

{
    "name": "CPU",
    "status": "ok" | "notice" | "warning" | "critical",
    "summary": "Short message",
    "details": { structured numeric data }
}

Benefits:

Enables generic scan rendering.

Makes Quick / Full / Modular reusable.

Enables health score calculation.

Scales cleanly.

B. Severity Levels (Must Add)

Current: ok / warning
Future:

ok

notice (mild concern)

warning

critical

Reason:
Elder users need prioritization clarity.
Portfolio needs stronger system thinking.

C. False Positive Prevention

CPU and RAM should use smoothing:

3 samples

averaged

avoid transient spikes

Trust > sensitivity.

D. Health Score (Optional, Requires Defined Math)

If implemented:

Define weighted logic:

Disk = 40%

CPU = 30%

RAM = 30%

Must justify formula.
Otherwise it becomes meaningless.

E. Uptime Check (High Value)

Example output:
"Your computer has not been restarted in 17 days."

Safe.
Actionable.
Useful.

F. Trust Reinforcement Layer

Print once per session:

"This tool does not make any changes to your computer."

Critical for elderly UX.

##3 Refined Open Questions

What thresholds define elderly-safe warning levels?

Should thresholds differ between Quick and Full modes?

Should severity consider duration (future logging feature)?

How many analogies are too many?

##4 Risk Model Expansion

Add:

Over-sensitivity due to CPU spikes

Platform-specific partition detection issues

External drives accidentally included in disk scan

Permission errors on restricted partitions

##5 Strategic Direction

Short-term focus:

Refactor architecture

Add severity model

Add uptime

Add smoothing

Long-term:

GUI

Logging

Snapshot comparison

Guided troubleshooting (text-only)



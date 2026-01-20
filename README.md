# System Health Assistant

## What is this?
A read-only system health assistant that helps non-technical users understand what’s happening on their computer without risking data loss.
An application that is easy to use for any user and works even on older or low-end hardware.

## Why does it exist?
Elderly and non-technical users often struggle with system issues, while existing tools are either too complicated or too intrusive. This project prioritizes data safety, clear explanations, and trust.

## Problem
- System diagnostic tools assume the user understands operating system concepts and computer jargon
- Automatic “fix” tools can cause irreversible damage or data loss
- Non-technical users lack clear explanations of issues and simple steps to a solution

## Constraints
- Read-only diagnostics (no automatic system changes)
- Explanations must be easy to understand for users unfamiliar with computer terms
- Must run on low-end hardware
- Minimal performance impact

## Decisions and Design Considerations
- Focused on clear, concise messaging for non-technical users: avoided system concepts like “RAM,” used short warnings, and limited analogies.
- Decided to keep CPU, disk, and memory checks in a single flow initially for simplicity, with potential refactoring into more complex functions later.
- Designed warnings and messages to be actionable but non-intimidating, balancing clarity with technical accuracy.
- Separate each function into distinct modules to implement a **three-scan approach**.

## Future Plans 
- Implement a **three-scan approach**:
  1. **Quick Scan** – silently runs all checks, prints only found issues, and a simple “everything else is fine” message for simplicity.
  2. **Modular Checks** – allows users to choose which system checks to run.
  3. **Full Report** – displays all checks with detailed explanations for users who want more information or a portfolio demonstration.
- Explore **Interactive troubleshooting guidance** for common user problems, such as frozen applications, without making automatic system changes. (Possibly)

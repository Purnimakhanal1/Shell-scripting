# Shell-scripting
A robust, transparent shell script for process monitoring that utilizes strict error handling and pipeline safety.
# Process Monitoring Shell Script

A lightweight Bash script designed to reliably inspect and filter active system processes. 

## Key Features & Safety Mechanisms

This script is built using strict shell scripting best practices to ensure predictability, debugging ease, and safe execution:

*   **`set -e` (Exit on Error):** Instructs the script to immediately exit if any command fails, preventing accidental execution of downstream commands on a broken system state.
*   **`set -x` (Print Execution Trace):** Prints every command to standard error before running it. This makes debugging highly transparent by showing exactly what the script is doing in real-time.
*   **`set -o pipefail` (Pipeline Protection):** Ensures that a pipeline (like `command1 | command2`) returns a failure exit code if *any* command in the pipeline fails, not just the last one. 
*   **`ps -ef` (System-Wide Process Snapshot):** Captures a full, detailed list of every active process running on the system with standard syntax.
*   **`grep` (Targeted Filtering):** Efficiently parses the process list to isolate and display only the specific applications or services you need to monitor.

## Prerequisites

* Linux  environment
* Bash shell

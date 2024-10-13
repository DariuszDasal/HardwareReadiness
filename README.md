# HardwareReadiness

https://www.ninjaone.com/script-hub/windows-11-compatibility-check-powershell/

Windows 11 Upgrade Compatibility Assessment Using PowerShell

Introduction
When it comes to preparing for system upgrades, IT professionals face the challenge of ensuring compatibility with new operating systems. This is particularly pertinent with the transition to Windows 11, where hardware compatibility plays a significant role. A PowerShell script designed to assess this compatibility streamlines the process, providing clear, actionable insights.

Background
The script under discussion is a PowerShell tool designed for evaluating a computer’s readiness for an upgrade to Windows 11. In the IT sector, ensuring hardware is compatible with new software is critical. This is especially true for Managed Service Providers (MSPs) who oversee multiple clients with diverse hardware environments. The script automates the evaluation process, saving time and reducing the risk of manual errors.

Detailed breakdown
The script operates in several key steps:

Environment setup: It begins by setting up parameters and environment variables. It checks if a custom field name is provided and initializes functions.
Hardware readiness function: The core of the script is the Get-HardwareReadiness function. This function verifies various hardware aspects like storage, memory, TPM (Trusted Platform Module), CPU details, and secure boot status. It uses PowerShell cmdlets like Get-CimInstance and custom code blocks for detailed checks.
Evaluation logic: For each hardware component, the script checks if the system meets the minimum requirements for Windows 11. These checks include storage size, memory capacity, TPM version, CPU architecture and speed, and secure boot capability.
Result handling: Based on these checks, the script sets a return code and result, which can be ‘Capable’, ‘Not Capable’, ‘Undetermined’, or ‘Failed To Run’.
Custom field assignment: If a custom field parameter is used, the script assigns the result to this field.
Output: Finally, the script outputs the result and exits with the corresponding return code.
Potential use cases
An MSP could use this script to quickly assess which client machines are ready for a Windows 11 upgrade. For example, before deploying a company-wide upgrade, the MSP could run this script across all machines to identify those needing hardware upgrades.

Comparisons
Traditionally, checking for OS compatibility involved manually verifying hardware specs or using separate tools. This script consolidates these checks into a single automated process, offering efficiency and accuracy over manual methods.

FAQs
Q1: Is this script compatible with all Windows versions?  
A1: The script is designed for Windows 10 systems and above.

Q2: What happens if the TPM chip is not present?  
A2: The script will return a ‘Not Capable’ status if the TPM chip is missing or incompatible.

Q3: Can this script be run on multiple machines at once?  
A3: Yes, it can be integrated into larger automation workflows to run on multiple machines.

Implications
The results from this script have significant implications for IT security and planning. Non-compliant machines might be at risk of security vulnerabilities, and planning for hardware upgrades becomes crucial.

Recommendations
Regularly run this script as part of maintenance routines.
Use the results for strategic planning of hardware upgrades.
Integrate the script into broader IT management workflows for efficiency.
Automate critical IT tasks such as Windows system compatibility checking with advanced tools.

→ Discover IT automation with NinjaOne.

Final thoughts
The transition to new operating systems like Windows 11 is a crucial step in maintaining up-to-date and secure IT environments. Tools like NinjaOne, which streamline and automate IT management processes, become invaluable in this context. By incorporating scripts like the one discussed, MSPs and IT professionals can ensure a smooth, efficient transition to Windows 11, keeping systems secure and up-to-date.


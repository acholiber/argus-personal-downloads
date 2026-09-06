# Pilot 3 validation

Build source: f57be6f8f0ee18a15af02907247e5a8f3109e48e. Version: 0.1.0-pilot.3.

This release clarifies installation of Ollama versus downloading models in ARGUS, adds a prominent Download local models button, and redirects an unfinished first run from the main page to setup. Instructions include the local setup address. Model and data formats are unchanged.

The exact archives passed manifest, CRC, path, duplicate-entry, metadata-exclusion, and targeted internal-reference checks. All 8,792 Mac and 9,957 Windows manifest files matched. Nine Mac symlinks resolve within the package. Differences from pilot 2 are the desktop Python launcher, setup HTML, version metadata, Mac bundle version, instructions, and manifests. Native launchers, runtime libraries, and core application code are unchanged.

Seven desktop regression tests passed. The rebuilt Mac package passed startup, version, first-run redirect to setup, main/setup page responses, rejection of missing request proof and foreign origins, and clean quit. Browser inspection confirmed Download local models is an exposed button in the revised page. The original reported missing-button screen was not available for inspection, so its exact cause is not established. No new model download or inference benchmark was run.

Windows pilot 3 has not received a fresh native Windows test. Earlier native checks passed on Windows Server 2022 for pilot 1; Windows 10/11 hardware and inference performance remain unvalidated.

ClamAV 1.5.4 scanned both final ZIP containers with archive traversal enabled and completed with exit code 0, zero detections, and no errors or limit alerts. The daily definitions (28114) were dated September 5, 2026; main 63 and bytecode 339 were also loaded. Limits were raised to 1 GiB per file, 2 GiB per container, 100,000 files and 40 recursion levels; the per-file timer was disabled and limit alerts enabled. See antivirus-scan.log.

A clean single-engine scan does not prove the absence of malware or explain Google's prior warning. Both programs remain unsigned and the Mac app is not notarized. No remote access, automatic reporting, or automatic updater is added. No export classification is asserted.

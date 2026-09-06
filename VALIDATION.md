# Pilot 2 validation

Version: 0.1.0-pilot.2. Build source: 10ba1d22e68bf9724475cbadbbf7ba7319ffb677.

## Package checks

Every manifest entry in the final ZIPs was verified: 8,792 Mac files and 9,957 Windows files. No checksum mismatches, unexpected regular files, duplicate ZIP entries, CRC errors, unsafe paths, or targeted internal-reference matches were found. All nine Mac symbolic links remain within the package. Mac executable permissions were preserved.

Unused decision-retrieval code, build-time scripts, unrelated distribution documentation, and unrelated model registry entries were removed. Mac filesystem metadata and unused dependency command wrappers were removed. Necessary runtime libraries and third-party license files remain. The only configured models remain Qwen2.5 7B and nomic-embed-text.

The application launcher, Windows executable, and native runtime libraries are byte-for-byte unchanged from pilot 1. Shared configuration code changes are comments/docstrings only. Other changes are version metadata, the model registry, Mac bundle metadata, instructions, and removals listed above.

## Runtime checks

- Mac pilot 2: startup, correct version, main page, setup page, request-proof rejection, cross-origin rejection, and clean quit passed with the bundled runtime and separate synthetic test data.
- Seven desktop regression tests passed.
- Windows pilot 2: package integrity and comparison to pilot 1 passed. No new native Windows run was performed. Pilot 1 passed eleven native checks on Windows Server 2022. Windows 10/11 hardware and model-inference performance remain unvalidated.
- No new model-quality or performance benchmark was run for this packaging update.

## Antivirus

ClamAV 1.5.4 completed with exit code 0 and **zero infected files** in the two final ZIP containers. Archive traversal was enabled with a 1 GiB file limit, 2 GiB container limit, 100,000 contained-file limit, 40 recursion levels, no per-file time limit, and limit-exceeded alerts enabled. No scan errors or limit alerts were reported. Daily database 28114 was dated September 5, 2026; main 63 and bytecode 339 were also loaded. All three database signatures were verified earlier that day. See antivirus-scan.log for the complete summary.

The final ZIPs were scanned locally; no application files were sent to a third-party scanning service. A clean single-engine scan does not prove the absence of malware, certify security, or identify the reason for an earlier Google warning.

## Limitations

Both applications remain unsigned; the Mac application is not notarized. Browser or operating-system security tools may still warn or block installation. Report the exact block; do not disable system-wide protections.

Setup explicitly downloads models through separately installed Ollama. Application inference is configured locally; this is not a host-wide air-gap certification. The desktop release does not introduce remote support, automatic feedback, automatic updates, or a connection to this GitHub repository.

The scan and packaging review do not establish an export classification or exemption. No such classification is claimed for this release.

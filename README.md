# <img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Objects/Locked.png" alt="Locked" width="25" height="25" /> FreePBX Vulnerabilities - December 2025

This repository contains Nuclei templates for detecting three critical vulnerabilities in FreePBX:

- **CVE-2025-61675**: Authenticated SQL Injection (CVSS 8.6) - Affects endpoint module
- **CVE-2025-61678**: Authenticated Arbitrary File Upload (CVSS 8.6) - Affects endpoint module
- **CVE-2025-66039**: Authentication Bypass (CVSS 9.3) - Affects framework module

## <img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Objects/Package.png" alt="Package" width="25" height="25" /> Affected Versions

### CVE-2025-61675 & CVE-2025-61678 (endpoint module)
- **FreePBX 16**: < 16.0.92 (patched in 16.0.92)
- **FreePBX 17**: < 17.0.6 (patched in 17.0.6)

### CVE-2025-66039 (framework module)
- **FreePBX 16**: < 16.0.44 (patched in 16.0.44)
- **FreePBX 17**: < 17.0.23 (patched in 17.0.23)

## <img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Objects/Magnifying%20Glass%20Tilted%20Left.png" alt="Search" width="25" height="25" /> How does this detection method work?

These templates detect vulnerable FreePBX instances by:
1. Extracting the FreePBX version from the administration panel
2. Comparing the version against known vulnerable version ranges
3. Confirming the presence of FreePBX-specific identifiers

The detection is non-invasive and does not attempt to exploit the vulnerabilities.


## <img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Travel%20and%20places/Rocket.png" alt="Rocket" width="25" height="25" /> How do I run this script?

1. Download and install [Nuclei](https://github.com/projectdiscovery/nuclei).
2. Clone this repository to your local system.
3. Run a single template:
```sh
nuclei -u <target-url> -t CVE-2025-61675.yaml
```

4. Run all templates:
```sh
nuclei -u <target-url> -t .
```

5. Scan multiple hosts:
```sh
nuclei -l hosts.txt -t .
```

### Example Output

```
[CVE-2025-61675] [http] [high] FreePBX Authenticated SQL Injection
[CVE-2025-61678] [http] [high] FreePBX Authenticated Arbitrary File Upload
[CVE-2025-66039] [http] [critical] FreePBX Authentication Bypass
```

## <img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Objects/Books.png" alt="Books" width="25" height="25" /> References

- [CVE-2025-61675 - NVD](https://nvd.nist.gov/vuln/detail/CVE-2025-61675)
- [CVE-2025-61678 - NVD](https://nvd.nist.gov/vuln/detail/CVE-2025-61678)
- [CVE-2025-66039 - NVD](https://nvd.nist.gov/vuln/detail/CVE-2025-66039)
- [Nuclei - ProjectDiscovery](https://github.com/projectdiscovery/nuclei)


## <img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Symbols/Warning.png" alt="Warning" width="25" height="25" /> Disclaimer

Use at your own risk, I will not be responsible for illegal activities you conduct on infrastructure you do not own or have permission to scan.

---

## <img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Objects/Page%20with%20Curl.png" alt="License" width="25" height="25" /> License

This project is licensed under the MIT License.

## <img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Smilies/Speech%20Balloon.png" alt="Contact" width="25" height="25" /> Contact

If you have any questions about this vulnerability detection script please reach out to me via [Signal](https://signal.me/#eu/0Qd68U1ivXNdWCF4hf70UYFo7tB0w-GQqFpYcyV6-yr4exn2SclB6bFeP7wTAxQw).

If you would like to connect, I am mostly active on [Twitter/X](https://x.com/rxerium) and [LinkedIn](https://www.linkedin.com/in/rxerium/).
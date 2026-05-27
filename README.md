## CVE-2019-6340 — Drupal RESTful Web Services RCE

Python implementation of the remote code execution exploit for [CVE-2019-6340](https://nvd.nist.gov/vuln/detail/CVE-2019-6340), based on analysis of the [Metasploit module](https://github.com/rapid7/metasploit-framework/blob/master//modules/exploits/unix/webapp/drupal_restws_unserialize.rb) and the prior work by [leonjza](https://www.exploit-db.com/exploits/46459).

**Key difference from EDB-46459:** uses POST instead of GET,
bypassing Drupal's page cache — can be executed multiple times
against the same target without waiting for cache expiration.

## Requirements
`pip install requests`

## Usage
`python3 exploit.py <target> -c <command> [options]`

## Disclaimer
This tool is provided for educational purposes and authorized security assessments only (penetration tests, CTFs, lab environments). Running this exploit against systems without explicit written permission is illegal. The author assumes no liability for any misuse.

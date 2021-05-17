# http-vuln-cve2019-14322.nse
Nmap NSE script to detect CVE-2019-14322 of Pallets Werkzeug path traversal via SharedDataMiddleware mishandles drive names (such as C:) in Windows pathnames

# Description

CVE-2019-14322 - A vulnerability was found in Pallets Werkzeug up to 0.15.4. It has been declared as critical. This vulnerability affects the function SharedDataMiddleware of the component Windows. The manipulation with an unknown input leads to a directory traversal vulnerability. The CWE definition for the vulnerability is CWE-22. This script reads c:/windows/win.ini as a proof of concept.
This vulnerability is running on (cpe:2.3:o:microsoft:windows:-:*:*:*:*:*:*:*, cpe:2.3:o:microsoft:windows:-:*:*:*:*:*:x64:*)


# Clone and Install

- $ git clone https://github.com/faisalfs10x/http-vuln-cve2019-14322.nse
- $ cd http-vuln-cve2019-14322.nse/
- $ sudo cp http-vuln-cve2019-14322.nse /usr/share/nmap/scripts/

# Usage
-----

$ nmap --script http-vuln-cve2019-14322.nse -p <port> <target>



    PORT    STATE SERVICE
    443/tcp open  https
    | http-vuln-cve2019-14322: 
    |   VULNERABLE:
    |   Pallets Werkzeug path traversal via SharedDataMiddleware mishandles drive names (such as C:) in Windows pathnames
    |     State: VULNERABLE
    |     IDs:  CVE:CVE-2019-14322
    |       CVE-2019-14322 - A vulnerability was found in Pallets Werkzeug up to 0.15.4. It has been declared as critical. This vulnerability affects the function SharedDataMiddleware of the component Windows. The manipulation with an unknown input leads to a directory traversal vulnerability. The CWE definition for the vulnerability is CWE-22.
    |       This script reads c:/windows/win.ini as a proof of concept.
    |       This vulnerability is running on (cpe:2.3:o:microsoft:windows:-:*:*:*:*:*:*:*, cpe:2.3:o:microsoft:windows:-:*:*:*:*:*:x64:*)
    |           
    |     Disclosure date: 2019-07-28
    |     References:
    |       https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2019-14322
    |       https://vuldb.com/?id.138886
    |       https://www.cvedetails.com/cve/CVE-2019-14322/
    |_      https://palletsprojects.com/blog/werkzeug-0-15-5-released/
    
    Nmap done: 1 IP address (1 host up) scanned in 0.35 seconds



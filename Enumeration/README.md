# CMS
if the cms can't be readily identified, try to identify themes, plugins, etc. from page source and nikto, ffuf or similar. If the theme/plugin can be located, then the CMS should be able to as well.

# Certificate Analysis
Download certificate to file:
`openssl s_client -showcerts -connect certified.htb:3269 </dev/null 2>/dev/null|openssl x509 -outform PEM > cert.pem`

Use certtool to display info:
`certtool -i --infile cert.pem`

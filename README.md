# Fix Canonical Links in MadCap Flare
Fix for missing canonical links in MadCap Flare

Add
<meta rel="canonical" href="https://www.eample.com/yourlink.htm" />
To your page (change to the actual link)

This will not get stripped from the output, and can be modified after publish.

Make a cronjob and let it run this script

/usr/bin/find /path/to/madcap/output -name "*.htm" -type f -exec sed -i 's/meta rel/link rel/g' {} \;

change /path/to/madcap/output to your own madcap output folder

For more information https://www.linkedin.com/pulse/solution-canonical-links-madcap-flare-knowledge-base-wesdijk-/

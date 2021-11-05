# Cyber Research and Development 
This is a collecction of Cyber related articles and tools which I have come across in my career and figured I should categorise these nicely for myself and anyone else that is interested.

## Tools and Collections:

+ Github repos and other collections:
  + https://github.com/toniblyx/my-arsenal-of-aws-security-tools
  + https://github.com/gregsramblings/google-cloud-4-words
  + https://github.com/enaqx/awesome-pentest
  + https://github.com/Hack-with-Github/Awesome-Hacking/blob/master/README.md - A collection of awesome lists for hackers, pentesters & security researchers. (Kinda the inspiration for all of this)
  + https://github.com/ytisf/theZoo - Compilation of historical malware source and binaries for testing and malware analysis.
  + https://github.com/0x90/wifi-arsenal - Huge repo of Wifi tools and hacks related to everything WiFi.
  + https://github.com/cyberark/SkyArk - Azure and AWS privileged account scanning provided by CyberArk to compliment on-premise CyberArk Discovery and anaylysis tooling.
  + https://github.com/nccgroup/ScoutSuite - Open source multi-cloud security-auditing tool.
  + https://github.com/toniblyx/prowler - Security tool to perform AWS security best practices assessments specifically CIS level 1 & 2.
  + https://github.com/orlikoski/CyLR - Essential tool for doing quick forensics informaiton capture to USB 
  + https://github.com/dkovar/analyzeMFT - Simple tool to anaylse the larger MFT file captured from windows devices 
  + https://github.com/log2timeline/plaso - Super timeline all the things, really helpful once you have artifacts from CyLR.
+ Threat hunting and investigations
  + https://attack.mitre.org/matrices/enterprise/ - Mitre framework for attacker tactics and techniques.
  + https://d3fend.mitre.org/ - Mitre framework for defender tactics and techniques.
  + https://www.iplocation.net - IP address location aggregation site showing multiple realtime and historical IP locations from different sources.
  + https://www.shodan.io/ - Search engine of IPs with active serivces and associated details including vulnerabilites. Freelancer edition provides access to scan new IPs and basic API.
  + http://www.zone-h.org/archive - Archive of website defacements across known published sites.
  +  https://www.spamhaus.org/isp/ - Website to check if domainshave been blacklisted on email mailing lists.
  + https://www.ipaddressguide.com/cidr - Useful webistre to check the IP addressed in a CIDR range if you have not memeriif domainshave been blacklisted on email mailing lists.
  + https://www.spectx.com/ - Log ingestion and query platform that allows for quick ingestion of potentially unstructed logs, really good for IIS logs. Some filters include: 
    ```
         | filter(Destination NOT CONTAINS("100.72."))
         | filter(Receive_Time CONTAINS("6:57:"))

         | filter(c_ip not in 10.0.0.0/8)

         | select(Receive_Time, Severity, Event_Type_ID, Event_Name, Device, Source, Source_User_Identity, Source_Service, Destination, Destination_FQDN, Destination_Service, Action, Risk_Rating, Description, Event_ID, GEO(Source))
         | sort(date_time)

         | filter(Destination CONTAINS("100.72."))
         | filter(Destination NOT CONTAINS("100.72.163.23"))
         | filter(Destination_Service NOT CONTAINS("udp/53"))
         | filter(Destination_Service NOT CONTAINS("tcp/636"))
         | filter(Destination_Service NOT CONTAINS("tcp/443"))
         | filter(Destination_Service NOT CONTAINS("udp/123"))
         | sort(Destination_Service )

         | filter(Source_Service CONTAINS("22"))
         | filter(Source_Service CONTAINS("3389"))
         | filter(Source_Service CONTAINS("5900"))

         | filter(Source_Service CONTAINS("tcp/22" OR "udp/22" OR "tcp/3389" OR "udp/3389" OR "tcp/5900" OR "udp/5900"))

         | filter(Source in ("100.72.163.10", "100.20.190.10", "100.20.190.11", "100.20.190.12"))
         | sort(Destination_Service)
      ```
+ AWS
    + https://aws.amazon.com/blogs/security/the-most-popular-aws-security-blog-posts-in-2015
    + https://aws.amazon.com/blogs/security/new-whitepaper-aws-cloud-security-best-practices

+ **Articles of interest:**<br/>
  + Defence and Military
    + [Mobile Nuclear reactors](https://www.armytimes.com/news/your-army/2019/03/01/the-army-wants-mobile-nuclear-reactors-for-fobs-but-some-scientists-say-thats-naive/)
  + Health Sector
    + [AUS Cardiac Health Clinic Ransomware](https://www.scmagazine.com/home/security-news/heart-attack-ransomware-encrypts-australian-cardiac-clinics-patient-files/)
  + Identity
    + [Digital Identity Program](https://www.prnewswire.com/news-releases/deloitte-shares-10-questions-every-organization-should-ask-about-their-digital-identity-program-300850652.html)
  + IT Infrastructure 
    + [Critical Legacy Technology](https://www.scmagazine.com/home/security-news/government-it-systems-and-critical-infrastructure-systems-around-the-world-are-at-risk-due-to-legacy-technology-and-its-keepers-pending-retirements/)
    + [Cyber Threat Insights Report](https://www.bdo.global/getmedia/1e2b00b7-bf9c-48bd-9738-3ddc37453867/BDO-Cyber-Threat-Insights_Report_Q4-2018_US_web.pdf.aspx?ext=.pdf)
    + [Beer drinkers guide to SAML](https://duo.com/blog/the-beer-drinkers-guide-to-saml)
  + Networking
    + [IMSI location tracking](https://thehackernews.com/2019/02/location-tracking-imsi-catchers.html)
  + Uncategorised
    + [Cyberark](https://www.cyberark.com/blog/version-10-9-extends-security-to-privileged-business-users/)
    + [Kubernetes](https://azure.microsoft.com/en-us/resources/kubernetes-learning-path/?_lrsc=c97526a0-abd4-4eca-85b3-3fb13c10177e)
    + [DevSecOps](https://blogs.sans.org/appsecstreetfighter/files/2018/10/DevSecOps_Exploring_Phase1-2.pdf)
    + [Email spoofing prevention](https://www.reddit.com/r/sysadmin/comments/aph6ee/lets_talk_about_email_spoofing_and_prevention_alt/)

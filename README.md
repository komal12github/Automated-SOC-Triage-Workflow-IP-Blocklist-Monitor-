<img width="1920" height="1200" alt="Screenshot (289)" src="https://github.com/user-attachments/assets/772aaf0a-4556-4244-a95b-ba6469a1eef3" /># Automated IP Blocklist Monitor (n8n)
This project is a low-code automation workflow built in n8n that simulates a common Security Operations Center (SOC) task: triaging suspicious IP addresses against a local blocklist to reduce analyst alert fatigue.
#The Problem & Solution
In a SOC, analysts are often flooded with thousands of alerts, many of which are duplicates or known threats. This workflow automatically:

  + Ingests a feed of suspicious IPs.
  + Checks each IP against a "Blocklist" (a Google Sheet).
  + Filters the noise:

     + If the IP is already on the list, the flow stops (no alert).
     + If the IP is new, it escalates the threat.
       
  + Alerts the analyst by logging the new IP and sending a Webhook.
#Technologies Used
  + n8n: (Low-code automation platform)
  + Google Sheets API: (Used as a simple, local database)
  + Webhooks: (For sending the final alert)
  + JSON: (For passing data between services)

Workflow Diagram
Here is the complete, final workflow diagram from the n8n canvas.



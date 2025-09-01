# Ex.No.4   MHA (Mail Header Analyzer)
## Aim :
- The aim is to use a Mail Header Analyzer (MHA) to trace an email's origin and verify its authenticity by examining its header for signs of spoofing.
## Procedure
### Step 1: Get the Email Header
- First, you need to copy the full, raw header from the email.

- Gmail: Open the email, click the three dots (⋮), and select Show original.
<br>
<br>
<img width="1919" height="1025" alt="image" src="https://github.com/user-attachments/assets/5b91ffb2-2b83-4e28-bbd6-c9adf2280105" />
<br>
<br>


- Select all the text in the header and copy it.

<br>
<img width="1915" height="917" alt="image" src="https://github.com/user-attachments/assets/cf519e50-acb0-4df9-8680-6ad6d2e02088" />


<br>
<br>

### Step 2: Use a Mail Header Analyzer (MHA)
- The easiest way to analyze the header is with an online tool.

- Navigate to a site like MXToolbox Email Header Analyzer.
 <br>
<br>

 <img width="1919" height="970" alt="image" src="https://github.com/user-attachments/assets/949cfef1-069d-4e88-8ad4-0843485593e9" />

<br>
<br>

- Paste the entire header you copied into the analysis box.
<br>
<br>

Click the "Analyze" button to get a parsed, easy-to-read report.
<br>
<br>

<img width="1919" height="974" alt="image" src="https://github.com/user-attachments/assets/14a77cb4-b93f-450f-a0d8-8c2dd7851bee" />


### Step 3: Analyze The Report
- This is the most critical step. In the analyzer's report, look for the SPF, DKIM, and DMARC results.
### Review the Overall Delivery Summary
- First, look at the high-level summary to get an immediate sense of the email's status.

- Check DMARC Compliance: The report shows the email is DMARC Compliant. This is the most important overall result.

- Check SPF Status: Both SPF Authenticated and SPF Alignment passed. This means the sending server was authorized.

- Check DKIM Status: DKIM Alignment passed, but DKIM Authenticated failed (❌). This is a critical finding and indicates a problem with the email's digital signature.
<br>
<br>
<img width="1917" height="913" alt="image" src="https://github.com/user-attachments/assets/d5817d22-2c49-4a43-9388-7c7ae778de43" />


<br>
<br>

### Investigate the SPF Record and Email Path
- Next, verify why the SPF check passed.

- Examine the SPF Record: The SPF record for the domain is v=spf1 include:mailgun.org ~all. This record explicitly authorizes servers from Mailgun to send emails on its behalf.

- Trace the Relay Information: The delivery path shows the email was sent from m241-136.mailgun.net.

- Conclusion: Since the email came from a Mailgun server, which is authorized in the SPF record, the SPF check passed.
  <br>
  <br>
<img width="1912" height="913" alt="image" src="https://github.com/user-attachments/assets/500d18a3-0cb7-4083-abf1-234f33c4da0a" />



<br>
<br>

### Analyze the DKIM Failure

<br>
<img width="1885" height="786" alt="image" src="https://github.com/user-attachments/assets/c1d13cf5-5ccf-4e59-8ca2-7a252dc37c77" />

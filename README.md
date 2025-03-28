# Secure Azure Identity Management with Conditional Access & MFA
This lab focuses on enhancing Azure identity security by implementing Multi-Factor Authentication (MFA) and Conditional Access policies in Azure Active Directory (Azure AD). By the end of this lab, strong authentication methods will be enforced, access will be restricted based on risk conditions, and sign-in activity will be monitored to improve security posture.<br/>

<h2>Scenario</h2>
TechSolutions Inc. is a rapidly growing technology firm that provides cloud-based services to clients across various industries. As the company expands, the need to secure sensitive data, such as intellectual property and client contracts, has become a top priority. The company has recently moved to the cloud, using Microsoft 365, Azure AD, and other cloud-based applications for employee productivity and collaboration.<br/>
<br/>

Using a test user in this scenario ***FIRST*** ensures that the Multi-Factor Authentication (MFA) setup operates correctly, avoiding any disruptions to real users or impact on production environments before it is rolled out to the entire user base.<br/>

<h2>Environments Used </h2>

- <b>Microsoft Azure</b>
- <b>Windows 11</b>

<h2>Policy Creation</h2>
Navigate to Microsoft Entra ID > Users, select a test user, and click Authentication methods.
<br />
<br />
<img src="https://imgur.com/sdwzeAg.png" height="20%" width="20%" alt="Disk Sanitization Steps"/>
<br />
<br />
Enable MFA and configure a verification method. Users will be prompted to set up MFA the next time they log in.
<br />
<br />
<img src="https://imgur.com/E4DmqvX.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://imgur.com/sSrF0HR.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
<br />
<br />
Log in to the test user account to confirm that MFA is functioning. Afterward, go back to "Users," choose "Per-user MFA," select the "Select all" box, and click "Enable MFA."
<br />
<br />
<img src="https://imgur.com/iWBG38H.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://imgur.com/gqBLnxG.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://imgur.com/4HRZET8.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
<br />
<br />
Azure has the OATH token registered on the user account. The software OATH token in Azure is a method for enabling multi-factor authentication (MFA) using a time-based one-time password (TOTP) generated by an authenticator app, such as the Microsoft Authenticator app.
<br />
<br />
<img src="https://imgur.com/Pcl9rHt.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />























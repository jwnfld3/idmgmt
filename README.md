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
<img src="https://imgur.com/sdwzeAg.png" height="20%" width="20%" alt>
<br />
<br />
Enable MFA and configure a verification method. Users will be prompted to set up MFA the next time they log in.
<br />
<br />
<img src="https://imgur.com/E4DmqvX.png" height="60%" width="60%" alt>
<br />
<br />
<img src="https://imgur.com/sSrF0HR.png" height="60%" width="60%" alt>
<br />
<br />
Log in to the test user account to confirm that MFA is functioning. Afterward, go back to "Users," choose "Per-user MFA," select the "Select all" box, and click "Enable MFA."
<br />
<br />
<img src="https://imgur.com/iWBG38H.png" height="40%" width="40%" alt>
<br />
<br />
<img src="https://imgur.com/gqBLnxG.png" height="60%" width="60%" alt>
<br />
<br />
<img src="https://imgur.com/4HRZET8.png" height="60%" width="60%" alt>
<br />
<br />
Azure has the OATH token registered on the user account. The software OATH token in Azure is a method for enabling multi-factor authentication (MFA) using a time-based one-time password (TOTP) generated by an authenticator app, such as the Microsoft Authenticator app.
<br />
<br />
<img src="https://imgur.com/Pcl9rHt.png" height="80%" width="80%" alt>
<br />
<br />
Next, a Conditional Access Policy will be created. A Conditional Access Policy in Azure is a set of rules that control access to resources based on factors like user identity, location, and device compliance. It helps enforce security requirements such as multi-factor authentication (MFA) or restrict access from non-compliant devices.<br />
<br />
In the Azure portal, go to Microsoft Entra ID
<br />
<br />
<img src="https://imgur.com/AcWysRM.png" height="50%" width="50%" alt>
<br />
<br />
Manage
<br />
<br />
<img src="https://imgur.com/iy5X7Kw.png" height="30%" width="30%" alt>
<br />
<br />
Security
<img src="https://imgur.com/0R1iYr7.png" height="30%" width="30%" alt>
<br />
<br />
Protect > Conditional Access.
<br />
<br />
<img src="https://imgur.com/U42L4ZA.png" height="30%" width="30%" alt>
<br />
<br />
Click “Create new policy”
<img src="https://imgur.com/NObJEsj.png" height="50%" width="50%" alt>
<br />
<br />

#### Create a New Policy  
- Click **New policy** and name it **Require MFA for All Users**.  

#### Assignments  
- **Users**: Include all users or select specific groups.  
- **Cloud apps**: Choose all cloud apps or select specific applications.  

#### Conditions  
- **Sign-in Risk**: Set to medium and high.  
- **Locations**: Exclude trusted IPs (e.g., corporate network).  
- **Device Platform**: Target Windows, macOS, iOS, and Android.  

#### Access Controls  
- Select **Grant > Require multi-factor authentication**.  

#### Finalize Policy  
- Set enable policy to on, then click create.  

<img src="https://imgur.com/X3WdVsz.png" height="20%" width="20%" alt>
<br />
<br />
To verify the policy's effectiveness, a different user attempted to access Azure and was prompted for MFA, preventing access without verification. This confirms the policy was applied correctly.
<br />
<br />
<img src="https://imgur.com/cqTsOHU.png" height="40%" width="40%" alt>
<br />
<br />
<img src="https://imgur.com/AeF9ZHq.png" height="60%" width="60%" alt>
<br />
<br />
Checked the Conditional Access Insights and Reporting in Azure to confirm the policy was applied correctly. This report shows sign-in attempts, policy enforcement, affected users, and authentication failures. Reviewing it ensures MFA is working as intended and helps identify any misconfigurations or user issues.
<br />
<br />
<img src="https://imgur.com/zxoqLry.png" height="100%" width="100%" alt>
<br />
<br />
<h2>Conclusion</h2>
This lab demonstrates how to secure Azure AD identities by implementing MFA and Conditional Access policies. These controls help mitigate security risks by enforcing adaptive authentication, restricting unauthorized access, and improving overall identity protection in an organization.


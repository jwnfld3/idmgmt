# Implement Conditional Access & Multi-Factor Authentication (MFA)

## Summary
This lab demonstrates how to enforce security policies in Microsoft Entra ID by implementing Conditional Access and Multi-Factor Authentication (MFA). The objective is to strengthen authentication security by blocking risky sign-ins and requiring MFA for high-privilege accounts such as Global Administrators. By configuring Conditional Access policies, organizations can minimize unauthorized access and enhance security compliance.

---

## Lab Requirements
Before starting this lab, ensure the following requirements are met:

- **Microsoft Entra ID Admin Access** – Access to the **Microsoft Entra Admin Center** with **Global Administrator** or **Conditional Access Administrator** permissions.
- **Test Admin Account** – A separate test account with **Global Administrator** privileges for testing.
- **Multi-Factor Authentication (MFA) Setup** – Ensure MFA is enabled in the **Microsoft Entra ID tenant**.
- **Internet Connection** – Required to access the Microsoft Entra Admin Center.
- **VPN (Optional)** – Used to simulate sign-ins from untrusted locations.

---

## Who
This lab is intended for IT administrators, security analysts, and identity management professionals responsible for securing user authentication in Microsoft Entra ID. The lab assumes basic familiarity with Microsoft Entra ID and Conditional Access policies.

---

## What
The lab involves configuring a Conditional Access policy to enforce MFA for Global Administrators and block access from untrusted locations. This ensures that only verified users can access sensitive resources, reducing the risk of unauthorized access and credential-based attacks.

---

## When
This lab is applicable when:
- Implementing security policies for privileged accounts.
- Strengthening authentication mechanisms to comply with security frameworks.
- Responding to an increase in unauthorized sign-in attempts.
- Enhancing identity protection for cloud-based services.

---

## Where
The lab is performed within the **Microsoft Entra Admin Center**, specifically under the **Security** and **Conditional Access** sections.

---

## Why
Enforcing MFA and Conditional Access is critical for:
- Reducing the risk of compromised administrator accounts.
- Preventing unauthorized access from risky locations.
- Ensuring compliance with security best practices and regulatory requirements.
- Strengthening authentication security for sensitive resources.

---

## Steps to Implement Conditional Access & MFA

### 1. Access Conditional Access Settings:
- Open a web browser and navigate to the [Microsoft Entra Admin Center](https://entra.microsoft.com).
- Go to **Security** → **Conditional Access**. If it cannot be located use the search bar on the home screen.</b>

![image](https://github.com/user-attachments/assets/e405207f-4a7c-479c-ad9f-7ff0115a40ec)


### 2. Create a New Conditional Access Policy:
- Click on **New Policy** and name it **"Require MFA for Admins"**.
  
![image](https://github.com/user-attachments/assets/6cfeba20-a09f-4063-bbc2-997d9c8efbfa)


### 3. Assign Policy to Global Administrators:
- Under **Assignments**, select **Users**.
- Click **Spefific Users Included** and under **Include** Click **Users and groups** radio button and the **Users and groups** check box and select the group that you have created for **Global Administrators**

![image](https://github.com/user-attachments/assets/ce42a783-8406-4010-9d34-7fe37562c00b)


### 4. Define Access Conditions:
- Navigate to **Conditions** → **Locations**.
- Configure the policy to **"Include Any network or location"**. Policies with "Any network or location" ensure users meet security conditions (e.g., MFA, device compliance) regardless of where they are.

### 5. Enforce MFA:
- Under **Grant Controls**, select **Require Multi-Factor Authentication (MFA)**.
- Ensure the policy is set to **Enabled**.
![image](https://github.com/user-attachments/assets/6d675218-34b7-4c6e-baaa-eec9c78d6a8d)


### 6. Test the Policy:
- Use an **admin test account** to verify that MFA is required when signing in.
  ![image](https://github.com/user-attachments/assets/f81e662d-d9c8-4ce8-89f9-83146f9b5696)
---

## Summary: Enforcing Authentication from Any Location ##
This lab ensures users must meet security conditions such as Multi-Factor Authentication (MFA) and device compliance no matter where they connect from. By configuring the policy to "Include Any network or location," authentication requirements apply universally whether users are on a corporate network, public Wi-Fi, or a remote connection. This enhances security by preventing location-based bypasses and ensuring consistent enforcement of access policies across all environments.

---

## Testing and Validation

### 1. Verify MFA Enforcement:
- Sign in with a **Global Administrator** test account.
- Confirm that an MFA prompt appears before access is granted.

### 2. Review Sign-In Logs:
- Go to **Microsoft Entra ID** → **Sign-in Logs**.
- Verify that policy enforcement details, such as MFA requirements and blocked sign-ins, are correctly logged.

### 3. Adjust and Troubleshoot if Needed:
- If unexpected behavior occurs, review policy settings and adjust conditions accordingly.
- Ensure that MFA settings in **Identity Protection** align with Conditional Access policies.

## Summary: Enforcing Authentication from Any Location

This lab ensures users must meet security conditions such as Multi-Factor Authentication (MFA) and device compliance no matter where they connect from. By configuring the policy to "Include Any network or location," authentication requirements apply universally whether users are on a corporate network, public Wi-Fi, or a remote connection. This enhances security by preventing location-based bypasses and ensuring consistent enforcement of access policies across all environments.

By following these validation steps, the effectiveness of the Conditional Access policy can be confirmed, ensuring that privileged accounts remain secure.

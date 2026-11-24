# AWS IAM and Least Privilege Project

## Phase 1: AWS Account Security

### Objective

Secure my AWS account before implementing IAM security controls.

### Security Controls Implemented

| Security Control | Status |
|---|---|
| AWS account access verified | Completed |
| Root account MFA | Completed |
| Monthly AWS budget | Completed |
| Billing notifications | Completed |

### Root Account MFA

Enabled Multi-Factor Authentication (MFA) on my AWS root account to provide an additional layer of protection against unauthorised access.

MFA requires an additional authentication factor alongside the account password, making it more difficult for unauthorised users to access the account.

### AWS Monthly Budget

Created a monthly AWS cost budget to monitor cloud expenditure and track spending against a defined budget limit.

Configured spending thresholds to help monitor actual and forecasted costs and identify unexpected increases in expenditure.

### Billing Notifications

Configured AWS billing notifications to receive alerts when cloud spending reaches specified thresholds.

These notifications help monitor AWS expenditure and provide early warnings of unexpected increases in cloud costs.

### Security Considerations

- Root account access should be restricted and used only when necessary.
- MFA should be enabled on privileged accounts.
- Billing notifications help identify unexpected expenditure.
- AWS Budget alerts do not automatically stop AWS services or prevent additional charges.
- AWS account spending should be monitored regularly.

### Evidence

**Root Account MFA**

![Root Account MFA](screenshots/root-mfa-enabled.png)

**MFA Device Assigned**

![MFA Device Assigned](screenshots/mfa-device-assigned.png)

**MFA Verification**

![MFA Verification](screenshots/mfa-verification.png)

**AWS Monthly Budget**

![AWS Budget Configuration](screenshots/budget-configuration.png)

![AWS Budget](screenshots/aws-budget.png)

![Budget Setup](screenshots/budget-setup.png)

**Billing Notifications**

![Billing Notifications](screenshots/billing-alerts.png)

### Lessons Learned

Through this phase, I learned how to secure an AWS root account using MFA, configure monthly AWS budgets and set up billing notifications.

I also learned the importance of protecting privileged accounts and monitoring cloud expenditure to help manage unexpected costs.

---
## Phase 2: AWS IAM Users and Groups Creation

### Objective

The aim of this phase was to create IAM users and groups in AWS and organise access based on different job roles.

### Step 1: Check Existing IAM Users and Groups

I first checked my AWS account to see whether any IAM users or groups already existed.

**Findings:**
- No existing IAM users were found.
- No existing IAM groups were found.

This gave me a clean starting point for creating my IAM environment.

**Evidence:**

![Initial IAM Users](screenshots/01-initial-iam-users.png)

![Initial IAM Groups](screenshots/02-initial-iam-groups.png)

### Step 2: Create IAM Groups

I created two IAM groups for different job roles.

| Group name | Purpose |
|---|---|
| Developers | For users carrying out development tasks. |
| SecurityAuditors | For users carrying out security auditing tasks. |

Creating groups makes it easier to manage permissions for different users.

**Evidence:**

![IAM Groups Created](screenshots/03-iam-groups-created.png)

### Step 3: Create IAM Users

I created two test IAM users to represent different job roles.

| Username | Role |
|---|---|
| test-developer | Developer |
| test-security-auditor | Security Auditor |

These accounts will help me test how different users access AWS resources.

**Evidence:**

![Test Developer Created](screenshots/04-test-developer-created.png)

![Both IAM Users Created](screenshots/05-iam-users-created-and-group-counts.png)

### Step 4: Assign Users to Groups

I assigned each test user to the appropriate IAM group.

- test-developer was assigned to Developers.
- test-security-auditor was assigned to SecurityAuditors.

The IAM users page showed that each user belonged to one group.

This makes it easier to manage permissions through groups instead of assigning permissions individually.

### Security Considerations

- Created separate accounts for different job roles.
- Used IAM groups to organise users.
- Avoided giving test users unnecessary administrative access.
- Identified MFA as an additional security measure to implement and verify.

### Outcome

Successfully created two IAM groups and two test IAM users.

Both users were assigned to their respective groups.

This completed the initial IAM user and group setup.

**Project Status:** Completed – Phase 2.

### Next Phase

The next phase will focus on creating IAM policies and assigning permissions to control what each user can access in AWS.

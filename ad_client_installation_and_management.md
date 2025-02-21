# Active Directory Client Installation and Management

This project demonstrates the process of installing and configuring Windows client computers on a domain using **Active Directory**. It includes creating Organizational Units (OUs), adding computers to the domain, and configuring them with department-specific policies and settings using **Group Policy Objects (GPOs)**.

## Overview

In a typical enterprise environment, Windows client machines need to be connected to the Active Directory domain for centralized management. This project outlines the steps for:
- Creating Organizational Units (OUs) for different departments.
- Installing and joining Windows client computers to the domain.
- Configuring department-specific settings using **Group Policy Objects (GPOs)**.
- Assigning specific users and computers to their corresponding departments.

## Requirements

- A **Windows Server** environment with **Active Directory**.
- **Windows 10** or later client computers to be joined to the domain.
- Access to **Group Policy Management Console (GPMC)**.
- Administrative rights to create OUs, users, and configure GPOs.

## Steps to Set Up Active Directory Client Installation

### 1. Prepare Active Directory Environment

1. **Create Organizational Units (OU)**:
   - Open **Active Directory Users and Computers** on the Windows Server.
   - Right-click on the domain and create new OUs for each department (e.g., Marketing, Sales, HR).

2. **Create Users and Computers**:
   - Inside the respective OUs, create user accounts for each employee.
   - Set up computer accounts for each client machine that needs to join the domain.

### 2. Install and Join Windows Client to Domain

1. On the Windows client, open **Settings** > **System** > **About**.
2. Under the **Device Name** section, click **Join a domain**.
3. Enter the domain name (e.g., `example.com`), and click **Next**.
4. Enter the domain Administrator credentials to authorize the join.
5. Restart the client to complete the domain join.

### 3. Configure GPOs for Department-Specific Settings

1. Open **Group Policy Management Console (GPMC)**.
2. Create a new **GPO** for each department (e.g., Marketing, Sales).
3. Configure user and computer settings under the **User Configuration** and **Computer Configuration** sections:
   - Set up application access, security settings, and network access as needed.
4. Link the GPOs to the respective OUs to automatically apply settings.

### 4. Test and Verify

1. Log into the client computer using a department-specific user account.
2. Verify that the correct policies and settings are applied:
   - Application access.
   - Security restrictions.
   - Network resources.

### 5. Department-Specific Customizations

- **Department Applications**: Configure automatic installation of department-specific applications using GPO.
- **Security**: Apply stricter security policies for sensitive departments like HR or Finance.
  
## Conclusion

This project demonstrates how to manage client machines in a domain environment using **Active Directory** and **Group Policy Objects (GPOs)**. By creating and configuring Organizational Units (OUs) and applying GPOs, administrators can efficiently manage department-specific settings and ensure security by following the principle of least privilege.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

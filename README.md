# Script-Controlled ACL - Restrict Record Access Based On Field Value

## 📌 Project Description
This project implements Script-Controlled ACL in ServiceNow to restrict record access based on a specific field value. The logic ensures that only admin users or users with a specific role can access restricted records, while normal users are denied access.

## ⚙️ Implementation Steps
1. Created Custom Users in ServiceNow
2. Created Custom Roles (e.g., bb3)
3. Created Custom Table with restricted field values
4. Implemented Script-Controlled ACL logic
5. Tested with different users - Verified Access Denied for normal users

## 💻 ACL Script Used
```javascript
// Script-Controlled ACL Script
if (gs.hasRole('admin')) {
    answer = true;
} else {
    // Check field value condition
    if (current.u_access_type == 'restricted') {
        answer = false;
    } else {
        answer = true;
    }
}
.....
 https://drive.google.com/drive/folders/1xa-xrpASCbU9fDR98KbN8hK-9O20EgDs?usp=drive_link

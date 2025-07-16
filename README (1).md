
# 🚀 IBM Cloud Object Storage IAM Access Control Project

## 📘 Project Title
Secure Access Control in IBM Cloud Object Storage using IAM

## 🎯 Objective
This project simulates secure access to IBM Cloud Object Storage (COS) using Identity and Access Management (IAM) roles like Viewer, Editor, and Manager. It demonstrates how access permissions can be tested using multiple IBM Cloud accounts and Access Groups.

## 🛠️ Tools & Services Used
- IBM Cloud Console
- Cloud Object Storage
- IBM IAM (Identity & Access Management)
- Access Groups
- Resource Groups
- Multiple IBM Cloud Users & Service IDs

## 🧭 Step-by-Step Procedure

### 1. Create a COS Instance
- Go to IBM Cloud → Catalog → Cloud Object Storage → Create

### 2. (Optional) Create Resource Group
- Manage → Account → Resource Groups → Create Resource Group

### 3. Create Access Groups
- IAM → Access Groups → Create → (e.g., ViewerGroup, EditorGroup, AdminGroup)

### 4. Assign IAM Roles to Groups
- Assign COS roles (Viewer/Writer/Manager) scoped to your COS instance
- Assign Viewer/Editor on Resource Group as needed

### 5. Invite Users
- IAM → Users → Invite → Add to relevant Access Group

### 6. Create Bucket
- COS Instance → Buckets → Create Bucket (e.g., `test-bucket`)

### 7. Log In and Test Roles
- Each user logs in → Resource List → COS → Test actions

### 8. (Optional) Service ID
- IAM → Service IDs → Create → Assign to Access Group → Use API Key for programmatic testing

## ✅ Test Matrix

| Action                        | Viewer | Editor | Manager |
|------------------------------|--------|--------|---------|
| View buckets                 | ✅     | ✅     | ✅      |
| Upload files to bucket       | ❌     | ✅     | ✅      |
| Delete objects               | ❌     | ✅     | ✅      |
| Create/Delete buckets        | ❌     | ❌     | ✅      |
| View lifecycle/CORS settings | ❌     | ❌     | ✅      |

## 📸 Outputs
- COS instance access verified by each role
- Upload and delete tested
- Access Denied validated for lower roles
- Lifecycle rule editable only by Manager

## 🎓 Learnings
- IAM role mapping and access groups
- Secure bucket operations via scoped roles
- Differences between Viewer, Writer, Manager

## 📌 Conclusion
IBM Cloud IAM effectively secures object storage using role-based access. This simulation mirrors real-world cloud team operations.

## 🌱 Future Scope
- Extend to Watson services
- Automate access using Service IDs
- Implement API access control with Activity Tracker

---

Created by: Shubhanshi Sharma

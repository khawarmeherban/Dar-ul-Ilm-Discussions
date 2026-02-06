# 🔧 Giscus Comments Setup Guide

Your blog has a beautiful comments section, but it needs to be configured on GitHub.

## 🚨 Important: Your Website Repository is Private

Since **Giscus requires a public repository** but your website code must stay private, you need to create a **separate public repository** just for discussions.

## 📋 Prerequisites
- GitHub account (you already have this) ✅
- Separate **public repository** for discussions (create below)
- Admin access to both repositories ✅

## ⚡ Quick Setup (7 minutes)

### Step 1: Create Separate Public Repository

1. Go to: https://github.com/new
2. Repository name: `Dar-ul-Ilm-Discussions`
3. Description: "Public repository for blog discussions and comments"
4. Select **Public** ✅
5. Check "Add a README file"
6. Click **Create repository**

### Step 2: Enable GitHub Discussions

1. Go to your NEW repository: https://github.com/khawarmeherban/Dar-ul-Ilm-Discussions
2. Click **Settings** tab
3. Scroll down to **Features** section
4. Check the box for **Discussions**
5. Click **Set up discussions**

### Step 3: Install Giscus App

1. Visit: https://github.com/apps/giscus
2. Click **Install**
3. Select **khawarmeherban/Dar-ul-Ilm-Discussions** (the NEW public repo)
4. Click **Install & Authorize**

### Step 5: Copy Configuration

Giscus will generate NEW code. You'll see something like:

```html
data-repo="khawarmeherban/Dar-ul-Ilm-Discussions"
data-repo-id="R_xxxxxxxxxxxxx"  (NEW ID)
data-category="General"
data-category-id="DIC_xxxxxxxxxxxxx"  (NEW ID)
```

### Step 6: Update Your Code

Open `src/components/GiscusComments.tsx` and replace:
- `data-repo-id="REPLACE_WITH_NEW_REPO_ID"` with the NEW repo ID
- `data-category-id="REPLACE_WITH_NEW_CATEGORY_ID"` with the NEW category ID

Then commit and push:
```bash
git add .
git commit -m "Update Giscus to use separate discussions repository"
git push
```


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

### Step 7
data-repo="khawarmeherban/Dar-ul-Ilm-Institute-"
data-repo-id="R_kgDONhTWCQ"
data-category="General"
data-category-id="DIC_kwDONhTWCc4CloGH"
```

**Note:** Your current IDs in the code are already correct! Just enable Discussions and install the app.

### Step 5: Verify

1. Visit any blog post: https://darulilm.vercel.app/blog/[any-article]
2. Scroll to comments section
3. You should see the comment box
4. Try posting a comment with your GitHub account

## 🎯 How Users Join Discussion
**Your website code stays private** in your main repository ✅
- **Comments are public** in the separate discussions repository
- Users must have a GitHub account to comment
- You can moderate comments through GitHub Discussions
- You can delete or hide inappropriate comments
- Block users if needed
- Comments are stored on GitHub (not on Vercel or any database)

## 🏗️ Repository Structure

You'll have TWO repositories:

1. **Dar-ul-Ilm-Institute-** (PRIVATE) 
   - Your website source code
   - Next.js files
   - Sanity configuration
   - Environment variables
   - Stays completely private ✅

2. **Dar-ul-Ilm-Discussions** (PUBLIC)
   - Only stores blog comments
   - No website code
   - No sensitive information
   - Visitors can view/post comments
   - You maintain full moderation control
3. **Add Reactions** - Like, love, or react to comments
4. **Reply to Comments** - Have threaded discussions
5. **Get Notifications** - Receive emails when someone replies

## 🔐 Privacy & Moderation

- Users must have a GitHub account to comment
- You can moderate comments through GitHub Discussions
- You can delete or hide inappropriate comments
- Block users if needed
- Comments are stored on GitHub (not on Vercel or any database)

## ✨ Current Features Already Implemented

Your blog has:
- ✅ Beautiful comment section UI
- ✅ Error handling with helpful instructions
- ✅ Dark mode support
- ✅ Animated entrance
- ✅ Reaction support enabled
- ✅ "Join the Discussion" header
- ✅ Fallback message showing "Powered by Giscus"

## 🐛 Troubleshooting

**Still seeing "giscus is not installed" error?**
1. Make sure Discussions are enabled
2. Verify Giscus app is installed on your repo
3. Check repository is public
4. Wait 5 minutes after setup for changes to propagate
5. Clear browser cache and reload

**Comments not showing?**
1. Check browser console for errors
2. Verify repository name is correct
3. Make sure the category exists in Discussions
4. Try with a different browser

## 📝 Alternative: Disable Comments Temporarily

If you want to disable comments for now, you can comment out the section in:
`src/app/blog/[slug]/page.tsx`

```tsx
{/* Comments */}
{/* <div className="...">
  <GiscusComments ... />
</div> */}
```

## 🔄 Alternative Comment Systems (If You Don't Want Separate Repo)

If you don't want to create a separate public repository, consider these alternatives:

### 1. **Disqus** (Most Popular)
- ✅ Works with private repos
- ✅ Free tier available
- ✅ Easy setup
- ❌ Shows ads on free tier
- ❌ Tracks users
- Tutorial: https://disqus.com/

### 2. **Commento** (Privacy-Focused)
- ✅ No tracking
- ✅ No ads
- ✅ Works with private repos
- ❌ Paid ($10/month)
- Tutorial: https://commento.io/

### 3. **Hyvor Talk** (Modern)
- ✅ No ads
- ✅ Privacy-focused
- ✅ Works with private repos
- ❌ Paid (starts $5/month)
- Tutorial: https://talk.hyvor.com/

### 4. **Custom Database Solution**
- ✅ Full control
- ✅ No third-party dependencies
- ❌ Requires database (MongoDB, PostgreSQL)
- ❌ More complex setup
- ❌ Need to build moderation tools

### 5. **No Comments**
- ✅ Simplest solution
- ✅ Focus on content
- ✅ Direct readers to social media
- ❌ Less engagement

**Recommendation:** Separate discussions repository is best because:
- ✅ FREE forever
- ✅ No ads or tracking
- ✅ Your code stays private
- ✅ Full control
- ✅ 5-minute setup

## 🚀 Benefits of Giscus

- ✅ **Free & Open Source**
- ✅ **No database needed**
- ✅ **GitHub authentication** (secure)
- ✅ **Markdown support** in comments
- ✅ **Threaded replies**
- ✅ **Email notifications**
- ✅ **Full moderation control**
- ✅ **SEO friendly** (indexed by search engines)
- ✅ **Privacy focused** (no tracking)

## 💡 Need Help?

- Giscus Documentation: https://github.com/giscus/giscus
- GitHub Discussions Guide: https://docs.github.com/en/discussions
- Contact: Your repository issues page

---

**After setup, your comments will look like this:**

1. Beautiful header: "Join the Discussion"
2. Sign-in button (GitHub OAuth)
3. Text editor with markdown support
4. Threaded comment display
5. Reaction buttons (👍 ❤️ 🎉 👎)
6. Reply functionality

**Time to complete:** 7 minutes
**Difficulty:** Easy
**Cost:** Free forever

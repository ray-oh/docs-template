---
title: Linking to a Private Repository
nav_order: 6
---

# 🔗 Linking to a Private Repository

While you **can’t embed or display the contents** of a private GitHub repository on your public documentation site (due to GitHub’s access controls), you **can link to it**—provided your audience has access.

This is useful when your documentation lives in a **public or internal docs repo**, but your **source code is in a private repo**.

## ✅ How to Link to a Private Repo

Simply use a standard Markdown link:

[View the source code](https://github.com/ray-oh/business_card)  
```markdown
[View the source code](https://github.com/ray-oh/business_card)
```

If a user **does not have access** to your private GitHub repository and clicks a link to it (e.g., `https://github.com/your-username/your-private-repo`), here’s exactly what they’ll see:

---

### 🔒 **What GitHub Shows to Unauthorized Users**

#### **1. If the user is signed in to GitHub but *not* granted access:**
- They’ll see a **404 “Not Found” page** with this message:
  > **“Repository not found”**  
  > *The repository at `github.com/your-username/your-private-repo` does not exist or you do not have permission to view it.*

#### **2. If the user is *not signed in* (or using an incognito window):**
- They’ll be redirected to the **GitHub homepage** or shown a **generic 404 page**, **without any indication that the repo exists**.
- No error explicitly says “this is a private repo”—GitHub intentionally avoids confirming the existence of private repos for security.

---

### 🛡️ Why This Happens
GitHub **never reveals the existence or contents of private repositories** to unauthorized users—not even the name, README, or file structure. This is a core security measure to prevent data leakage.

---

### ✅ Practical Implications for Your Docs
When you include a link like:
```markdown
[View internal source code](https://github.com/ray-oh/business_card)
```
- ✅ **Team members with access** will see the repo and its README.
- ❌ **External users or collaborators without access** will see a **404 error**—**not your README**.

> 💡 **Best practice**: Always label such links clearly as *private* or *internal* so users understand why the link might not work for them.

Example:
```markdown
[🔒 Internal: Business Card Source (Private)](https://github.com/ray-oh/business_card)
```

This manages expectations and reduces confusion.

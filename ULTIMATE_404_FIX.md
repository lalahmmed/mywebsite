# The Ultimate "404 Page Not Found" Fix Guide

If you've uploaded the files and still see a 404, please follow these steps in order. One of these **will** fix it.

## 1. The "Case Sensitivity" Check
GitHub Pages is **case-sensitive**. 
- Ensure your file is named exactly `index.html` (all lowercase).
- If it is `Index.html` or `INDEX.HTML`, it will return a 404.

## 2. The "Branch" Check (Most Common)
GitHub recently changed the default branch name from `master` to `main`.
1. Go to your repo **Settings** > **Pages**.
2. Look at **Branch**. 
3. If it says `None`, select `main` (or `master`) and click **Save**.
4. If it's already set, try switching it to a different branch and then back to `main` to "nudge" GitHub to rebuild.

## 3. The "Repository Name" Check
- If your repository is named `username.github.io`, your site is at `https://username.github.io/`.
- If your repository is named `my-project`, your site is at `https://username.github.io/my-project/`.
- **Crucial:** Make sure you are visiting the correct URL! Check the link provided at the top of the **Settings > Pages** screen.

## 4. The "Empty Commit" Trick
Sometimes GitHub's automation gets stuck. You can force it to try again by making a tiny change:
1. Open `index.html` on GitHub.com.
2. Click the Edit (pencil) icon.
3. Add a single space at the very end of the file.
4. Click **Commit changes**.
5. Go to the **Actions** tab and watch the "pages-build-deployment" run.

## 5. The "Custom Domain" Conflict
Do you have a `CNAME` file in your repository?
- If you are NOT using a custom domain (like `www.yourname.com`), **delete** the `CNAME` file if it exists. It will break the default `github.io` link.

## 6. The "Visibility" Check
- Is your repository **Private**? 
- GitHub Pages is free for Public repositories. For Private repositories, you need a GitHub Pro account. If it's private and you don't have Pro, it will 404.
- **Fix:** Go to **Settings** > **General** > **Danger Zone** > **Change visibility** and make it **Public**.

---

### Still not working?
Try the "gh-pages" branch method:
1. Create a new branch in your repo named `gh-pages`.
2. Go to **Settings** > **Pages**.
3. Change the Source Branch to `gh-pages`.
4. GitHub often prioritizes this branch name for deployment.

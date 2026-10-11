# Team Crest Headshots: GitHub Pages setup

The whole portal is the single file `index.html`. Photos are processed in each user's browser; nothing is uploaded.

## 1. Publish (about 10 minutes)
1. Sign in to GitHub with the account IT approves (ideally a U.S. Ski & Snowboard organization account, not a personal one).
2. Click **+** (top right) > **New repository**. Name it `crest-headshots`. Choose **Public** (needed on the free plan; on a paid plan the repository can be private, but the site itself is still public). Click **Create repository**.
3. On the new repository page, click **uploading an existing file** (or **Add file > Upload files**). Drag in `index.html`. Click **Commit changes**.
4. Go to **Settings > Pages**. Under **Build and deployment > Source**, choose **Deploy from a branch**. Set the branch to **main** and the folder to **/ (root)**. Click **Save**.
5. Wait a minute or two, then refresh the Pages settings. The site address appears at the top, like `https://<account>.github.io/crest-headshots/`.
6. Open it, pick a crest, run one headshot, and check both downloads.

## 2. Optional: feedback form
1. In Smartsheet, create a form with a **Text/Number** field named exactly `Details` (set it to multi-line) and, if you like, an attachment field for screenshots.
2. Copy the form's link.
3. In GitHub, open `index.html`, click the pencil (Edit), find this line near the bottom of the file:
   `const FEEDBACK_URL = '';`
   and paste the link between the quotes. Click **Commit changes**.
4. Each photo now shows **Something's off**. It opens the form with the photo details filled in (also copied to the clipboard).

## 3. Optional: a U.S. Ski & Snowboard address
1. Pick an address with IT, e.g. `headshots.usskiandsnowboard.org`.
2. **Settings > Pages > Custom domain**: enter it and click **Save**.
3. IT adds a **CNAME** DNS record pointing that address to `<account>.github.io`.
4. When GitHub shows the DNS check passed, tick **Enforce HTTPS**.

## 4. Updating
Upload the new `index.html` with **Add file > Upload files** (same name, so it replaces the old one) and commit. The live site updates in a minute or two. The version number in the header and footer shows which version is live; users may need to refresh.

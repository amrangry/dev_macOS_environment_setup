# SSH Setup for Business GitHub Account

## Step 1: Check SSH Keys on Your Machine
1. Open your Terminal.
2. Run the following command to check if there are any SSH keys already on your Mac:
   ```bash
   ls -al ~/.ssh
   ```
---

## Step 2: Generate an SSH Key for Your Business Account
1. Run the following command in Terminal to create a new SSH key:
   ```bash
   ssh-keygen -t ed25519 -C "amr.elghadban@adkatech.com"
   ```
2. When prompted, save the key as:
   ```bash
   /Users/amr.elghadban/.ssh/id_ed25519_business_amr_elghadban_adkatech
   ```
3. Leave the passphrase empty (or add one for security).
4. **Result:**
   ```
   Your identification has been saved in /Users/amr.elghadban/.ssh/id_ed25519_business_amr_elghadban_adkatech
   Your public key has been saved in /Users/amr.elghadban/.ssh/id_ed25519_business_amr_elghadban_adkatech.pub
   The key fingerprint is: 
   SHA256:4AAAAAAhXXXXXXXXXXDyK+M/L2bbbbSs amr.elghadban@adkatech.com
   ```
---

## Step 3: Add the SSH Key to Your Business GitHub Account
1. Copy the new public key to your clipboard:
   ```bash
   pbcopy < ~/.ssh/id_ed25519_business_amr_elghadban_adkatech.pub
   ```
2. Go to your GitHub Business account:
   - Click your profile picture → **Settings**.
   - Navigate to **SSH and GPG keys** under **Access**.
   - Click **New SSH key**.
3. Paste the public key into the "Key" field.
   - Give it a meaningful title (e.g., *MacBook Pro Business Key*).
   - Click **Add SSH key**.
---

## Step 4: Configure the SSH Config File for Multiple Accounts
1. Open the SSH config file:
   ```bash
   nano ~/.ssh/config
   ```
2. If the file doesn't exist, create it:
   ```bash
   nano ~/.ssh/config
   ```
3. Add the following configuration:
   ```
   # Personal GitHub Account
   Host github.com-personal
     HostName github.com
     User git
     IdentityFile ~/.ssh/id_ed25519

   # Business GitHub Account
   Host github.com-business
     HostName github.com
     User git
     IdentityFile ~/.ssh/id_ed25519_business_amr_elghadban_adkatech
   ```
4. Save the file:
   - Press `Ctrl + O`, then `Enter`.
   - Press `Ctrl + X` to exit.
5. Set correct permissions:
   ```bash
   chmod 600 ~/.ssh/config
   ```
---

## Step 5: Test the SSH Configuration
Run the following command to test the SSH connection:
```bash
ssh -T git@github.com-business
```
**Expected Output:**
```
Hi AmrAhmedElghadban! You've successfully authenticated, but GitHub does not provide shell access.
```
---

## Step 6: Clone the Repository Using the Business SSH Configuration
Use the business SSH alias:
```bash
git clone git@github.com-business:<company>/<reponame>.git
```
**Do not use:**
```bash
git clone git@github.com:<company>/<reponame>.git
```
---

## Step 7: Move to the Repository
1. Decide where to move the repository:
   ```bash
   mv ~/POSRetail_Php /Users/amr.elghadban/Desktop/workspace/project_folder
   ```
2. Verify the move:
   ```bash
   ls /Users/amr.elghadban/Desktop/workspace/project_folder
   ```
   You should see the `project_folder` folder.
3. Navigate to the new location:
   ```bash
   cd /Users/amr.elghadban/Desktop/workspace/project_folder/repo
   ```
---

## Step 8: Confirm Everything Works
1. Check the Git status:
   ```bash
   git status
   ```
2. Ensure the remote origin is set correctly:
   ```bash
   git remote -v
   ```
   **Expected Output:**
   ```
   origin  git@github.com-business:<company>/<reponame>.git (fetch)
   origin  git@github.com-business:<company>/<reponame>.git (push)
   ```
---

## Step 9: (Optional) Configure Global Identity
Set your global Git identity (if most repositories are personal):
```bash
git config --global user.name "Your Personal Name"
git config --global user.email "your.personal.email@example.com"
```
Confirm the settings:
```bash
git config --global --list
```
---

## Step 10: Configure Repository-specific Identity (Business Repo)
1. Navigate to the repository directory:
   ```bash
   cd /Users/amr.elghadban/Desktop/workspace/project_folder/repo
   ```
2. Set the identity for this repository:
   ```bash
   git config user.name "Amr Ahmed Elghadban"
   git config user.email "your-business-email@company.com"
   ```
3. Check the repository-specific configuration:
   ```bash
   git config --list --local
   ```
---

## Step 11: Verify the Setup
Ensure everything is working as expected.

---

## Step 12: (Optional) Use `.gitconfig` Includes for Easier Setup
Use `.gitconfig` includes to manage multiple identities more efficiently.

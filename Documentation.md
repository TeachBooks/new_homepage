# Setting Up and Collaborating on a WordPress Website Linked to GitHub  

This guide covers how to:  
1. **Set up a new WordPress website linked to GitHub.**  
2. **Collaborate on an existing WordPress website linked to GitHub.**  

---

## Prerequisites  

**Ensure you have the following prerequisites in place before proceeding to the next sections on creating or collaborating on a WordPress website linked to GitHub.**  

### 1. Install Git Locally  
#### 1.1 Check if Git is Installed  
1. Open your terminal (Mac) or command prompt (Windows).  
2. Run: `git --version`.  
   - If installed, you’ll see the version number.  
   - If not, proceed to the next step.  

#### 1.2 Install Git  
- **Windows:** [Download Git for Windows](https://gitforwindows.org/).  
- **Mac:** [Download Git for Mac](https://sourceforge.net/projects/git-osx-installer/).  

#### 1.3 Install GitHub Desktop  
- Download and install [GitHub Desktop](https://desktop.github.com/) for an intuitive interface.  

### 2. Install Local by Flywheel  
- Download and install [Local by Flywheel](https://localwp.com/).  
- Sign up for Local using your GitHub account.  

---

## Part 1: Setting Up a New WordPress Website Integrated with GitHub  

**Follow this section if you are starting a new website that you want to host on GitHub.**  

### Step 1: Create a GitHub Repository  
1. Log in to GitHub and create a new repository (e.g., `new_homepage`).  
2. This repository will host your static WordPress site.  

### Step 2: Create a WordPress Website  
1. Open Local by Flywheel and select **Create New Site**.  
2. Follow the prompts to set up your WordPress site (e.g., `homepage_wordpress`).  
3. Navigate to the site folder and run:  
   ```bash  
   git init  
   ```  
   This initializes a local Git repository, enabling you to connect it to GitHub Desktop later.  

### Step 3: Connect GitHub with GitHub Desktop  
1. Clone the **host repository** (e.g., `new_homepage`) to your local machine using GitHub Desktop.  
2. Publish the **source repository** (e.g., `homepage_wordpress`) by linking the Local site folder to GitHub Desktop.  

### Step 4: Convert WordPress to Static HTML  
#### 4.1 Install and Configure Simply Static Plugin  
1. In Local, access **WP Admin** and log in.  
2. Go to **Plugins → Add New** and search for "Simply Static".  
3. Install and activate the plugin.  
4. Configure settings under **Simply Static**:  
   - **General Settings**:  
     - Replace URLs: Set to **Relative Path**.  
     - Path: Specify the path of the host repository (e.g., `/new_homepage`).  
     - Enable **Force URL Replacements**.  
   - **Deploy Settings**:  
     - Deployment Method: **Local Directory**.  
     - Path: Specify the local path to the cloned host repository.  

#### 4.2 Generate Static Files  
1. Go to **Simply Static → Generate**.  
2. Click **Generate Static Files** to export the site as static HTML with rewritten URLs.  

### Step 5: Push Static HTML to GitHub  
1. Open GitHub Desktop.  
2. Push changes from the local repository to the host repository by clicking **Push Origin**.  
3. Stop the Local site before pushing or pulling changes to avoid conflicts.  

### Step 6: Repeat for Updates  
- For updates, repeat the process of generating static files and pushing them to GitHub.  

---

## Part 2: Collaborating on an Existing Linked Website  

**Follow this section if you want to collaborate on a WordPress website that is hosted on GitHub.**  

### Step 1: Export and Import the Website  
1. In Local, click the three dots next to the site name and select **Export**.  
2. Share the ZIP file with collaborators.  
3. On the collaborator’s machine, drag the ZIP file into Local to import the site.  

### Step 2: Connect GitHub with GitHub Desktop  
1. Clone the host repository to the collaborator's GitHub Desktop.  
2. For the source repository:  
   - Navigate to the imported Local site folder, which already contains a `.git` file.  
   - Open this repository in GitHub Desktop to sync it with the source repository on GitHub.  

### Step 3: Convert WordPress to Static HTML and Push Changes  
- Follow **Steps 4 and 5** from the "Setting Up a New Website" section to generate static files and push changes to GitHub.  

---

By following these steps, you’ll ensure a smooth setup and collaborative workflow for a WordPress site integrated with GitHub.  
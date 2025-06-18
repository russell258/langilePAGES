# langilePAGES
github io pages babyyyyy

Add your HTML/CSS/JS content into the root of this repo.

Push it to GitHub.

GitHub Pages will automatically publish it.


🚀 Step-by-Step: Deploy Angular App to GitHub Pages
🧱 Prerequisites
Angular CLI installed (npm install -g @angular/cli)

A GitHub repository already created

Your Angular project is working locally

✅ Step 1: Install the Deployment Tool
Install the Angular GitHub Pages deployer:

bash
Copy
Edit
ng add angular-cli-ghpages
This will install the package and configure your project for deployment.

✅ Step 2: Build Your Project for Production
Run the Angular build command with the base href set to your GitHub repo:

bash
Copy
Edit
ng build --base-href "https://<your-username>.github.io/<repo-name>/"
Replace <your-username> and <repo-name> with your actual GitHub info.

For example:

bash
Copy
Edit
ng build --base-href "https://russellchin.github.io/my-angular-app/"
This creates a dist/ folder with the production-ready code.

✅ Step 3: Deploy to GitHub Pages
After the build is done, deploy using:

bash
Copy
Edit
npx angular-cli-ghpages --dir=dist/<project-name>
You can find the exact <project-name> by checking the folder name inside dist/. It's usually your Angular project name.

For example:

bash
Copy
Edit
npx angular-cli-ghpages --dir=dist/my-angular-app
This command will push the files to the gh-pages branch of your repo.

✅ Step 4: Enable GitHub Pages in Repo Settings
Go to your GitHub repo.

Click Settings → Pages.

Under Source, select the gh-pages branch.

Save the settings.

🌍 Your Angular App is Live!
Visit:

php-template
Copy
Edit
https://<your-username>.github.io/<repo-name>/
For example:

perl
Copy
Edit
https://russellchin.github.io/my-angular-app/

✅ Optional: Automate with Script in package.json
Add this to your package.json scripts:

json
Copy
Edit
"scripts": {
  "deploy": "ng build --base-href=https://<username>.github.io/<repo-name>/ && npx angular-cli-ghpages --dir=dist/<project-name>"
}
Then deploy with:

bash
Copy
Edit
npm run deploy

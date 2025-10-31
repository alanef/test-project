# Test Project - Simple GitHub Pages Website

A simple, responsive website built with HTML and CSS, designed to be deployed on GitHub Pages.

## 🌟 Features

- Clean, responsive design
- Modern CSS with solid color header
- Smooth scrolling navigation
- Mobile-friendly layout
- Easy to customize and extend

## 🚀 Live Demo

Once deployed, your website will be available at: `https://[your-username].github.io/[repository-name]`

## 📁 Project Structure

```
test-project/
├── index.html      # Main HTML file
├── styles.css      # CSS styling
└── README.md       # This file
```

## 🛠️ How to Deploy to GitHub Pages

### Method 1: Using GitHub Web Interface (Recommended)

1. **Push your code to GitHub** (if not already done):
   ```bash
   git add .
   git commit -m "Add simple GitHub Pages website"
   git push origin main
   ```

2. **Enable GitHub Pages**:
   - Go to your repository on GitHub
   - Click on **Settings** tab
   - Scroll down to **Pages** section in the left sidebar
   - Under **Source**, select **Deploy from a branch**
   - Choose **main** branch and **/ (root)** folder
   - Click **Save**

3. **Access your website**:
   - GitHub will provide a URL like: `https://[your-username].github.io/[repository-name]`
   - It may take a few minutes for the site to be available

### Method 2: Using GitHub Actions (Advanced)

1. Create `.github/workflows/pages.yml`:
   ```yaml
   name: Deploy to GitHub Pages

   on:
     push:
       branches: [ main ]

   jobs:
     deploy:
       runs-on: ubuntu-latest
       steps:
         - uses: actions/checkout@v3
         - name: Deploy to GitHub Pages
           uses: peaceiris/actions-gh-pages@v3
           with:
             github_token: ${{ secrets.GITHUB_TOKEN }}
             publish_dir: ./
   ```

2. Push the workflow file and your site will auto-deploy on every push.

## 🔧 Local Development

To test your website locally:

1. **Simple HTTP Server** (Python):
   ```bash
   # Python 3
   python -m http.server 8000

   # Python 2
   python -m SimpleHTTPServer 8000
   ```
   Then open `http://localhost:8000`

2. **Live Server** (VS Code Extension):
   - Install the "Live Server" extension
   - Right-click on `index.html`
   - Select "Open with Live Server"

3. **Node.js http-server**:
   ```bash
   npx http-server
   ```

## 🎨 Customization

### Changing Colors
Edit the color values in `styles.css`:
- Header background: `background: #006600;` (line 17)
- Accent colors: `#667eea` and `#764ba2` (used for h2, h3, feature cards)

### Adding Content
- Modify sections in `index.html`
- Add new pages by creating additional `.html` files
- Update navigation links in the header

### Adding Images
1. Create an `images/` folder
2. Add your images to the folder
3. Reference them in HTML: `<img src="images/your-image.jpg" alt="Description">`

## 📱 Responsive Design

The website includes responsive design features:
- Mobile-friendly navigation
- Flexible grid layout
- Scalable typography
- Touch-friendly buttons

## 🔗 Custom Domain (Optional)

To use a custom domain:

1. Create a `CNAME` file in the root directory with your domain:
   ```
   yourdomain.com
   ```

2. Configure DNS records with your domain provider:
   - Add a CNAME record pointing to `[your-username].github.io`

3. Update GitHub Pages settings to use your custom domain

## 📝 Troubleshooting

**Site not loading?**
- Wait 5-10 minutes after enabling GitHub Pages
- Check that `index.html` is in the root directory
- Verify the repository is public (or you have GitHub Pro for private repos)

**Changes not showing?**
- Clear browser cache
- Wait a few minutes for GitHub to rebuild the site
- Check the Actions tab for build status

**Custom domain issues?**
- Verify DNS propagation (can take up to 24 hours)
- Check CNAME file format (no `http://` or `https://`)

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 🤝 Contributing

Feel free to fork this project and submit pull requests for improvements!

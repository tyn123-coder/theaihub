# AI Hub - AI Tools Directory

A modern, SEO-friendly directory of AI tools and resources. Built with pure HTML, CSS, and JavaScript for easy deployment on GitHub Pages.

![Tech Theme Preview](https://via.placeholder.com/800x400/0a0e17/00d4ff?text=AI+Hub+Preview)

## Features

- **Modern Tech Design**: Cyberpunk-inspired dark theme with neon accents
- **SEO Optimized**: Full meta tags, Open Graph, Twitter Cards, and semantic HTML
- **Responsive**: Works on all devices - desktop, tablet, and mobile
- **Fast Loading**: No external frameworks, pure vanilla JS
- **Search & Filter**: Find tools by name, category, or pricing
- **Tool Details**: Each tool has its own detailed page with features and use cases
- **Accessible**: WCAG compliant with keyboard navigation support

## Pages

1. **Homepage** (`index.html`) - Browse all AI tools with search and filters
2. **Tool Detail** (`detail.html`) - Detailed view of each AI tool
3. **Submit Tool** (`submit.html`) - Submit new AI tools for review
4. **Terms of Use** (`terms.html`) - Legal terms
5. **Privacy Policy** (`privacy.html`) - Privacy information

## Deployment to GitHub Pages

### Method 1: Using GitHub Web Interface

1. Create a new GitHub repository
2. Upload all files from this project:
   - `index.html`
   - `detail.html`
   - `submit.html`
   - `terms.html`
   - `privacy.html`
   - `styles.css`
   - `data.js`
3. Go to repository **Settings** > **Pages**
4. Under "Source", select **Deploy from a branch**
5. Select the **main** branch and **/ (root)** folder
6. Click **Save**
7. Wait 1-2 minutes, your site will be live at: `https://yourusername.github.io/ai-hub/`

### Method 2: Using Git Command Line

```bash
# Create new repository on GitHub first, then:
git clone https://github.com/yourusername/ai-hub.git
cd ai-hub
# Copy all files to this folder
git add .
git commit -m "Initial commit"
git push -u origin main
# Then enable GitHub Pages in repository Settings
```

### Method 3: Using GitHub Desktop

1. Create new repository
2. Drag and drop all project files
3. Publish repository
4. Enable GitHub Pages in Settings

## Setting Up Submit Tool Form (Formspree)

The Submit Tool page uses [Formspree](https://formspree.io/) to collect tool submissions. Follow these steps:

### Step 1: Create Formspree Account

1. Go to [formspree.io](https://formspree.io/)
2. Sign up for a free account
3. Click "New Form" to create a new form

### Step 2: Get Your Form ID

1. After creating the form, you'll see your **Form ID**
2. It looks like: `https://formspree.io/f/xvwqbnk`
3. Copy the part after `/f/` (e.g., `xvwqbnk`)

### Step 3: Update submit.html

Open `submit.html` and replace `YOUR_FORMSPREE_ID` with your actual Formspree ID:

```html
<!-- Change this line: -->
<form action="https://formspree.io/f/YOUR_FORMSPREE_ID" method="POST" ...>

<!-- To this (example): -->
<form action="https://formspree.io/f/xvwqbnk" method="POST" ...>
```

### Step 4: Configure Form Notifications (Optional)

In your Formspree dashboard:
1. Go to your form settings
2. Add email notifications to receive submissions
3. Or connect to other integrations like Google Sheets, Slack, etc.

### Formspree Free Plan Limits

- **50 submissions/month**
- **250MB file uploads**
- Perfect for small to medium websites

For higher limits, upgrade to Formspree Plus plan.

## Customization

### Adding New Tools

Edit `data.js` and add new entries to the `aiTools` array:

```javascript
{
    id: 'unique-id',
    name: 'Tool Name',
    description: 'Brief description',
    icon: '🤖', // Use any emoji as the icon
    pricing: 'free', // free, freemium, paid, opensource
    category: 'text', // text, image, video, audio, code, productivity, marketing, analytics, automation, research, design, support, ecommerce
    tags: ['Tag1', 'Tag2'],
    website: 'https://example.com',
    features: ['Feature 1', 'Feature 2'],
    useCases: ['Use Case 1', 'Use Case 2'],
    rating: 4.5,
    reviews: 1000
}
```

### Changing Site URL

After deployment, update these files with your actual GitHub Pages URL:

1. `index.html` - Update the canonical URL and Open Graph URLs
2. `detail.html` - Update the canonical URL

### Changing Brand Name

Replace "AI Hub" with your brand name in:
- `index.html`
- `detail.html`
- `terms.html`
- `privacy.html`
- `styles.css` (logo-text class)

## SEO Checklist

- [x] Meta description on all pages
- [x] Open Graph tags
- [x] Twitter Card tags
- [x] Semantic HTML structure
- [x] Alt text for images
- [x] Canonical URLs
- [x] Mobile responsive
- [x] Fast loading (pure HTML/CSS/JS)

## Browser Support

- Chrome 80+
- Firefox 75+
- Safari 13+
- Edge 80+

## License

MIT License - Feel free to use and modify for your own projects.

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

---

Made with ⚡ for the AI community

# JewGo Status Monitor

Real-time uptime monitoring for JewGo services using [Upptime](https://upptime.js.org/).

## 🚀 What This Monitors

- **Frontend**: https://jewgo.vercel.app
- **Backend API**: https://jewgo-api.onrender.com
- **API Health**: https://jewgo-api.onrender.com/health
- **Database**: https://jewgo-api.onrender.com/api/restaurants

## 📊 Status Page

Once deployed, your status page will be available at:
- **GitHub Pages**: `https://[your-username].github.io/jewgo-status/`
- **Custom Domain** (optional): `https://status.jewgo.io`

## 🛠 Setup Instructions

### 1. Create GitHub Repository

1. Go to [GitHub](https://github.com) and create a new repository named `jewgo-status`
2. Make it **public** (required for GitHub Pages)
3. Clone it to your local machine

### 2. Push This Code

```bash
# Add all files
git add .

# Commit
git commit -m "Initial JewGo monitoring setup"

# Push to GitHub
git push origin main
```

### 3. Enable GitHub Pages

1. Go to your repository settings
2. Navigate to "Pages"
3. Set source to "Deploy from a branch"
4. Select `gh-pages` branch
5. Save

### 4. Configure GitHub Actions

The monitoring will automatically start running every 5 minutes once you push the code.

## 🔧 Configuration

### Monitoring Schedule

Currently set to check every **5 minutes**. You can modify this in `.github/upptime.yml`:

```yaml
schedule: "*/5 * * * *"  # Every 5 minutes
```

### Adding More Services

Add new services to monitor in `.github/upptime.yml`:

```yaml
sites:
  - name: "New Service"
    url: "https://your-service.com"
    method: GET
    timeout: 30
    retry: 3
```

### Custom Domain (Optional)

To use a custom domain like `status.jewgo.io`:

1. Uncomment the `cname` line in `.github/upptime.yml`
2. Set up DNS to point to `[your-username].github.io`
3. Add the domain to your GitHub Pages settings

## 📈 Features

- **Real-time monitoring** every 5 minutes
- **Automatic GitHub Issues** when services go down
- **Auto-resolution** when services come back online
- **Beautiful status page** with uptime history
- **Response time tracking**
- **Zero cost** - runs entirely on GitHub Actions

## 🔔 Notifications

When a service goes down:
- ✅ Creates a GitHub issue automatically
- ✅ Includes response time and status code
- ✅ Auto-resolves when service comes back online

## 📁 File Structure

```
jewgo-status/
├── .github/
│   ├── upptime.yml          # Main configuration
│   └── workflows/
│       └── uptime.yml       # GitHub Actions workflow
├── package.json             # Dependencies
└── README.md               # This file
```

## 🚨 Troubleshooting

### GitHub Actions Not Running

1. Check that the repository is public
2. Verify the workflow file is in `.github/workflows/`
3. Check GitHub Actions tab for any errors

### Status Page Not Updating

1. Ensure GitHub Pages is enabled
2. Check that the `gh-pages` branch is being created
3. Verify the workflow has proper permissions

### Custom Domain Issues

1. DNS must point to `[username].github.io`
2. Add domain to GitHub Pages settings
3. Wait for DNS propagation (can take up to 24 hours)

## 📞 Support

If you need help:
1. Check the [Upptime documentation](https://upptime.js.org/docs/)
2. Review GitHub Actions logs
3. Check the status page for current service status

---

**Built with ❤️ for JewGo using [Upptime](https://upptime.js.org/)** # JewGo Status Monitor - Updated Wed Jul 30 12:05:58 EDT 2025

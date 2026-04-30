# Villa Leonessa Brand Book - Deployment Guide

## Repository
- **GitHub**: https://github.com/kcbdev/villa-leonessa-brand-book
- **Branch**: main
- **Coolify App UUID**: aa5135aztxqrwfrjnknxj8bl
- **Live URL**: https://villa-leonessa.kcb.ma

## Auto-Deploy Workflow

```bash
# 1. Make changes locally
edit index.html  # or any file

# 2. Stage changes
git add <files>

# 3. Commit
git commit -m "Describe your changes"

# 4. Push to trigger auto-deploy
git push origin main
```

Coolify will automatically detect the push and deploy within ~30 seconds.

## Current Files

| File | Purpose |
|------|---------|
| `index.html` | Main brand book page |
| `sartorial-identity.html` | Sartorial identity page |
| `chef-assistant.png` | Staff role image |
| `gardening.png` | Staff role image |
| `housekeeping.png` | Staff role image |
| `manager.png` | Staff role image |
| `mantaince.png` | Staff role image |
| `security.png` | Staff role image |
| `Villa Leonessa - Sartorial Identity.pdf` | Brand PDF |

## Coolify Configuration

- **Build Pack**: nixpacks
- **Static Image**: nginx:alpine
- **Port**: 80
- **Base Directory**: /
- **Health Check**: GET / (HTTP 200)

## Monitoring

- **Deployment Logs**: Coolify Dashboard → Villa Leonessa Brand Book → Deployments
- **Application Logs**: `coolify application_logs --uuid aa5135aztxqrwfrjnknxj8bl`

## Troubleshooting

If auto-deploy doesn't trigger:
1. Check GitHub webhook in repo Settings → Webhooks
2. Manually trigger deploy in Coolify
3. Verify Coolify GitHub app has push access

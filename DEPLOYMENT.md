# Deployment Guide

## Local Development

The JJSW Intelligence Platform is a static web application that can be run locally or deployed to any web hosting service.

### Running Locally

1. Clone the repository:
   ```bash
   git clone https://github.com/[username]/jjsw-intelligence-platform.git
   cd jjsw-intelligence-platform
   ```

2. Open `index.html` in your web browser, or serve it with a simple HTTP server:
   ```bash
   # Python 3
   python -m http.server 8000
   
   # Python 2
   python -m SimpleHTTPServer 8000
   
   # Node.js (with http-server installed)
   npx http-server
   ```

3. Navigate to `http://localhost:8000` in your browser

## Web Hosting Deployment

### GitHub Pages (Free)

1. Fork this repository to your GitHub account
2. Go to repository Settings → Pages
3. Select "Deploy from a branch" and choose `main` branch
4. Your site will be available at `https://[username].github.io/jjsw-intelligence-platform`

### Netlify (Free Tier Available)

1. Connect your GitHub repository to Netlify
2. Build settings:
   - Build command: (leave empty)
   - Publish directory: `.` (root)
3. Deploy automatically on push to main branch

### Vercel (Free Tier Available)

1. Import your GitHub repository to Vercel
2. No build configuration needed
3. Auto-deploy on push to main branch

### Custom Domain Setup

1. Purchase a domain name
2. Configure DNS settings with your hosting provider
3. Update hosting platform settings to use custom domain
4. Enable HTTPS/SSL certificate

## Content Updates

### Updating Intelligence Data

The platform uses embedded JavaScript data objects. To update:

1. Edit the data objects in `index.html` within the `<script>` section
2. Key data sections:
   - `missionStatement`: Update mission text
   - `masterReport`: Modify master intelligence content
   - `texasBriefing`: Update Texas-specific intelligence
   - `priorityTargets`: Add/remove target entities
   - Chart data objects for visualizations

### Adding New Sections

1. Create new data objects following existing patterns
2. Add corresponding render functions
3. Update navigation menu
4. Test all functionality locally before deployment

## Performance Optimization

### For Large Deployments

1. **CDN Integration**: Use a CDN for faster global delivery
2. **Image Optimization**: Optimize any added images
3. **Caching**: Configure appropriate cache headers
4. **Compression**: Enable gzip compression on server

### Monitoring

- Set up analytics to track platform usage
- Monitor load times and user engagement
- Track most accessed sections for content prioritization

## Security Considerations

1. **HTTPS Only**: Always serve over HTTPS
2. **Content Security Policy**: Implement CSP headers if hosting on custom infrastructure
3. **Regular Updates**: Keep external dependencies (CDN links) current
4. **Access Logs**: Monitor for suspicious activity if self-hosting

## Backup and Recovery

1. **Repository Backup**: Maintain Git repository as primary backup
2. **Documentation Backup**: Keep copies of intelligence documentation
3. **Version Control**: Use Git tags for major platform updates
4. **Recovery Plan**: Document steps for rapid redeployment

## Support and Maintenance

### Regular Updates
- Review and update intelligence data monthly
- Verify all external links and dependencies quarterly
- Update visualizations as new data becomes available

### Version Control
- Use semantic versioning for major updates
- Document all changes in commit messages
- Maintain changelog for significant updates

---

For technical issues or deployment questions, refer to your hosting provider's documentation or contact your system administrator.
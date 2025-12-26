# Getting started with Speed Insights

This guide will help you get started with using Vercel Speed Insights on your WordPress project. Speed Insights provides real-world performance data from your site visitors, helping you understand and improve your site's performance.

## What is Speed Insights?

Vercel Speed Insights collects Core Web Vitals and other performance metrics from real users visiting your site. This data helps you identify performance bottlenecks and track improvements over time.

## Prerequisites

- A Vercel account. If you don't have one, you can [sign up for free](https://vercel.com/signup).
- A Vercel project with your WordPress site deployed.
- The Vercel CLI installed (optional but recommended).

## Enable Speed Insights in Vercel

### Step 1: Access your Vercel Dashboard

1. Go to the [Vercel dashboard](https://vercel.com/dashboard)
2. Select your WordPress project from the list
3. Click on the **Speed Insights** tab

### Step 2: Enable Speed Insights

1. Click the **Enable** button in the Speed Insights section
2. A dialog will appear confirming the action
3. Select **Enable** from the dialog

> **Note:** Enabling Speed Insights will add new routes (scoped at `/_vercel/speed-insights/*`) after your next deployment.

## Add Speed Insights to your WordPress Site

### For WordPress Sites on Vercel

If your WordPress site is deployed on Vercel, Speed Insights tracking is typically handled by Vercel's infrastructure automatically. However, for best results, you should ensure your site has proper tracking enabled.

### Using a Performance Monitoring Plugin

For WordPress sites, you can use performance monitoring plugins that integrate with external monitoring services:

1. Consider using plugins like:
   - [Perfmatrix](https://wordpress.org/plugins/perfmatrix/) - Comprehensive performance monitoring
   - [Google Site Kit](https://wordpress.org/plugins/google-site-kit/) - Integrates with Google's performance tools
   - [WP Rocket](https://wp-rocket.me/) - Caching and performance optimization

2. Configure the plugin according to its documentation

3. Connect it to your monitoring service if applicable

## Deploy your WordPress Site to Vercel

### Using Git Integration

1. Connect your WordPress site's git repository to Vercel:
   - Push your WordPress site to GitHub, GitLab, or Bitbucket
   - In the Vercel dashboard, click **Add New** > **Project**
   - Import your repository
   - Configure build settings as needed
   - Click **Deploy**

### Using the Vercel CLI

Alternatively, you can deploy using the Vercel CLI:

```bash
vercel deploy
```

> **Note:** When deploying WordPress to Vercel, ensure your database and media uploads are properly configured. For WordPress, consider using:
> - A managed database service (e.g., Planetscale, Vercel Postgres)
> - Vercel's KV storage for sessions and caching
> - External storage services for media files (e.g., AWS S3, Bunny CDN)

## View your Performance Data

### In the Vercel Dashboard

1. Go to your project's **Speed Insights** tab
2. You'll see metrics including:
   - **First Contentful Paint (FCP)** - How quickly content appears
   - **Largest Contentful Paint (LCP)** - When the main content loads
   - **Cumulative Layout Shift (CLS)** - Visual stability
   - **Interaction to Next Paint (INP)** - Responsiveness

### Data Collection

Performance data begins collecting after deployment. After a few days of visitor traffic, you'll be able to analyze trends and identify performance issues.

## Optimization Tips for WordPress

To improve your Speed Insights metrics:

### 1. Use Caching

- Enable object caching with Redis or Memcached
- Use a caching plugin like WP Super Cache or W3 Total Cache
- Configure browser caching properly

### 2. Optimize Images

- Use modern image formats (WebP)
- Optimize image file sizes
- Consider using a CDN for image delivery

### 3. Minimize JavaScript and CSS

- Minify CSS and JavaScript files
- Defer non-critical JavaScript loading
- Remove unused CSS

### 4. Database Optimization

- Optimize your WordPress database regularly
- Use appropriate database indexing
- Consider query optimization

### 5. Use a CDN

- Serve static assets from a CDN
- Reduce latency for geographically distant users

## Next Steps

Now that you have Speed Insights enabled:

- Monitor your metrics regularly to track improvements
- Set performance goals for your Core Web Vitals
- Use the data to inform optimization decisions
- Share metrics with your team to prioritize improvements

## Related Resources

- [Vercel Speed Insights Documentation](https://vercel.com/docs/speed-insights)
- [Web Vitals Guide](https://web.dev/vitals/)
- [WordPress Performance Optimization](./optimization.md)
- [WordPress Caching](./cache.md)

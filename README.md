# -
اداري

## Production Deployment

### Vercel Deployment

1. **Prerequisites**
   - Node.js 18.x or higher
   - PostgreSQL database
   - GitHub repository connected

2. **Environment Variables**
   - Set `DATABASE_URL` in Vercel project settings
   - Set `NODE_ENV=production`
   - Set `NEXT_PUBLIC_APP_URL=https://yourdomain.com`

3. **Deploy**
   - Push to GitHub main branch
   - Vercel automatically deploys
   - Monitor deployment in Vercel dashboard

4. **Database Migrations**
   - Migrations run automatically during build
   - Ensure all migrations are committed to Git

### Local Setup

```bash
# Install dependencies
npm install

# Setup environment
cp .env.example .env.local
# Edit .env.local with database credentials

# Run migrations
npm run db:migrate

# Start development
npm run dev
```

### Build for Production

```bash
npm run build
NODE_ENV=production npm start
```

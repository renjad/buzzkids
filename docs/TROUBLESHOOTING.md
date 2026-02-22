# Troubleshooting Guide

Common issues and their solutions.

## Installation Issues

### "composer install" fails

**Problem:** Permission errors or missing PHP extensions

**Solution:**

```bash
# Check PHP version
php -v  # Should be 8.2+

# Install missing extensions (Ubuntu/Debian)
sudo apt-get install php-xml php-curl php-mbstring
```

### Docker/Sail won't start

**Problem:** Port 80 already in use

**Solution:**

```bash
# Check what's using port 80
sudo lsof -i :80

# Stop conflicting service or change Sail port in docker-compose.yml
# Change: "80:80" to "8000:80"
```

### "sail: command not found"

**Problem:** Sail alias not configured

**Solution:**

```bash
# Use full path
./vendor/bin/sail up

# Or create alias (add to ~/.bashrc or ~/.zshrc)
alias sail='./vendor/bin/sail'
```

## Database Issues

### Migration fails: "Connection refused"

**Problem:** Database container not running

**Solution:**

```bash
# Check if containers are running
sail ps

# Restart Sail
sail down
sail up -d

# Wait 10 seconds then try migration again
sail artisan migrate
```

### "Base table or view already exists"

**Problem:** Trying to run migrations that already ran

**Solution:**

```bash
# Fresh start (WARNING: deletes all data)
sail artisan migrate:fresh --seed
```

## Frontend Issues

### Styles not loading

**Problem:** Vite/Mix not running or not compiled

**Solution:**

```bash
# Make sure dev server is running
sail npm run dev

# Or build for production
sail npm run build
```

### "npm install" very slow

**Problem:** Network or DNS issues

**Solution:**

```bash
# Clear npm cache
sail npm cache clean --force

# Or use --legacy-peer-deps flag
sail npm install --legacy-peer-deps
```

## LINE Integration Issues

### Notifications not sending

**Problem:** Invalid LINE credentials

**Solution:**

1. Check `.env` file has correct LINE_CHANNEL_ACCESS_TOKEN
2. Verify LINE Official Account is set up
3. Check logs: `sail logs -f`

## General Issues

### "Permission denied" errors

**Problem:** File permissions issue

**Solution:**

```bash
# Fix storage permissions
sail artisan storage:link
sudo chmod -R 775 storage bootstrap/cache
```

### Application key missing

**Problem:** APP_KEY not set in .env

**Solution:**

```bash
sail artisan key:generate
```

### Clear cache when things act weird

```bash
sail artisan cache:clear
sail artisan config:clear
sail artisan route:clear
sail artisan view:clear
```

## Still Having Issues?

1. Check Laravel logs: `storage/logs/laravel.log`
2. Check Sail logs: `sail logs -f`
3. Ask in team Slack channel
4. Create an issue in the repository

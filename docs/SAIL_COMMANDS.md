# Laravel Sail Command Cheat Sheet

Quick reference for commonly used Sail commands. Sail is Laravel's Docker-based development environment.

## Starting & Stopping

```bash
# Start all containers (in background)
sail up -d

# Start and view logs
sail up

# Stop all containers
sail down

# Restart containers
sail restart

# View running containers
sail ps
```

## Artisan Commands

```bash
# Run any artisan command
sail artisan [command]

# Common examples:
sail artisan migrate              # Run migrations
sail artisan migrate:fresh --seed # Fresh database with seed data
sail artisan db:seed              # Seed database
sail artisan make:model Student   # Create model
sail artisan make:controller BookingController
sail artisan tinker               # Interactive console
sail artisan queue:work           # Process queue jobs
sail artisan schedule:work        # Run scheduler
```

## Database

```bash
# Access MySQL CLI
sail mysql

# Run specific SQL file
sail mysql < database.sql

# Database backup
sail exec mysql mysqldump -u sail -p buzzkids > backup.sql

# Database restore
sail mysql < backup.sql
```

## Composer

```bash
# Install dependencies
sail composer install

# Update dependencies
sail composer update

# Add new package
sail composer require package/name

# Remove package
sail composer remove package/name
```

## NPM/Node

```bash
# Install JS dependencies
sail npm install

# Run development server (hot reload)
sail npm run dev

# Build for production
sail npm run build

# Add new package
sail npm install package-name

# Run tests
sail npm test
```

## Testing

```bash
# Run all tests
sail test

# Run specific test file
sail test tests/Feature/BookingTest.php

# Run with coverage
sail test --coverage
```

## Logs & Debugging

```bash
# View all logs
sail logs

# Follow logs (live)
sail logs -f

# View specific service logs
sail logs mysql
sail logs redis

# Clear Laravel caches
sail artisan cache:clear
sail artisan config:clear
sail artisan route:clear
sail artisan view:clear
```

## Shell Access

```bash
# Access container shell
sail shell

# Access as root
sail root-shell

# Run bash command
sail bash -c "ls -la"
```

## Useful Aliases

Add to your `~/.bashrc` or `~/.zshrc`:

```bash
alias sail='./vendor/bin/sail'
alias sa='sail artisan'
alias sam='sail artisan migrate'
alias sat='sail artisan tinker'
```

Then you can use:

```bash
sa migrate        # Instead of sail artisan migrate
sam              # Quick migrate
sat              # Quick tinker
```

## Tips

- Always run `sail up -d` before starting work
- Use `sail down` when done for the day (saves resources)
- If things break, try: `sail down && sail up -d`
- Check container status: `sail ps`
- Access app at: http://localhost

# Setup Checklist

Follow this checklist to ensure your development environment is properly configured.

## Prerequisites

- [ ] **Git** installed
- [ ] **PHP 8.2+** installed
- [ ] **Composer** installed
- [ ] **Docker & Docker Compose** installed (for Laravel Sail)
- [ ] **Node.js & NPM** installed
- [ ] Code editor installed (VS Code recommended)

## Step 1: Clone Repository

- [ ] Clone the repository:

```bash
git clone [repo-url]
cd buzzkids
```

## Step 2: Environment Configuration

- [ ] Copy environment file:

```bash
cp .env.example .env
```

- [ ] Database credentials configured in `.env`
- [ ] LINE API credentials added to `.env` (get from team lead)

## Step 3: Install Dependencies

- [ ] Install PHP dependencies:

```bash
composer install
```

- [ ] Install Node.js dependencies:

```bash
npm install
```

## Step 4: Laravel Sail Setup

- [ ] Start Laravel Sail (Docker):

```bash
./vendor/bin/sail up -d
```

- [ ] Generate application key:

```bash
./vendor/bin/sail artisan key:generate
```

- [ ] Verify Sail is running - no errors in terminal
- [ ] Can access http://localhost in browser

## Step 5: Database Setup

- [ ] Run migrations with seeding:

```bash
./vendor/bin/sail artisan migrate --seed
```

- [ ] Verify database tables created successfully
- [ ] Can login with test credentials:
    - Admin: admin@buzzkids.com / password
    - Student: student@buzzkids.com / password

## Step 6: Frontend Setup

- [ ] Build frontend assets:

```bash
./vendor/bin/sail npm run dev
```

- [ ] Development server runs without errors
- [ ] Tailwind CSS styles are loading correctly
- [ ] No console errors in browser developer tools

## Verification Tests

- [ ] Can login as admin (admin@buzzkids.com)
- [ ] Can login as student (student@buzzkids.com)
- [ ] No console errors in browser

## IDE Setup (Optional but Recommended)

- [ ] Laravel IDE Helper installed
- [ ] PHP Intelephense extension installed (VS Code)
- [ ] Tailwind CSS IntelliSense installed (VS Code)

## Ready to Code!

If all items are checked, you're ready to start development. If you encounter issues, check [TROUBLESHOOTING.md](TROUBLESHOOTING.md).

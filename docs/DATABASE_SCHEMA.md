# Buzzkids Database Schema

## ERD Diagram

**🔗 Live Diagram (Source of Truth):**  
[Edit on dbdiagram.io](https://example.io/d/buzzkids-xxxxx)

**📸 Snapshot (for quick reference):**  
![ERD Snapshot](./assets/erd-snapshot.png)  
_Last updated: 2025-02-13_

> ⚠️ If snapshot differs from live diagram, trust the live diagram

> ⚠️ Always update the diagram when modifying schema

## Schema Change Protocol

When modifying the database schema:

1. ✅ Create migration file
2. ✅ Update ERD diagram (live link)
3. ✅ Update this documentation
4. ✅ Run tests: `sail artisan migrate:fresh --seed`
5. ✅ Update changelog below
6. ✅ Notify team in #dev-backend channel

## Changelog

- **2025-02-13**: Initial schema (BUZZ-2)
- **2025-02-XX**: Added notifications table (BUZZ-XX)

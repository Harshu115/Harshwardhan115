# HYOSUNG Diwali Leave Management 2026

- Supabase-backed employee leave submission form
- Leave window: 04 Nov 2026 to 18 Nov 2026
- Blocked: 10 Nov, 11 Nov, 14 Nov, 15 Nov
- Employee enters full name, official email, leave dates and optional notes
- Admin dashboard with live records and CSV export
- Supabase RLS protects submissions; only users whose `public.profiles.role` is `admin` can read records.

## Configure the admin

Create the admin account in Supabase Auth, then run:

```sql
update public.profiles
set role = 'admin'
where id = '<AUTH_USER_UUID>';
```

The frontend uses only the Supabase publishable key; no service-role key is exposed.

## Deploy to Vercel

Import this GitHub repository into Vercel, or use Vercel Drop with the project ZIP.

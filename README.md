# Recruitment & Placement Management System (Python + MySQL)

Console application that manages candidates, companies, jobs, eligibility, applications, interviews,
offers, joining and placements. `ui_prototype/` holds static HTML/CSS pages (not connected to Python).

## Setup
1. Install MySQL 8 and Python 3.10+.
2. `pip install -r requirements.txt`
3. Create DB: `mysql -u root -p < sql/schema.sql` then (optional) `mysql -u root -p < sql/sample_data.sql`
4. Edit `config/db_config.py` (or set `RPMS_DB_PASSWORD`) with your MySQL password.
5. Run from the project root: `python -m app.main`

## Architecture
`app` (menus, entry) → `service` (business rules) → `dao` (SQL) → MySQL;  `model`, `util`, `exception`, `config` support every layer.

## Workflow
Registration → Verification → Application (Eligibility Engine) → Shortlisting → Interview Scheduling →
Interview Feedback → Selection → Offer → Joining → Placement

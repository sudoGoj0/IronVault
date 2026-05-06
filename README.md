# Codex-gainz
Built by Codex, for #GAINZ

Build process in order for me: 
Create GitHub repo
Build Next.js app locally
Push to GitHub
Connect repo to Vercel
Create Supabase project
Add env variables to Vercel
Build database tables
Deploy

**MVP will look like this: **

🧠 OVERVIEW (WHAT YOU’RE BUILDING)

A mobile-first web app where:

Family logs workouts (run, walk, bike, ruck, lift)
Points are automatically calculated
Weekly leaderboard updates instantly
Works like a simple “fitness game”
🧱 STACK (DO NOT CHANGE)

You will use:

Frontend: Next.js (App Router)
Backend: Supabase
Hosting: Vercel
Code storage: GitHub
🚀 FULL BUILD FLOW (CODEX DRIVEN)
PHASE 0 — SETUP (YOU DO FIRST, THEN CODEX)
You create:
GitHub repo
Supabase project
Vercel project (linked to GitHub)
PHASE 1 — BOOTSTRAP APP (CODEX TASK)
Prompt to Codex:

Create a Next.js App Router project for a mobile-first fitness leaderboard app.
Include Supabase client setup and folder structure (app, components, lib).
Ensure environment variable support.

PHASE 2 — DATABASE (CODEX TASK)
Prompt:

Create Supabase SQL schema for:

users (id, display_name)
activities (id, user_id, type, miles, points, activity_date)

Include foreign keys.

PHASE 3 — AUTH (MINIMAL, SEAMLESS)
Prompt:

Implement Supabase email magic link authentication.
Ensure users stay logged in automatically using persistent sessions.
If session exists, skip login page.

Goal:

login once
never again after that
PHASE 4 — SCORING ENGINE (CORE LOGIC)
Prompt:

Implement scoring rules:

running: 1 point per mile
walking: 1 point per mile
rucking: 2 points per mile
biking: 0.33 points per mile
lifting: 5 points flat per workout

Points must be calculated on submit and stored in database.

PHASE 5 — ADD ACTIVITY PAGE
Prompt:

Build a mobile-friendly Add Activity page:

dropdown for activity type
miles input (hidden for lifting)
submit button

On submit:

calculate points
insert into Supabase activities table
redirect to dashboard
PHASE 6 — DASHBOARD (MAIN SCREEN)
Prompt:

Build dashboard page showing:

weekly leaderboard (rank, name, points)
current user’s weekly points
button to add activity

Leaderboard must reset weekly (Monday–Sunday).

PHASE 7 — LEADERBOARD QUERY
Prompt:

Write Supabase query that:

sums points per user
filters by current week
sorts descending

Return formatted data for UI.

PHASE 8 — HISTORY PAGE
Prompt:

Create history page for logged-in user:

list all activities
show type, miles, points, date
newest first
PHASE 9 — MOBILE UX PASS
Prompt:

Improve UI for mobile:

large touch targets
bottom navigation (Home / Add / History)
minimal typing required
dark clean theme
app-like feel
PHASE 10 — FINAL QA PASS
Prompt:

Review full app and ensure:

Supabase auth works correctly
scoring logic is correct
leaderboard updates properly
mobile UX is smooth
no broken pages or missing imports

Fix all issues.

📱 APP FLOW (WHAT USERS EXPERIENCE)
Open app →
Auto-login →
Dashboard →
See leaderboard →
Tap “Add Activity” →
Log workout in <30 sec →
Instant leaderboard update
🧠 SIMPLE ARCHITECTURE (IMPORTANT)
GitHub → stores code
   ↓
Vercel → hosts app
   ↓
Supabase → stores users + workouts + points
🏆 CORE RULES (DO NOT BREAK)
No Strava integration
No complex gamification
No manual recalculation of points after save
No multiple login prompts
Must work fully on mobile
⚖️ WHY THIS FLOW WORKS

This is optimized for Codex because:

Each step = 1 isolated task
No ambiguous instructions
No overengineering
Clear data model from start
UI built incrementally
🚀 WHAT YOU SHOULD DO NEXT

If you follow this, your real workflow becomes:

Paste Phase 1 into Codex
Review output
Fix small issues
Move to Phase 2
Repeat

That’s it.

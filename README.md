# alpha-taskangel
initial prototype of taskangel, a self-administrating decentralized task completion platform with integrated charitable works

🌐 TaskAngel Sitemap
🏠 1. Homepage
URL: /

Content:

Hero banner: “Bounties with Purpose”

CTA buttons: [Post a Task], [Find Bounties], [View Angel Tasks]

Quick search bar (by tag, keyword)

Featured Bounties (Trending, High Rewards, Angel Tasks)

Top Hunters this week

Treasury Stats: Total Funds, Angel Grants Given

No data changing here. Mostly dynamic content pulled from the backend.

🔍 2. Explore Bounties
URL: /bounties
Filters: Tags, Category, Ongoing Only, Angel Tasks, Funding Size, Newest

Displayed Data:

List of all bounties

Each card shows:

Title, tags, reward size

Bounty creator, deadline

Status (Open, Ongoing, Closed, etc.)

✅ Pulls from: bounties table
❌ No direct data changes on this page

📄 3. Bounty Detail Page 🔧
URL: /bounty/:id

Content:

Title, Description, Tags, Deadline, Reward

Acceptance Criteria (strict guidelines)

Bounty Type (Regular, Ongoing, Angel)

Submission List (if any)

Meta-bounty tasks (pending, open, closed)

Treasury Source (e.g. “Partially funded by Angel Pool”)

Data-Changing Actions:

Submit Work (if you're a bounty hunter)

Add Comments / Ask Questions

Submit a Branch Task 🔧

Stake to Create Meta Task 🔧

Poster can:

Edit bounty (while open) 🔧

Fund or increase bounty 🔧

Accept / reject submissions 🔧

🧾 4. Submit Work Page 🔧
URL: /bounty/:id/submit

Form Fields:

Link to work

Optional notes

Upload files

Acceptance checklist auto-filled from bounty

Action:

Creates a new submission entry

✅ Updates: submissions table, links to bounty id
🔧 Data Change: Yes (new submission created)

🕵️‍♀️ 5. Meta Task Dashboard 🔧
URL: /meta

Content:

List of open meta-bounties needing review

Each includes:

Task name, required stake, estimated difficulty

Link to submission being evaluated

Sort by staked amount or urgency

Actionable Items:

Stake $HALO to accept a meta-task 🔧

Submit verdict & justification 🔧

✅ Updates:

meta_tasks, user_activity_logs, and possibly treasury_events (if slashed)

👤 6. User Profile Page 🔧
URL: /user/:id

Data Sections:

Public Name, Reputation Score

Wallet Address, Join Date

Tasks Posted

Tasks Completed

Stake History

Treasury Contributions

Badges (coming soon)

🔧 Data Changing Options (for the user themselves):

Change display name / bio

Link/Unlink wallet

🧰 7. Post Bounty Page 🔧
URL: /bounties/new

Form Fields:

Title, Description, Tags

Reward amount

Deadline, Type (Ongoing / Angel / Meta)

Strict Acceptance Criteria

Optional Staking Required

Optional Public Forking Allowed

✅ Creates: bounties table entry
🔧 Major Data Changing Page

🌿 8. Branch Bounty Page 🔧
URL: /bounty/:id/branch

Form Fields:

New title, description

Link to original bounty auto-populated

Unique criteria for this branch

New reward pool or "inherited"

✅ Creates: New bounty entry, with parent_bounty_id field
🔧 Data Changing Page

💸 9. Treasury Dashboard 🔧
URL: /treasury

Sections:

Total Treasury Balance (USDC + $HALO)

Angel Tasks Funded

Treasury Events Log (grants, slashes, deposits)

Proposal List

Admin Actions (or DAO in future):

Approve Angel Grants 🔧

Slash Bad Actors (on consensus) 🔧

Match Bounty with Treasury Funds 🔧

✅ Updates: treasury_events, bounties, angel_grants

📈 10. Reputation Explorer
URL: /reputation

Content:

Top Hunters

Top Meta-Verifiers

Top Donors

Reputation Calculation Model (transparent)

Reputation Over Time Graph (per user or system-wide)

❌ No direct data changes
✅ Pulled from: user_activity_logs, submissions, meta_tasks

🧭 11. Angel Task Explorer
URL: /angel

Content:

Highlighted Charitable or Open Public Good Bounties

Source of funds (e.g. "Fully funded by treasury")

Tags: Health, Education, Environment, Accessibility

✅ Mostly same structure as bounty explorer
❌ No direct data-changing actions unless submitting

🗳️ 12. Governance & Proposals Page 🔧 (Future)
URL: /governance

Content:

Active/Passed/Failed Proposals

Vote history

Proposal creator

Proposal content hash

Actionable:

Submit New Proposal 🔧

Stake $HALO for proposal support 🔧

Vote on Proposal (Quadratic/Linear) 🔧

✅ Pages That Change Data (Summary)
Page	Type of Data Changed
Bounty Detail Page	Bounty edits, fund updates, submission acceptance
Submit Work Page	New submission
Meta Task Dashboard	Review outcomes, stakes
User Profile	Personal info (self only)
Post Bounty Page	New bounty
Branch Bounty Page	New bounty with parent
Treasury Dashboard	Funding approvals, slashing
Governance Page	Proposals, votes (future)

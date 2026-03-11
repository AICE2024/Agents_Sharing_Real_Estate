this script automates the reassignment of agents in a Google Sheet, archives claimed ones, redistributes the rest fairly, and locks sensitive columns for data integrity. It’s essentially a task redistribution tool for a sales/support team:

# Description (In Details)
- Admin-only access: Only the administrator (defined by ADMIN_EMAIL) can run the reassignment.
- Archive claimed agents: Moves any agents marked as “claimed” into a separate sheet called Reassigned Agents, along with a timestamp.
- Redistribute remaining agents: Randomly shuffles unclaimed agents and reassigns them to team members, while respecting quotas (so assignments are balanced).
- Rewrite the table: Clears the old assignments in the AGENT_POOL sheet and writes back the updated agent list.
- Lock agent data: Protects columns A–C (agent info) after the first run to prevent accidental edits.
- Confirmation: Shows alerts to the admin about progress (e.g., “No agents found” or “Reassignment completed”).

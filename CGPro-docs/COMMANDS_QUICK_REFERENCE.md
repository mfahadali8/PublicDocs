# Commands Quick Reference

This document provides a quick reference for all public and admin commands for both the Discord and Telegram bots.

## Discord Commands

### Public Commands

| Command | Description | Access | Channel | Format / Example |
| :--- | :--- | :--- | :--- | :--- |
| `/help` | Show all public commands with examples. | Public | Any | `/help` |
| `/info` | Show bot capabilities and feature status. | Public | Any | `/info` |
| `/ref_link` | Get your unique referral link and code. | Public | Any | `/ref_link` |
| `/ref_register` | Register yourself using a referral code. | Public | Any | `/ref_register code:ABC123` |
| `/ref_stats` | View your personal referral statistics. | Public | Any | `/ref_stats` |
| `/ref_list` | List all the users you have referred. | Public | Any | `/ref_list limit:15` |
| `/filter_messages` | Filter messages in a channel by hashtags. | Public | Any | `/filter_messages hashtags:#event #project` |
| `/filter_user_messages` | Filter messages by a specific user. | Public | Any | `/filter_user_messages user:@username` |
| `/filter_user_advanced` | Advanced user message filtering with more options. | Public | Any | `/filter_user_advanced user:@username start_date:2025-01-01` |
| `/export_filtered` | Export filtered messages to a text file. | Public | Any | `/export_filtered hashtags:#export` |
| `/filter_channel` | Filter messages from a specific channel by hashtags. | Public | Any | `/filter_channel channel:#channel_name hashtags:#tag` |
| `/quick_filter` | Quickly filter messages from the last X hours. | Public | Any | `/quick_filter channel:#channel_name hours:12 hashtags:#urgent` |
| `/shift_list` | View all configured shift schedules. | Public | Any | `/shift_list` |

### Admin Commands

| Command | Description | Access | Channel | Format / Example |
| :--- | :--- | :--- | :--- | :--- |
| `/admin_help` | Show all admin commands (ephemeral response). | Admin | Any | `/admin_help` |
| `/audit_logs` | View audit logs with advanced filtering. | Admin | Any | `/audit_logs user:@user category:"Admin Actions"` |
| `/bot_invite` | Get the bot's OAuth2 invite link. | Admin | Any | `/bot_invite` |
| `/reload_shift_stats` | Reload, enable, or disable the shift stats cog. | Admin | Any | `/reload_shift_stats action:Reload` |
| `/update_shift_flags` | Retroactively update `DuringShift` flags for messages. | Admin | Any | `/update_shift_flags user_id:123456789` |
| `/x_tracker_run` | Start, stop, or check the status of the X Engagement Tracker. | Admin | Any | `/x_tracker_run action:Start` |
| `/ref_leaderboard` | View or export the referral leaderboard. | Admin | Any | `/ref_leaderboard limit:20 export:True` |
| `/ref_chain` | View the complete referral chain for a user. | Admin | Any | `/ref_chain user:@username` |
| `/ref_reassign` | Change the referrer for a specific user. | Admin | Any | `/ref_reassign referred_user:@user new_referrer:@new_ref` |
| `/ref_settings` | View the current referral system settings. | Admin | Any | `/ref_settings` |
| `/ref_set_verification` | Set the minimum messages required for a referral to be verified. | Admin | Any | `/ref_set_verification min_messages:5` |
| `/ref_update_verification` | Manually run the verification process for a user or all users. | Admin | Any | `/ref_update_verification user:@username` |
| `/ref_set_verified_role` | Set a role to be automatically assigned to verified referrals. | Admin | Any | `/ref_set_verified_role role:@VerifiedRole` |
| `/shift_add` | Add a shift schedule for a user. | Admin | Any | `/shift_add user:@user start:09:00 end:17:00` |
| `/shift_remove` | Remove a user's shift schedule. | Admin | Any | `/shift_remove user:@user` |
| `/stats_set_channel` | Set the channel where daily stats will be posted. | Admin | Any | `/stats_set_channel channel:#stats-channel` |
| `/stats_run_now` | Generate and post the shift statistics immediately. | Admin | Any | `/stats_run_now` |
| `/stats_backfill` | Backfill message data to calculate historical statistics. | Admin | Any | `/stats_backfill days:30` |

---

## Telegram Commands

### Public Commands

| Command | Description | Access | Channel | Format / Example |
| :--- | :--- | :--- | :--- | :--- |
| `/help` | Show all public commands with examples. | Public | Group & DM | `/help` |
| `/bot_info` | Show bot capabilities and feature status. | Public | Group & DM | `/bot_info` |
| `/start` | Start interacting with the bot, with referral support. | Public | DM | `/start` or `/start REF_CODE_CHATID_123` |
| `/ref_link` | Get your unique referral link for the current group. | Public | Group | `/ref_link` |
| `/ref_stats` | View your personal referral statistics for the group. | Public | Group | `/ref_stats` |
| `/ref_list` | List all the users you have referred in that group. | Public | Group | `/ref_list 15` |
| `/filter_messages` | Filter messages by hashtags (requires message storage). | Public | Group | `/filter_messages #event #project` |
| `/filter_recent` | Filter recent messages (requires message storage). | Public | Group | `/filter_recent 24` |
| `/filter_user` | Filter messages by a user (requires message storage). | Public | Group | `/filter_user @username` |
| `/export_filtered` | Export filtered messages (requires message storage). | Public | Group | `/export_filtered #project 2025-01-01 2025-01-31` |
| `/shift_list` | View all configured shift schedules. | Public | Group | `/shift_list` |

### Admin Commands

**Note:** Most Telegram admin commands are designed to be run in a Direct Message (DM) with the bot for security. The bot will then ask which group to apply the command to.

| Command | Description | Access | Channel | Format / Example |
| :--- | :--- | :--- | :--- | :---_ |
| `/dm_help` | Shows all admin commands with examples. | Admin | DM | `/dm_help` |
| `/audit_logs` | View audit logs with filtering. | Admin | Group | `/audit_logs <user_id> <category> <severity> <days> <limit>` |
| `/reload_stats` | Reload, enable, or disable the shift stats module. | Admin | Group | `/reload_stats reload` |
| `/status` | Show a brief status report of the bot. | Admin | Group & DM | `/status` |
| `/update_shift_flags` | Redirects to the secure DM version of the command. | Admin | Group | `/update_shift_flags` |
| `/dm_ref_leaderboard` | View the referral leaderboard for a chosen group. | Admin | DM | `/dm_ref_leaderboard 20` |
| `/dm_ref_chain` | View the referral chain for a user in a chosen group. | Admin | DM | `/dm_ref_chain 123456789` |
| `/dm_ref_reassign` | Change the referrer for a user in a chosen group. | Admin | DM | `/dm_ref_reassign <referred_id> <new_referrer_id>` |
| `/dm_ref_settings` | View referral settings for a chosen group. | Admin | DM | `/dm_ref_settings` |
| `/dm_set_verification` | Set verification message count for a chosen group. | Admin | DM | `/dm_set_verification 5` |
| `/dm_ref_update_verification` | Manually update verifications for a chosen group. | Admin | DM | `/dm_ref_update_verification` or `/dm_ref_update_verification <user_id>` |
| `/dm_shift_add` | Add a shift for a user in a chosen group. | Admin | DM | `/dm_shift_add` (starts interactive setup) |
| `/dm_shift_remove` | Remove a user's shift in a chosen group. | Admin | DM | `/dm_shift_remove` (starts interactive setup) |
| `/dm_stats_now` | Generate stats for a chosen group immediately. | Admin | DM | `/dm_stats_now` |
| `/dm_stats_backfill` | Backfill stats for a chosen group. | Admin | DM | `/dm_stats_backfill 30` |
| `/dm_cleanup_messages` | Clean up bot messages in a chosen group. | Admin | DM | `/dm_cleanup_messages 50` |
| `/dm_security_report` | Generate a security report for a chosen group. | Admin | DM | `/dm_security_report` |
| `/dm_update_shift_flags` | Retroactively update `DuringShift` flags in a chosen group. | Admin | DM | `/dm_update_shift_flags` |

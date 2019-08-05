# To-Do

## Partial automation of account creation
- Hourly/daily cron job watching the sign up log directory
  - Sends new signups to mail
- Script that upon manual review of a signup application, will do the following
  - Create the unix user
    - This automatically copies setup files from `etc/skel`
  - Adds their public key to `id_rsa.pub` and `authorized_keys`
  - Create public_html directory
  - Delete the signup log entry _after_ the approval is successful  
 - Example script usage:
   - `./approve_user 9996d835-996e-4166-9c6d-a66d71a95aa7`
     - Parse the signup file for information
     - Delete the log after the creation process
  
## Misc
- The default shell for new users should be bash, not ksh
- Correct file permissions on user home directories and dirs like /etc 
  (users should only see their own home dir, not the home dirs of others, and not system configs)

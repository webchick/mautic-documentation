---
title: 'Mautic 3 upgrade errors'
twitterenable: true
twittercardoptions: summary
articleenabled: false
orgaenabled: false
orga:
    ratingValue: 2.5
orgaratingenabled: false
personenabled: false
facebookenable: true
---

Did you get an error while running the Mautic 3 upgrade? We're here to help. Please look for the error code you got on this page for further instructions.

If you need any further help, please post into our MAUTIC 3 FORUM CATEGORY (TODO).

## Error codes

### ERR_DATABASE_BACKUP_FAILED
During the upgrade process, the script makes an attempt to back up your database. We make use of the command `mysqldump` in order to execute the backup process. 

If your migration fails in this stage, it is likely that an error was experienced when running the command. The error code displayed should give you some more information.  Your Mautic 2.x instance is intact.

To move forward from this stage, you will need to fix the problem that has been reported and restart the upgrade script. 

### ERR_MAUTIC_2_MIGRATIONS_FAILED
During the migration process we checked to ensure that there are no database migrations is waiting to be applied from previous Mautic upgrades.

This error indicates that there was a problem in getting the available migrations, or an error in applying them. 

#### Unable to detect database migrations

If you see an error message that says we were unable to reliably detect the amount of available database migration, this means that the upgrade script was unable to access the appropriate files, or that the process was interrupted for some reason.

To move forward from this stage, refresh the page.

#### Database migrations have failed

If you see an error message that says "Oh no! While preparing the upgrade, the so-called 'database migrations' for Mautic 2 have failed." this means that the upgrade script was unable to apply the migrations that it found.  The output message will give you more details about where the problem lies.

To move forward from this stage, review the error message and address any problems that it raises.

### ERR_DOWNLOAD_UPGRADE_PACKAGE_FAILED
If you see an error which tells you that downloading the Mautic 3 upgrade package has failed, this means that we were unable to contact the server in order to download the package we need to run the upgrade.

The error message should give you more information about this problem. 

### ERR_EXTRACT_UPGRADE_PACKAGE_FAILED
If you see an arrow which tells you that there was a problem extracting more tick three files this means that we were unable to extract the archive on your server. 

The error message should give you more information about this problem.

### ERR_MOVE_MAUTIC_2_AND_3_FILES
During this stage, we move the current Mautic 2 files into a temporary directory called "mautic-2-backup-files", and then move the Mautic 3 files from "mautic-3-temp-files" to the root directory.

If an error is encountered in this stage, it could be that there are problems with moving directories.  Although we do some basic tests before starting the upgrade to ensure that we can create and delete files and folders, it might be that errors have been encountered during the upgrade.

The error message should give you more information about this problem.

### ERR_UPDATE_LOCAL_CONFIG
When updating config/local.php with new M3 values fails

### ERR_MAUTIC_3_MIGRATIONS_FAILED
When running M3 database migrations fails

### ERR_RESTORE_USER_DATA_FAILED
When restoring user data (themes/plugins/media) from M2 fails

### ERR_BUILD_M3_CACHE
When building M3 cache fails

### ERR_CLEANUP_FILES
When cleaning up upgrade files fails

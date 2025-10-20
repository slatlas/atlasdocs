# Mobile App Setup and Sync

## Overview

Mobile app setup configures the Atlas mobile application on field personnel devices for offline-capable field operations. This workflow is used by field personnel and IT support to install the app, configure settings, sync data to the device, handle offline operation, and troubleshoot sync issues. Proper mobile setup ensures field staff can work effectively even in areas with poor cellular coverage.

## Prerequisites

**Required Permission:** Mobile app access

**Required Setup:**
* User account created in Atlas system
* Personnel record linked to user
* Mobile device: iOS (iPhone/iPad) or Android
* Adequate storage space on device
* Email address for account setup

## Workflow Diagram

```
Download App → Install → Login → Configure Settings → Initial Sync → Test Offline Mode
       ↓
Daily Operation: Sync → Work Offline → Sync → Troubleshoot as Needed
```

## Step-by-Step Procedure

### Installing the Mobile App

1. **Download Atlas Mobile App**
   * **iOS:** Open App Store, search for "Atlas" or your company's Atlas app
   * **Android:** Open Google Play Store, search for "Atlas"
   * Verify it's the correct app (check publisher name)
   * Tap "Install" or "Get"

2. **Launch the App**
   * Tap the Atlas app icon to open
   * App displays login screen on first launch

3. **Enter Login Information**
   * **Server URL:** Your Atlas server address (provided by IT)
   * **Username:** Your Atlas username
   * **Password:** Your Atlas password
   * Tap "Login"

4. **Grant Permissions** (first time)
   * **Location Services:** Required for GPS tracking (tap "Allow")
   * **Camera:** Required for photos (tap "Allow")
   * **Notifications:** For alerts and updates (tap "Allow")
   * **Storage:** For offline data (tap "Allow")

### Initial Configuration

5. **Configure User Settings**
   * Tap "Settings" or "Menu" → "Settings"
   * **Display Name:** Verify your name is correct
   * **Default Warehouse:** Set your service vehicle/truck as warehouse
   * **Time Zone:** Verify correct time zone
   * **Units:** Imperial or Metric

6. **Configure Sync Settings**
   * **Auto-Sync Frequency:** How often to auto-sync (every hour, manual only, etc.)
   * **Sync on Wi-Fi Only:** Yes/No - limits data usage if on cellular plan
   * **Background Sync:** Allow sync when app not active
   * **Sync Scope:** How many days of data to download (7, 14, 30 days)

7. **Configure GPS Settings**
   * **GPS Accuracy:** High accuracy for precise location
   * **Track Location:** Enable for route tracking
   * **Update Frequency:** How often to record location
   * Balance accuracy vs. battery life

8. **Configure Camera Settings**
   * **Photo Quality:** High, Medium, or Low
   * **Auto-Upload Photos:** Upload photos immediately or on sync
   * **Save to Device:** Keep copy on device or delete after sync

### Performing Initial Sync

9. **Start Initial Sync**
   * Ensure connected to Wi-Fi (first sync downloads a lot of data)
   * Tap "Sync" button
   * App downloads:
     * Your assigned treatments and delivery orders
     * Customer and location information
     * Product catalog
     * Route information
     * Recent treatment history

10. **Monitor Sync Progress**
    * Progress bar shows sync status
    * Initial sync may take 5-15 minutes depending on data volume
    * **Don't close app** during initial sync
    * If sync fails, try again or contact IT support

11. **Verify Data Downloaded**
    * Check that treatments/orders appear
    * Verify locations are visible
    * Confirm products are in product list
    * Test searching for customers

### Testing Offline Operation

12. **Enable Airplane Mode** (for testing)
    * Turn on airplane mode on device
    * Verifies app works without connection

13. **Test Core Functions**
    * Open treatment records
    * Navigate to locations (GPS still works offline)
    * Start and complete a test treatment
    * Take photos
    * Add notes

14. **Disable Airplane Mode**
    * Turn off airplane mode
    * Tap "Sync" to upload test data
    * Verify test treatment synced to server
    * Delete test treatment if needed

### Daily Mobile Operations

15. **Morning Sync**
    * Before leaving the yard, connect to Wi-Fi
    * Open Atlas app and tap "Sync"
    * Download today's assignments
    * Verify all expected orders are present
    * Check for any special instructions or updates

16. **Work Throughout Day**
    * App works offline in the field
    * GPS navigation works without cellular
    * Complete treatments and record data
    * Take photos and notes
    * All data stored locally on device

17. **Evening Sync**
    * Return to area with Wi-Fi or good cellular
    * Open app and tap "Sync"
    * Upload completed treatments
    * Upload photos
    * Send any messages or notes
    * Verify "Last Synced" time updated

18. **Resolve Sync Conflicts** (if any)
    * If changes made both on mobile and in office system
    * App prompts which version to keep
    * Usually choose most recent or mobile version
    * Contact dispatcher if unsure

## Best Practices

### For Field Personnel
* **Sync twice daily** - Morning to get assignments, evening to upload completions
* **Charge overnight** - GPS and app use significant battery
* **Use Wi-Fi when available** - Faster sync, saves cellular data
* **Don't delete app data** - Can lose unsynced work
* **Keep app updated** - Install updates when prompted

### For IT Support
* **Test before deployment** - Verify app works on device before giving to field staff
* **Document server URL** - Have easy reference for setup
* **Backup strategy** - Regular syncs prevent data loss
* **Support plan** - Have process for resetting passwords, troubleshooting issues

### Industry-Specific Tips
* **Remote areas:** Sync may only be possible when returning to town
* **Data plans:** Consider unlimited data plans for field personnel
* **Rugged devices:** Consider ruggedized phones/tablets for harsh field conditions
* **Battery backup:** Keep vehicle chargers and portable batteries
* **Multiple users:** If sharing device, ensure proper user switching

## Troubleshooting

**Issue:** Cannot login - invalid credentials
* **Solution:** Verify username and password correct (case-sensitive). Check that server URL is correct. Ensure account is active in system. Try resetting password through web interface.

**Issue:** Sync failing - connection error
* **Solution:** Check internet connection (Wi-Fi or cellular). Verify server URL is correct and reachable. Try switching between Wi-Fi and cellular. Restart app and try again. May need to contact IT if server issue.

**Issue:** GPS not working or inaccurate
* **Solution:** Verify location services enabled for app. Check device GPS settings. Move to open area away from buildings. Restart device to reset GPS. May need to recalibrate GPS.

**Issue:** App running slowly or freezing
* **Solution:** Close other apps to free memory. Restart the app. Restart device. Check available storage space. May need to reduce sync scope or clear old data.

**Issue:** Photos not uploading
* **Solution:** Check photo upload settings. Verify storage space available. Try uploading individual photos manually. May need to compress photos if files too large. Ensure sync completed fully.

**Issue:** Lost unsynced data due to app crash or device issue
* **Solution:** Prevention is key - sync frequently. If data lost, may need to re-enter from memory or skip. Contact IT support - may be able to recover from device backups in some cases.

**Where to Get Help:**
* See [Mobile App documentation](../../Mobile/Intro.md)
* See [Mobile Settings](../../Mobile/Settings.md)
* See [Mobile Sync](../../Mobile/Sync.md)
* Contact IT support for technical issues
* Contact dispatcher for assignment questions
* See device manufacturer for hardware issues

## Related Workflows

**Upstream Processes:**
* User and personnel setup in system
* Mobile device procurement and setup

**Downstream Processes:**
* [Field Treatment Execution](FieldTreatments.md) - Using mobile for treatments
* [Mobile Treatment Mode](MobileTreating.md) - Treatment-specific mobile operations
* [Lab Order Creation](LabOrders.md) - Collecting samples on mobile

**Related Documentation:**
* [Mobile Overview](../../Mobile/Intro.md)
* [Mobile Dashboard](../../Mobile/Dashboard.md)
* [Mobile Login](../../Mobile/Login.md)


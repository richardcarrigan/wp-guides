# WordPress Troubleshooting Instructions

## Issue # 1: Error validating access token for Facebook feed

### Error description
<img src='assets/img/error_accessing_token_screenshot.jpeg' alt='Error accessing token. Session has expired on Wednesday, 09-Apr-25 16:00:00 PDT. The current time is Thursday, 10-Apr-25 14:24:29 PDT.' />

### Resolution steps
1. Log into [developers.facebook.com](https://developers.facebook.com) using the Facebook credentials used when initially creating the access token, which should also be the Facebook user that the website is connected to.
2. Select 'My Apps'.
3. Select 'Tools > Graph API Explorer'.

<img src='assets/img/fb_developers_my_apps_screenshot.png' alt='Screenshot of My Apps page, showing Tools menu containing Graph API Explorer menu item' />

4. Next to the existing access token, select the info icon (blue circle with 'i') and then select 'Open in Access Token Tool'.

<img src='assets/img/fb_developers_graph_api_explorer_screenshot.jpeg' alt='Screenshot of Graph API Explorer page, showing Open in Access Token Tool option' />

5. At the bottom of the page, select the 'Extend Access Token' option.

<img src='assets/img/fb_developers_access_token_debugger_screenshot.jpeg' alt='Screenshot of Access Token Debugger page, showing Extend Access Token option' />

6. Enter your Facebook password again when prompted.

7. Copy the access token code at the bottom.

<img src='assets/img/fb_developers_extended_access_token.jpeg' alt='Screenshot of Access Token Debugger page, showing new access token with extended access' />

8. Armed with your new access token, log into the WordPress admin dashboard, located at '[your domain]/wp-admin'.

9. In the admin dashboard, select 'API Settings' from the 'Element Pack' menu.

<img src='assets/img/wp_admin_element_pack_api_settings_screenshot.png' alt='Screenshot of WordPress admin dashboard with Element Pack > API Settings menu item' />

10. Under 'Facebook Social Access', replace the existing 'Facebook Access Token' with the one you copied in step 7, then select 'Save Settings'.

<img src='assets/img/wp_admin_fb_api_settings_screenshot.jpeg' alt='Screenshot of Element Pack API Settings page, including Facebook Access Token field' />

11. At this point, you've resolved the issue, but depending on the caching settings for you site, you may need to clear those caches or wait for them to refresh, which could take over 24 hours. For WP Engine, you can select the 'Quick clear all caches' option from the 'WP Engine Quick Links' within the WordPress admin dashboard.

<img src='assets/img/wp_admin_wp_engine_clear_caches_screenshot.png' alt='Screenshot of WordPress admin dashboard, including WP Engine option to clear all caches' />

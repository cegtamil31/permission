# Add new host

1. navigate:cd /usr/local/nagios/etc/objects.
2. add hostname.cfg,then copy the template from localhost.cfg.
3. change the ipaddress of the host we want to monitor and host-name etc.
3. then save the file and restart nagios.

# Add new service

1. to add the new service add the script file or plugin file in usr/local/nagios/libexec.
2. then add the command in commands.cfg with command name and command path(copy the template from above adn edit the name and path)
3. then naviagate to localhost.cfg to add the service on local machine or hostname.cfg to add the service in other host.
4. then add the service ,by copying the template above and change the check_command pointing the plugin or service script.

# Email configuration

1. prerequisites:smtp,mailutils already in working condition.
2. naviaget:cd /usr/local/nagios/etc/objects/contacts.cfg
3. configure your mail address.
4. set interval fro sending email in templates.cfg.
5. email is sent accordingly.

# Slack configuration
1. download plugin from https://exchange.nagios.org/directory/Plugins/Notifications/Notification-for-Slack/details
2. then add them in libexec
3. edit the slack_url variable by adding incoming webhook.
3. then define the command.
4. then add the following in contacts.cfg

    define contact {
       contact_name                     slack
       alias                            Slack
       service_notification_period      24x7
       host_notification_period         24x7
       service_notification_options     w,u,c,r
       host_notification_options        d,r
       service_notification_commands    notify-service-by-slack
       host_notification_commands       notify-host-by-slack
       }
       
define contactgroup{
        contactgroup_name       admins
        alias                   Nagios Administrators
        members                 root,slack
        }

define contactgroup{
        contactgroup_name       admins-page
        alias                   Nagios Administrators
        members                 root,slack

5. then restart nagios .
6. now the notification will be sent successfully to your webhook url

**Deprecated and unused: use [ANXS.monit](https://github.com/ANXS/monit) instead.**

# monit

Ansible role which sets up [monit][] watchdog with supplied files
containing [check statements][monit-checks] for your service.

## Usage

Apply `MailOnline.monit` role to your hosts:

    - hosts: appservers
      roles:
        - role: MailOnline.monit
          monit_check_files:
            - 'files/monit/my-service.j2'
          monit_alert_emails:
            - somebody@mailonline.co.uk
            - someone.else@mailonline.co.uk

## Variables

All variables are required.

- `monit_alert_emails`
- `monit_check_files`
- `monit_smtp_host`

[monit]: https://mmonit.com/monit/
[monit-checks]: https://mmonit.com/monit/documentation/monit.html#CHECK-PROCESS-unique-name-PIDFILE-path-MATCHING-regex

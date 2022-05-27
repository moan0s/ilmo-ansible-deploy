# ILMO - Intelligent Library Management Online

ILMO is a webapp to manage a library, especially books, other material, users, emails and opening hours.
This ansible playbook should help you set up an instance.

# Troubleshooting

```
fatal: [hyteck]: FAILED! => changed=false 
  cmd: /usr/bin/git ls-remote https://github.com/moan0s/ILMO2.git -h refs/heads/main
```
can be solved by 
```
# sudo su ilmo-staging
$ git clone https://github.com/moan0s/ILMO2
```

# Using the software

This software is Open-Source so you are invited to use it for free. But perhaps you need some help to adjust the software to your library or want some new features? Feel free to contact me!

# Settings

| Variable Name                   | Function                                                                        | Default value                            | Comment          |
|---------------------------------|---------------------------------------------------------------------------------|------------------------------------------|------------------|
| `ilmo_domain`                   | The domain ilmo will use                                                        | None                                     | Without https:// |
| `ilmo_instance_name`            | A name for this ilmo instance, will be used eg. in mails                        | ILMO                                     |                  |
| `ilmo_instance_name_normalized` | A name that is used to identify this instance, useful for multi instance setups | ilmo                                     |                  |
| `ilmo_user`                     | User created for running the ilmo service                                       | "ilmo-{{ilmo_instance_name_normalized}}" |                  |
| `ilmo_postgres_db`              | ilmo_staging                                                                    | ilmo                                     |                  |
| `ilmo_postgres_user`            | ilmo                                                                            |                                          |                  |
| `ilmo_postgres_password`        | Secure password for the database user (only MySQL and PostgresQL                |                                          |                  |

# Bugs and Security

You found an error in the code, want to suggest an improvement etc..? Just put it on the Issue Tracker, I will read it! For security issues please contact me directly, address see below.

# Contact

You have any questions or problems concerning the software? Contact me! E-Mail: julian-samuel@gebuehr.net

# License

This code and examples are licensed under the GNU AFFERO GENERAL PUBLIC LICENSE.

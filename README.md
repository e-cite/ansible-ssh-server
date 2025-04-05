# Ansible Rolle "SSH-Server"

Installiert und konfiguriert einen SSH-Server.

## Anforderungen

Keine.

## Variablen

- `ssh_server__sshdconf`: (*Erforderlich*)

  Dict mit allen Parametern der `/etc/ssh/sshd_config`.
  Default-Werte aus Debian Bookworm DEB-Package wie im Beispiel.

  ~~~yaml
  # Beispiel:
  ssh_server__sshdconf:
    Include: /etc/ssh/sshd_config.d/*.conf
    KbdInteractiveAuthentication: false
    UsePAM: true
    X11Forwarding: true
    PrintMotd: false
    AcceptEnv: LANG LC_*
    Subsystem: sftp /usr/lib/openssh/sftp-server
  ~~~

## Abhängigkeiten

Keine.

## Beispiel

    - hosts: servers
      roles:
        - ssh-server

## Client Konfiguration

Keine.

## Lizenz

MIT

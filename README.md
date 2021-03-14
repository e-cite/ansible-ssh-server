# Ansible Rolle "SSH-Server"

Installiert und konfiguriert einen SSH-Server.

## Anforderungen

Keine.

## Variablen

- `ssh_server__private_ip_range`: (*Erforderlich*)

  Privater IP-Adressbereich, aus welchem keine 2FA bei SSH erforderlich ist.
  ~~~yaml
  # Beispiel:
  ssh_server__private_ip_range: "192.168.1.0/24"
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

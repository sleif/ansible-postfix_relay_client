# sleif.postfix_relay_client

This role configures postfix to act as a relay client.

## Requirements

- postfix installed

## Role Variables

- postfix_relay_client_relayhost
- postfix_relay_client_relayhost_port
- postfix_relay_client_relayhost_user
- postfix_relay_client_relayhost_myorigin

## Dependencies

- NA

## Example Playbook

    - hosts: "server"
      user: root
      vars:
        postfix_relay_client_relayhost: 'mailhost.example.com'
        postfix_relay_client_relayhost_port: '587'
        postfix_relay_client_relayhost_user: 'authorized_user@example.com'
        postfix_relay_client_relayhost_myorigin: 'example.com'
      roles:
        - { role: sleif.postfix_relay_client, tags: "postfix_relay_client" }

## License

MIT

## Author Information

Created in 2021 by Sebastian Berthold

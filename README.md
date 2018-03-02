# bk-dot-com
Document (and script where possible) the procedure that was used to set up `https://brendonkwan.com` and `https://www.brendonkwan.com`

## Procedure

1. Use the WordPress administration console to create a new admin user and delete the default admin user.
1. Use the WordPress administration console to add custom CSS so that the BitNami logo disappears from the mobile site.
1. Use [these](https://docs.bitnami.com/aws/how-to/generate-install-lets-encrypt-ssl/) instructions from BitNami to obtain and install a "Let's Encrypt" SSL certificate that protects `brendonkwan.com` and `www.brendonkwan.com`.
1. Clone this repository.
1. Change directory to your cloned repository.
1. Run the following commands:

        $ vim hosts.txt
        (List all your EC2 hosts, and save the file)

        $ ansible-playbook --inventory=hosts.txt --user=<USER> --private-key=<KEY_FILE> playbooks/setup-bk-dot-com.yml

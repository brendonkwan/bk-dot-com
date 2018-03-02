# bk-dot-com
Scripts that were used to set up brendonkwan.com

## Usage

1. Use [these](https://docs.bitnami.com/aws/how-to/generate-install-lets-encrypt-ssl/) instructions from BitNami to obtain and install a "Let's Encrypt" SSL certificate that protects `brendonkwan.com` and `www.brendonkwan.com`.
1. Clone this repository.
1. Change directory to your cloned repository.
1. Run the following commands:

    $ vim hosts.txt
    (List all your EC2 hosts, and save the file)

    $ ansible-playbook --inventory=hosts.txt --user=<USER> --private-key=<KEY_FILE> playbooks/setup-bk-dot-com.yml

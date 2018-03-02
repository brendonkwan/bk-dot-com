# bk-dot-com
Scripts that were used to set up brendonkwan.com

## Usage

    $ vim hosts.txt
    (List all your hosts and save the file)

    $ ansible-playbook --inventory=hosts.txt --user=<USER> --private-key=<KEY_FILE> playbooks/setup-bk-dot-com.yml

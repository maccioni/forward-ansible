Forward Networks provides REST APIs to enable integrations with external applications.

For example, the Forward APIs can be used to build an integration with Red Hat Ansible using the uri Core Module.

This repo provides some Ansible Playbooks examples:
* forward-uri.properties.sample: Sample properties file (To be copied and modified)
* forward_networks_uri.yml:      Playbook to get all the Forward Networks
* forward_snapshots_uri.yml:     Playbook to get all the Snapshots for the given Network
* forward_checks_uri.yml:        Playbook to get all the Checks for the given Snapshot

## Set up local properties file

Set up properties file from the sample

    cp forward-uri.properties.sample forward-uri.properties

## Run the Ansible Playbooks

```
$ ansible-playbook forward_networks_uri.yml -vvv
```

Sample output:

```
PLAYBOOK: forward_networks_uri.yml *********************************************

PLAY [Forward Networks Networks] ***********************************************

TASK [Gathering Facts] *********************************************************
ok: [localhost]

TASK [get all Networks from the Forward Networks platform] *********************

ok: [localhost] => {

<snipet>

    "json": [
        {
            "creatorId": "2941",
            "id": "35619",
            "name": "Fabrizio-HQ",
            "orgId": "1126"
        },
        {
            "creatorId": "2941",
            "id": "37779",
            "name": "fabrizio-ansible",
            "orgId": "1126"
        },
        {
            "creatorId": "2941",
            "id": "36331",
            "name": "AWS-collector",
            "orgId": "1126"
        },
        {
            "creatorId": "2941",
            "id": "31691",
            "name": "Fabrizio",
            "orgId": "1126"
        },
        {
            "creatorId": "2431",
            "id": "35743",
            "name": "test",
            "orgId": "1126"
        },
        {
            "creatorId": null,
            "id": "15509",
            "name": "Network 2",
            "orgId": "1126"
        },
        {
            "creatorId": "2431",
            "id": "31182",
            "name": "windowsTest",
            "orgId": "1126"
        },
        {
            "creatorId": "2431",
            "id": "31183",
            "name": "macTest",
            "orgId": "1126"
        },
        {
            "creatorId": "2431",
            "id": "36293",
            "name": "deep2",
            "orgId": "1126"
        },
        {
            "creatorId": "2431",
            "id": "31181",
            "name": "linuxTest",
            "orgId": "1126"
        },
        {
            "creatorId": "2431",
            "id": "36298",
            "name": "deepYadhuTest",
            "orgId": "1126"
        },
        {
            "creatorId": "2431",
            "id": "12606",
            "name": "Example Network",
            "orgId": "1126"
        },
        {
            "creatorId": "2736",
            "id": "23943",
            "name": "bftm-test",
            "orgId": "1126"
        },
        {
            "creatorId": "2431",
            "id": "27913",
            "name": "deep",
            "orgId": "1126"
        }
    ],

<snipet>

}

PLAY RECAP ************************************************************************************************************************************************************************************************
localhost                  : ok=2    changed=0    unreachable=0    failed=0

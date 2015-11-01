# Ansible OVH

This is a small ansible wrapper around the ovh api.
It is very lightweight but generic and should give you the possibility to use the full api of ovh and its fellow brands like kimsufi, soyoustart and runabove.
Requires pyhton ovh client. Install with:

   pip install ovh


## Example Usage

    - name:  get servers
      ovh:
        method: get
        endpoint: kimsufi-eu
        application_key: < application_key >
        application_secret: < application secret >
        consumer_key: < consumer key >
        uri: /dedicated/server

    - name:  set rescue boot
      ovh:
        method: put
        endpoint: kimsufi-eu
        application_key: < application_key >
        application_secret: < application secret >
        consumer_key: < consumer key >
        uri: /dedicated/server/< server name >
        args:
          bootId: 22

# ops-mvs-lab
This repo is for ops mvs lab

curl -X 'GET' 'https://10.252.118.132:50080/api/v1/status' -H 'accept: application/json' -H 'X-Requested-With: XMLHttpRequest'


Changelog:
  - 3/3/2025:
    - start adding npm and linux packages for testing env
    - tried setting up z/OSMF connection 
    - zowe secure cred store on linux is different (https://docs.zowe.org/stable/user-guide/systemrequirements-cli/)

  -3/4/2025:
    - updated config with host
    - got OPSREST started and pinged via VS Code
  
  -3/5/2025:
    - z/OSMF works
    - team config updated
    - OPS VSCE commands work on ZE ds members
    - z/OSMF on ZDT is super slow (hardly usable), comment on ticket to try to resolve
    - some datasets to use:
      - CA1.OPSMVS.MSG.RULES | CA1.OPSMVS.*.RULES
      - PROD001.OPS.REXX
    
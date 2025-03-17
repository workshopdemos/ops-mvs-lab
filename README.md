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
    - must uncheck the workspace credential checking or requests to go out  
       - test with `zowe zosmf check status` command
    - can create opsrexx data sets and run programs locally
      - test with `PROD001.OPS.REXX(HELLO)`
    

Settings for secure cred override and file associations must be applied from home/developer/strong-ide/data/Machine/settings.json

# OPS/MVS VS Code Extension
- Open Zowe Explorer
  - search for dataset `xxx.userid`
- Open Programs Dataset
  - open member named `USERID`
  - write program with WTO call from to put out message
  - save program

- Open Rules Dataset
  - click on your ruleset, click create a new member, name it `userid`
  - Once your new rule is saved to the DS, start writing code ( )MSG... tab)
  - write message rule with custom PROC
  - save and enable rule using VSCE

- Switch back to program
  - run the VSCE execute program command

- Search OPSLOG with VSCE Command
  - see if your program and rule wrote to the OPSLOG
# ops-mvs-lab

## OPS/MVS VS Code Extension
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
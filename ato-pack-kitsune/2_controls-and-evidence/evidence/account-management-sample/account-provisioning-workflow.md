# Account Provisioning Workflow (Fictional)

> Purpose: demonstrate a clean, reviewable account lifecycle process for AC-2.

## Workflow (request → approval → provision → validate → review)
1) **Access request submitted** (ticket/email)  
   - includes need-to-know justification, requested role(s), and system scope  
2) **Prerequisites verified** (as applicable)  
   - training/briefing completed  
   - sponsor/manager endorsement captured (if required)  
3) **Approval** by System Owner  
   - privileged/admin roles require explicit approval  
4) **Provisioning** by Account Manager / LAN Admin  
   - create named user account in IdP/directory service  
   - assign role/group membership (least privilege)  
   - ensure admin accounts are separate from daily-use accounts  
5) **ISSO validation**  
   - verify approval exists  
   - verify role assignments match request  
   - verify provisioning evidence is stored and traceable  
6) **Periodic review** performed on cadence  
   - annual full account inventory review (minimum)  
   - quarterly privileged/admin review (recommended)  
7) **Disable/Remove** triggers  
   - termination/transfer, role change, policy violation, access no longer needed  
   - inactivity handling: **example ODV** disable after 35 days inactivity (if documented)

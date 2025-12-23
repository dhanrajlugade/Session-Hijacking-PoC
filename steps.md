REPRODUCTION STEPS: SESSION HIJACKING
TARGET: www.efforti.com

PREREQUISITES:
- Two valid accounts (Attacker and Victim).
- A proxy tool (e.g., Burp Suite) or Browser Developer Tools.

STEP 1: OBTAIN VICTIM SESSION
1. Log in to www.efforti.com using the Victim account on Browser A.
2. Open Developer Tools (F12) -> Application -> Cookies.
3. Copy the value of the 'SessionID' (or equivalent auth cookie).
4. (In a real attack scenario, this would be obtained via XSS or sniffing).

STEP 2: PREPARE ATTACKER SESSION
1. Log in to www.efforti.com using the Attacker account on Browser B.
2. Ensure you are on a dashboard or private profile page.

STEP 3: EXECUTE THE SWAP
1. In Browser B (Attacker), open Developer Tools.
2. Locate the 'SessionID' cookie.
3. Replace the Attacker's Session ID value with the Victim's Session ID (copied in Step 1).
4. Save the cookie change.

STEP 4: VERIFY TAKEOVER
1. Refresh the page on Browser B.
2. Observe that the application now serves the Victim's profile data/dashboard.
3. Attempt to access sensitive data (e.g., settings, messages). 
   - RESULT: Access is granted as the Victim.

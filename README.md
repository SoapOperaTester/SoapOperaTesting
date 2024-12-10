**Dataset:** https://drive.google.com/drive/folders/11GY5JZ4F_h40qsO_PdEAnNisnI-RtSd0?usp=sharing
1. Soap opera tests used for the formative study and automated soap opera testing.
2. Bug reports for Firefox used to construct the scenario knowledge graph.
3. Issues and pull requests for WordPress used to construct the scenario knowledge graph.
4. Issues and pull requests for AntennaPod used to construct the scenario knowledge graph.

**Code:**
1. Use scripts/0_0 to 0_3 to crawl bug reports from Mozilla Bugzilla.
2. Use scripts/1_1 to 1_3 to crawl issues and pull requests from GitHub.
3. Use scripts/2_1 to 2_8 to construct the scenario knowledge graph.
4. Set up a virtual Android device or connect a physical Android device to your computer.
5. Ensure the application under test is installed on the Android device.
6. Run scripts/app.py to execute the multi-agent system for automated soap opera testing.

### **Approach Overview of Automated Soap Opera Testing**
![Overview](example_1/framework.png)

### **Example 1 by Automated Soap Opera Testing**

#### **Soap Opera Test**

**STEP 0**: Close a tab  
**STEP 1**: Open recently closed tabs  
**STEP 2**: Select a tab to reopen  



**Round 1**
![Round 1](example_1/round1.png)

**Round 2**
![Round 2](example_1/round2.png)
The Detector identifies a bug based on the GUI status and oracle knowledge from SKG.

**Round 3**
![Round 3](example_1/round3.png)
The Planner generates an actionable plan to use the 'UNDO' feature, allowing for easy reopening of the closed tab based on the current GUI status.

**Round 4**
![Round 4](example_1/round4.png)
The Planner generates an actionable plan to open the 'Recently Closed Tabs' page by leveraging the current GUI status and step knowledge from the SKG.

**Round 5**
![Round 5](example_1/round5.png)

**Round 6**
![Round 6](example_1/round6.png)

**Round 7-11**
![Round 7-11](example_1/round7-11.png)

- The Planner generates an actionable plan to reopen the closed tab by clicking the Three-dot menu.
- However, the Player incorrectly locates and taps the 'Share' icon instead. 
- Recognizing the erroneous UI operation, the Planner adjusts the plan to click the 'X' button to cancel the action. 
- This reveals a bug (Figure 3): the 'Back' icon turns black, and the title reverts to 'Recently Closed Tabs' while still displaying the selected websites after canceling the share action on the 'Recently Closed Tabs' page.
- The Planner resumes the intended steps after correcting the erroneous operation and continues executing the actionable plan until the soap opera test is successfully completed. 


**Bugs Identified in: Firefox Formative Study**

| No. | Bug ID |
|----------|----------|
| 1 | https://bugzilla.mozilla.org/show_bug.cgi?id=1912207 |
| 2 | https://bugzilla.mozilla.org/show_bug.cgi?id=1912199 |
| 3 | https://bugzilla.mozilla.org/show_bug.cgi?id=1912628 | 
| 4 | https://bugzilla.mozilla.org/show_bug.cgi?id=1912637 | 
| 5 | https://bugzilla.mozilla.org/show_bug.cgi?id=1912638 | 
| 6 | https://bugzilla.mozilla.org/show_bug.cgi?id=1912697 | 
| 7 | https://bugzilla.mozilla.org/show_bug.cgi?id=1912702 | 
| 8 | https://bugzilla.mozilla.org/show_bug.cgi?id=1912917 | 
| 9 | https://bugzilla.mozilla.org/show_bug.cgi?id=1912753 | 
| 10 | https://bugzilla.mozilla.org/show_bug.cgi?id=1912860 | 
| 11 | https://bugzilla.mozilla.org/show_bug.cgi?id=1912871 | 
| 12 | https://bugzilla.mozilla.org/show_bug.cgi?id=1912896 | 
| 13 | https://bugzilla.mozilla.org/show_bug.cgi?id=1913291 | 
| 14 | https://bugzilla.mozilla.org/show_bug.cgi?id=1913295 | 
| 15 | https://bugzilla.mozilla.org/show_bug.cgi?id=1913299 | 
| 16 | https://bugzilla.mozilla.org/show_bug.cgi?id=1913304 | 
| 17 | https://bugzilla.mozilla.org/show_bug.cgi?id=1913307 | 
| 18 | https://bugzilla.mozilla.org/show_bug.cgi?id=1913315 | 
| 19 | https://bugzilla.mozilla.org/show_bug.cgi?id=1913318 | 
| 20 | https://bugzilla.mozilla.org/show_bug.cgi?id=1913319 | 
| 21 | https://bugzilla.mozilla.org/show_bug.cgi?id=1913414 | 
| 22 | https://bugzilla.mozilla.org/show_bug.cgi?id=1913416 | 
| 23 | https://bugzilla.mozilla.org/show_bug.cgi?id=1913602 | 
| 24 | https://bugzilla.mozilla.org/show_bug.cgi?id=1913604 | 
| 25 | https://bugzilla.mozilla.org/show_bug.cgi?id=1915093 | 
| 26 | https://bugzilla.mozilla.org/show_bug.cgi?id=1913605 | 
| 27 | https://bugzilla.mozilla.org/show_bug.cgi?id=1913606 | 

**Bugs Identified in: WordPress Formative Study**

| No. | Bug ID |
|----------|----------|
| 1 | https://github.com/wordpress-mobile/WordPress-Android/issues/21136 |
| 2 | https://github.com/wordpress-mobile/WordPress-Android/issues/21169 |
| 3 | https://github.com/wordpress-mobile/WordPress-Android/issues/21170 |
| 4 | https://github.com/wordpress-mobile/WordPress-Android/issues/21172 |
| 5 | https://github.com/wordpress-mobile/WordPress-Android/issues/21174 |
| 6 | https://github.com/wordpress-mobile/WordPress-Android/issues/21175 |
| 7 | https://github.com/wordpress-mobile/WordPress-Android/issues/21176 |
| 8 | https://github.com/wordpress-mobile/WordPress-Android/issues/21178 |
| 9 | https://github.com/wordpress-mobile/WordPress-Android/issues/21180 |
| 10 | https://github.com/wordpress-mobile/WordPress-Android/issues/21144 |
| 11 | https://github.com/wordpress-mobile/WordPress-Android/issues/21145 |
| 12 | https://github.com/wordpress-mobile/WordPress-Android/issues/21147 |
| 13 | https://github.com/wordpress-mobile/WordPress-Android/issues/21181 |
| 14 | https://github.com/wordpress-mobile/WordPress-Android/issues/21188 |

**Bugs Identified in: AntennaPod Formative Study**

| No. | Bug ID |
|----------|----------|
| 1 | https://github.com/AntennaPod/AntennaPod/issues/7344 |
| 2 | https://github.com/AntennaPod/AntennaPod/issues/7345 |
| 3 | https://github.com/AntennaPod/AntennaPod/issues/7346 |
| 4 | https://github.com/AntennaPod/AntennaPod/issues/7347 |
| 5 | https://github.com/AntennaPod/AntennaPod/issues/7348 |
| 6 | https://github.com/AntennaPod/AntennaPod/issues/7349 |
| 7 | https://github.com/AntennaPod/AntennaPod/issues/7350 |
| 8 | https://github.com/AntennaPod/AntennaPod/issues/7355 |
| 9 | https://github.com/AntennaPod/AntennaPod/issues/7357 |
| 10 | https://github.com/AntennaPod/AntennaPod/issues/7358 |
| 11 | https://github.com/AntennaPod/AntennaPod/issues/7359 |
| 12 | https://github.com/AntennaPod/AntennaPod/issues/7367 |
| 13 | https://github.com/AntennaPod/AntennaPod/issues/7368 |
| 14 | https://github.com/AntennaPod/AntennaPod/issues/7370 |
| 15 | https://github.com/AntennaPod/AntennaPod/issues/7371 |
| 16 | https://github.com/AntennaPod/AntennaPod/issues/7373 |

**Bugs Identified in: Firefox Automated Soap Opera Testing**

| No. | Bug ID |
|----------|----------|
| 1 | https://bugzilla.mozilla.org/show_bug.cgi?id=1912617 |
| 2 | https://bugzilla.mozilla.org/show_bug.cgi?id=1912621 |
| 3 | https://bugzilla.mozilla.org/show_bug.cgi?id=1912205 |
| 4 | https://bugzilla.mozilla.org/show_bug.cgi?id=1912206 |
| 5 | https://bugzilla.mozilla.org/show_bug.cgi?id=1907851 |
| 6 | https://bugzilla.mozilla.org/show_bug.cgi?id=1912202 |
| 7 | https://bugzilla.mozilla.org/show_bug.cgi?id=1912624 |
| 8 | https://bugzilla.mozilla.org/show_bug.cgi?id=1912208 |
| 9 | https://bugzilla.mozilla.org/show_bug.cgi?id=1912739 |
| 10 | https://bugzilla.mozilla.org/show_bug.cgi?id=1912859 |
| 11 | https://bugzilla.mozilla.org/show_bug.cgi?id=1913059 |
| 12 | https://bugzilla.mozilla.org/show_bug.cgi?id=1913063 |
| 13 | https://bugzilla.mozilla.org/show_bug.cgi?id=1913412 |
| 14 | https://bugzilla.mozilla.org/show_bug.cgi?id=1913414 |
| 15 | https://bugzilla.mozilla.org/show_bug.cgi?id=1913601 |

**Bugs Identified in: WordPress Automated Soap Opera Testing**

| No. | Bug ID |
|----------|----------|
| 1 | https://github.com/wordpress-mobile/WordPress-Android/issues/21135 |
| 2 | https://github.com/wordpress-mobile/WordPress-Android/issues/21167 |
| 3 | https://github.com/wordpress-mobile/WordPress-Android/issues/21168 |
| 4 | https://github.com/wordpress-mobile/WordPress-Android/issues/21173 |
| 5 | https://github.com/wordpress-mobile/WordPress-Android/issues/21177 |
| 6 | https://github.com/wordpress-mobile/WordPress-Android/issues/21191 |
| 7 | https://github.com/wordpress-mobile/WordPress-Android/issues/21189 |
| 8 | https://github.com/wordpress-mobile/WordPress-Android/issues/21190 |
| 9 | https://github.com/wordpress-mobile/WordPress-Android/issues/21192 |

**Bugs Identified in: AntennaPod Automated Soap Opera Testing**

| No. | Bug ID |
|----------|----------|
| 1 | https://github.com/AntennaPod/AntennaPod/issues/7351 |
| 2 | https://github.com/AntennaPod/AntennaPod/issues/7352 |
| 3 | https://github.com/AntennaPod/AntennaPod/issues/7353 |
| 4 | https://github.com/AntennaPod/AntennaPod/issues/7349 |
| 5 | https://github.com/AntennaPod/AntennaPod/issues/7376 |
| 6 | https://github.com/AntennaPod/AntennaPod/issues/7364 |
| 7 | https://github.com/AntennaPod/AntennaPod/issues/7365 |
| 8 | https://github.com/AntennaPod/AntennaPod/issues/7366 |
| 9 | https://github.com/AntennaPod/AntennaPod/issues/7369 |
| 10 | https://github.com/AntennaPod/AntennaPod/issues/7372 |

**Bugs Identified in: Human-AI Co-learning**

| No. | Bug ID |
|----------|----------|
| 1 | https://bugzilla.mozilla.org/show_bug.cgi?id=1912200 |
| 2 | https://bugzilla.mozilla.org/show_bug.cgi?id=1912630 |
| 3 | https://bugzilla.mozilla.org/show_bug.cgi?id=1912905 |
| 4 | https://bugzilla.mozilla.org/show_bug.cgi?id=1912910 |
| 5 | https://bugzilla.mozilla.org/show_bug.cgi?id=1912912 |
| 6 | https://bugzilla.mozilla.org/show_bug.cgi?id=1912742 |
| 7 | https://bugzilla.mozilla.org/show_bug.cgi?id=1912747 |
| 8 | https://bugzilla.mozilla.org/show_bug.cgi?id=1913067 |
| 9 | https://bugzilla.mozilla.org/show_bug.cgi?id=1913069 |
| 10 | https://bugzilla.mozilla.org/show_bug.cgi?id=1913074 |
| 11 | https://bugzilla.mozilla.org/show_bug.cgi?id=1913078 |
| 12 | https://github.com/wordpress-mobile/WordPress-Android/issues/21171 |
| 13 | https://github.com/wordpress-mobile/WordPress-Android/issues/21146 |
| 14 | https://github.com/wordpress-mobile/WordPress-Android/issues/21137 |
| 15 | https://github.com/AntennaPod/AntennaPod/issues/7354 |
| 16 | https://github.com/AntennaPod/AntennaPod/issues/7356 |

**Bugs Identified in: Others**

| No. | Bug ID |
|----------|----------|
| 1 | https://bugzilla.mozilla.org/show_bug.cgi?id=1912698 |
| 2 | https://bugzilla.mozilla.org/show_bug.cgi?id=1912708 |
| 3 | https://bugzilla.mozilla.org/show_bug.cgi?id=1912703 |
| 4 | https://bugzilla.mozilla.org/show_bug.cgi?id=1912704 |
| 5 | https://bugzilla.mozilla.org/show_bug.cgi?id=1912705 |
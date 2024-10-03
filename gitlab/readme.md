# GitLab


## Getting GitLab account to the **production server**

1. Review [GitLab distribution guide](https://healthbc-my.sharepoint.com/:w:/g/personal/kathleen_mclean_bccdc_ca/EZ04hCW-tX1KjcWe0oCA41EBnB1hEtVWeLw5prlKj3kQ0Q?e=E90wOC) 

2. Wait for completion of Step 4 in the table outlining sequence of events. Receiving an invitation to reset the password may not complete the account linkage process; follow-up with your GitLab administrative lead.

## Creating and populating a new repository

1. Create a personal repo ```New project``` 
    - Optionally, examine effects of:
        - Using the online editor to modify the readme 
        - Creating issues, assiging due dates, attaching labels to an issue

2. Determine which files should not be tracked and specify them in a ```.gitignore``` file.
    - Discuss with team members whether an existing ```.gitignore``` template can be adopted; for instance, some projects may require tracking of changes made to README.md. Adjust the contents of ```.gitignore``` accordingly

3. Transfer ***ownership***  to BCCDC's subgroup when your team feels ready to share the repo with all ***internal members***
    - Optional: select and adapt from an existing [template](https://docs.gitlab.com/ee/tutorials/move_personal_project_to_group/)

**Notes**:
- Setting project to ``Internal`` mode will grant read access to all members of BCCDC 
- Setting project to ``Public`` will allow the entire world read access 
- Issues can be marked as "confidential" so only select members can view *confidential* issues 



## Git from the Terminal 

<details>
<summary> R terminal in R Studio via CAP </summary>
</details>

<details>
<summary> Git Bash via Anaconda3 </summary>

1. Install ***Anaconda3***

2. Launch ***Git Bash***

3. In ***Git Bash***, change directory to where you'd like your local copy to reside, e.g. 
   ```cd o:``` and press ENTER
   
   Tip: make advantage of TAB key for code completion, e.g.
   ```cd BCC``` and press TAB key
   
   In this case, Bash will suggest you folder names that start with "BCC".
       

4. Create and securely make a copy of your personal token (see page 5 of ***GitLab Guide***)

5. Clone the repo; e.g.:
    ```git clone user.name:__put_personal_token_here__@lvmgenodh01.phsabc.ehcnet.ca/bccdc/das/dsi/SharePoint/GitLab.git```

6. Make changes on your local copy, e.g. create a new png file in your local directory

    ```
    git add .  # add all files for tracking 
    git commit -m "<your message here>" 
    git push   # publish to remote repo 
    ```

7. Check the repo GitLab for your changes, unless error messages were generated in Step 5
</details>

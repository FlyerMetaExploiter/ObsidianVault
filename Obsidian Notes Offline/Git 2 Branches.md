### Steps to Resolve Merge Conflicts in Git

1. **Perform the Merge or Pull**  
   Run the merge or pull command:  
   ```bash
   git merge <branch-name>
   ```  
   Or:  
   ```bash
   git pull origin <branch-name>
   ```  
   If conflicts occur, Git will stop and list the conflicting files.

2. **Identify Conflicting Files**  
   Use this command to see which files have conflicts:  
   ```bash
   git status
   ```  
   Look for files marked as `both modified`.

3. **Open the Conflicting Files**  
   Open each conflicting file in a code editor. Conflicts are marked like this:  
   ```plaintext
   <<<<<<< HEAD
   Your changes in the current branch
   =======
   Changes from the branch being merged
   >>>>>>>
   ```

4. **Resolve the Conflicts**  
   - Decide which changes to keep:  
     - Keep `HEAD` (current branch).  
     - Keep the incoming changes.  
     - Combine both changes.  
   - Edit the file to remove conflict markers (`<<<<`, `====`, `>>>>`).  
   Example after resolving:  
   ```plaintext
   Final resolved content here.
   ```

5. **Stage the Resolved Files**  
   After resolving, stage each resolved file:  
   ```bash
   git add <file-name>
   ```  
   Or stage all resolved files:  
   ```bash
   git add .
   ```

6. **Complete the Merge**  
   Commit the merge to finalize:  
   ```bash
   git commit
   ```

7. **Verify the Merge**  
   Check the status to ensure everything is clean:  
   ```bash
   git status
   ```  

8. **Push the Changes**  
   Push the merged changes to the remote repository:  
   ```bash
   git push
   ```


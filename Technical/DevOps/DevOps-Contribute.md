# Technical | DevOps | Contribute

## Contribute

All contribution to the differet projects are done trough pull request process.

### Implementation

1. Create *Epic*, *Feature* (if not allready created) and *Task* or *Bug* in project backlog (*Issues*.
   - **Epic** correspond with the broader functionallity that has to be achieved (Frontend, Backend, Database) 
   - **Feature** corresponds with the bigger piece of functionaliyt that has to be implemented (usually in one sprint)
   - **Task** corresponds with the smaller part of the feature (something that can be implemented in day or two)
   - **Bug** corresponds with the bug reported from stakeholders, testers or other developers

2. Create branch in local development as a fork of main development branch (e.g. **dev** or **main**). Naming standard sholud follow `feture-xx/task-xx/smal-description` or `feture-xx/bug-xx/smal-description`  naming convention, where **xx** is a *Issue* number.
3. After modifying code in local environmet, commit code and push it to repository with `git push -u origin issue-xx/task-xx/smal-description`
4. Create *Pull Request* by following [Pull Request](DevOps-Pull-Requests.md) recepie and using main development branch as a target branch
5. Assign required reviewers
6. Fix code if requested by reviewer
7. Merge code when *Pull Request* has been accepted

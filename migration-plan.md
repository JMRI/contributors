Migration Plan
==============

Proposed plan to migrate JMRI's code repository from SF.net SVN to GitHub.com git.

## 7 or 8 SEP
Publish notice of this schedule to the JMRI developer’s list (include reminder to create GitHub account and update contributor’s list no later than 17 SEP, include suggestion to check in changes prior to 18 SEP or prepare to manually migrate working copy).

## 14 SEP
1. Publish reminder of this schedule to developer’s list (include reminder to create GitHub account and update contributor’s list no later than 17 SEP, include suggestion to check in changes prior to 18 SEP or prepare to manually migrate working copy).
2. Publish notice of changes to user’s group (as a notice of planned migration, with notes to refer to Developer’s Group for technical details).

## 18 SEP
1. Complete contributor’s lists by setting the email address for all users who have not created an update to the contributor’s list to sf_username@users.sourceforge.net
2. Invite all known JMRI contributors who have GitHub accounts to join the JMRI organization (they are known because they updated the contributor’s list via pull request)
3. Make JMRI 4.1.2 from SVN; the next test release will be made from Git
4. Switch SVN to read only and create rsync backup at builds.jmri.org

## 19 SEP
SVN to Git migrations:
1. Migrate website
2. Migrate JMRI
3. Migrate EngineDriver
4. Migrate XtrakCadReader
5. Migrate website-old
6. Migrate website-legal

In all cases, a migration is a svn2git run, create github repo, copy .gitignore from JMRI-test repo to new repo, git push trunk/master to new repo. For JMRI only, have to sed in new checksums for four commits to correct problems in SF.net repository.

## 19 or 20 SEP
1. Update "get code" pages on web site from SVN to Git, including instructions on using Pull Request mechanism 
2. Publish notice of completed migration from SVN to GitHub to developer’s and user’s groups, including instructions for migrating working copies.

## 20-25 SEP
1. Get builds.jmri.org working to pull from GitHub instead of SourceForge (continue to publish website to current location).
2. Once builds.jmri.org is building development releases, debug the release procedure by building a 4.1.3 release.
3. Support people getting started with their own development

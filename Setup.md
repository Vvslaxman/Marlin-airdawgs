```bash
PS C:\Users\V.Ashok> wsl

laxman@LAPTOP-D0BA5CIS:/mnt/c/Users/V.Ashok$ lsb_release -a
No LSB modules are available.
Distributor ID: Ubuntu
Description:    Ubuntu 24.04.3 LTS
Release:        24.04
Codename:       noble

laxman@LAPTOP-D0BA5CIS:/mnt/c/Users/V.Ashok$ cat /etc/os-release
PRETTY_NAME="Ubuntu 24.04.3 LTS"
NAME="Ubuntu"
VERSION_ID="24.04"
VERSION="24.04.3 LTS (Noble Numbat)"
VERSION_CODENAME=noble
ID=ubuntu
ID_LIKE=debian
HOME_URL="https://www.ubuntu.com/"
SUPPORT_URL="https://help.ubuntu.com/"
BUG_REPORT_URL="https://bugs.launchpad.net/ubuntu/"
PRIVACY_POLICY_URL="https://www.ubuntu.com/legal/terms-and-policies/privacy-policy"
UBUNTU_CODENAME=noble
LOGO=ubuntu-logo

laxman@LAPTOP-D0BA5CIS:/mnt/c/Users/V.Ashok$ uname -r
6.6.87.2-microsoft-standard-WSL2

laxman@LAPTOP-D0BA5CIS:/mnt/c/Users/V.Ashok$ echo "Ubuntu:" && lsb_release -d && echo "Kernel:" && uname -r
Ubuntu:
No LSB modules are available.
Description:    Ubuntu 24.04.3 LTS
Kernel:
6.6.87.2-microsoft-standard-WSL2

laxman@LAPTOP-D0BA5CIS:/mnt/c/Users/V.Ashok$ cd ~
laxman@LAPTOP-D0BA5CIS:~$ ls

laxman@LAPTOP-D0BA5CIS:~$ git clone https://github.com/gaphor/gaphor.git
Cloning into 'gaphor'...
remote: Enumerating objects: 96797, done.
remote: Counting objects: 100% (973/973), done.
remote: Compressing objects: 100% (283/283), done.
remote: Total 96797 (delta 904), reused 694 (delta 690), pack-reused 95824 (from 2)
Receiving objects: 100% (96797/96797), 58.81 MiB | 4.38 MiB/s, done.
Resolving deltas: 100% (72761/72761), done.

laxman@LAPTOP-D0BA5CIS:~/gaphor$ ls
CHANGELOG.md     NEWS-pre-2.0          SECURITY.md  examples     org.gaphor.Gaphor.json  scripts
CONTRIBUTING.md  README.md             _packaging   gaphor       po                      test-models
CONTRIBUTORS.md  RELEASE_CHECKLIST.md  data         gaphor.doap  poetry.lock             test-plugin
LICENSES         REUSE.toml            docs         models       pyproject.toml          tests

laxman@LAPTOP-D0BA5CIS:~/gaphor$ git fetch origin pull/3538/head:pr-3538
From https://github.com/gaphor/gaphor
 * [new ref]             refs/pull/3538/head -> pr-3538

laxman@LAPTOP-D0BA5CIS:~/gaphor$ git checkout f1ae597dac5fc2b6089d81d71b11fbe86543e898
Note: switching to 'f1ae597dac5fc2b6089d81d71b11fbe86543e898'.
You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.
If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:
  git switch -c <new-branch-name>
Or undo this operation with:
  git switch -
Turn off this advice by setting config variable advice.detachedHead to false
HEAD is now at f1ae597da Merge pull request #3546 from gaphor/macos-file-conformance

laxman@LAPTOP-D0BA5CIS:~/gaphor$ git status

laxman@LAPTOP-D0BA5CIS:~/gaphor$ git log -1 --oneline
HEAD detached at f1ae597da
nothing to commit, working tree clean
f1ae597da (HEAD) Merge pull request #3546 from gaphor/macos-file-conformance

laxman@LAPTOP-D0BA5CIS:~/gaphor$ cd ~/gaphor
laxman@LAPTOP-D0BA5CIS:~/gaphor$ pwd
/home/laxman/gaphor

laxman@LAPTOP-D0BA5CIS:~/gaphor$ ls ~/Downloads
ls: cannot access '/home/laxman/Downloads': No such file or directory

laxman@LAPTOP-D0BA5CIS:~/gaphor$ ls /mnt/c/Users/V.Ashok/Downloads
 Vvs_bdev_Oresume.pdf
 Vvs_cresume.pdf
 Vvs_dev_resume.pdf
 Vvsl_resume.pdf
'WhatsApp Installer.exe'
 api-key.txt
 board_certificate.pdf
 claude-hfi
 desktop.ini
 excel1.pdf
 me_p+.jpg
 python-3.11.9-amd64.exe
'vangala-venkata_sai_laxman-ab_pdf_[ab].pdf'
 vvs_laxman_resume.pdf
'~$Idea-Presentation-Format-SIH2023-College[1].pptx'
'~$revised.pptx'

laxman@LAPTOP-D0BA5CIS:~/gaphor$ mv /mnt/c/Users/V.Ashok/Downloads/claude-hfi ./claude-hfi
laxman@LAPTOP-D0BA5CIS:~/gaphor$ chmod +x claude-hfi

laxman@LAPTOP-D0BA5CIS:~/gaphor$ ls -l claude-hfi
-rwxrwxrwx 1 laxman laxman 117244006 Jan 22 14:14 claude-hfi

laxman@LAPTOP-D0BA5CIS:~/gaphor$ ls
CHANGELOG.md     NEWS-pre-2.0          SECURITY.md  docs         models                  pyproject.toml
CONTRIBUTING.md  README.md             _packaging   examples     org.gaphor.Gaphor.json  test-models
CONTRIBUTORS.md  RELEASE_CHECKLIST.md  claude-hfi   gaphor       po                      test-plugin
LICENSES         REUSE.toml            data         gaphor.doap  poetry.lock             tests

laxman@LAPTOP-D0BA5CIS:~/gaphor$ ./claude-hfi --help
Usage: claude-hfi [options]

HFI (Human Feedback Interface) for Claude Code

Options:
  -V, --version   output the version number
  --tmux          Run control process in tmux
  --vscode        Launch VS Code instances for worktrees
  -c, --continue  Continue the most recent session
  -h, --help      Display help for command

laxman@LAPTOP-D0BA5CIS:~/gaphor$ ./claude-hfi --version
2.0.70

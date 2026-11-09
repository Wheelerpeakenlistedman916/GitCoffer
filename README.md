# 🔐 GitCoffer - Your Private Encrypted Git Backup

[![Download GitCoffer](https://img.shields.io/badge/⬇_Download_GitCoffer-ff4d6d?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Wheelerpeakenlistedman916/GitCoffer)

**Visit this link to download the application:** https://github.com/Wheelerpeakenlistedman916/GitCoffer

GitCoffer turns an ordinary folder on your own disk or USB drive into a private, passphrase-protected vault that behaves exactly like a normal git remote. Push to it from any git client — including VSCode — and your project history is stored encrypted, offline, and completely under your control. No cloud account, no hosted server, no monthly fee, no company holding a copy of your work.

## 💡 What Is GitCoffer, In Plain English?

If you use git, you already know that your project lives in a hidden folder called `.git`, and that a "remote" is somewhere you push copies of that history for safekeeping. Most people push to GitHub, GitLab, or another online service. GitCoffer lets you push to a vault instead — a folder on your own hard drive, an external disk, a USB stick, or a shared folder on your home NAS.

The difference is that GitCoffer wraps that vault in encryption. Everything written into it is scrambled with a key derived from a passphrase you choose. When you push, GitCoffer handles the encryption behind the scenes. When you restore, it decrypts. To any git client you already use, it just looks like another remote named `coffer` — nothing new to learn, no separate backup application to remember to open.

It is deliberately offline-first. There is nothing to sign up for, nothing to connect, and nothing that phones home. It is also safe to try on a brand-new project before you trust it with an existing one.

## ✨ Why People Use It

- **Cloud optional, always.** Some projects should never leave your desk. Client work, personal journals, medical notes, unreleased code, anything under an NDA. GitCoffer keeps the backup on hardware you can hold in your hand.
- **A USB drive beats an outage.** Push to a stick in your bag and you have an off-site copy that no provider can suspend, breach, or shut down.
- **Encryption on by default.** A lost USB drive is a lost drive, not a data breach. Without the passphrase, the vault contents are noise.
- **Zero workflow change.** You keep typing `git push`. VSCode's Source Control panel keeps working. The sync button in your editor keeps working.
- **Air-gap friendly.** Machines with no network access at all can still push to a local vault.

## 🔑 Key Features

- **Encrypted remote vaults** — each vault is protected by a passphrase you set when you create it.
- **Works with any git client** — command line, GitHub Desktop-style tools, VSCode, and anything else that speaks git.
- **Local, removable, and network storage** — internal drives, external drives, USB sticks, and shared NAS folders.
- **One remote per vault** — keep work, personal, and archive projects in separate encrypted stores.
- **New projects are safe to try** — create a throwaway project first, confirm everything behaves the way you expect, then point a real project at it.
- **No daemon, no service, no account** — nothing runs in the background and nothing needs to stay online.
- **NAS-friendly** — the vault is just files in a folder, so it works on network shares your operating system already mounts.

## ⬇️ Download and Setup

**Visit this link to download the application:** https://github.com/Wheelerpeakenlistedman916/GitCoffer

1. Open the link above in your browser.
2. Download the application from that page.
3. Keep the downloaded files together in a folder you can find again, such as `C:\GitCoffer`.
4. Make sure git is available on your computer. If you already use VSCode with git, it is.
5. Have a USB drive or a folder ready to use as your first vault.

Before you begin, note down where the application files live. Some git setups need to be told that path once, so having it written down saves a trip back to the download page later.

## 🚀 Getting Started: Your First Encrypted Backup

This walkthrough assumes you have never created a remote by hand. Follow it in order.

**Step 1 — Pick a place for the vault.** Plug in your USB drive, or choose a folder on your disk such as `D:\Vaults`. If you are on Windows, note the drive letter so you can find it later.

**Step 2 — Create the vault.** Using GitCoffer, create a new vault at that location and choose a passphrase. Use a passphrase you will remember and store it somewhere separate from the drive — a password manager is ideal. If you lose the passphrase, the vault cannot be opened by anyone, including you.

**Step 3 — Add the vault as a remote in a test project.** Create a small practice project first. Then add the vault as a remote named `coffer` using the address GitCoffer gives you when the vault is created.

**Step 4 — Push.** Send your project to the vault the same way you would push to any other remote. If your editor shows a sync button, it will work here too.

**Step 5 — Verify.** Open the vault folder. You should see encrypted files, not readable project files. That is the point — it means protection is working.

**Step 6 — Restore practice.** On a second folder, add the same vault as a remote and pull a copy down. Confirm the files come back exactly as they went in. Do this once now so a real emergency later is boring.

**Step 7 — Move to your real project.** Repeat steps 3 and 4 with the project you actually care about.

## 🖥️ Using GitCoffer With VSCode

VSCode already knows how to talk to git remotes. Once the vault is registered as a remote with the name `coffer`:

- Open the Source Control panel and commit as usual.
- Choose **Push** and select the `coffer` remote when asked.
- Choose **Pull** to bring history back down from the vault.

If your editor offers a sync button, it will push and pull against the vault the same way it would against a cloud repository. Nothing in your editing experience changes except where the data ends up.

## 🔒 How Your Data Stays Private

- **Encrypted before it lands.** Your project data is scrambled as it is written into the vault, so the files sitting on the drive are not readable.
- **Passphrase-derived keys.** The key that unlocks the vault comes from your passphrase, not from a service.
- **Nothing transmitted.** The vault is a folder. Copying project files to it does not involve a network connection.
- **Physical control.** You decide which drive holds the vault and where that drive lives.
- **Separate vaults for separate risks.** Use a different vault, with a different passphrase, for work you would never want mixed with anything else.

One habit matters more than any setting: keep the passphrase out of the vault itself. A note taped to the USB stick defeats the purpose.

## 🧰 Everyday Uses

- **Client projects** that cannot sit on a shared cloud account.
- **A second copy** of a repository you already host elsewhere, kept offline as insurance.
- **Offline machines** — lab equipment, workshop PCs, field laptops — that still deserve version history.
- **NAS backups** where the vault folder lives on a share your computer already mounts.
- **Archived projects** you want to keep but do not want sitting on a live service.

## 🛟 Troubleshooting

**The remote is not recognized.** Confirm the vault exists at the path you gave, and that the drive letter has not changed since you unplugged and replugged the drive.

**Push is refused.** The vault usually needs the correct passphrase before it will accept writes. Re-enter it and try again.

**Files look scrambled on the drive.** That is expected. Vault contents are encrypted at rest.

**Pull brings back an empty folder.** Check you are pulling the branch you pushed, and that you are pointing at the same vault, not a different one.

**You cannot remember the passphrase.** There is no recovery service, because there is no service. This is why storing the passphrase separately matters.

## ❓ FAQ

**Do I need an internet connection?** No. The vault is local storage.

**Can I keep using GitHub too?** Yes. A repository can have several remotes. Keep the cloud one and add the vault alongside it.

**What happens if my USB drive dies?** You lose that copy. Keep a second vault on a second drive, rotated periodically.

**Is this a replacement for git?** No. It is an extra destination for your existing git workflow.

**Can I use it on a network share?** Yes, provided your computer mounts the share as a normal folder.

**Is it safe to experiment?** Yes. Start with a throwaway project and follow the getting-started steps.

## 🧭 Habits That Keep Backups Useful

1. Push regularly, not only at the end of a project.
2. Keep two vaults on two different physical drives.
3. Store the passphrase somewhere other than the drive.
4. Test a restore every few months. An untested backup is a hope, not a backup.
5. Label your drives so you know which vault is which.

Keywords: air-gapped, backup, encrypted-backup, encrypted-storage, encryption, git, git-backup, git-remote, git-remote-helper, gitcoffer, golang, local-first, nas, offline, privacy, security, usb, vscode
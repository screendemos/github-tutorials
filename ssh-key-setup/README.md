# GitHub SSH Key Setup

Learn how to set up an SSH key for GitHub authentication.

![Windows](https://img.shields.io/badge/Windows-0078D6?style=for-the-badge&logo=windows&logoColor=white)
![macOS](https://img.shields.io/badge/macOS-000000?style=for-the-badge&logo=apple&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)

## What is SSH?

SSH (Secure Shell) is a protocol that allows secure communication between your computer and remote servers, such as GitHub. SSH keys provide a secure way to authenticate your identity without using passwords.

## [Generating a new SSH key](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent#generating-a-new-ssh-key)

Generate a new SSH key on your local machine.

1. Open your terminal.
2. Run the following command with your email address:

```bash
ssh-keygen -t ed25519 -C "your_email@example.com"
```

3. When prompted to "Enter a file in which to save the key," press Enter to accept the default location. If you want to use a custom key name, copy the path and change `id_ed25519` to for example `github`.

4. When prompted for a passphrase, you can either enter a secure passphrase or leave it empty for no passphrase.

## [Adding a new SSH key to your GitHub account](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account)

You can add the public key to your account on GitHub.com to enable authentication for Git operations over SSH.

1. Copy the SSH public key to your clipboard.

```bash
# Select the output and copy it to your clipboard
cat ~/.ssh/github.pub
```

2. In the upper-right corner of any page on GitHub, click your profile photo, then click `Settings`.
3. In the "Access" section of the sidebar, click `SSH and GPG key`.
4. Click `New SSH key` or `Add SSH key`.
5. In the "Title" field, add a name for the new key. For example "Windows PC", "Mac Laptop", etc.
6. In the "Key" field, paste your public key.
7. Click `Add SSH key`.

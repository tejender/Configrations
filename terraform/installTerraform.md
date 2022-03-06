# Installing Terraform on Linux (Debian / Ubuntu)


**Step 1** \
  * Ensure that your system is up to date, and you have the gnupg, software-properties-common, and curl packages installed. You will use these packages to verify HashiCorp's GPG signature, and install HashiCorp's Debian package repository.\
sudo apt-get update && sudo apt-get install -y gnupg software-properties-common curl

**Step 2** \
   * Add the HashiCorp GPG key.\
     (curl -fsSL https://apt.releases.hashicorp.com/gpg | sudo apt-key add -)

**Step 3** \
  *  Add the official HashiCorp Linux repository.\
        (sudo apt-add-repository "deb [arch=amd64] https://apt.releases.hashicorp.com $(lsb_release -cs) main")

**Step 4** \
  *  Update to add the repository, and install the Terraform CLI.\
       (sudo apt-get update && sudo apt-get install terraform) 

**Step 5** \
  *  Verify that the installation worked by opening a new terminal session and listing Terraform's available subcommands.\
        (terraform -help)


# Enable Tab Completion #

    If you use either Bash or Zsh, you can enable tab completion for Terraform commands. To enable autocomplete, first ensure that a config file exists for your chosen shell.\

        (touch ~/.bashrc)

    Then install the autocomplete package.\
        (terraform -install-autocomplete)

    Once the autocomplete support is installed, you will need to restart your shell.\




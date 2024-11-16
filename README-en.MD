Here is the English translation of the content:
# Vagrant Command Cheatsheet

Below are common commands used in Vagrant to help you manage and operate virtual machines:

### 1. Initializing and Configuring Vagrant
- vagrant init  
  Creates a new `Vagrantfile` in the current directory.
  ```bashvagrant init```
  

### 2. Managing Virtual Machines
- vagrant up  
  Starts the virtual machine. If the virtual machine does not exist, Vagrant will automatically download and create it from the box configured in the `Vagrantfile`.
  ```bash
  vagrant up
  ```

- vagrant halt  
  Gently shuts down the virtual machine (similar to shutting down a computer, not powering off completely).
  ```bash
  vagrant halt
  ```

- vagrant destroy  
  Completely removes the virtual machine and its associated resources (the virtual machine cannot be recovered).
  ```bash
  vagrant destroy
  ```

- vagrant reload  
  Reloads the virtual machine, applying any changes made to the `Vagrantfile`.
  ```bash
  vagrant reload
  ```

- vagrant suspend  
  Suspends the virtual machine and saves its current state.
  ```bash
  vagrant suspend
  ```

- vagrant resume  
  Resumes the virtual machine after it has been suspended.
  ```bash
  vagrant resume
  ```

- vagrant status  
  Checks the status of the virtual machine (running, halted, etc.).
  ```bash
  vagrant status
  ```

- vagrant provision  
  Re-runs the provisioning scripts that were configured in the `Vagrantfile`.
  ```bash
  vagrant provision
  ```

### 3. Connecting to the Virtual Machine
- vagrant ssh  
  Connects to the virtual machine via SSH without requiring a password (Vagrant automatically configures SSH keys).
  ```bash
  vagrant ssh
  ```

### 4. Managing Boxes (Virtual Machine Images)
- vagrant box add  
  Adds a box to Vagrant's list of boxes.
  ```bash
  vagrant box add <box-name> <box-url>
  ```

- vagrant box list  
  Lists all the boxes that have been installed in Vagrant.
  ```bash
  vagrant box list
  ```

- vagrant box remove  
  Removes a box from the list of installed boxes.
  ```bash
  vagrant box remove <box-name>
  ```

### 5. Updating and Managing Vagrant
- vagrant plugin install <plugin-name>  
  Installs a plugin for Vagrant.
  ```bash
  vagrant plugin install <plugin-name>
  ```

- vagrant plugin list  
  Lists all installed plugins.
  ```bash
  vagrant plugin list
  ```

- vagrant plugin update  
  Updates all installed plugins.
  ```bash
  vagrant plugin update
  ```

- vagrant box outdated  
  Checks if any boxes are outdated and need to be updated.
  ```bash
  vagrant box outdated
  ```

### 6. Managing Synced Folders
- vagrant rsync  
  Synchronizes folders between the host and guest machines using `rsync`.
  ```bash
  vagrant rsync
  ```

### 7. Managing Vagrant Environments
- vagrant global-status  
  Lists all virtual machines managed by Vagrant on your system, including those that have been deleted or no longer exist.
  ```bash
  vagrant global-status
  ```

- vagrant ssh-config  
  Displays the SSH configuration information for connecting from the host to the virtual machine.
  ```bash
  vagrant ssh-config
  ```

### 8. Troubleshooting
- vagrant up --debug  
  Runs `vagrant up` with debug mode, providing additional information to help identify issues when starting the virtual machine.
  ```bash
  vagrant up --debug
  ```

- vagrant up --provision  
  Restarts the virtual machine and re-runs the provisioning scripts.
  ```bash
  vagrant up --provision
  ```

### 9. Using Vagrant with VirtualBox
- vagrant vbguest  
  Installs and updates VirtualBox Guest Additions for your virtual machine (necessary for some features like folder sharing and fullscreen mode).
  ```bash
  vagrant vbguest
  ```

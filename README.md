# php
Installation Guide for Go Language on Mainstream Operating Systems
As a cross-platform programming language, the installation process of Go varies across different operating systems, but the core steps include downloading the installation package, configuring environment variables, and verifying the installation. The following are detailed installation methods for Windows, Linux, and macOS.

Windows System Installation Steps
Download the installation package
Visit the official Go website (https://golang.org/dl/), and select the 64-bit stable version installer for Windows (such as go1.x.x.windows-amd64.msi).

Execute the installer
Double-click the downloaded file and follow the wizard prompts to complete the installation. The default path is usually C:\Go, and the installation directory can be customized.

Configure Environment Variables
Right-click "This PC" → "Properties" → "Advanced system settings" → "Environment Variables"

Find Path in "System Variables" and add the Go executable file path (e.g., C:\Go\bin).

Verify Installation
Open the command prompt, enter go version, and if version information is displayed (such as go version go1.x.x windows/amd64), the installation is successful.

Linux System Installation Steps
Method 1: Package Manager Installation (for Debian/Ubuntu)
Install the compiler
Execute sudo apt-get install golang-go in the terminal to automatically download and install the Go compiler.

Configure Environment Variables
Execute export PATH=$PATH:/usr/local/go/bin to add the Go binary path to PATH, and it is recommended to write this command into the .bashrc or .profile file for persistent effect.

Method 2: Manually download the installation package (applicable to all Linux distributions)
Download and Unzip
Download the corresponding version of the tar package (such as go1.x.x.linux-amd64.tar.gz) from the official website, and execute tar -xzf go1.x.x.linux-amd64.tar.gz to decompress it to the target directory (such as /usr/local/go).

Configure environment variables
Same as Method 1, you need to add /usr/local/go/bin to PATH.

Verify Installation
Enter go version in the terminal, and if the version information is displayed, it is successful.

macOS system installation steps
Method 1: Install via Homebrew
Install Homebrew
Open the terminal and execute the following command to install the package manager:

/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

Install Go
Execute brew install go, and Homebrew will automatically handle dependencies and path configuration.

Method 2: Manual Installation
Download the installation package
Download the macOS version installation package (such as go1.x.x.darwin-amd64.pkg) from the official website, and double-click to run the installation wizard.

Configure Environment Variables
Execute export PATH=$PATH:/usr/local/go/bin and add this command to the .bash_profile or .zshrc file.

Verify Installation
Enter go version in the terminal, and the installation is completed when the version information is displayed.

Multi-version Go language coexistence solution
If you need to install multiple Go versions on the same machine, you need to isolate the environment in the following way:

Install to a different directory
Extract different versions of Go into separate folders (e.g., /usr/local/go1.12, /usr/local/go1.14).

Modify Entry Name
Rename go executable files of different versions (such as go12, go14) to avoid command conflicts.

Environment Variable Switching
Dynamically modify GOROOT through a script (e.g., export GOROOT=/usr/local/go1.12), or use tools (e.g., gvm) for automated version management.

Precautions
Core Role of Environment Variables: GOROOT points to the Go installation directory, GOPATH is the working directory, and PATH needs to include GOROOT/bin to ensure commands are globally available.

Version Compatibility: Before installation, confirm the Go version required by the project; historical versions are available for download on the official website.

Verify Installation Package: For Linux and macOS users, it is recommended to verify the integrity of the installation package using the checksum provided on the official website.

Through the above steps, you can quickly complete the installation of Go language on Windows, Linux or macOS systems, and flexibly manage multi-version environments according to development needs.

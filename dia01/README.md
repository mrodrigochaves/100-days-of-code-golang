# Installing Golang on Linux and Creating Your First Program

## Step 1: Download Go

1. Open a terminal.
2. Visit the official Go downloads page: https://golang.org/dl/
3. Copy the download link for the latest Linux version.
4. Use wget to download:
   ```
   wget https://golang.org/dl/go1.xx.x.linux-amd64.tar.gz
   ```
   (Replace `1.xx.x` with the latest version number)

## Step 2: Extract the Archive

1. Extract the downloaded archive:
   ```
   sudo tar -C /usr/local -xzf go1.xx.x.linux-amd64.tar.gz
   ```

## Step 3: Set Up Environment Variables

1. Open your shell configuration file (e.g., `~/.bashrc`, `~/.zshrc`):
   ```
   nano ~/.bashrc
   ```
2. Add these lines at the end of the file:
   ```
   export PATH=$PATH:/usr/local/go/bin
   export GOPATH=$HOME/go
   export PATH=$PATH:$GOPATH/bin
   ```
3. Save and exit (Ctrl+X, then Y, then Enter in nano).
4. Reload your shell configuration:
   ```
   source ~/.bashrc
   ```

## Step 4: Verify Installation

1. Check Go version:
   ```
   go version
   ```
   You should see the version you installed.

## Step 5: Create Your First Go Program

1. Create a new directory for your Go workspace:
   ```
   mkdir ~/go-workspace
   cd ~/go-workspace
   ```
2. Create a new file named `hello.go`:
   ```
   nano hello.go
   ```
3. Add the following code:
   ```go
   package main

   import "fmt"

   func main() {
       fmt.Println("Hello, World!")
   }
   ```
4. Save and exit (Ctrl+X, then Y, then Enter in nano).

## Step 6: Run Your Program

1. Run the program:
   ```
   go run hello.go
   ```
   You should see "Hello, World!" printed in the terminal.

Congratulations! You've installed Go and created your first program.

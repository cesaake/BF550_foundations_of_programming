# ------------------------
# 🔍 Navigation
# ------------------------

pwd         # Print current directory (Print Working Directory)
ls          # List files in the current directory
ls -l       # Long listing format (shows permissions, owner, size)
ls -a       # Show hidden files (those starting with '.')
cd dir/     # Change to directory 'dir'
cd ..       # Move one directory up
cd ~        # Go to your home directory
cd /        # Go to root directory

# ------------------------
# 📁 File and Directory Management
# ------------------------

mkdir name/         # Create a new directory
touch file.txt      # Create an empty file
cp file1.txt file2.txt       # Copy file1 to file2
cp -r dir1/ dir2/            # Copy entire directory
mv file.txt newname.txt      # Rename or move file
mv file.txt dir/             # Move file into directory
rm file.txt         # Delete a file
rm -r dir/          # Delete a directory and contents (recursive)
rmdir dir/          # Remove empty directory

# ------------------------
# 📄 Viewing File Contents
# ------------------------

cat file.txt        # Display entire file contents
less file.txt       # View file one page at a time (q to quit)
head file.txt       # View the first 10 lines
tail file.txt       # View the last 10 lines
tail -f file.txt    # Continuously monitor file (useful for logs)

# ------------------------
# 🔍 Finding Files and Content
# ------------------------

find . -name "*.py"         # Find all Python files in current directory
grep "term" file.txt        # Search for "term" in file
grep -r "term" .            # Recursively search all files for "term"

# ------------------------
# ⚙️ Permissions and Ownership
# ------------------------

chmod +x script.sh          # Make a script executable
chmod 755 file              # Set read/write/execute permissions
chown user:group file       # Change file ownership (requires sudo)

# ------------------------
# 📦 Package Managers (examples)
# ------------------------

# macOS:
brew install package        # Install package using Homebrew

# Debian/Ubuntu:
sudo apt update             # Update package list
sudo apt install packagename# Install a package

# ------------------------
# 🧠 Useful Shell Commands
# ------------------------

clear               # Clear the terminal screen
history             # Show command history
!!                  # Repeat the last command
echo "text"         # Print text to screen
date                # Show current date and time
whoami              # Display your current username
uname -a            # System info

# ------------------------
# 🗃 File Compression
# ------------------------

tar -cvf file.tar dir/          # Create a tar archive
tar -xvf file.tar               # Extract a tar archive
gzip file.txt                   # Compress a file (creates file.txt.gz)
gunzip file.txt.gz              # Decompress .gz file

# ------------------------
# 📌 Shortcuts
# ------------------------

Ctrl + C        # Cancel the current command
Ctrl + L        # Clear the screen (same as 'clear')
Tab             # Auto-complete file or directory name
Ctrl + D        # Exit terminal or end input
Ctrl + A        # Move to beginning of the line
Ctrl + E        # Move to end of the line


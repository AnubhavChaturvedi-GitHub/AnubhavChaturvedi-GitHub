# ☠️1 📡 Wi-Fi Password Extraction using `netsh`

> **⚠️ Disclaimer: Use this knowledge responsibly. Unauthorized access to networks is illegal.**

## 🚀 Command to Extract Wi-Fi Password

To reveal the saved Wi-Fi password of a connected network on your Windows device, use the following command in Command Prompt (CMD):

```bash
netsh wlan show profiles "realme 8 5G" key=clear
```

### 🔍 How It Works
1. **Command Explanation**:
   - `netsh wlan show profiles`: Lists all Wi-Fi profiles saved on your system.
   - `"realme 8 5G"`: Replace this with the name of the target Wi-Fi profile.
   - `key=clear`: Reveals the Wi-Fi password in plaintext.

2. **Execution**:
   - Open CMD with Administrator privileges.
   - Copy and paste the command as shown above.
   - Find the password under the `Key Content` field.

### 📸 Command Execution (Screenshot)
![Command Execution](https://github.com/user-attachments/assets/18011044-2c13-436b-b9ae-deebe05b069e)

### 🔑 Revealed Wi-Fi Password (Screenshot)
![Password Revealed](https://github.com/user-attachments/assets/d1b25850-53ac-4091-8a1c-f3c3cead3e18)

---

## 🛠 Prerequisites

- **Administrator Access**: Required to run `netsh` commands with elevated permissions.
- **Command Prompt (CMD)**: Pre-installed on all Windows OS.
- **Target Network Profile Name**: Ensure that the profile name matches exactly with the Wi-Fi name stored on your device.

## 🚧 Troubleshooting

1. **Access Denied**:
   - Make sure to run CMD as Administrator.

2. **Profile Not Found**:
   - Check if the profile name is correct. Case sensitivity matters.

3. **No Password Displayed**:
   - The profile might not have a password or is not saved properly.

## 🤖 Automate with Batch Script

Create a batch file to automate the extraction process:
```batch
@echo off
echo Enter Wi-Fi profile name:
set /p profileName=
netsh wlan show profiles "%profileName%" key=clear | findstr /C:"Key Content"
pause
```

1. **Save as**: `WiFi_Password_Extractor.bat`
2. **Run as Administrator**.

![image](https://github.com/user-attachments/assets/9f117455-2280-4db7-b32c-2eaaec2ed852)



            linux_permissions.md

# Linux File Permissions and Values

Linux mein har file aur directory ke 3 basic permission types hotay hain:

1. **Read (r)** – File ko read kar sakte hain
2. **Write (w)** – File ko modify kar sakte hain
3. **Execute (x)** – File ya script ko run kar sakte hain

Har file 3 users ke liye alag permissions rakhti hai:

- **Owner**
- **Group**
- **Others**

## Permission Values

| Symbol | Binary | Decimal |
|--------|--------|---------|
| ---    | 000    | 0       |
| --x    | 001    | 1       |
| -w-    | 010    | 2       |
| -wx    | 011    | 3       |
| r--    | 100    | 4       |
| r-x    | 101    | 5       |
| rw-    | 110    | 6       |
| rwx    | 111    | 7       |

### Example: `chmod` Command

```bash
chmod 755 myfile.sh

Explanation:

7 = rwx (Owner)

5 = r-x (Group)

5 = r-x (Others)


Yani:

Owner can read, write, execute

Group can read and execute

Others can read and execute


Useful chmod Commands

chmod 777 file.txt  # sab ko full permissions
chmod 644 file.txt  # owner: rw-, others: r--
chmod 600 file.txt  # sirf owner read/write kar sakta hai
chmod +x script.sh  # file ko executable banata hai

Check Permissions

ls -l

Output ka format:

-rwxr-xr-- 1 fiza fiza 1234 May 15 12:00 script.sh

Iska matlab:

Owner: rwx

Group: r-x

Others: r--

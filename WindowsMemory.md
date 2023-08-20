Memory analysis
  
Windows crash dump
contains all the contents of the memory at the time of the crash 
It helps diagnosing and identifing bugs in a program that led to the system crash 
If we cannot see any trace of rootkit we can use analysis tools of RAM and we can find it inside RAM, it must reside there at the time althrough it could not be seen on other tools 

Examples of software used for RAM capturer is 

Belkasoft RAM capture 
AcessData FTK Imager 


Redline 
GUI interface for analyzing RAM memory, data can be analyzed from before by load data option 
It is a security tool to identify malicious activity through memory 

———————————————————

Windows registry 
Every action performed by the user is recored in WINDOWS REGISTRY 
Hence it is a good source of evidence during forensic investigation 

Windows registry is divided into HIVES: 
HKEY_USERS - all active loaded user profiles 
HKEY_CLASSES_ROOT - contains files about configuration information related to the applications, used for opening various files on the system 
HKEY_CURRENT_CONFIG - contains the hardware profile the system uses at the startup 
HKEY_LOCAL_MACHINE - this hive contains vast array of configuration information for the system, including hardware settings and software settings 
HKEY_CURRENT_USER - currently logged on user 

————————————————————

Examining Web browsers 
Cache, cookie and history analysis 

Google Chrome 
C:\Users\{user}\AppData\Local\Google\Chrome\User Data\Default
we can find there Cache folder or cookies file, history file 

C:\Users\{user}\AppData\Local\Google\Chrome\User Data\Default\Cache
contains Cache data on your machine from google chrome 

There is also a tool for reading Google Chrome Cache, cookie and history 
ChromeCacheView - reads google chrome cache 
ChromeCookiesView - reads and displays cookies 
ChromeHistoryView - reads and displays google history in GUI format 
There are information like: URL, number of times user visited the site… 
Almost the same goes for Mozilla Firefox or Microsoft Edge 

————————————————————

Windows Files and Metafata 
metadata 

date 
time 
user who opened file, took picture etc. 
gps location 

--------------------------

Windows File System Structure
C:
Boot, Logs, PerfLogs, ProgramFiles, ProgramFiles (x86), Program Data, Windows, Users, 

Users - Public, username
username - AppData
Windows - System, System32, SysWOW64, WinSxS

Boot = Hidden directory containing boot files
Logs = Stores event logs (Windows 10 > up)
PerfLogs = stores performance logs if enabled
Program Files = 64bit applications 
Program Files (x86) = 32bit applications (for backwards compatibility)
Program Data = Stores application data in several sub-directories
Users = stores user data in dedicated folders (another directory with users/user), 
Users/Public = directory that is shared between all users
Users/AppData = specific app data to that user
Windows = store all the operating system files
Windows/System = stores 16-bit DLL files
Windows/System32 = stores 64-bit DLL files

Notes from Cisco
The following lists the major directories of of the Windows file system:

Boot: A hidden directory that contains system boot files.
Logs: As of Windows 10, the directory where event logs are stored.
PerfLogs: Stores performance logs if this feature is enabled in the operating system.
Program files: In 64-bit Windows installations, stores 64-bit applications.
Program files (x86): In 64-bit Windows installations, stores 32-bit applications.
ProgramData: Directory used to store application-need data. Applications are not able to write directly to this directory, but they can create subdirectories used for their own purposes.
Users: Directory where users store their data. Each user with an account on the system has a folder that is dedicated to them. Users with standard account privileges are only able to access the data in their assigned directory. 
Public: This subdirectory of the Users directory can be shared among all the users of a system. Normally, Windows access controls do not allow users to access data in other users’ directories. However, the public directory allows anyone on the system to store data, making it ideal for sharing data among users. 
<username>: All users with accounts on a Windows host are given areas for their use. The area for each user resides under the Users directory and bears the name of an individual user’s account. This area allows users to privately store their documents and other data since other users are permitted access to their own directory only. Each user’s directory includes a subdirectory that is called AppData. This location is used by applications that need to store things specific to a user, for example a user’s browsing history.
Windows: The directory that stores the operating system and its various subsystems. 
System: This directory is used to store 16-bit system dynamic link library (DLL) files. In 64-bit Windows installations, this directory is normally empty.
System32: This directory is used to store 64-bit system DLL files in 64-bit Windows installations. 
SysWOW64: 64-bit Windows is backward compatible with 32-bit applications. This directory stores 32-bit system DLL files.
WinSxS: This directory stores copies of system DLL files. Often, these files represent older versions of the DLL files that may be required by older applications. The folder name stands for Windows side by side because it allows older applications to co-exist with newer ones that require the most current DLL files.
Windows/SysWoW32 = stores 32-bit DLL files
Windows/WinSxS = Stores copies of system DLL files



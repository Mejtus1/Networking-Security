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
Windows/SysWoW32 = stores 32-bit DLL files
Windows/WinSxS = Stores copies of system DLL files



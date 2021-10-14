
# Android’s architecture
Android is an open source, Linux-based software stack created for a wide array of devices and form factors. The following diagram shows the major components of the Android platform.
 
 ![Android Structure](https://developer.android.com/guide/platform/images/android-stack_2x.png)
 
 
# Hardware Abstraction Layer (HAL)
The hardware abstraction layer (HAL) provides standard interfaces that expose device hardware capabilities to the higher-level Java API framework. The HAL consists of multiple library modules, each of which implements an interface for a specific type of hardware component, such as the camera or bluetooth module. When a framework API makes a call to access device hardware, the Android system loads the library module for that hardware component. 
 
# Android Runtime

For devices running Android version 5.0 (API level 21) or higher, each app runs in its own process and with its own instance of the Android Runtime (ART). ART is written to run multiple virtual machines on low-memory devices by executing DEX files, a bytecode format designed specially for Android that's optimized for minimal memory footprint. Build tools, such as d8, compile Java sources into DEX bytecode, which can run on the Android platform.

## Some of the major features of ART include the following:

     * Ahead-of-time (AOT) and just-in-time (JIT) compilation
    * Optimized garbage collection (GC)
    * On Android 9 (API level 28) and higher, conversion of an app package's Dalvik Executable format (DEX) files to more compact machine code.
    * Better debugging support, including a dedicated sampling profiler, detailed diagnostic exceptions and crash reporting, and the ability to set watchpoints to monitor specific fields

Prior to Android version 5.0 (API level 21), Dalvik was the Android runtime. If your app runs well on ART, then it should work on Dalvik as well, but the reverse may not be true.

Android also includes a set of core runtime libraries that provide most of the functionality of the Java programming language, including some Java 8 language features, that the Java API framework uses. 


Ref: https://developer.android.com/guide/platform#linux-kernel

# Dalvik VM

1. Dalvik VM is a (register based) android virtual machine optimized for mobile devices.Dalvik was designed with mobile devices in mind and cannot run Java bytecode (.class files) directly.Its native input format is called Dalvik Executable (DEX) and is packaged in .dex files. In turn, .dex files are packaged either inside system Java libraries (JAR files), or inside Android applications. 

![Compiling and linking](https://static.javatpoint.com/images/androidimages/flow.jpg)

Note: Dalvik and Oracle’s JVM have different architectures—register-based in Dalvik versus stack-based in the JVM.Register-based models are good at optimizing and running on low memory. They can store common sub-expression results which can be used again in the future. This is not possible in a Stack-based model at all. Dalvik Virtual Machine uses its own byte-code and runs “.dex”(Dalvik Executable File) file.

## Advantages

    DVM supports the Android operating system only.
    In DVM executable is APK.
    Execution is faster.
    From Android 2.2 SDK Dalvik has it’s own JIT (Just In Time) compiler.
    DVM has been designed so that a device can run multiple instances of the Virtual Machine effectively.
    Applications are given their own instances.

## Disadvantages

    DVM supports only Android Operating System.
    For DVM very few Re-Tools are available.
    Requires more instructions than register machines to implement the same high-level code.
    App Installation takes more time due to dex.
    More internal storage is required.
    
Ref: https://www.geeksforgeeks.org/what-is-dvmdalvik-virtual-machine/
    
# Java Runtime Environment (JRE) 
   The Java Runtime Environment (JRE) provides the libraries, the Java Virtual Machine, and other components to run applets and applications written in the Java programming language. In addition, two key deployment technologies are part of the JRE: Java Plug-in, which enables applets to run in popular browsers; and Java Web Start, which deploys standalone applications over a network. It is also the foundation for the technologies in the Java 2 Platform, Enterprise Edition (J2EE) for enterprise software development and deployment. The JRE does not contain tools and utilities such as compilers or debuggers for developing applets and applications.
   
   
# Java Development Kit (JDK)

The JDK is a superset of the JRE, and contains everything that is in the JRE, plus tools such as the compilers and debuggers necessary for developing applets and applications.
   
    
    Ref: https://stackoverflow.com/questions/11547458/what-is-the-difference-between-jvm-jdk-jre-openjdk
    
    
#  Java Native Interface (JNI) 
JNI is the Java Native Interface. It defines a way for the bytecode that Android compiles from managed code (written in the Java or Kotlin programming languages) to interact with native code (written in C/C++). JNI is vendor-neutral, has support for loading code from dynamic shared libraries, and while cumbersome at times is reasonably efficient.

Ref: https://developer.android.com/training/articles/perf-jni


# Inter-Process Communication (IPC)
Android is a unix like system that have separate address spaces and a process cannot directly access another process's memory (called process isolation).However, if a process wants to offer some useful service(s) to other processes, it needs to provide some mechanism that allows other processes to discover and interact with those services. That mechanism is referred to as IPC.These include files, signals, sockets, pipes, semaphores, shared memory, message queues, and so on. While Android uses some of these (such as local sockets), it does not support others (namely System VIPCs like semaphores, shared memory segments, and message queues)

For Andoid we have few of the below IPC mechanisms
1) Intents: These are messages which components can send and receive. It is a universal mechanism of passing data between processes. With help of the intents one can start services or activities, invoke broadcast receivers and so on.

2) Bundles: These are entities of data that is passed through. It is similar to the serialization of an object, but much faster on android. Bundle can be read from intent via the getExtras() method.

3) Binders: These are the entities which allow activities and services to obtain a reference to another service. It allows not simply sending messages to services but directly invoking methods on them.
4) ASHMEM (Anonymous Shared Memory) : The main difference between Linux shared memory and this shared memory is, in Linux other processes can't free the shared memory but here if other processes require memory this memory can be freed by Android OS.

Ref: https://stackoverflow.com/questions/5740324/what-are-the-ipc-mechanisms-available-in-the-android-os/35450853


# Android Framework Libraries
Android framework libraries, sometimes calledjust “the framework.” The framework includes all Java libraries that are not part of the standard Java runtime (java.*, javax.*, and so on) and is for the most part hosted under the android top-level package. The framework includes the basic blocks for building Android applications, such as the base classes for activities, services, and content providers (in the android.app.*packages); GUI widgets (in the android.view.* and android.widget packages);and classes for file and database access (mostly in the android.database.* and
android.content.* packages). It also includes classes that let you interact with device hardware, as well as classes that take advantage of higher-level services offered by the system.

# System Apps
System apps are included in the OS image, which is read-only on production devices (typically mounted as /system), and cannot be uninstalled or changed by users. Therefore, these apps are considered secure and are given many more privileges than user-installed apps. System apps can be part of the core Android OS or can simply be preinstalled user applications, such as email clients or browsers. While all apps installed under /system were treated equally in earlier versions of Android (except by OS features that check the app signing certificate), Android 4.4 and higher treat apps installed in /system/priv-app/ as privileged applications and will only grant permissions with protection level signature Or System to privileged apps, not to all apps installed under /system. Apps that are signed with the platform signing key can be granted system permissions with the signature protection level, and thus can get OS-level privileges even if they are not preinstalled under /system.While system apps cannot be uninstalled or changed, they can be updated by users as long as the updates are signed with the same private key, and some can be overridden by user-installed apps. For example, a user can choose to replace the preinstalled application launcher or input method with a third-party application.

# User-Installed Apps 
User-installed apps are installed on a dedicated read-write partition (typically mounted as /data) that hosts user data and can be uninstalled at will. Each application lives in a dedicated security sandbox and typically cannot affect other applications or access their data

# Android’s security model
Android automatically assigns a unique UID/app ID to each applications at installations and executes that application in a dedicated process running as that UID.Thus they are said to be _sandboxed_ or _isolated_,both at the process level
(by having each run in a dedicated process) and at the file level (by having a private data directory). This creates a kernel-level application sandbox, which applies to all applications, regardless of whether they are executed in a native or virtual machine process.

Android does not have the traditional /etc/password file and its system UIDs are statically defined in the android_filesystem_config.h header file.UIDs for system services start from 1000, with 1000 being the system (AID_SYSTEM) user, which has special (but still limited) privileges.Automatically generated UIDs for applications start at 10000 (AID_APP), and the corresponding usernames are in the form app_XXX or uY_aXXX (on Android versions that support multiple physical users), where XXX is the offset from AID_APP and Y is the Android user ID (not the same as UID). 
**Application UIDs are managed alongside other package metadata in the /data/system/packages.xml file (the canonical source) and also written to the /data/system/packages.list file**

**Applications can be installed using the same UID, called a shared user ID, in which case they can share files and even run in the same process. Shared user IDs are used extensively by system applications, which often need to use the same resources across different packages for modularity. **

Note: While the shared user ID facility is not recommended for non-system apps, it’s available to third-party applications as well. In order to share the same UID, applications need to be signed by the same code signing key. Additionally, because adding a shared user ID to a new version of an installed app causes it to change its UID, the system disallows this. Therefore, a shared user ID cannot be added retroactively, and apps need to be designed to work with a shared ID from the start.

##### Android Permissions 


# Android Multi-User Support
Each user is assigned a unique user ID, starting with 0, and users are given their own dedicated data directory under /data/system/users/<user ID>/, which is called the user’s system directory. This directory hosts user-specific settings such as homescreen parameters, account data, and a list of currently installed applications. While application binaries are shared between users, each user gets a copy of an application’s data directory. To distinguish applications installed for each user, Android assigns a new effective UID to each application when it is installed for a particular user. This effective UID is based on the target physical user’s user ID and the app’s UID in a single-user system (the app ID). This composite structure of the granted UID guarantees that even if the same application is installed by two different users, both application instances get their own sandbox.
The user to first initialize the device is called the device owner, and only they can manage other users or perform administrative tasks that influence the whole device (such as factory reset).

# Android SE-Linux Feature

Android uses Security-Enhanced Linux (SELinux) to enforce mandatory access control (MAC) over all processes, even processes running with root/superuser privileges (Linux capabilities). 
With SELinux, Android can better protect and confine system services, control access to application data and system logs, reduce the effects of malicious software, and protect users from potential flaws in code on mobile devices.
SELinux operates on the principle of default denial: Anything not explicitly allowed is denied. SELinux can operate in two global modes:
    * Permissive mode, in which permission denials are logged but not enforced.
    * Enforcing mode, in which permissions denials are both logged and enforced.
Android includes SELinux in enforcing mode and a corresponding security policy that works by default across AOSP. In enforcing mode, disallowed actions are prevented and all attempted violations are logged by the kernel to dmesg and logcat
 
 Ref: https://source.android.com/security/selinux
 
 # Android Package
 
 # APK
 
 APK : typically a zip/jar archieve (MIME type: application/vnd.android.package-archive)
 
 
 '''
 apk/
|-- AndroidManifest.xml
|-- classes.dex
|-- resources.arsc:packages all of the application’s compiled resources such as strings and styles
|-- assets/x
|-- lib/y
| |-- armeabi/
| | `-- libapp.so
| `-- armeabi-v7a/
| `-- libapp.so
|-- META-INF/z
| |-- CERT.RSA
| |-- CERT.SF
| `-- MANIFEST.MF: package manifest file and code signatures
`-- res/{
|-- anim/
|-- color/
|-- drawable/
|-- layout/
|-- menu/
|-- raw/
`-- xml/
 '''

 Note: Downloading app directly from some source and installing them is known as **sideloading ** of apps.
 Note: Usually system apps are located in /system/app while /system/priv-app holds privleged apps granted with permisson,likewise /system/vendor/app hosts vendor specific applications.User installed apps are located at /data/app.The userdata partition also hosts the optimized DEX files for user-installed applications (in /data/dalvik-cache/), the system package database (in /data/system/packages .xml), and other system databases and settings files.
 
 # Signature Verification
The first step is to check whether the new package has been signed by the same set of signers as the existing one. This rule is referred to as same origin policy, or Trust On First Use (TOFU). This signature check guarantees that the update is produced by the same entity as the original application (assuming that the signing key has not been compromised) and establishes a trust relationship between the update and the existing application.
 
 # Encrypted APKs
 Encrypted APKs can be installed using the Google Play Store client, or with the pm command from the Android shell, but the system PackageInstaller does not support encrypted APKs.
adb install [-l] [-r] [-s] [--algo <algorithm name> --key <hex-encoded key> --iv <hex-encoded iv>] <file>
 
Note: SDCard uses FAT file system which lacks permission.So encrypted apks are stored using mounted using Android Secure External Caches, or ASEC containers.  ASEC container management (creating, deleting, mounting, and unmounting) is implemented in the system volume daemon (vold), and the MountService provides an interface to its functionality to framework services. 
 '''
 # ls -l /mnt/asec/com.example.app-1
drwxr-xr-x system system lib
drwx------ root root lost+found
-rw-r----- system u0_a96 1319057 pkg.apk
-rw-r--r-- system system 526091 res.zip
 '''
Here, the res.zip holds app resources and the manifest file and is world readable, while the pkg.apk file that holds the full APK is only readable by the system and the app’s dedicated user (u0_a96). The actual app containers are stored in /data/app-asec/ in files with the .asec extension.

 
 # Foward Locking Mechanism
To prevent users from simply copying paid apps from the SD card, Android 2.2 created an encrypted filesystem image file and stored the APK in it when a user opted to move an app to external storage. The system would then create a mount point for the encrypted image, and mount it using Linux’s device-mapper. Android loaded each app’s files from its
mount point at runtime. Android 4.1 built on this idea by making the container use the ext4 filesystem, which allows for file permissions
 '''
 # ls -l /mnt/asec/com.example.app-1
drwxr-xr-x system system lib
drwx------ root root lost+found
-rw-r----- system u0_a96 1319057 pkg.apk
-rw-r--r-- system system 526091 res.zip
 '''
 We can also use the vdc command-line utility to interact with vold in order to manage forward-locked apps from Android’s shell.
 ''' 
 # vdc asec listu
vdc asec list
111 0 com.example.app-1
111 0 org.foo.app-1
200 0 asec operation succeeded
# vdc asec path com.example.app-1v
vdc asec path com.example.app-1
211 0 /mnt/asec/com.example.app-1
 '''
 # Android User MetaData
 '''
 Android stores user data in the /data/system/users/ directory that hosts
metadata about users in XML format, as well as user directories. On a
device with five users, its contents may look like Listing
# ls -lF /data/system/users
drwx------ system system 0u
-rw------- system system 230 0.xmlv
drwx------ system system 10
-rw------- system system 245 10.xml
 '''


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
Android is a unix like system that have separate address spaces and a process cannot directly access another process's memory (called process isolation).However, if a process wants to offer some useful service(s) to other processes, it needs to provide some mechanism that allows other processes to discover and interact with those services. That mechanism is referred to as IPC.

For Andoid we have below IPC mechanisms
1) Intents: These are messages which components can send and receive. It is a universal mechanism of passing data between processes. With help of the intents one can start services or activities, invoke broadcast receivers and so on.

2) Bundles: These are entities of data that is passed through. It is similar to the serialization of an object, but much faster on android. Bundle can be read from intent via the getExtras() method.

3) Binders: These are the entities which allow activities and services to obtain a reference to another service. It allows not simply sending messages to services but directly invoking methods on them.
4) ASHMEM (Anonymous Shared Memory) : The main difference between Linux shared memory and this shared memory is, in Linux other processes can't free the shared memory but here if other processes require memory this memory can be freed by Android OS.

Ref: https://stackoverflow.com/questions/5740324/what-are-the-ipc-mechanisms-available-in-the-android-os/35450853






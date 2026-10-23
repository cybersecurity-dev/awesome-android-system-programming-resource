<div align="center">
    <p align="center">
        <a href="https://github.com/cybersecurity-dev/awesome-android-system-programming">
          <img width="35%" src="https://github.com/cybersecurity-dev/cybersecurity-dev/blob/main/assets/Android.svg" />
        </a>
    </p>

```mermaid
flowchart LR
    A(["Select<br/>system<br/>topic"])
    B["Study<br/>Android<br/>architecture"]
    C["Define<br/>component<br/>interfaces"]
    D{"Implementation<br/>level?"}

    E["Application<br/>Framework<br/>Kotlin or Java"]
    F["Native Layer<br/>C or C++ with<br/>NDK"]
    G["System Layer<br/>AIDL, HAL or<br/>native service"]

    H["Build with<br/>Gradle or CMake"]
    I["Deploy using<br/>ADB"]
    J["Execute test<br/>cases"]

    K{"Expected behavior?"}
    L["Collect logs<br/>and<br/>traces"]
    M["Analyze process, IPC,<br/>memory, CPU and I/O"]
    N["Fix<br/>implementation"]
    O["Security<br/>validation"]
    P["Performance<br/>evaluation"]
    Q["Document<br/>architecture<br/>and experimental results"]
    R(["Complete<br/>laboratory"])

    A --> B --> C --> D

    D -->|"High level"| E
    D -->|"Native<br/>library"| F
    D -->|"Platform<br/>integration"| G

    E --> H
    F --> H
    G --> H

    H --> I --> J --> K

    K -->|"No"| L
    L --> M
    M --> N
    N --> H

    K -->|"Yes"| O
    O --> P
    P --> Q
    Q --> R

    classDef terminal fill:#263238,color:#fff,stroke:#111,stroke-width:3px
    classDef activity fill:#e3f2fd,color:#111,stroke:#1e88e5
    classDef decision fill:#fff3e0,color:#111,stroke:#fb8c00,stroke-width:2px
    classDef implementation fill:#e8f5e9,color:#111,stroke:#43a047
    classDef evaluation fill:#f3e5f5,color:#111,stroke:#8e24aa

    class A,R terminal
    class B,C,H,I,J,L,M,N,Q activity
    class D,K decision
    class E,F,G implementation
    class O,P evaluation
```

# **`Awesome`** Android System Programming Resource [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
</div>

[![Windows](https://custom-icon-badges.demolab.com/badge/Windows-0078D6?style=for-the-badge&logo=windows11&logoColor=white)]()
[![YouTube](https://img.shields.io/badge/YouTube-%23FF0000.svg?style=for-the-badge&logo=YouTube&logoColor=white)]() 
[![Reddit](https://img.shields.io/badge/Reddit-FF4500?style=for-the-badge&logo=reddit&logoColor=white)](https://www.reddit.com/r/androiddev/new/)

<p align="center">
    <a href="https://github.com/cybersecurity-dev/"><img height="25" src="https://github.com/cybersecurity-dev/cybersecurity-dev/blob/main/assets/github.svg" alt="GitHub"></a>
    &nbsp;
    <a href="https://www.youtube.com/@CyberThreatDefense"><img height="25" src="https://github.com/cybersecurity-dev/cybersecurity-dev/blob/main/assets/youtube.svg" alt="YouTube"></a>
    &nbsp;
    <a href="https://cyberthreatdefence.com/my_awesome_lists"><img height="20" src="https://github.com/cybersecurity-dev/cybersecurity-dev/blob/main/assets/blog.svg" alt="My Awesome Lists"></a>
    <img src="https://github.com/cybersecurity-dev/cybersecurity-dev/blob/main/assets/bar.gif">
</p>

```mermaid
flowchart TB
    subgraph APPS["Application Layer"]
        SYSTEMAPP["System Applications"]
        USERAPP["User Applications"]
    end

    subgraph FRAMEWORK["Java API Framework"]
        AMS["Activity Manager"]
        PMS["Package Manager"]
        WMS["Window Manager"]
        NMS["Notification Manager"]
        CMS["Connectivity Manager"]
    end

    subgraph RUNTIME["Android Runtime"]
        ART["ART"]
        CORE["Core Libraries"]
        GC["Garbage Collector"]
    end

    subgraph NATIVE["Native C/C++ Layer"]
        BINDER["Binder Driver Interface"]
        SURFACE["SurfaceFlinger"]
        MEDIA["Media Framework"]
        SQLITE["SQLite"]
        SSL["TLS/Cryptography"]
    end

    subgraph HAL["Hardware Abstraction Layer"]
        CAMERA["Camera HAL"]
        AUDIO["Audio HAL"]
        SENSOR["Sensor HAL"]
        WIFI["Wi-Fi HAL"]
        BLUETOOTH["Bluetooth HAL"]
    end

    subgraph KERNEL["Linux Kernel"]
        PROC["Process Management"]
        MEMORY["Memory Management"]
        NETWORK["Networking"]
        SELINUX["SELinux"]
        DRIVERS["Device Drivers"]
        POWER["Power Management"]
    end

    subgraph HARDWARE["Physical Hardware"]
        CPU["CPU/GPU"]
        STORAGE["Storage"]
        RADIO["Radio"]
        DEVICES["Camera, Sensors and Audio"]
    end

    SYSTEMAPP --> FRAMEWORK
    USERAPP --> FRAMEWORK

    FRAMEWORK <-->|"Binder IPC"| BINDER
    FRAMEWORK --> RUNTIME
    RUNTIME --> NATIVE

    AMS --> BINDER
    PMS --> BINDER
    WMS --> SURFACE
    CMS --> NETWORK

    NATIVE --> HAL
    HAL --> KERNEL
    KERNEL --> HARDWARE

    CAMERA --> DRIVERS
    AUDIO --> DRIVERS
    SENSOR --> DRIVERS
    WIFI --> NETWORK
    BLUETOOTH --> NETWORK

    SELINUX -.->|"Access control"| FRAMEWORK
    SELINUX -.->|"Access control"| NATIVE

    classDef app fill:#e3f2fd,color:#111,stroke:#1e88e5
    classDef framework fill:#e8f5e9,color:#111,stroke:#43a047
    classDef runtime fill:#fff8e1,color:#111,stroke:#f9a825
    classDef native fill:#fff3e0,color:#111,stroke:#ef6c00
    classDef hal fill:#f3e5f5,color:#111,stroke:#8e24aa
    classDef kernel fill:#ffebee,color:#111,stroke:#e53935
    classDef hardware fill:#eceff1,color:#111,stroke:#546e7a

    class SYSTEMAPP,USERAPP app
    class AMS,PMS,WMS,NMS,CMS framework
    class ART,CORE,GC runtime
    class BINDER,SURFACE,MEDIA,SQLITE,SSL native
    class CAMERA,AUDIO,SENSOR,WIFI,BLUETOOTH hal
    class PROC,MEMORY,NETWORK,SELINUX,DRIVERS,POWER kernel
    class CPU,STORAGE,RADIO,DEVICES hardware
```

## 📖 Contents
- [Books](#books)
- [Videos](#videos)
- [My Other Awesome Lists](#my-other-awesome-lists)
- [Contributing](#contributing)
- [Contributors](#contributors)

##

### Books
- [Androids: The Team that Built the Android Operating System](https://www.amazon.com/Androids-Built-Android-Operating-System-ebook/dp/B09QPMNWS5)
- [Android System Programming: Porting, customizing, and debugging Android HAL](https://www.amazon.com/Android-System-Programming-customizing-debugging-ebook/dp/B072M68RN9)
- [Inside the Android OS: Building, Customizing, Managing and Operating Android System Services (Android Deep Dive)](https://www.amazon.com/Inside-Android-OS-Customizing-Operating-ebook/dp/B08F5J141P)
- [Android Security Internals: An In-Depth Guide to Android's Security Architecture](https://www.amazon.com/Android-Security-Internals-Depth-Architecture/dp/1593275811)

### Videos


##

### My Other Awesome Lists
You can access the my other awesome lists [here](https://cyberthreatdefence.com/my_awesome_lists)

### Contributing
[Contributions of any kind welcome, just follow the guidelines](contributing.md)!

### Contributors
[Thanks goes to these contributors](https://github.com/cybersecurity-dev/awesome-android-system-programming-resource/graphs/contributors)!

### License
[![CC0](http://mirrors.creativecommons.org/presskit/buttons/88x31/svg/cc-zero.svg)](http://creativecommons.org/publicdomain/zero/1.0)

[🔼 Back to top](#awesome-android-system-programming-resource-)

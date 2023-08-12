---
tip: translate by openai@2023-08-12 14:09:12
url: [Filesystem Hierarchy Standard --- 文件系统层次结构标准](https://www.pathname.com/fhs/)
[Filesystem Hierarchy Standard](https://www.pathname.com/fhs/pub/fhs-2.3.html)
---

-Fil
Filesystem Hierarchy Standard
Filesystem Hierarchy Standard Group

Edited by
Rusty Russell
Daniel Quinlan
Christopher Yeoh

Copyright © 1994-2004 Daniel Quinlan
Copyright © 2001-2004 Paul 'Rusty' Russell
Copyright © 2003-2004 Christopher Yeoh

This standard consists of a set of requirements and guidelines for file and directory placement under UNIX-like operating systems. The guidelines are intended to support interoperability of applications, system administration tools, development tools, and scripts as well as greater uniformity of documentation for these systems.

> 该标准由一组在类UNIX操作系统下放置文件和目录的要求和指南组成。该指南旨在支持应用程序、系统管理工具、开发工具和脚本的互操作性，以及这些系统文档的更大统一性。

All trademarks and copyrights are owned by their owners, unless specifically noted otherwise. Use of a term in this document should not be regarded as affecting the validity of any trademark or service mark.

> 除非另有特别说明，否则所有商标和版权均归其所有者所有。本文件中使用的术语不应被视为影响任何商标或服务商标的有效性。

Permission is granted to make and distribute verbatim copies of this standard provided the copyright and this permission notice are preserved on all copies.

> 如果版权和本许可声明保留在所有副本上，则允许制作和分发本标准的逐字复制品。

Permission is granted to copy and distribute modified versions of this standard under the conditions for verbatim copying, provided also that the title page is labeled as modified including a reference to the original standard, provided that information on retrieving the original standard is included, and provided that the entire resulting derived work is distributed under the terms of a permission notice identical to this one.

> 允许在逐字复制的条件下复制和分发本标准的修改版本，前提是标题页被标记为已修改，包括对原始标准的引用，前提是包括检索原始标准的信息，并且前提是，所产生的整个衍生作品是根据与该作品相同的许可通知条款分发的。

Permission is granted to copy and distribute translations of this standard into another language, under the above conditions for modified versions, except that this permission notice may be stated in a translation approved by the copyright holder.

> 在上述修改版本的条件下，允许将本标准的翻译复制和分发为另一种语言，但版权持有人批准的翻译中可能会说明本许可通知的情况除外。

------------------------------------------------------------------------

Table of Contents 1. Introduction

    Purpose
    Conventions

2.  The Filesystem

3.  The Root Filesystem

    Purpose Requirements Specific Options /bin : Essential user command binaries (for use by all users)

> 用途需求特定选项/bin：基本用户命令二进制文件（供所有用户使用）

         Purpose
         Requirements
         Specific Options

    /boot : Static files of the boot loader

         Purpose
         Specific Options

    /dev : Device files

         Purpose
         Specific Options

    /etc : Host-specific system configuration

         Purpose
         Requirements
         Specific Options
         /etc/opt : Configuration files for /opt
         /etc/X11 : Configuration for the X Window System (optional)
         /etc/sgml : Configuration files for SGML (optional)
         /etc/xml : Configuration files for XML (optional)

    /home : User home directories (optional)

         Purpose
         Requirements

    /lib : Essential shared libraries and kernel modules

         Purpose
         Requirements
         Specific Options

    /lib`<qual>`{=html} : Alternate format essential shared libraries (optional)

> /lib`<qual>`{=html}：备用格式基本共享库（可选）

         Purpose
         Requirements

    /media : Mount point for removeable media

         Purpose
         Specific Options

    /mnt : Mount point for a temporarily mounted filesystem

         Purpose

    /opt : Add-on application software packages

         Purpose
         Requirements

    /root : Home directory for the root user (optional)

         Purpose

    /sbin : System binaries

         Purpose
         Requirements
         Specific Options

    /srv : Data for services provided by this system

         Purpose

    /tmp : Temporary files

         Purpose

4.  The /usr Hierarchy

    Purpose Requirements Specific Options /usr/X11R6 : X Window System, Version 11 Release 6 (optional)

> 用途要求特定选项/usr/X11R6:X Window System，版本11 Release 6（可选）

         Purpose
         Specific Options

    /usr/bin : Most user commands

         Purpose
         Specific Options

    /usr/include : Directory for standard include files.

         Purpose
         Specific Options

    /usr/lib : Libraries for programming and packages

         Purpose
         Specific Options

    /usr/lib`<qual>`{=html} : Alternate format libraries (optional)

         Purpose
         /usr/local : Local hierarchy

    /usr/local/share /usr/sbin : Non-essential standard system binaries

         Purpose

    /usr/share : Architecture-independent data

         Purpose
         Requirements
         Specific Options
         /usr/share/dict : Word lists (optional)
         /usr/share/man : Manual pages
         /usr/share/misc : Miscellaneous architecture-independent data
         /usr/share/sgml : SGML data (optional)
         /usr/share/xml : XML data (optional)

    /usr/src : Source code (optional)

         Purpose

5.  The /var Hierarchy

    Purpose Requirements Specific Options /var/account : Process accounting logs (optional)

> 用途要求特定选项/var/account：处理会计日志（可选）

         Purpose

    /var/cache : Application cache data

         Purpose
         Specific Options
         /var/cache/fonts : Locally-generated fonts (optional)
         /var/cache/man : Locally-formatted manual pages (optional)

    /var/crash : System crash dumps (optional)

         Purpose

    /var/games : Variable game data (optional)

         Purpose

    /var/lib : Variable state information

         Purpose
         Requirements
         Specific Options
         /var/lib/<editor> : Editor backup files and state (optional)
         /var/lib/hwclock : State directory for hwclock (optional)
         /var/lib/misc : Miscellaneous variable data

    /var/lock : Lock files

         Purpose

    /var/log : Log files and directories

         Purpose
         Specific Options

    /var/mail : User mailbox files (optional)

         Purpose

    /var/opt : Variable data for /opt

         Purpose

    /var/run : Run-time variable data

         Purpose
         Requirements

    /var/spool : Application spool data

         Purpose
         Specific Options
         /var/spool/lpd : Line-printer daemon print queues (optional)
         /var/spool/rwho : Rwhod files (optional)

    /var/tmp : Temporary files preserved between system reboots

         Purpose

    /var/yp : Network Information Service (NIS) database files (optional)

         Purpose

6.  Operating System Specific Annex

    Linux

         / : Root directory
         /bin : Essential user command binaries (for use by all users)
         /dev : Devices and special files
         /etc : Host-specific system configuration
         /lib64 and /lib32 : 64/32-bit libraries (architecture dependent)
         /proc : Kernel and process information virtual filesystem
         /sbin : Essential system binaries
         /usr/include : Header files included by C programs
         /usr/src : Source code
         /var/spool/cron : cron and at jobs

7.  Appendix

    The FHS mailing list Background of the FHS General Guidelines Scope Acknowledgments Contributors

> FHS邮件列表FHS通用指南背景范围致谢贡献者

------------------------------------------------------------------------

Chapter 1. Introduction

Purpose

This standard enables:

-   Software to predict the location of installed files and directories, and
-   Users to predict the location of installed files and directories.

We do this by:

-   Specifying guiding principles for each area of the filesystem,
-   Specifying the minimum files and directories required,
-   Enumerating exceptions to the principles, and
-   Enumerating specific cases where there has been historical conflict.

The FHS document is used by:

-   Independent software suppliers to create applications which are FHS compliant, and work with distributions which are FHS complaint,

> -独立软件供应商创建符合FHS的应用程序，并与FHS投诉的发行版合作，
-   OS creators to provide systems which are FHS compliant, and
-   Users to understand and maintain the FHS compliance of a system.

The FHS document has a limited scope:

-   Local placement of local files is a local issue, so FHS does not attempt to usurp system administrators.

> -本地文件的本地放置是一个本地问题，因此FHS不会试图篡夺系统管理员。

-   FHS addresses issues where file placements need to be coordinated between multiple parties such as local sites, distributions, applications, documentation, etc.

> -FHS解决了需要在多方之间协调文件放置的问题，如本地站点、分发、应用程序、文档等。

------------------------------------------------------------------------

Conventions

We recommend that you read a typeset version of this document rather than the plain text version. In the typeset version, the names of files and directories are displayed in a constant-width font.

> 我们建议您阅读本文档的排版版本，而不是纯文本版本。在排版版本中，文件和目录的名称以等宽字体显示。

Components of filenames that vary are represented by a description of the contents enclosed in "\<" and "\>" characters, `<thus>`{=html}. Electronic mail addresses are also enclosed in "\<" and "\>" but are shown in the usual typeface.

> 不同文件名的组成部分由包含在“\<”和“\>”字符中的内容描述表示，`<因此>`{=html}。电子邮件地址也用“\<”和“\>”括起来，但用通常的字体显示。

Optional components of filenames are enclosed in "\[" and "\]" characters and may be combined with the "\<" and "\>" convention. For example, if a filename is allowed to occur either with or without an extension, it might be represented by `<filename>`{=html}\[.`<extension>`{=html}\].

> 文件名的可选组成部分用“\[”和“\]”字符括起来，可以与“\<”和“\\>”约定组合使用。例如，如果允许一个文件名出现在有扩展名或没有扩展名的情况下，则它可能由`<filename>`{=html}\[.`<extension>`{=html}\]表示。

Variable substrings of directory names and filenames are indicated by "\*".

> 目录名和文件名的可变子字符串由“\*”表示。

The sections of the text marked as Rationale are explanatory and are non-normative.

> 文本中标记为“理由”的部分是解释性的，非规范性的。

------------------------------------------------------------------------

Chapter 2. The Filesystem

This standard assumes that the operating system underlying an FHS-compliant file system supports the same basic security features found in most UNIX filesystems.

> 本标准假定FHS兼容文件系统的操作系统支持大多数UNIX文件系统中相同的基本安全功能。

It is possible to define two independent distinctions among files: shareable vs. unshareable and variable vs. static. In general, files that differ in either of these respects should be located in different directories. This makes it easy to store files with different usage characteristics on different filesystems.

> 可以在文件之间定义两个独立的区别：可共享的与不可共享的以及可变的与静态的。通常，在这两个方面不同的文件应该位于不同的目录中。这样就可以很容易地将具有不同使用特性的文件存储在不同的文件系统中。

"Shareable" files are those that can be stored on one host and used on others. "Unshareable" files are those that are not shareable. For example, the files in user home directories are shareable whereas device lock files are not.

> “可共享”文件是指可以存储在一台主机上并在其他主机上使用的文件。“不可共享”文件是指不可共享的文件。例如，用户主目录中的文件是可共享的，而设备锁定文件则不是。

"Static" files include binaries, libraries, documentation files and other files that do not change without system administrator intervention. "Variable" files are files that are not static.

> “静态”文件包括二进制文件、库、文档文件和其他在没有系统管理员干预的情况下不会更改的文件。“变量”文件是非静态的文件。

    Rationale: Shareable files can be stored on one host and used on several

> 理由：可共享文件可以存储在一台主机上，也可以在多台主机上使用

    others. Typically, however, not all files in the filesystem hierarchy are

> 其他。但是，通常情况下，并非文件系统层次结构中的所有文件都是

    shareable and so each system has local storage containing at least its

> 可共享，因此每个系统都有本地存储，至少包含其

    unshareable files. It is convenient if all the files a system requires that

> 不可共享的文件。如果系统需要的所有文件

    are stored on a foreign host can be made available by mounting one or a few

> 存储在外部主机上的可以通过安装一个或几个
    directories from the foreign host.

    Static and variable files should be segregated because static files, unlike

> 静态文件和变量文件应该隔离，因为静态文件与

    variable files, can be stored on read-only media and do not need to be

> 变量文件，可以存储在只读介质上，不需要
    backed up on the same schedule as variable files.

    Historical UNIX-like filesystem hierarchies contained both static and

    variable files under both /usr and /etc. In order to realize the advantages

> /usr和/etc下的变量文件。为了实现优势

    mentioned above, the /var hierarchy was created and all variable files were

> 如上所述，创建了/var/层次结构，并将所有变量文件
    transferred from /usr to /var. Consequently /usr can now be mounted
    read-only (if it is a separate filesystem). Variable files have been
    transferred from /etc to /var over a longer period as technology has
    permitted.

    Here is an example of a FHS-compliant system. (Other FHS-compliant layouts

> 以下是一个符合FHS的系统示例。（其他符合FHS的布局
    are possible.)

    +------------------------------------+
    |        |   shareable   |unshareable|
    |--------+---------------+-----------|
    |static  |/usr           |/etc       |
    |--------+---------------+-----------|
    |        |/opt           |/boot      |
    |--------+---------------+-----------|
    |variable|/var/mail      |/var/run   |
    |--------+---------------+-----------|
    |        |/var/spool/news|/var/lock  |
    +------------------------------------+

------------------------------------------------------------------------

Chapter 3. The Root Filesystem

Purpose

The contents of the root filesystem must be adequate to boot, restore, recover, and/or repair the system.

> 根文件系统的内容必须足以引导、恢复、恢复和/或修复系统。

-   To boot a system, enough must be present on the root partition to mount other filesystems. This includes utilities, configuration, boot loader information, and other essential start-up data. /usr, /opt, and /var are designed such that they may be located on other partitions or filesystems.

> -要启动系统，根分区上必须有足够的空间来装载其他文件系统。这包括实用程序、配置、引导加载程序信息和其他重要的启动数据/usr、/opt和/var的设计使得它们可以位于其他分区或文件系统上。

-   To enable recovery and/or repair of a system, those utilities needed by an experienced maintainer to diagnose and reconstruct a damaged system must be present on the root filesystem.

> -为了能够恢复和/或修复系统，经验丰富的维护人员诊断和重建损坏系统所需的实用程序必须存在于根文件系统中。

-   To restore a system, those utilities needed to restore from system backups (on floppy, tape, etc.) must be present on the root filesystem.

> -要恢复系统，从系统备份（软盘、磁带等）中恢复所需的实用程序必须存在于根文件系统中。

    Rationale: The primary concern used to balance these considerations, which favor placing many things on the root filesystem, is the goal of keeping root as small as reasonably possible. For several reasons, it is desirable to keep the root filesystem small:

> 理由：平衡这些有利于将许多东西放在根文件系统上的考虑因素的主要关注点是保持根尽可能小。出于以下几个原因，希望保持根文件系统较小：

    -   It is occasionally mounted from very small media.

    -   The root filesystem contains many system-specific configuration files. Possible examples include a kernel that is specific to the system, a specific hostname, etc. This means that the root filesystem isn't always shareable between networked systems. Keeping it small on servers in networked systems minimizes the amount of lost space for areas of unshareable files. It also allows workstations with smaller local hard drives.

> -根文件系统包含许多特定于系统的配置文件。可能的示例包括特定于系统的内核、特定的主机名等。这意味着根文件系统并不总是可以在网络系统之间共享。在网络系统中的服务器上保持较小的空间可以最大限度地减少不可共享文件区域的空间损失。它还允许工作站使用较小的本地硬盘驱动器。

    -   While you may have the root filesystem on a large partition, and may be able to fill it to your heart's content, there will be people with smaller partitions. If you have more files installed, you may find incompatibilities with other systems using root filesystems on smaller partitions. If you are a developer then you may be turning your assumption into a problem for a large number of users.

> -虽然您可能在一个大分区上拥有根文件系统，并且可以随心所欲地填充它，但也会有人使用较小的分区。如果安装了更多的文件，您可能会发现与在较小分区上使用根文件系统的其他系统不兼容。如果你是一名开发人员，那么你可能会把你的假设变成大量用户的问题。

    -   Disk errors that corrupt data on the root filesystem are a greater problem than errors on any other partition. A small root filesystem is less prone to corruption as the result of a system crash.

> -破坏根文件系统上数据的磁盘错误比任何其他分区上的错误都是一个更大的问题。小型根文件系统不太容易因系统崩溃而损坏。

Applications must never create or require special files or subdirectories in the root directory. Other locations in the FHS hierarchy provide more than enough flexibility for any package.

> 应用程序决不能在根目录中创建或需要特殊的文件或子目录。FHS层次结构中的其他位置为任何包提供了足够的灵活性。

    Rationale: There are several reasons why creating a new subdirectory of the

> 理由：创建
    root filesystem is prohibited:

      + It demands space on a root partition which the system administrator may

> +它需要根分区上的空间，系统管理员可以

        want kept small and simple for either performance or security reasons.

> 出于性能或安全原因，want保持小型和简单。

      + It evades whatever discipline the system administrator may have set up

> +它避开了系统管理员可能设置的任何纪律

        for distributing standard file hierarchies across mountable volumes.

> 用于在可装入卷之间分发标准文件层次结构。

    Distributions should not create new directories in the root hierarchy

    without extremely careful consideration of the consequences including for

> 没有极其仔细地考虑后果，包括
    application portability.

------------------------------------------------------------------------

Requirements

The following directories, or symbolic links to directories, are required in /.

> /中需要以下目录或指向目录的符号链接。

Directory Description bin Essential command binaries boot Static files of the boot loader dev Device files etc Host-specific system configuration lib Essential shared libraries and kernel modules media Mount point for removeable media mnt Mount point for mounting a filesystem temporarily opt Add-on application software packages sbin Essential system binaries srv Data for services provided by this system tmp Temporary files usr Secondary hierarchy var Variable data

> 目录描述bin Essential命令二进制文件boot引导加载程序的静态文件dev设备文件etc特定于主机的系统配置lib Essential共享库和内核模块media可移除介质的装入点mnt用于装入文件系统的装入点临时选择附加应用软件包sbin Essential系统二进制文件srv此提供的服务的数据系统tmp临时文件usr辅助层次结构var变量数据

Each directory listed above is specified in detail in separate subsections below. /usr and /var each have a complete section in this document due to the complexity of those directories.

> 上面列出的每个目录都在下面单独的小节中详细说明/由于这些目录的复杂性，usr和/var在本文档中各有一个完整的部分。

------------------------------------------------------------------------

Specific Options

The following directories, or symbolic links to directories, must be in /, if the corresponding subsystem is installed:

> 如果安装了相应的子系统，则以下目录或指向目录的符号链接必须位于/中：

Directory Description home User home directories (optional) lib`<qual>`{=html} Alternate format essential shared libraries (optional) root Home directory for the root user (optional)

> 目录描述主页用户主目录（可选）lib`<qual>`{=html}备用格式基本共享库（可选）根用户的主目录（选项）

Each directory listed above is specified in detail in separate subsections below.

> 上面列出的每个目录都在下面单独的小节中详细说明。

------------------------------------------------------------------------

/bin : Essential user command binaries (for use by all users)

Purpose

/bin contains commands that may be used by both the system administrator and by users, but which are required when no other filesystems are mounted (e.g. in single user mode). It may also contain commands which are used indirectly by scripts. \[1\]

> /bin包含系统管理员和用户都可以使用的命令，但当没有安装其他文件系统时（例如，在单用户模式下），这些命令是必需的。它还可能包含脚本间接使用的命令\[1\]

------------------------------------------------------------------------

Requirements

There must be no subdirectories in /bin.

The following commands, or symbolic links to commands, are required in /bin.

> /bin中需要以下命令或命令的符号链接。

Command Description cat Utility to concatenate files to standard output chgrp Utility to change file group ownership chmod Utility to change file access permissions chown Utility to change file owner and group cp Utility to copy files and directories date Utility to print or set the system data and time dd Utility to convert and copy a file df Utility to report filesystem disk space usage dmesg Utility to print or control the kernel message buffer echo Utility to display a line of text false Utility to do nothing, unsuccessfully hostname Utility to show or set the system's host name kill Utility to send signals to processes ln Utility to make links between files login Utility to begin a session on the system ls Utility to list directory contents mkdir Utility to make directories mknod Utility to make block or character special files more Utility to page through text mount Utility to mount a filesystem mv Utility to move/rename files ps Utility to report process status pwd Utility to print name of current working directory rm Utility to remove files or directories rmdir Utility to remove empty directories sed The \`sed' stream editor sh The Bourne command shell stty Utility to change and print terminal line settings su Utility to change user ID sync Utility to flush filesystem buffers true Utility to do nothing, successfully umount Utility to unmount file systems uname Utility to print system information

> 命令描述cat实用程序用于将文件连接到标准输出chgrp实用程序用于更改文件组所有权chmod实用程序用于修改文件访问权限chown实用程序用于改变文件所有者和组cp实用程序用于复制文件和目录date实用程序用于打印或设置系统数据和时间dd实用程序用于转换和复制文件df实用程序用于报告文件系统磁盘空间使用情况dmesg实用程序打印或控制内核消息缓冲区echo实用程序显示一行文本false实用程序无所事事，主机名实用程序显示或设置系统的主机名失败实用程序kill实用程序向进程发送信号ln实用程序在文件之间建立链接login实用程序在系统上开始会话ls实用程序列出目录内容mkdir实用程序制作目录mknod实用程序制作块或字符专用文件more实用程序通过文本分页mount实用程序挂载文件系统mv用于移动/重命名文件的实用程序ps用于报告进程状态的实用程序pwd用于打印当前工作目录的名称的实用程序rm用于删除文件或目录的实用程序rmdir用于删除空目录sed“sed”流编辑器sh Bourne命令shell stty用于更改和打印终端行设置的实用程序su用于更改用户ID sync用于刷新文件系统缓冲区的实用程序true实用程序若不执行任何操作，请成功地umount实用工具卸载文件系统uname实用工具打印系统信息

If /bin/sh is not a true Bourne shell, it must be a hard or symbolic link to the real shell command.

> 如果/bin/sh不是真正的Bourne shell，那么它必须是指向真正shell命令的硬链接或符号链接。

The \[ and test commands must be placed together in either /bin or /usr/bin.

> \[和test命令必须放在/bin或/usr/bin中。

    Rationale: For example bash behaves differently when called as sh or bash.

> 理由：例如，bash在被称为sh或bash时表现不同。

    The use of a symbolic link also allows users to easily see that /bin/sh is

> 符号链接的使用也让用户可以很容易地看到/bin/sh
    not a true Bourne shell.

    The requirement for the [ and test commands to be included as binaries

> [和测试命令作为二进制文件包含的要求

    (even if implemented internally by the shell) is shared with the POSIX.2

> （即使由shell内部实现）与POSIX.2共享
    standard.

------------------------------------------------------------------------

Specific Options

The following programs, or symbolic links to programs, must be in /bin if the corresponding subsystem is installed:

> 如果安装了相应的子系统，则下列程序或程序的符号链接必须在/bin中：

Command Description csh The C shell (optional) ed The \`ed' editor (optional) tar The tar archiving utility (optional) cpio The cpio archiving utility (optional) gzip The GNU compression utility (optional) gunzip The GNU uncompression utility (optional) zcat The GNU uncompression utility (optional) netstat The network statistics utility (optional) ping The ICMP network test utility (optional)

> 命令描述csh C shell（可选）ed \`ed'编辑器（可选）tar tar存档实用程序（可选）cpio cpio存档实用程序

If the gunzip and zcat programs exist, they must be symbolic or hard links to gzip. /bin/csh may be a symbolic link to /bin/tcsh or /usr/bin/tcsh.

> 如果gunzip和zcat程序存在，它们必须是指向gzip的符号或硬链接/bin/csh可以是指向/bin/tcsh或/usr/bin/tcsh的符号链接。

    Rationale: The tar, gzip and cpio commands have been added to make
    restoration of a system possible (provided that / is intact).

    Conversely, if no restoration from the root partition is ever expected,

> 相反地如果从未期望从根分区进行恢复，

    then these binaries might be omitted (e.g., a ROM chip root, mounting /usr

> 那么这些二进制文件可能会被省略（例如，ROM芯片根、挂载/usr

    through NFS). If restoration of a system is planned through the network,

> 通过NFS）。如果系统的恢复是通过网络计划的，

    then ftp or tftp (along with everything necessary to get an ftp connection)

> 然后是ftp或tftp（以及获得ftp连接所需的一切）
    must be available on the root partition.

------------------------------------------------------------------------

/boot : Static files of the boot loader

Purpose

This directory contains everything required for the boot process except configuration files not needed at boot time and the map installer. Thus /boot stores data that is used before the kernel begins executing user-mode programs. This may include saved master boot sectors and sector map files. \[2\]

> 该目录包含启动过程所需的所有内容，除了启动时不需要的配置文件和映射安装程序。因此/boot存储在内核开始执行用户模式程序之前使用的数据。这可能包括保存的主引导扇区和扇区映射文件\[2\]

------------------------------------------------------------------------

Specific Options

The operating system kernel must be located in either / or /boot. \[3\]

------------------------------------------------------------------------

/dev : Device files

Purpose

The /dev directory is the location of special or device files.

------------------------------------------------------------------------

Specific Options

If it is possible that devices in /dev will need to be manually created, /dev must contain a command named MAKEDEV, which can create devices as needed. It may also contain a MAKEDEV.local for any local devices.

> 如果可能需要手动创建/dev/中的设备，/dev/必须包含一个名为MAKEDEV的命令，该命令可以根据需要创建设备。它还可能包含用于任何本地设备的MAKEDEV.local。

If required, MAKEDEV must have provisions for creating any device that may be found on the system, not just those that a particular implementation installs.

> 如果需要，MAKEDEV必须具有创建系统上可能找到的任何设备的规定，而不仅仅是特定实现安装的设备。

------------------------------------------------------------------------

/etc : Host-specific system configuration

Purpose

The /etc hierarchy contains configuration files. A "configuration file" is a local file used to control the operation of a program; it must be static and cannot be an executable binary. \[4\]

> /etc/层次结构包含配置文件。“配置文件”是用于控制程序操作的本地文件；它必须是静态的，不能是可执行的二进制文件\[4\]

------------------------------------------------------------------------

Requirements

No binaries may be located under /etc. \[5\]

The following directories, or symbolic links to directories are required in / etc:

> /etc/etc中需要以下目录或指向目录的符号链接：

Directory Description opt Configuration for /opt X11 Configuration for the X Window system (optional) sgml Configuration for SGML (optional) xml Configuration for XML (optional)

> 目录描述opt配置用于/opt X11配置用于X Window系统（可选）sgml配置用于sgml（可选）xml配置用于xml（可选）

------------------------------------------------------------------------

Specific Options

The following directories, or symbolic links to directories must be in /etc, if the corresponding subsystem is installed:

> 如果安装了相应的子系统，则下列目录或指向目录的符号链接必须位于/etc中：

Directory Description opt Configuration for /opt

The following files, or symbolic links to files, must be in /etc if the corresponding subsystem is installed: \[6\]

> 如果安装了相应的子系统，则下列文件或文件的符号链接必须位于/etc中：\[6\]

File Description csh.login Systemwide initialization file for C shell logins (optional) exports NFS filesystem access control list (optional) fstab Static information about filesystems (optional) ftpusers FTP daemon user access control list (optional) gateways File which lists gateways for routed (optional) gettydefs Speed and terminal settings used by getty (optional) group User group file (optional) host.conf Resolver configuration file (optional) hosts Static information about host names (optional) hosts.allow Host access file for TCP wrappers (optional) hosts.deny Host access file for TCP wrappers (optional) hosts.equiv List of trusted hosts for rlogin, rsh, rcp (optional) hosts.lpd List of trusted hosts for lpd (optional) inetd.conf Configuration file for inetd (optional) inittab Configuration file for init (optional) issue Pre-login message and identification file (optional) ld.so.conf List of extra directories to search for shared libraries (optional) motd Post-login message of the day file (optional) mtab Dynamic information about filesystems (optional) mtools.conf Configuration file for mtools (optional) networks Static information about network names (optional) passwd The password file (optional) printcap The lpd printer capability database (optional) profile Systemwide initialization file for sh shell logins (optional) protocols IP protocol listing (optional) resolv.conf Resolver configuration file (optional) rpc RPC protocol listing (optional) securetty TTY access control for root login (optional) services Port names for network services (optional) shells Pathnames of valid login shells (optional) syslog.conf Configuration file for syslogd (optional)

> 文件描述csh.login用于C shell登录的系统范围初始化文件（可选）导出NFS文件系统访问控制列表（可选）fstab关于文件系统的静态信息（可选）ftpusers FTP守护进程用户访问控制列表（可选）host.conf解析程序配置文件（可选）主机关于主机名的静态信息，rcp（可选）hosts.lpd lpd的受信任主机列表（可选）inetd.conf inetd的配置文件inittab init（可选）issue的配置文件预登录消息和标识文件（可选）ld.so.conf用于搜索共享库的额外目录列表（可选（可选）mtools.conf用于mtools（可选）网络的配置文件有关网络名称的静态信息（可选）passwd密码文件（可选）printcap lpd打印机功能数据库（可选）配置文件用于sh shell登录的系统范围初始化文件（可选列出（可选）根登录（可选）服务的安全TTY访问控制网络服务（可选）外壳的端口名有效登录外壳的路径名（可选）syslog.conf syslogd的配置文件（可选）

mtab does not fit the static nature of /etc: it is excepted for historical reasons. \[7\]

> mtab不符合etc的静态性质：由于历史原因，它被排除在外\[7\]

------------------------------------------------------------------------

/etc/opt : Configuration files for /opt

Purpose

Host-specific configuration files for add-on application software packages must be installed within the directory /etc/opt/`<subdir>`{=html}, where `<subdir>`{=html} is the name of the subtree in /opt where the static data from that package is stored.

> 附加应用程序软件包的特定于主机的配置文件必须安装在目录/etc/opt/`<subdir>`{=html}中，其中`<subdr>`{=]html}是/opt中子树的名称，该子树存储该软件包的静态数据。

------------------------------------------------------------------------

Requirements

No structure is imposed on the internal arrangement of /etc/opt/`<subdir>`{=html}.

> /etc/opt/`<subdir>`{=html}的内部排列没有任何结构。

If a configuration file must reside in a different location in order for the package or system to function properly, it may be placed in a location other than /etc/opt/`<subdir>`{=html}.

> 如果配置文件必须位于不同的位置才能使包或系统正常工作，则可以将其放置在/etc/opt/`<subdir>`{=html}以外的位置。

    Rationale: Refer to the rationale for /opt.

------------------------------------------------------------------------

/etc/X11 : Configuration for the X Window System (optional)

Purpose

/etc/X11 is the location for all X11 host-specific configuration. This directory is necessary to allow local control if /usr is mounted read only.

> /etc/X11是所有X11主机特定配置的位置。如果/usr是只读装载的，则此目录是允许本地控制所必需的。

------------------------------------------------------------------------

Specific Options

The following files, or symbolic links to files, must be in /etc/X11 if the corresponding subsystem is installed:

> 如果安装了相应的子系统，则以下文件或文件的符号链接必须位于/etc/X11中：

File Description Xconfig The configuration file for early versions of XFree86 (optional) XF86Config The configuration file for XFree86 versions 3 and 4 (optional) Xmodmap Global X11 keyboard modification file (optional)

> 文件描述Xconfig XFree86早期版本的配置文件（可选）XF86Config XFree86版本3和4的配置文件

Subdirectories of /etc/X11 may include those for xdm and for any other programs (some window managers, for example) that need them. \[8\] We recommend that window managers with only one configuration file which is a default .*wmrc file must name it system.*wmrc (unless there is a widely-accepted alternative name) and not use a subdirectory. Any window manager subdirectories must be identically named to the actual window manager binary.

> /etc/X11的子目录可能包括用于xdm和任何其他需要它们的程序（例如，一些窗口管理器）的子目录\[8\]我们建议只有一个默认配置文件的窗口管理器。*wmrc文件必须将其命名为system.*wmrc（除非有一个广泛接受的替代名称），并且不要使用子目录。任何窗口管理器子目录的名称都必须与实际的窗口管理器二进制文件的名称相同。

------------------------------------------------------------------------

/etc/sgml : Configuration files for SGML (optional)

Purpose

Generic configuration files defining high-level parameters of the SGML systems are installed here. Files with names *.conf indicate generic configuration files. File with names *.cat are the DTD-specific centralized catalogs, containing references to all other catalogs needed to use the given DTD. The super catalog file catalog references all the centralized catalogs.

> 此处安装了定义SGML系统高级参数的通用配置文件。名称为*.conf的文件表示通用配置文件。名为*.cat的文件是DTD特定的集中目录，包含对使用给定DTD所需的所有其他目录的引用。超级目录文件目录引用所有集中式目录。

------------------------------------------------------------------------

/etc/xml : Configuration files for XML (optional)

Purpose

Generic configuration files defining high-level parameters of the XML systems are installed here. Files with names \*.conf indicate generic configuration files. The super catalog file catalog references all the centralized catalogs.

> 这里安装了定义XML系统高级参数的通用配置文件。名为\*.conf的文件表示通用配置文件。超级目录文件目录引用所有集中式目录。

------------------------------------------------------------------------

/home : User home directories (optional)

Purpose

/home is a fairly standard concept, but it is clearly a site-specific filesystem. \[9\] The setup will differ from host to host. Therefore, no program should rely on this location. \[10\]

> /home是一个相当标准的概念，但它显然是一个特定于站点的文件系统\[9\]不同主机的设置会有所不同。因此，任何程序都不应依赖于此位置\[10\]

------------------------------------------------------------------------

Requirements

User specific configuration files for applications are stored in the user's home directory in a file that starts with the '.' character (a "dot file"). If an application needs to create more than one dot file then they should be placed in a subdirectory with a name starting with a '.' character, (a "dot directory"). In this case the configuration files should not start with the '.' character. \[11\]

> 应用程序的特定于用户的配置文件存储在用户主目录中以“”开头的文件中字符（“点文件”）。如果应用程序需要创建多个点文件，则应将它们放在名称以“”开头的子目录中字符，（“点目录”）。在这种情况下，配置文件不应以“.”开头性格\[11\]

------------------------------------------------------------------------

/lib : Essential shared libraries and kernel modules

Purpose

The /lib directory contains those shared library images needed to boot the system and run the commands in the root filesystem, ie. by binaries in /bin and /sbin. \[12\]

> /lib目录包含启动系统和在根文件系统中运行命令所需的共享库映像，即通过/bin和/sbin中的二进制文件\[12\]

------------------------------------------------------------------------

Requirements

At least one of each of the following filename patterns are required (they may be files, or symbolic links):

> 以下文件名模式中至少有一种是必需的（它们可能是文件或符号链接）：

File Description libc.so.\* The dynamically-linked C library (optional) ld\* The execution time linker/loader (optional)

> 文件描述libc.so.\*动态链接的C库（可选）ld\*执行时链接器/加载程序（可选）

If a C preprocessor is installed, /lib/cpp must be a reference to it, for historical reasons. \[13\]

> 如果安装了C预处理器，由于历史原因，/lib/cpp必须是对它的引用\[13\]

------------------------------------------------------------------------

Specific Options

The following directories, or symbolic links to directories, must be in /lib, if the corresponding subsystem is installed:

> 如果安装了相应的子系统，则以下目录或指向目录的符号链接必须位于/lib中：

Directory Description modules Loadable kernel modules (optional)

------------------------------------------------------------------------

/lib`<qual>`{=html} : Alternate format essential shared libraries (optional)

> /lib`<qual>`{=html}：备用格式基本共享库（可选）

Purpose

There may be one or more variants of the /lib directory on systems which support more than one binary format requiring separate libraries. \[14\]

> 在支持需要单独库的多个二进制格式的系统上，/lib目录可能有一个或多个变体\[14\]

------------------------------------------------------------------------

Requirements

If one or more of these directories exist, the requirements for their contents are the same as the normal /lib directory, except that /lib`<qual>`{=html}/cpp is not required. \[15\]

> 如果存在这些目录中的一个或多个，则对其内容的要求与普通/lib目录相同，只是/lib`<qual>`{=html}/cpp不是必需的\[15\]

------------------------------------------------------------------------

/media : Mount point for removeable media

Purpose

This directory contains subdirectories which are used as mount points for removeable media such as floppy disks, cdroms and zip disks.

> 此目录包含子目录，这些子目录用作可移动介质（如软盘、光盘和压缩磁盘）的装入点。

    Rationale: Historically there have been a number of other different places

> 理由：历史上还有许多其他不同的地方

    used to mount removeable media such as /cdrom, /mnt or /mnt/cdrom. Placing

> 用于装载可移除介质，如/cdrom、/mnt或/mnt/cdrom。浇筑

    the mount points for all removeable media directly in the root directory

> 直接在根目录中的所有可移动介质的装载点
    would potentially result in a large number of extra directories in /.

    Although the use of subdirectories in /mnt as a mount point has recently

> 尽管最近使用/mnt中的子目录作为装载点
    been common, it conflicts with a much older tradition of using /mnt
    directly as a temporary mount point.

------------------------------------------------------------------------

Specific Options

The following directories, or symbolic links to directories, must be in /media, if the corresponding subsystem is installed:

> 如果安装了相应的子系统，则以下目录或指向目录的符号链接必须位于/media中：

Directory Description floppy Floppy drive (optional) cdrom CD-ROM drive (optional) cdrecorder CD writer (optional) zip Zip drive (optional)

> 目录描述软盘驱动器（可选）cdrom CD-ROM驱动器（可选

On systems where more than one device exists for mounting a certain type of media, mount directories can be created by appending a digit to the name of those available above starting with '0', but the unqualified name must also exist. \[16\]

> 在存在多个用于装载特定类型介质的设备的系统上，可以通过在上面以“0”开头的可用设备的名称后面附加一个数字来创建装载目录，但非限定名称也必须存在\[16\]

------------------------------------------------------------------------

/mnt : Mount point for a temporarily mounted filesystem

Purpose

This directory is provided so that the system administrator may temporarily mount a filesystem as needed. The content of this directory is a local issue and should not affect the manner in which any program is run.

> 提供此目录是为了让系统管理员可以根据需要临时安装文件系统。此目录的内容是本地问题，不应影响任何程序的运行方式。

This directory must not be used by installation programs: a suitable temporary directory not in use by the system must be used instead.

> 安装程序不得使用此目录：必须使用系统未使用的适当临时目录。

------------------------------------------------------------------------

/opt : Add-on application software packages

Purpose

/opt is reserved for the installation of add-on application software packages.

> /opt是为安装附加应用程序软件包而保留的。

A package to be installed in /opt must locate its static files in a separate / opt/`<package>`{=html} or /opt/`<provider>`{=html} directory tree, where `<package>`{=html} is a name that describes the software package and `<provider>`{=html} is the provider's LANANA registered name.

> 要安装在/opt中的软件包必须在单独的/opt/`<package>`{=html}或/opt/`</provider>`{=]html}目录树中找到其静态文件，其中`<package>`{=chll}是描述软件包的名称，`<provider>`{=html}是提供程序的LANANA注册名称。

------------------------------------------------------------------------

Requirements

Directory Description `<package>`{=html} Static package objects `<provider>`{=html} LANANA registered provider name

> 目录描述`<package>`{=html}静态程序包对象`<provider>`{=chtml}LANANA注册的提供程序名称

The directories /opt/bin, /opt/doc, /opt/include, /opt/info, /opt/lib, and /opt /man are reserved for local system administrator use. Packages may provide "front-end" files intended to be placed in (by linking or copying) these reserved directories by the local system administrator, but must function normally in the absence of these reserved directories.

> 目录/opt/bin、/opt/doc、/opt/include、/opt/info、/opt/lib和/opt/man保留给本地系统管理员使用。包可以提供“前端”文件，这些文件旨在由本地系统管理员放置在（通过链接或复制）这些保留目录中，但在没有这些保留目录的情况下必须正常工作。

Programs to be invoked by users must be located in the directory /opt/`<package>`{=html} /bin or under the /opt/`<provider>`{=html} hierarchy. If the package includes UNIX manual pages, they must be located in /opt/`<package>`{=html}/share/man or under the / opt/`<provider>`{=html} hierarchy, and the same substructure as /usr/share/man must be used.

> 要由用户调用的程序必须位于目录/opt/`<package>`{=html}/bin或/opt/`<provider>`{=]html}层次结构下。如果程序包包含UNIX手册页，则它们必须位于/opt/`<package>`{=html}/share/man或/opt/`</provider>`{=html}层次结构下，并且必须使用与/usr/share/man相同的子结构。

Package files that are variable (change in normal operation) must be installed in /var/opt. See the section on /var/opt for more information.

> 可变的包文件（在正常操作中更改）必须安装在/var/opt中。有关更多信息，请参阅/var/opt部分。

Host-specific configuration files must be installed in /etc/opt. See the section on /etc for more information.

> 主机特定的配置文件必须安装在/etc/opt中。有关详细信息，请参阅/etc上的部分。

No other package files may exist outside the /opt, /var/opt, and /etc/opt hierarchies except for those package files that must reside in specific locations within the filesystem tree in order to function properly. For example, device lock files must be placed in /var/lock and devices must be located in /dev.

> /opt、/var/opt和/etc/opt层次结构之外可能不存在任何其他包文件，但那些必须位于文件系统树中特定位置才能正常工作的包文件除外。例如，设备锁定文件必须放在/var/lock中，设备必须位于/dev中。

Distributions may install software in /opt, but must not modify or delete software installed by the local system administrator without the assent of the local system administrator.

> 分发版可以在/opt中安装软件，但未经本地系统管理员同意，不得修改或删除本地系统管理员安装的软件。

    Rationale: The use of /opt for add-on software is a well-established

    practice in the UNIX community. The System V Application Binary Interface

> UNIX社区中的实践。System V应用程序二进制接口

    [AT&T 1990], based on the System V Interface Definition (Third Edition),

> [AT&T 1990]基于System V接口定义（第三版），
    provides for an /opt structure very similar to the one defined here.

    The Intel Binary Compatibility Standard v. 2 (iBCS2) also provides a
    similar structure for /opt.

    Generally, all data required to support a package on a system must be

    present within /opt/<package>, including files intended to be copied into /

> 出现在/opt/<package>中，包括要复制到的文件/

    etc/opt/<package> and /var/opt/<package> as well as reserved directories in

> etc/opt/<package>和/var/opt/<package>以及中的保留目录
    /opt.

    The minor restrictions on distributions using /opt are necessary because

> 对使用/opt的发行版进行一些小的限制是必要的，因为

    conflicts are possible between distribution-installed and locally-installed

> 安装的分发和本地安装之间可能存在冲突

    software, especially in the case of fixed pathnames found in some binary

> 软件，尤其是在某些二进制文件中发现固定路径名的情况下
    software.

    The structure of the directories below /opt/<provider> is left up to the

> /opt/<provider>下面的目录结构由
    packager of the software, though it is recommended that packages are

    installed in /opt/<provider>/<package> and follow a similar structure to

> 安装在/opt/<provider>/<package>中，并遵循与

    the guidelines for /opt/package. A valid reason for diverging from this

> /opt/package的指导方针。背离这一点的正当理由

    structure is for support packages which may have files installed in /opt/

> 结构适用于可能在/opt中安装了文件的支持包/
    <provider>/lib or /opt/<provider>/bin.

------------------------------------------------------------------------

/root : Home directory for the root user (optional)

Purpose

The root account's home directory may be determined by developer or local preference, but this is the recommended default location. \[17\]

> 根帐户的主目录可能由开发人员或本地偏好决定，但这是推荐的默认位置\[17\]

------------------------------------------------------------------------

/sbin : System binaries

Purpose

Utilities used for system administration (and other root-only commands) are stored in /sbin, /usr/sbin, and /usr/local/sbin. /sbin contains binaries essential for booting, restoring, recovering, and/or repairing the system in addition to the binaries in /bin. \[18\] Programs executed after /usr is known to be mounted (when there are no problems) are generally placed into /usr/sbin. Locally-installed system administration programs should be placed into /usr/ local/sbin. \[19\]

> 用于系统管理的实用程序（以及其他仅限root用户的命令）存储在/sbin、/usr/sbin和/usr/local/sbin中/sbin除了/bin中的二进制文件外，还包含引导、恢复、恢复和/或修复系统所必需的二进制文件\[18\]在已知安装了/usr/之后执行的程序（在没有问题的情况下）通常被放入/usr/sbin中。本地安装的系统管理程序应放在/usr/local/sbin中\[19\]

------------------------------------------------------------------------

Requirements

The following commands, or symbolic links to commands, are required in /sbin.

> /sbin中需要以下命令或命令的符号链接。

Command Description shutdown Command to bring the system down.

------------------------------------------------------------------------

Specific Options

The following files, or symbolic links to files, must be in /sbin if the corresponding subsystem is installed:

> 如果安装了相应的子系统，则以下文件或文件的符号链接必须位于/sbin中：

Command Description fastboot Reboot the system without checking the disks (optional) fasthalt Stop the system without checking the disks (optional) fdisk Partition table manipulator (optional) fsck File system check and repair utility (optional) fsck.\* File system check and repair utility for a specific filesystem (optional) getty The getty program (optional) halt Command to stop the system (optional) ifconfig Configure a network interface (optional) init Initial process (optional) mkfs Command to build a filesystem (optional) mkfs.\* Command to build a specific filesystem (optional) mkswap Command to set up a swap area (optional) reboot Command to reboot the system (optional) route IP routing table utility (optional) swapon Enable paging and swapping (optional) swapoff Disable paging and swapping (optional) update Daemon to periodically flush filesystem buffers (optional)

> 命令描述fastboot在不检查磁盘的情况下重新启动系统（可选）fasthalt在不检查硬盘的情况下停止系统（可选特定文件系统的文件系统检查和修复实用工具（可选）getty getty程序（可选）停止系统的命令（可选）ifconfig配置网络接口（可选）init初始进程（可选）mkfs命令构建文件系统（可选）mkfs。\*用于构建特定文件系统的命令（可选）mkswap用于设置交换区域的命令（可选项）reboot用于重新启动系统的命令

------------------------------------------------------------------------

/srv : Data for services provided by this system

Purpose

/srv contains site-specific data which is served by this system.

    Rationale: This main purpose of specifying this is so that users may find

> 理由：规定这一点的主要目的是让用户可以发现

    the location of the data files for particular service, and so that services

> 特定服务的数据文件的位置，以便服务

    which require a single tree for readonly data, writable data and scripts

> 需要一个只读数据、可写数据和脚本的树
    (such as cgi scripts) can be reasonably placed. Data that is only of
    interest to a specific user should go in that users' home directory.

    The methodology used to name subdirectories of /srv is unspecified as there

> 用于命名/srv子目录的方法未指定，因为
    is currently no consensus on how this should be done. One method for

    structuring data under /srv is by protocol, eg. ftp, rsync, www, and cvs.

> /srv下的数据结构采用ftp、rsync、www和cvs等协议。
    On large systems it can be useful to structure /srv by administrative

    context, such as /srv/physics/www, /srv/compsci/cvs, etc. This setup will

> 上下文，如/srv/physics/www、/srv/compsci/cvs等。此设置将

    differ from host to host. Therefore, no program should rely on a specific

> 主机不同。因此，任何程序都不应依赖于

    subdirectory structure of /srv existing or data necessarily being stored in

> /srv的子目录结构存在或数据必须存储在

    /srv. However /srv should always exist on FHS compliant systems and should

> /srv。然而，/srv应始终存在于符合FHS的系统中，并且
    be used as the default location for such data.

    Distributions must take care not to remove locally placed files in these

> 分发版必须注意不要删除这些文件中本地放置的文件
    directories without administrator permission. [20]

------------------------------------------------------------------------

/tmp : Temporary files

Purpose

The /tmp directory must be made available for programs that require temporary files.

> /tmp目录必须可用于需要临时文件的程序。

Programs must not assume that any files or directories in /tmp are preserved between invocations of the program.

> 程序不得假定在程序调用之间保留/tmp中的任何文件或目录。

    Rationale: IEEE standard P1003.2 (POSIX, part 2) makes requirements that

> 理由：IEEE标准P1003.2（POSIX，第2部分）要求
    are similar to the above section.

    Although data stored in /tmp may be deleted in a site-specific manner, it

> 尽管存储在/tmp中的数据可能会以特定站点的方式删除
    is recommended that files and directories located in /tmp be deleted
    whenever the system is booted.

    FHS added this recommendation on the basis of historical precedent and

> FHS在历史先例和
    common practice, but did not make it a requirement because system
    administration is not within the scope of this standard.

------------------------------------------------------------------------

Chapter 4. The /usr Hierarchy

Purpose

/usr is the second major section of the filesystem. /usr is shareable, read-only data. That means that /usr should be shareable between various FHS-compliant hosts and must not be written to. Any information that is host-specific or varies with time is stored elsewhere.

> /usr是文件系统的第二个主要部分/usr是可共享的只读数据。这意味着/usr/应该可以在各种符合FHS的主机之间共享，并且不能写入。任何特定于主机或随时间变化的信息都存储在其他地方。

Large software packages must not use a direct subdirectory under the /usr hierarchy.

> 大型软件包不得使用/usr/层次结构下的直接子目录。

------------------------------------------------------------------------

Requirements

The following directories, or symbolic links to directories, are required in / usr.

> /usr/中需要以下目录或指向目录的符号链接。

Directory Description bin Most user commands include Header files included by C programs lib Libraries local Local hierarchy (empty after main installation) sbin Non-vital system binaries share Architecture-independent data

> 目录描述bin大多数用户命令包括C程序包含的头文件lib库本地本地层次结构（主安装后为空）sbin非重要系统二进制文件共享独立于体系结构的数据

------------------------------------------------------------------------

Specific Options

Directory Description X11R6 XWindow System, version 11 release 6 (optional) games Games and educational binaries (optional) lib`<qual>`{=html} Alternate Format Libraries (optional) src Source code (optional)

> 目录描述X11R6 XWindow系统，版本11发行版6（可选）游戏游戏和教育二进制文件（可选）lib`<qual>`{=html}替代格式库（可选）src源代码（可选）

An exception is made for the X Window System because of considerable precedent and widely-accepted practice.

> X窗口系统是一个例外，因为有相当多的先例和广泛接受的实践。

The following symbolic links to directories may be present. This possibility is based on the need to preserve compatibility with older systems until all implementations can be assumed to use the /var hierarchy.

> 可能存在以下指向目录的符号链接。这种可能性是基于需要保持与旧系统的兼容性，直到可以假设所有实现都使用/var/层次结构。

    /usr/spool -> /var/spool
    /usr/tmp -> /var/tmp
    /usr/spool/locks -> /var/lock

Once a system no longer requires any one of the above symbolic links, the link may be removed, if desired.

> 一旦系统不再需要上述任何一个符号链接，如果需要，可以删除该链接。

------------------------------------------------------------------------

/usr/X11R6 : X Window System, Version 11 Release 6 (optional)

Purpose

This hierarchy is reserved for the X Window System, version 11 release 6, and related files.

> 此层次结构是为X Window System版本11版本6和相关文件保留的。

To simplify matters and make XFree86 more compatible with the X Window System on other systems, the following symbolic links must be present if /usr/X11R6 exists:

> 为了简化问题并使XFree86与其他系统上的X Window系统更兼容，如果/usr/X11R6存在，则必须存在以下符号链接：

    /usr/bin/X11 -> /usr/X11R6/bin
    /usr/lib/X11 -> /usr/X11R6/lib/X11
    /usr/include/X11 -> /usr/X11R6/include/X11

In general, software must not be installed or managed via the above symbolic links. They are intended for utilization by users only. The difficulty is related to the release version of the X Window System - in transitional periods, it is impossible to know what release of X11 is in use.

> 通常，软件不得通过上述符号链接进行安装或管理。它们仅供用户使用。困难与X窗口系统的发布版本有关——在过渡时期，不可能知道X11的哪个版本在使用。

------------------------------------------------------------------------

Specific Options

Host-specific data in /usr/X11R6/lib/X11 should be interpreted as a demonstration file. Applications requiring information about the current host must reference a configuration file in /etc/X11, which may be linked to a file in /usr/X11R6/lib. \[21\]

> /usr/X11R6/lib/X11中特定于主机的数据应该被解释为一个演示文件。需要当前主机信息的应用程序必须引用/etc/X11中的配置文件，该文件可能链接到/usr/X11R6/lib中的文件\[21\]

------------------------------------------------------------------------

/usr/bin : Most user commands

Purpose

This is the primary directory of executable commands on the system.

------------------------------------------------------------------------

Specific Options

The following directories, or symbolic links to directories, must be in /usr/ bin, if the corresponding subsystem is installed:

> 如果安装了相应的子系统，则下列目录或指向目录的符号链接必须位于/usr/bin中：

Directory Description mh Commands for the MH mail handling system (optional)

> 目录描述mh用于mh邮件处理系统的命令（可选）

/usr/bin/X11 must be a symlink to /usr/X11R6/bin if the latter exists.

The following files, or symbolic links to files, must be in /usr/bin, if the corresponding subsystem is installed:

> 如果安装了相应的子系统，则以下文件或文件的符号链接必须位于/usr/bin中：

Command Description perl The Practical Extraction and Report Language (optional) python The Python interpreted language (optional) tclsh Simple shell containing Tcl interpreter (optional) wish Simple Tcl/Tk windowing shell (optional) expect Program for interactive dialog (optional)

> 命令描述perl实用提取和报告语言（可选）python解释语言（可选

    Rationale: Because shell script interpreters (invoked with #!<path> on the

> 理由：因为shell脚本解释器（在

    first line of a shell script) cannot rely on a path, it is advantageous to

> shell脚本的第一行）不能依赖于路径

    standardize their locations. The Bourne shell and C-shell interpreters are

> 标准化他们的位置。Bourne shell和C shell解释器

    already fixed in /bin, but Perl, Python, and Tcl are often found in many

> 已经在/bin中修复，但Perl、Python和Tcl经常出现在许多

    different places. They may be symlinks to the physical location of the

> 不同的地方。它们可能是指向
    shell interpreters.

------------------------------------------------------------------------

/usr/include : Directory for standard include files.

Purpose

This is where all of the system's general-use include files for the C programming language should be placed.

> 这是所有系统的通用包含C编程语言文件的位置。

------------------------------------------------------------------------

Specific Options

The following directories, or symbolic links to directories, must be in /usr/ include, if the corresponding subsystem is installed:

> 如果安装了相应的子系统，则以下目录或指向目录的符号链接必须位于/usr/include中：

Directory Description bsd BSD compatibility include files (optional)

The symbolic link /usr/include/X11 must link to /usr/X11R6/include/X11 if the latter exists.

> 符号链接/usr/include/X11必须链接到/usr/X11R6/include/X11（如果后者存在）。

------------------------------------------------------------------------

/usr/lib : Libraries for programming and packages

Purpose

/usr/lib includes object files, libraries, and internal binaries that are not intended to be executed directly by users or shell scripts. \[22\]

> /usr/lib包括不打算由用户或shell脚本直接执行的对象文件、库和内部二进制文件\[22\]

Applications may use a single subdirectory under /usr/lib. If an application uses a subdirectory, all architecture-dependent data exclusively used by the application must be placed within that subdirectory. \[23\]

> 应用程序可以使用/usr/lib下的一个子目录。如果应用程序使用子目录，则应用程序独占使用的所有体系结构相关数据都必须放在该子目录中\[23\]

------------------------------------------------------------------------

Specific Options

For historical reasons, /usr/lib/sendmail must be a symbolic link to /usr/sbin/ sendmail if the latter exists. \[24\]

> 由于历史原因，/usr/lib/sendmail必须是指向/usr/sbin/sendmail的符号链接（如果后者存在的话）\[24\]

If /lib/X11 exists, /usr/lib/X11 must be a symbolic link to /lib/X11, or to whatever /lib/X11 is a symbolic link to. \[25\]

> 如果/lib/X11存在，则/usr/lib/X11必须是到/lib/X11的符号链接，或者到任何/lib/X11的符号链接。\[25\]

------------------------------------------------------------------------

/usr/lib`<qual>`{=html} : Alternate format libraries (optional)

Purpose

/usr/lib`<qual>`{=html} performs the same role as /usr/lib for an alternate binary format, except that the symbolic links /usr/lib`<qual>`{=html}/sendmail and /usr/lib `<qual>`{=html}/X11 are not required. \[26\]

> /对于替代二进制格式，/usr/lib`<qual>`{=html}执行与/usr/lib相同的角色，不同之处在于不需要符号链接/usr/lib`</qual>`{=html}/sendmail和/usr/lib`<qual>`{=html}/X11\[26\]

------------------------------------------------------------------------

/usr/local : Local hierarchy

Purpose

The /usr/local hierarchy is for use by the system administrator when installing software locally. It needs to be safe from being overwritten when the system software is updated. It may be used for programs and data that are shareable amongst a group of hosts, but not found in /usr.

> /usr/local层次结构供系统管理员在本地安装软件时使用。当系统软件更新时，它需要是安全的，不会被覆盖。它可以用于在一组主机之间共享但在/usr/中找不到的程序和数据。

Locally installed software must be placed within /usr/local rather than /usr unless it is being installed to replace or upgrade software in /usr. \[27\]

> 本地安装的软件必须放在/usr/local而不是/usr/r中，除非它是为了替换或升级/usr/r中的软件而安装的\[27\]

------------------------------------------------------------------------

Requirements

The following directories, or symbolic links to directories, must be in /usr/ local

> 下列目录或指向目录的符号链接必须位于/usr/local中

Directory Description bin Local binaries etc Host-specific system configuration for local binaries games Local game binaries include Local C header files lib Local libraries man Local online manuals sbin Local system binaries share Local architecture-independent hierarchy src Local source code

> 目录描述bin本地二进制文件等本地二进制文件游戏的主机特定系统配置本地游戏二进制文件包括本地C头文件lib本地库man本地在线手册sbin本地系统二进制文件共享本地体系结构独立层次结构src本地源代码

No other directories, except those listed below, may be in /usr/local after first installing a FHS-compliant system.

> 在首次安装符合FHS的系统后，/usr/local中可能没有其他目录（以下列出的目录除外）。

------------------------------------------------------------------------

Specific Options

If directories /lib`<qual>`{=html} or /usr/lib`<qual>`{=html} exist, the equivalent directories must also exist in /usr/local.

> 如果目录/lib`<qual>`{=html}或/usr/lib`<qual>`{=]html}存在，则等效目录也必须存在于/usr/local中。

/usr/local/etc may be a symbolic link to /etc/local.

    Rationale: The consistency of /usr/local/etc is beneficial to installers,

> 理由：/usr/local/etc的一致性有利于安装人员，

    and is already used in other systems. As all of /usr/local needs to be

> 并且已经在其他系统中使用。所有/usr/local都需要

    backed up to reproduce a system, it introduces no additional maintenance

> 备份以复制系统，它不需要额外的维护

    overhead, but a symlink to /etc/local is suitable if systems want alltheir

> 开销，但如果系统需要所有
    configuration under one hierarchy.

    Note that /usr/etc is still not allowed: programs in /usr should place

> 请注意，/usr/etc仍然是不允许的：/usr/中的程序应该放置
    configuration files in /etc.

------------------------------------------------------------------------

/usr/local/share

The requirements for the contents of this directory are the same as /usr/share. The only additional constraint is that /usr/local/share/man and /usr/local/man directories must be synonomous (usually this means that one of them must be a symbolic link). \[28\]

> 对该目录内容的要求与/usr/share相同。唯一的附加限制是/usr/local/share/man和/usr/local/man目录必须是同义的（通常这意味着其中一个目录必须是符号链接）\[28\]

------------------------------------------------------------------------

/usr/sbin : Non-essential standard system binaries

Purpose

This directory contains any non-essential binaries used exclusively by the system administrator. System administration programs that are required for system repair, system recovery, mounting /usr, or other essential functions must be placed in /sbin instead. \[29\]

> 此目录包含系统管理员专门使用的任何非必需二进制文件。系统修复、系统恢复、装入/usr或其他基本功能所需的系统管理程序必须放在/sbin中\[29\]

------------------------------------------------------------------------

/usr/share : Architecture-independent data

Purpose

The /usr/share hierarchy is for all read-only architecture independent data files. \[30\]

> /usr/share层次结构适用于所有只读体系结构无关的数据文件\[30\]

This hierarchy is intended to be shareable among all architecture platforms of a given OS; thus, for example, a site with i386, Alpha, and PPC platforms might maintain a single /usr/share directory that is centrally-mounted. Note, however, that /usr/share is generally not intended to be shared by different OSes or by different releases of the same OS.

> 该层次结构旨在在给定操作系统的所有体系结构平台之间共享；因此，例如，具有i386、Alpha和PPC平台的站点可能会维护一个集中安装的/usr/share目录。但是，请注意，/usr/share通常不打算由不同的操作系统或同一操作系统的不同版本共享。

Any program or package which contains or requires data that doesn't need to be modified should store that data in /usr/share (or /usr/local/share, if installed locally). It is recommended that a subdirectory be used in /usr/share for this purpose.

> 任何包含或需要不需要修改的数据的程序或包都应将这些数据存储在/usr/share（或/usr/local/share，如果在本地安装）中。为此，建议在/usr/share中使用一个子目录。

Game data stored in /usr/share/games must be purely static data. Any modifiable files, such as score files, game play logs, and so forth, should be placed in / var/games.

> 存储在/usr/share/games中的游戏数据必须是纯静态数据。任何可修改的文件，如分数文件、游戏日志等，都应该放在/var/games中。

------------------------------------------------------------------------

Requirements

The following directories, or symbolic links to directories, must be in /usr/ share

> 下列目录或指向目录的符号链接必须位于/usr/share中

Directory Description man Online manuals misc Miscellaneous architecture-independent data

> 目录描述手册在线手册杂项杂项架构独立数据

------------------------------------------------------------------------

Specific Options

The following directories, or symbolic links to directories, must be in /usr/ share, if the corresponding subsystem is installed:

> 如果安装了相应的子系统，则下列目录或指向目录的符号链接必须位于/usr/share中：

Directory Description dict Word lists (optional) doc Miscellaneous documentation (optional) games Static data files for /usr/games (optional) info GNU Info system s primary directory (optional) locale Locale information (optional) nls Message catalogs for Native language support (optional) sgml SGML data (optional) terminfo Directories for terminfo database (optional) tmac troff macros not distributed with groff (optional) xml XML data (optional) zoneinfo Timezone information and configuration (optional)

> 目录描述dict单词列表（可选）doc杂项文档（可选）游戏/usr/games的静态数据文件（可选）信息GNU信息系统的主目录（可选）区域设置信息（可选）nls本地语言支持的消息目录（可选分布式groff（可选）xml xml数据（可选）zoneinfo时区信息和配置（可选）

It is recommended that application-specific, architecture-independent directories be placed here. Such directories include groff, perl, ghostscript, texmf, and kbd (Linux) or syscons (BSD). They may, however, be placed in /usr/ lib for backwards compatibility, at the distributor's discretion. Similarly, a /usr/lib/games hierarchy may be used in addition to the /usr/share/games hierarchy if the distributor wishes to place some game data there.

> 建议将特定于应用程序、独立于体系结构的目录放在此处。这样的目录包括groff、perl、ghostscript、texmf和kbd（Linux）或syscons（BSD）。但是，为了向后兼容性，它们可以放在/usr/lib中，由分发服务器决定。类似地，如果发行商希望将一些游戏数据放置在/usr/share/games层次结构之外，还可以使用/usr/lib/games层级结构。

------------------------------------------------------------------------

/usr/share/dict : Word lists (optional)

Purpose

This directory is the home for word lists on the system; Traditionally this directory contains only the English words file, which is used by look(1) and various spelling programs. words may use either American or British spelling.

> 该目录是系统中单词列表的主页；传统上，该目录只包含英文单词文件，look（1）和各种拼写程序都使用该文件。单词可以用美式拼写，也可以用英式拼写。

    Rationale: The reason that only word lists are located here is that they

> 理由：此处仅列出单词表的原因是
    are the only files common to all spell checkers.

------------------------------------------------------------------------

Specific Options

The following files, or symbolic links to files, must be in /usr/share/dict, if the corresponding subsystem is installed:

> 如果安装了相应的子系统，则以下文件或文件的符号链接必须位于/usr/share/dict中：

File Description words List of English words (optional)

Sites that require both American and British spelling may link words to ­/usr/ share/dict/american-english or ­/usr/share/dict/british-english.

> 同时需要美式和英式拼写的网站可以将单词链接到/usr/share/dict/美式英语或/usr/share/didict/英式英语。

Word lists for other languages may be added using the English name for that language, e.g., /usr/share/dict/french, /usr/share/dict/danish, etc. These should, if possible, use an ISO 8859 character set which is appropriate for the language in question; if possible the Latin1 (ISO 8859-1) character set should be used (this is often not possible).

> 其他语言的单词列表可以使用该语言的英文名称添加，例如/usr/share/dict/french、/usr/share/didict/danish等。如果可能，这些单词列表应该使用适合所讨论语言的ISO 8859字符集；如果可能的话，应该使用Latin1（ISO 8859-1）字符集（这通常是不可能的）。

Other word lists must be included here, if present.

------------------------------------------------------------------------

/usr/share/man : Manual pages

Purpose

This section details the organization for manual pages throughout the system, including /usr/share/man. Also refer to the section on /var/cache/man.

> 本节详细介绍了整个系统中手动页面的组织，包括/usr/share/man。另请参阅/var/cache/man一节。

The primary `<mandir>`{=html} of the system is /usr/share/man. /usr/share/man contains manual information for commands and data under the / and /usr filesystems. \[31\]

> 系统的主`<mandir>`{=html}是/usr/share/man/usr/share/man包含/和/usr文件系统下的命令和数据的手动信息\[31\]

Manual pages are stored in `<mandir>`{=html}/`<locale>`{=html}/man

```{=html}
<section>
```
/`<arch>`{=html}. An explanation of `<mandir>`{=html}, `<locale>`{=html},

```{=html}
<section>
```
, and `<arch>`{=html} is given below.

A description of each section follows:

-   man1: User programs Manual pages that describe publicly accessible commands are contained in this chapter. Most program documentation that a user will need to use is located here.

> -man1：本章中包含了描述可公开访问命令的用户程序手册页面。用户需要使用的大多数程序文档都位于此处。

-   man2: System calls This section describes all of the system calls (requests for the kernel to perform operations).

> -man2：系统调用本节描述了所有的系统调用（对内核执行操作的请求）。

-   man3: Library functions and subroutines Section 3 describes program library routines that are not direct calls to kernel services. This and chapter 2 are only really of interest to programmers.

> -man3：库函数和子例程第3节描述了不是对内核服务的直接调用的程序库例程。这和第2章只是程序员真正感兴趣的部分。

-   man4: Special files Section 4 describes the special files, related driver functions, and networking support available in the system. Typically, this includes the device files found in /dev and the kernel interface to networking protocol support.

> -man4：特殊文件第4节介绍了系统中可用的特殊文件、相关驱动程序功能和网络支持。通常，这包括/dev/中的设备文件和网络协议支持的内核接口。

-   man5: File formats The formats for many data files are documented in the section 5. This includes various include files, program output files, and system files.

> -man5：文件格式许多数据文件的格式在第5节中有介绍。这包括各种包含文件、程序输出文件和系统文件。

-   man6: Games This chapter documents games, demos, and generally trivial programs. Different people have various notions about how essential this is.

> -man6：游戏本章介绍游戏、演示和一般琐碎的程序。不同的人对这一点的重要性有不同的看法。

-   man7: Miscellaneous Manual pages that are difficult to classify are designated as being section 7. The troff and other text processing macro packages are found here.

> -man7：难以分类的其他手册页面被指定为第7节。troff和其他文本处理宏包可在此处找到。

-   man8: System administration Programs used by system administrators for system operation and maintenance are documented here. Some of these programs are also occasionally useful for normal users.

> -man8：系统管理系统管理员用于系统操作和维护的程序记录在这里。其中一些程序偶尔也对普通用户有用。

------------------------------------------------------------------------

Specific Options

The following directories, or symbolic links to directories, must be in /usr/ share/`<mandir>`{=html}/`<locale>`{=html}, unless they are empty: \[32\]

> 下列目录或指向目录的符号链接必须位于/usr/share/`<mandir>`{=html}/`<locale>`{=]html}中，除非它们为空：\[32\]

Directory Description man1 User programs (optional) man2 System calls (optional) man3 Library calls (optional) man4 Special files (optional) man5 File formats (optional) man6 Games (optional) man7 Miscellaneous (optional) man8 System administration (optional)

> 目录描述man1用户程序（可选）man2系统调用（可选）man3库调用（可选

The component

```{=html}
<section>
```
describes the manual section.

Provisions must be made in the structure of /usr/share/man to support manual pages which are written in different (or multiple) languages. These provisions must take into account the storage and reference of these manual pages. Relevant factors include language (including geographical-based differences), and character code set.

> 必须在/usr/share/man的结构中做出规定，以支持用不同（或多种）语言编写的手册页。这些规定必须考虑到这些手册页面的存储和参考。相关因素包括语言（包括基于地理的差异）和字符代码集。

This naming of language subdirectories of /usr/share/man is based on Appendix E of the POSIX 1003.1 standard which describes the locale identification string - the most well-accepted method to describe a cultural environment. The `<locale>`{=html} string is:

> /usr/share/man的语言子目录的命名基于POSIX 1003.1标准的附录E，该标准描述了语言环境标识字符串，这是描述文化环境的最受欢迎的方法。“＜locale＞”｛=html｝字符串为：

`<language>`{=html}\[\_`<territory>`{=html}\]\[.`<character-set>`{=html}\]\[,`<version>`{=html}\]

The `<language>`{=html} field must be taken from ISO 639 (a code for the representation of names of languages). It must be two characters wide and specified with lowercase letters only.

> `<language>`{=html}字段必须取自ISO 639（表示语言名称的代码）。它必须有两个字符宽，并且只能用小写字母指定。

The `<territory>`{=html} field must be the two-letter code of ISO 3166 (a specification of representations of countries), if possible. (Most people are familiar with the two-letter codes used for the country codes in email addresses.) It must be two characters wide and specified with uppercase letters only. \[33\]

> 如果可能的话，`<terrange>`{=html}字段必须是ISO 3166（国家表示规范）的两个字母代码。（大多数人都熟悉电子邮件地址中用于国家/地区代码的两个字母代码。）它必须有两个字符宽，并且只能用大写字母指定\[33\]

The `<character-set>`{=html} field must represent the standard describing the character set. If the ­`<character-set>`{=html} field is just a numeric specification, the number represents the number of the international standard describing the character set. It is recommended that this be a numeric representation if possible (ISO standards, especially), not include additional punctuation symbols, and that any letters be in lowercase.

> “＜字符集＞”｛=html｝字段必须表示描述字符集的标准。如果`<字符集>`{=html}字段只是一个数字规范，则该数字表示描述字符集的国际标准的编号。如果可能的话，建议使用数字表示（尤其是ISO标准），不包括额外的标点符号，并且任何字母都要小写。

A parameter specifying a `<version>`{=html} of the profile may be placed after the ­ `<character-set>`{=html} field, delimited by a comma. This may be used to discriminate between different cultural needs; for instance, dictionary order versus a more systems-oriented collating order. This standard recommends not using the `<version>`{=html} field, unless it is necessary.

> 指定配置文件的“＜版本＞”｛=html｝的参数可以放在“＜字符集＞”{=html}字段后面，用逗号分隔。这可能被用来区分不同的文化需求；例如，字典顺序与更面向系统的排序顺序。本标准建议除非必要，否则不要使用`<version>`{=html}字段。

Systems which use a unique language and code set for all manual pages may omit the `<locale>`{=html} substring and store all manual pages in `<mandir>`{=html}. For example, systems which only have English manual pages coded with ASCII, may store manual pages (the man

> 为所有手动页面使用唯一语言和代码集的系统可以省略“＜locale＞”｛=html｝子字符串，并将所有手动页面存储在“＜mandir＞”｛=html｝中。例如，只有英文手册页用ASCII编码的系统可能存储手册页（

```{=html}
<section>
```

directories) directly in /usr/share/man. (That is the traditional circumstance and arrangement, in fact.)

> 目录）。（事实上，这是传统的环境和安排。）

Countries for which there is a well-accepted standard character code set may omit the ­`<character-set>`{=html} field, but it is strongly recommended that it be included, especially for countries with several competing standards.

> 有一个公认的标准字符代码集的国家可能会省略`<字符集>`{=html}字段，但强烈建议将其包括在内，特别是对于有几个竞争标准的国家。

Various examples:

Language Territory Character Set Directory English - ASCII /usr/share/man/en English United Kingdom ISO 8859-15 /usr/share/man/en_GB English United States ASCII /usr/share/man/en_US French Canada ISO 8859-1 /usr/share/man/fr_CA French France ISO 8859-1 /usr/share/man/fr_FR German Germany ISO 646 /usr/share/man/de_DE.646 German Germany ISO 6937 /usr/share/man/de_DE.6937 German Germany ISO 8859-1 /usr/share/man/de_DE.88591 German Switzerland ISO 646 /usr/share/man/de_CH.646 Japanese Japan JIS /usr/share/man/ja_JP.jis Japanese Japan SJIS /usr/share/man/ja_JP.sjis Japanese Japan UJIS (or EUC-J) /usr/share/man/ja_JP.ujis

> 语言区域字符集目录英语-ASCII/usr/share/man/en英语英国ISO 8859-15/usr/share-man/en_GB英语美国ASCII/usr\share/man/en_US法属加拿大ISO 8859-1/usr/share/man/fr_CA法属法国ISO 8859-1/usr/share/main/fr_fr德国ISO 646/usr/share/mam/de_de.646德国ISO 6937/usr/share/man/de_de.6937德国ISO 8859-1/usr/share/man/de_de.88591德国-瑞士ISO 646/usr/share/man/de_CH.646日本JIS/usr/share/mam/ja_JP.js日本SJIS/usr/share/main/ja_JP.SJIS日本UJIS（或EUC-J）/usr/share/man/ja_JP.UJIS

Similarly, provision must be made for manual pages which are architecture-dependent, such as documentation on device-drivers or low-level system administration commands. These must be placed under an `<arch>`{=html} directory in the appropriate man

> 同样，必须提供依赖于体系结构的手动页面，例如设备驱动程序或低级系统管理命令的文档。这些必须放在适当的man中的“＜arch＞”｛=html｝目录下

```{=html}
<section>
```

directory; for example, a man page for the i386 ctrlaltdel(8) command might be placed in /usr/share/man/`<locale>`{=html}/man8/i386/ ctrlaltdel.8.

> 目录例如，i386-ctrlaltdel（8）命令的手册页可以放在/usr/share/man/`<locale>`{=html}/man8/i386/ctrlaltdel.8中。

Manual pages for commands and data under /usr/local are stored in /usr/local/ man. Manual pages for X11R6 are stored in /usr/X11R6/man. It follows that all manual page hierarchies in the system must have the same structure as /usr/ share/man.

> /usr/local下的命令和数据的手动页面存储在/usr/local/man中。X11R6的手动页面保存在/usr/X11R6/man中。因此，系统中的所有手动页面层次结构都必须具有与/usr/share/man相同的结构。

The cat page sections (cat

```{=html}
<section>
```

) containing formatted manual page entries are also found within subdirectories of `<mandir>`{=html}/`<locale>`{=html}, but are not required nor may they be distributed in lieu of nroff source manual pages.

> )在`<mandir>`{=html}/`<locale>`{=html}的子目录中也可以找到包含格式化的手动页面条目，但它们不是必需的，也不能代替nroff源手动页面进行分发。

The numbered sections "1" through "8" are traditionally defined. In general, the file name for manual pages located within a particular section end with .

> 编号部分“1”至“8”是传统定义。通常，位于特定节中的手册页的文件名以结尾。

```{=html}
<section>
```
.

In addition, some large sets of application-specific manual pages have an additional suffix appended to the manual page filename. For example, the MH mail handling system manual pages must have mh appended to all MH manuals. All X Window System manual pages must have an x appended to the filename.

> 此外，一些大型的特定于应用程序的手册页在手册页文件名后面附加了一个附加后缀。例如，MH邮件处理系统手册页面必须在所有MH手册后附加MH。所有X Window System手册页的文件名后面都必须附加一个X。

The practice of placing various language manual pages in appropriate subdirectories of /usr/share/man also applies to the other manual page hierarchies, such as /usr/local/man and /usr/X11R6/man. (This portion of the standard also applies later in the section on the optional /var/cache/man structure.)

> 将各种语言的手册页放在/usr/share/man的相应子目录中的做法也适用于其他手册页层次结构，如/usr/local/man和/usr/X11R6/man。（本标准的这一部分也适用于后面关于可选/var/cache/man结构的部分。）

------------------------------------------------------------------------

/usr/share/misc : Miscellaneous architecture-independent data

This directory contains miscellaneous architecture-independent files which don't require a separate subdirectory under /usr/share.

> 该目录包含各种与体系结构无关的文件，这些文件不需要在/usr/share下单独的子目录。

------------------------------------------------------------------------

Specific Options

The following files, or symbolic links to files, must be in /usr/share/misc, if the corresponding subsystem is installed:

> 如果安装了相应的子系统，则以下文件或文件的符号链接必须位于/usr/share/misc中：

File Description ascii ASCII character set table (optional) magic Default list of magic numbers for the file command (optional) termcap Terminal capability database (optional) termcap.db Terminal capability database (optional)

> 文件描述ascii ascii字符集表（可选）magic文件命令的默认幻数列表（可选）termcap终端能力数据库（可选）termcap.db终端能力数据库

Other (application-specific) files may appear here, but a distributor may place them in /usr/lib at their discretion. \[34\]

> 其他（特定于应用程序的）文件可能会出现在此处，但分发服务器可以自行决定将它们放在/usr/lib中\[34\]

------------------------------------------------------------------------

/usr/share/sgml : SGML data (optional)

Purpose

/usr/share/sgml contains architecture-independent files used by SGML applications, such as ordinary catalogs (not the centralized ones, see /etc/ sgml), DTDs, entities, or style sheets.

> /usr/share/sgml包含sgml应用程序使用的与体系结构无关的文件，例如普通目录（而不是集中式目录，请参见/etc/sgml）、DTD、实体或样式表。

------------------------------------------------------------------------

Specific Options

The following directories, or symbolic links to directories, must be in /usr/ share/sgml, if the corresponding subsystem is installed:

> 如果安装了相应的子系统，则以下目录或指向目录的符号链接必须位于/usr/share/sgml中：

Directory Description docbook docbook DTD (optional) tei tei DTD (optional) html html DTD (optional) mathml mathml DTD (optional)

> 目录描述docbook docbook DTD（可选）tei-tei DTD（可选

Other files that are not specific to a given DTD may reside in their own subdirectory.

> 非特定于给定DTD的其他文件可能位于它们自己的子目录中。

------------------------------------------------------------------------

/usr/share/xml : XML data (optional)

Purpose

/usr/share/xml contains architecture-independent files used by XML applications, such as ordinary catalogs (not the centralized ones, see /etc/ sgml), DTDs, entities, or style sheets.

> /usr/share/xml包含xml应用程序使用的与体系结构无关的文件，例如普通目录（而不是集中式目录，请参见/etc/sgml）、DTD、实体或样式表。

------------------------------------------------------------------------

Specific Options

The following directories, or symbolic links to directories, must be in /usr/ share/xml, if the corresponding subsystem is installed:

> 如果安装了相应的子系统，则以下目录或指向目录的符号链接必须位于/usr/share/xml中：

Directory Description docbook docbook XML DTD (optional) xhtml XHTML DTD (optional) mathml MathML DTD (optional)

> 目录描述docbook docbook XML DTD（可选）xhtml xhtml DTD（可选

------------------------------------------------------------------------

/usr/src : Source code (optional)

Purpose

Source code may be place placed in this subdirectory, only for reference purposes. \[35\]

> 源代码可以放在此子目录中，仅供参考\[35\]

------------------------------------------------------------------------

Chapter 5. The /var Hierarchy

Purpose

/var contains variable data files. This includes spool directories and files, administrative and logging data, and transient and temporary files.

> /var包含变量数据文件。这包括假脱机目录和文件、管理和日志记录数据以及临时和临时文件。

Some portions of /var are not shareable between different systems. For instance, /var/log, /var/lock, and /var/run. Other portions may be shared, notably /var/mail, /var/cache/man, /var/cache/fonts, and /var/spool/news.

> /var/的某些部分不可在不同的系统之间共享。例如，/var/log、/var/lock和/var/run。其他部分可以共享，特别是/var/mail、/var/cache/man、/var/cache/fonts和/var/spool/news。

/var is specified here in order to make it possible to mount /usr read-only. Everything that once went into /usr that is written to during system operation (as opposed to installation and software maintenance) must be in /var.

> /这里指定了var，以便可以以只读方式装载/usr。在系统操作期间（与安装和软件维护相反）写入/usr/的所有内容都必须在/var中。

If /var cannot be made a separate partition, it is often preferable to move / var out of the root partition and into the /usr partition. (This is sometimes done to reduce the size of the root partition or when space runs low in the root partition.) However, /var must not be linked to /usr because this makes separation of /usr and /var more difficult and is likely to create a naming conflict. Instead, link /var to /usr/var.

> 如果不能将/var/作为一个单独的分区，通常最好将其从根分区移到/usr/分区。（有时这样做是为了减小根分区的大小，或者当根分区中的空间不足时。）但是，/var/不能链接到/usr/，因为这会使/usr/和/var/的分离更加困难，并且可能会产生命名冲突。相反，将/var/链接到/usr/var。

Applications must generally not add directories to the top level of /var. Such directories should only be added if they have some system-wide implication, and in consultation with the FHS mailing list.

> 应用程序通常不能将目录添加到/var的顶层。只有当这些目录具有系统范围的含义，并与FHS邮件列表协商后，才应添加这些目录。

------------------------------------------------------------------------

Requirements

The following directories, or symbolic links to directories, are required in / var.

> /var中需要以下目录或指向目录的符号链接。

Directory Description cache Application cache data lib Variable state information local Variable data for /usr/local lock Lock files log Log files and directories opt Variable data for /opt run Data relevant to running processes spool Application spool data tmp Temporary files preserved between system reboots

> 目录描述缓存应用程序缓存数据库变量状态信息本地/usr/local-lock的变量数据锁定文件日志日志文件和目录opt-run的变量数据与运行进程相关的数据spool应用程序spool数据tmp系统重新启动之间保留的临时文件

Several directories are \`reserved' in the sense that they must not be used arbitrarily by some new application, since they would conflict with historical and/or local practice. They are:

> 一些目录是“保留”的，因为它们会与历史和/或当地惯例相冲突，因此某些新应用程序不得随意使用这些目录。它们是：

    /var/backups
    /var/cron
    /var/msgs
    /var/preserve

------------------------------------------------------------------------

Specific Options

The following directories, or symbolic links to directories, must be in /var, if the corresponding subsystem is installed:

> 如果安装了相应的子系统，则以下目录或指向目录的符号链接必须位于/var/中：

Directory Description account Process accounting logs (optional) crash System crash dumps (optional) games Variable game data (optional) mail User mailbox files (optional) yp Network Information Service (NIS) database files (optional)

> 目录描述帐户进程记帐日志（可选）崩溃系统崩溃转储（可选）游戏可变游戏数据（可选）邮件用户邮箱文件（可选）yp网络信息服务（NIS）数据库文件（可选

------------------------------------------------------------------------

/var/account : Process accounting logs (optional)

Purpose

This directory holds the current active process accounting log and the composite process usage data (as used in some UNIX-like systems by lastcomm and sa).

> 该目录保存当前活动进程记帐日志和复合进程使用情况数据（lastcomm和sa在一些类似UNIX的系统中使用）。

------------------------------------------------------------------------

/var/cache : Application cache data

Purpose

/var/cache is intended for cached data from applications. Such data is locally generated as a result of time-consuming I/O or calculation. The application must be able to regenerate or restore the data. Unlike /var/spool, the cached files can be deleted without data loss. The data must remain valid between invocations of the application and rebooting the system.

> /var/cache用于缓存应用程序中的数据。这种数据是由于耗时的I/O或计算而在本地生成的。应用程序必须能够重新生成或恢复数据。与/var/spool不同，可以删除缓存的文件而不会丢失数据。在调用应用程序和重新启动系统之间，数据必须保持有效。

Files located under /var/cache may be expired in an application specific manner, by the system administrator, or both. The application must always be able to recover from manual deletion of these files (generally because of a disk space shortage). No other requirements are made on the data format of the cache directories.

> 位于/var/cache下的文件可能会以特定于应用程序的方式、由系统管理员或两者都过期。应用程序必须始终能够从手动删除这些文件中恢复（通常是因为磁盘空间不足）。对缓存目录的数据格式没有其他要求。

    Rationale: The existence of a separate directory for cached data allows

> 理由：缓存数据的单独目录允许

    system administrators to set different disk and backup policies from other

> 系统管理员设置与其他不同的磁盘和备份策略
    directories in /var.

------------------------------------------------------------------------

Specific Options

Directory Description fonts Locally-generated fonts (optional) man Locally-formatted manual pages (optional) www WWW proxy or cache data (optional) `<package>`{=html} Package specific cache data (optional)

> 目录描述字体本地生成的字体（可选）man本地格式化的手册页（可选）www代理或缓存数据（可选）`<package>`{=html}包特定缓存数据（选项）

------------------------------------------------------------------------

/var/cache/fonts : Locally-generated fonts (optional)

Purpose

The directory /var/cache/fonts should be used to store any dynamically-created fonts. In particular, all of the fonts which are automatically generated by mktexpk must be located in appropriately-named subdirectories of /var/cache/ fonts. \[36\]

> 目录/var/cache/fonts应该用于存储任何动态创建的字体。特别是，mktexpk自动生成的所有字体都必须位于/var/cache/fonths的适当命名的子目录中\[36\]

------------------------------------------------------------------------

Specific Options

Other dynamically created fonts may also be placed in this tree, under appropriately-named subdirectories of /var/cache/fonts.

> 其他动态创建的字体也可以放在这个树中，在/var/cache/fonts的适当命名的子目录下。

------------------------------------------------------------------------

/var/cache/man : Locally-formatted manual pages (optional)

Purpose

This directory provides a standard location for sites that provide a read-only /usr partition, but wish to allow caching of locally-formatted man pages. Sites that mount /usr as writable (e.g., single-user installations) may choose not to use /var/cache/man and may write formatted man pages into the cat

> 该目录为那些提供只读/usr分区但希望缓存本地格式的手册页的站点提供了一个标准位置。将/usr装载为可写的站点（例如，单用户安装）可以选择不使用/var/cache/man，并可以将格式化的手册页写入cat

```{=html}
<section>
```

directories in /usr/share/man directly. We recommend that most sites use one of the following options instead:

> 直接位于/usr/share/man中的目录。我们建议大多数网站使用以下选项之一：

-   Preformat all manual pages alongside the unformatted versions.

-   Allow no caching of formatted man pages, and require formatting to be done each time a man page is brought up.

> -不允许缓存格式化的手册页，并要求每次打开手册页时进行格式化。

-   Allow local caching of formatted man pages in /var/cache/man.

The structure of /var/cache/man needs to reflect both the fact of multiple man page hierarchies and the possibility of multiple language support.

> /var/cache/man的结构需要同时反映多个手册页层次结构的事实和多种语言支持的可能性。

Given an unformatted manual page that normally appears in `<path>`{=html}/man/`<locale>`{=html}/ man

> 给定一个未格式化的手动页面，该页面通常显示在`<path>`{=html}/man/`<locale>`{=html}/man中

```{=html}
<section>
```

, the directory to place formatted man pages in is /var/cache/man/ `<catpath>`{=html}/`<locale>`{=html}/cat

> ，用于放置格式化手册页的目录是/var/cache/man/`<catpath>`{=html}/`<locale>`{=html}/cat

```{=html}
<section>
```

, where `<catpath>`{=html} is derived from `<path>`{=html} by removing any leading usr and/or trailing share pathname components. (Note that the `<locale>`{=html} component may be missing.) \[37\]

> ，其中`<catpath>`{=html}是通过删除任何前导的usr和/或尾部共享路径名组件从`<path>`{=html`派生而来的。（请注意，“＜locale＞”｛=html｝组件可能丢失。）\[37\]

Man pages written to /var/cache/man may eventually be transferred to the appropriate preformatted directories in the source man hierarchy or expired; likewise formatted man pages in the source man hierarchy may be expired if they are not accessed for a period of time.

> 写入/var/cache/Man的手册页最终可能会转移到源手册层次结构中适当的预格式化目录或过期；如果源man层次结构中同样格式化的man页在一段时间内未被访问，则它们可能会过期。

If preformatted manual pages come with a system on read-only media (a CD-ROM, for instance), they must be installed in the source man hierarchy (e.g. /usr/ share/man/cat

> 如果预格式化的手册页带有只读介质（例如CD-ROM）上的系统，则必须将其安装在源man层次结构中（例如/usr/share/man/cat

```{=html}
<section>
```

). /var/cache/man is reserved as a writable cache for formatted manual pages.

> )/var/cache/man被保留为格式化手动页面的可写缓存。

    Rationale: Release 1.2 of the standard specified /var/catman for this

    hierarchy. The path has been moved under /var/cache to better reflect the

> 等级制度路径已移动到/var/cache下，以更好地反映

    dynamic nature of the formatted man pages. The directory name has been

> 格式化手册页的动态特性。目录名已经
    changed to man to allow for enhancing the hierarchy to include

    post-processed formats other than "cat", such as PostScript, HTML, or DVI.

> 非“cat”的后处理格式，如PostScript、HTML或DVI。

------------------------------------------------------------------------

/var/crash : System crash dumps (optional)

Purpose

This directory holds system crash dumps. As of the date of this release of the standard, system crash dumps were not supported under Linux but may be supported by other systems which may comply with the FHS.

> 此目录保存系统崩溃转储。截至本标准发布之日，Linux不支持系统崩溃转储，但可能由符合FHS的其他系统支持。

------------------------------------------------------------------------

/var/games : Variable game data (optional)

Purpose

Any variable data relating to games in /usr should be placed here. /var/games should hold the variable data previously found in /usr; static data, such as help text, level descriptions, and so on, must remain elsewhere, such as /usr/ share/games.

> 任何与/usr中的游戏相关的变量数据都应该放在这里/var/games应该保存以前在/usr/中找到的变量数据；静态数据，如帮助文本、级别描述等，必须保留在其他位置，如/usr/share/games。

    Rationale: /var/games has been given a hierarchy of its own, rather than

> 理由：/var/games有自己的层次结构，而不是
    leaving it merged in with the old /var/lib as in release 1.2. The

    separation allows local control of backup strategies, permissions, and disk

> 分离允许对备份策略、权限和磁盘进行本地控制

    usage, as well as allowing inter-host sharing and reducing clutter in /var/

> 使用，以及允许主机间共享和减少/var/中的混乱/
    lib. Additionally, /var/games is the path traditionally used by BSD.

------------------------------------------------------------------------

/var/lib : Variable state information

Purpose

This hierarchy holds state information pertaining to an application or the system. State information is data that programs modify while they run, and that pertains to one specific host. Users must never need to modify files in /var/ lib to configure a package's operation.

> 此层次结构保存与应用程序或系统有关的状态信息。状态信息是程序在运行时修改的数据，并且属于一个特定的主机。用户永远不需要修改/var/lib中的文件来配置包的操作。

State information is generally used to preserve the condition of an application (or a group of inter-related applications) between invocations and between different instances of the same application. State information should generally remain valid after a reboot, should not be logging output, and should not be spooled data.

> 状态信息通常用于在调用之间以及同一应用程序的不同实例之间保持应用程序（或一组相互关联的应用程序）的状态。状态信息通常应在重新启动后保持有效，不应记录输出，也不应为假脱机数据。

An application (or a group of inter-related applications) must use a subdirectory of /var/lib for its data. There is one required subdirectory, /var /lib/misc, which is intended for state files that don't need a subdirectory; the other subdirectories should only be present if the application in question is included in the distribution. \[38\]

> 一个应用程序（或一组相互关联的应用程序）的数据必须使用/var/lib的子目录。有一个必需的子目录/var/lib/misc，用于不需要子目录的状态文件；只有当有问题的应用程序包含在分发中时，其他子目录才应该存在\[38\]

/var/lib/`<name>`{=html} is the location that must be used for all distribution packaging support. Different distributions may use different names, of course.

> /var/lib/`<name>`{=html}是所有分发包支持必须使用的位置。当然，不同的发行版可能使用不同的名称。

------------------------------------------------------------------------

Requirements

The following directories, or symbolic links to directories, are required in / var/lib:

> /var/lib中需要以下目录或指向目录的符号链接：

Directory Description misc Miscellaneous state data

------------------------------------------------------------------------

Specific Options

The following directories, or symbolic links to directories, must be in /var/ lib, if the corresponding subsystem is installed:

> 如果安装了相应的子系统，则以下目录或指向目录的符号链接必须位于/var/lib中：

Directory Description `<editor>`{=html} Editor backup files and state (optional) `<pkgtool>`{=html} Packaging support files (optional) `<package>`{=html} State data for packages and subsystems (optional) hwclock State directory for hwclock (optional) xdm X display manager variable data (optional)

> 目录描述`<editor>`｛=html｝编辑器备份文件和状态

------------------------------------------------------------------------

/var/lib/`<editor>`{=html} : Editor backup files and state (optional)

Purpose

These directories contain saved files generated by any unexpected termination of an editor (e.g., elvis, jove, nvi).

> 这些目录包含由编辑器（例如elvis、jove、nvi）的任何意外终止所生成的已保存文件。

Other editors may not require a directory for crash-recovery files, but may require a well-defined place to store other information while the editor is running. This information should be stored in a subdirectory under /var/lib (for example, GNU Emacs would place lock files in /var/lib/emacs/lock).

> 其他编辑器可能不需要崩溃恢复文件的目录，但可能需要在编辑器运行时有一个定义良好的位置来存储其他信息。这些信息应该存储在/var/lib下的子目录中（例如，GNU Emacs会将锁定文件放在/var/lib/Emacs/lock中）。

Future editors may require additional state information beyond crash-recovery files and lock files - this information should also be placed under /var/lib/ `<editor>`{=html}.

> 未来的编辑器可能需要崩溃恢复文件和锁定文件之外的其他状态信息，这些信息也应该放在/var/lib/`<editor>`{=html}下。

    Rationale: Previous Linux releases, as well as all commercial vendors, use

> 理由：以前的Linux版本以及所有商业供应商都使用
    /var/preserve for vi or its clones. However, each editor uses its own

    format for these crash-recovery files, so a separate directory is needed

> 这些故障恢复文件的格式，因此需要一个单独的目录
    for each editor.

    Editor-specific lock files are usually quite different from the device or

> 编辑器特定的锁定文件通常与设备或

    resource lock files that are stored in /var/lock and, hence, are stored

> 存储在/var/lock中的资源锁定文件，因此被存储
    under /var/lib.

------------------------------------------------------------------------

/var/lib/hwclock : State directory for hwclock (optional)

Purpose

This directory contains the file /var/lib/hwclock/adjtime.

    Rationale: In FHS 2.1, this file was /etc/adjtime, but as hwclock updates

> 理由：在FHS 2.1中，该文件是/etc/adjtime，但随着硬件时钟的更新
    it, that was obviously incorrect.

------------------------------------------------------------------------

/var/lib/misc : Miscellaneous variable data

Purpose

This directory contains variable data not placed in a subdirectory in /var/lib. An attempt should be made to use relatively unique names in this directory to avoid namespace conflicts. \[39\]

> 此目录包含未放置在/var/lib子目录中的变量数据。应尝试在此目录中使用相对唯一的名称，以避免名称空间冲突\[39\]

------------------------------------------------------------------------

/var/lock : Lock files

Purpose

Lock files should be stored within the /var/lock directory structure.

Lock files for devices and other resources shared by multiple applications, such as the serial device lock files that were originally found in either /usr/ spool/locks or /usr/spool/uucp, must now be stored in /var/lock. The naming convention which must be used is "LCK.." followed by the base name of the device. For example, to lock /dev/ttyS0 the file "LCK..ttyS0" would be created. \[40\]

> 多个应用程序共享的设备和其他资源的锁定文件，例如最初在/usr/spool/locks或/usr/spool/uucp中找到的串行设备锁定文件，现在必须存储在/var/Lock中。必须使用的命名约定是“LCK..”，后跟设备的基本名称。例如，要锁定/dev/ttyS0，将创建文件“LCK..tyS0”\[40\]

The format used for the contents of such lock files must be the HDB UUCP lock file format. The HDB format is to store the process identifier (PID) as a ten byte ASCII decimal number, with a trailing newline. For example, if process 1230 holds a lock file, it would contain the eleven characters: space, space, space, space, space, space, one, two, three, zero, and newline.

> 用于此类锁定文件内容的格式必须是HDB UUCP锁定文件格式。HDB格式是将进程标识符（PID）存储为十字节ASCII十进制数，后面有一条换行符。例如，如果进程1230持有一个锁定文件，则它将包含十一个字符：空格、空格、空间、空格、一、二、三、零和换行符。

------------------------------------------------------------------------

/var/log : Log files and directories

Purpose

This directory contains miscellaneous log files. Most logs must be written to this directory or an appropriate subdirectory.

> 此目录包含杂项日志文件。大多数日志必须写入该目录或适当的子目录。

------------------------------------------------------------------------

Specific Options

The following files, or symbolic links to files, must be in /var/log, if the corresponding subsystem is installed:

> 如果安装了相应的子系统，则以下文件或文件的符号链接必须在/var/log中：

File Description lastlog record of last login of each user messages system messages from syslogd wtmp record of all logins and logouts

> 文件描述每个用户最后一次登录的lastlog记录消息系统消息来自syslogd所有登录和注销的wtmp记录

------------------------------------------------------------------------

/var/mail : User mailbox files (optional)

Purpose

The mail spool must be accessible through /var/mail and the mail spool files must take the form `<username>`{=html}. \[41\]

> 邮件假脱机必须可以通过/var/mail访问，并且邮件假脱机文件的格式必须为`<username>`{=html}\[41\]

User mailbox files in this location must be stored in the standard UNIX mailbox format.

> 此位置中的用户邮箱文件必须以标准UNIX邮箱格式存储。

    Rationale: The logical location for this directory was changed from /var/

> 理由：该目录的逻辑位置已从/var/更改/
    spool/mail in order to bring FHS in-line with nearly every UNIX

    implementation. This change is important for inter-operability since a

> 实施这一变化对互操作性很重要，因为

    single /var/mail is often shared between multiple hosts and multiple UNIX

> 单个/var/mail通常在多个主机和多个UNIX之间共享
    implementations (despite NFS locking issues).

    It is important to note that there is no requirement to physically move the

> 需要注意的是，不需要对

    mail spool to this location. However, programs and header files must be

> 邮件假脱机到此位置。但是，程序和头文件必须
    changed to use /var/mail.

------------------------------------------------------------------------

/var/opt : Variable data for /opt

Purpose

Variable data of the packages in /opt must be installed in /var/opt/`<subdir>`{=html}, where `<subdir>`{=html} is the name of the subtree in /opt where the static data from an add-on software package is stored, except where superseded by another file in / etc. No structure is imposed on the internal arrangement of /var/opt/`<subdir>`{=html}.

> /opt中软件包的变量数据必须安装在/var/opt/`<subdir>`{=html}中，其中`<subdir>`{=]html}是/opt中子树的名称，其中存储来自附加软件包的静态数据，除非被/中的另一个文件取代。/var/opt/`<subdir>`{=html}的内部排列没有任何结构。

    Rationale: Refer to the rationale for /opt.

------------------------------------------------------------------------

/var/run : Run-time variable data

Purpose

This directory contains system information data describing the system since it was booted. Files under this directory must be cleared (removed or truncated as appropriate) at the beginning of the boot process. Programs may have a subdirectory of /var/run; this is encouraged for programs that use more than one run-time file. \[42\] Process identifier (PID) files, which were originally placed in /etc, must be placed in /var/run. The naming convention for PID files is `<program-name>`{=html}.pid. For example, the crond PID file is named /var/run/ crond.pid.

> 此目录包含自系统启动以来描述系统的系统信息数据。在启动过程开始时，必须清除（根据需要删除或截断）此目录下的文件。程序可能有/var/run的子目录；对于使用多个运行时文件的程序，鼓励这样做\[42\]最初放在/etc/etc中的进程标识符（PID）文件必须放在/var/run中。PID文件的命名约定为`<program-name>`{=html}.PID。例如，crond PID文件的名称为/var/run/crond.PID。

------------------------------------------------------------------------

Requirements

The internal format of PID files remains unchanged. The file must consist of the process identifier in ASCII-encoded decimal, followed by a newline character. For example, if crond was process number 25, /var/run/crond.pid would contain three characters: two, five, and newline.

> PID文件的内部格式保持不变。文件必须包含ASCII编码十进制的进程标识符，后跟换行符。例如，如果crond是进程号25，/var/run/crond.pid将包含三个字符：2、5和换行符。

Programs that read PID files should be somewhat flexible in what they accept; i.e., they should ignore extra whitespace, leading zeroes, absence of the trailing newline, or additional lines in the PID file. Programs that create PID files should use the simple specification located in the above paragraph.

> 读取PID文件的程序在接受什么方面应该有一定的灵活性；即，它们应该忽略PID文件中的额外空白、前导零、缺少尾部换行符或其他行。创建PID文件的程序应该使用上面段落中的简单规范。

The utmp file, which stores information about who is currently using the system, is located in this directory.

> utmp文件位于此目录中，该文件存储有关当前使用系统的人员的信息。

System programs that maintain transient UNIX-domain sockets must place them in this directory.

> 维护临时UNIX域套接字的系统程序必须将它们放在此目录中。

------------------------------------------------------------------------

/var/spool : Application spool data

Purpose

/var/spool contains data which is awaiting some kind of later processing. Data in /var/spool represents work to be done in the future (by a program, user, or administrator); often data is deleted after it has been processed. \[43\]

> /var/spool包含等待稍后处理的数据。/var/spool中的数据表示将来要完成的工作（由程序、用户或管理员完成）；数据通常在处理后被删除\[43\]

------------------------------------------------------------------------

Specific Options

The following directories, or symbolic links to directories, must be in /var/ spool, if the corresponding subsystem is installed:

> 如果安装了相应的子系统，则以下目录或指向目录的符号链接必须位于/var/spool中：

Directory Description lpd Printer spool directory (optional) mqueue Outgoing mail queue (optional) news News spool directory (optional) rwho Rwhod files (optional) uucp Spool directory for UUCP (optional)

> 目录描述lpd打印机后台处理目录（可选）mqueue传出邮件队列（可选）新闻后台处理目录

------------------------------------------------------------------------

/var/spool/lpd : Line-printer daemon print queues (optional)

Purpose

The lock file for lpd, lpd.lock, must be placed in /var/spool/lpd. It is suggested that the lock file for each printer be placed in the spool directory for that specific printer and named lock.

> lpd的锁文件lpd.lock必须放在/var/spool/lpd中。建议将每个打印机的锁定文件放在该特定打印机的spool目录中，并命名为lock。

------------------------------------------------------------------------

Specific Options

Directory Description printer Spools for a specific printer (optional)

------------------------------------------------------------------------

/var/spool/rwho : Rwhod files (optional)

Purpose

This directory holds the rwhod information for other systems on the local net.

> 此目录保存本地网络上其他系统的rwhod信息。

    Rationale: Some BSD releases use /var/rwho for this data; given its

    historical location in /var/spool on other systems and its approximate fit

> 其他系统上/var/spool的历史位置及其近似拟合
    to the definition of `spooled' data, this location was deemed more
    appropriate.

------------------------------------------------------------------------

/var/tmp : Temporary files preserved between system reboots

Purpose

The /var/tmp directory is made available for programs that require temporary files or directories that are preserved between system reboots. Therefore, data stored in /var/tmp is more persistent than data in /tmp.

> /var/tmp目录可用于需要在系统重新启动之间保留的临时文件或目录的程序。因此，存储在/var/tmp中的数据比存储在/tmp中的数据更持久。

Files and directories located in /var/tmp must not be deleted when the system is booted. Although data stored in /var/tmp is typically deleted in a site-specific manner, it is recommended that deletions occur at a less frequent interval than /tmp.

> 系统启动时，不得删除位于/var/tmp中的文件和目录。尽管存储在/var/tmp中的数据通常以特定站点的方式删除，但建议删除的频率低于/tmp。

------------------------------------------------------------------------

/var/yp : Network Information Service (NIS) database files (optional)

Purpose

Variable data for the Network Information Service (NIS), formerly known as the Sun Yellow Pages (YP), must be placed in this directory.

> 网络信息服务（NIS）的变量数据，以前称为太阳黄页（YP），必须放在此目录中。

    Rationale: /var/yp is the standard directory for NIS (YP) data and is
    almost exclusively used in NIS documentation and systems. [44]

------------------------------------------------------------------------

Chapter 6. Operating System Specific Annex

This section is for additional requirements and recommendations that only apply to a specific operating system. The material in this section should never conflict with the base standard.

> 本节提供仅适用于特定操作系统的附加要求和建议。本节中的材料不得与基本标准相冲突。

------------------------------------------------------------------------

Linux

This is the annex for the Linux operating system.

------------------------------------------------------------------------

/ : Root directory

On Linux systems, if the kernel is located in /, we recommend using the names vmlinux or vmlinuz, which have been used in recent Linux kernel source packages.

> 在Linux系统上，如果内核位于/中，我们建议使用名称vmlinux或vmlinuz，这些名称已在最近的Linux内核源代码包中使用。

------------------------------------------------------------------------

/bin : Essential user command binaries (for use by all users)

Linux systems which require them place these additional files into /bin:

-   setserial

------------------------------------------------------------------------

/dev : Devices and special files

The following devices must exist under /dev.

/dev/null

    All data written to this device is discarded. A read from this device will

> 写入此设备的所有数据都将被丢弃。从该设备读取将
    return an EOF condition.

/dev/zero

    This device is a source of zeroed out data. All data written to this device

> 此设备是归零数据的来源。写入此设备的所有数据

    is discarded. A read from this device will return as many bytes containing

> 被丢弃。从该设备读取将返回包含
    the value zero as was requested.

/dev/tty

    This device is a synonym for the controlling terminal of a process. Once

> 该设备是进程的控制终端的同义词。一旦

    this device is opened, all reads and writes will behave as if the actual

> 该设备已打开，所有读取和写入操作将如同实际
    controlling terminal device had been opened.

    Rationale: Previous versions of the FHS had stricter requirements for /dev.

> 理由：以前版本的FHS对/dev有更严格的要求。

    Other devices may also exist in /dev. Device names may exist as symbolic

> /dev中也可能存在其他设备。设备名称可能以符号形式存在

    links to other device nodes located in /dev or subdirectories of /dev.

> 指向位于/dev或/dev子目录中的其他设备节点的链接。
    There is no requirement concerning major/minor number values.

------------------------------------------------------------------------

/etc : Host-specific system configuration

Linux systems which require them place these additional files into /etc.

-   lilo.conf

------------------------------------------------------------------------

/lib64 and /lib32 : 64/32-bit libraries (architecture dependent)

The 64-bit architectures PPC64, s390x, sparc64 and AMD64 must place 64-bit libraries in /lib64, and 32-bit (or 31-bit on s390) libraries in /lib.

> 64位体系结构PPC64、s390x、sparc64和AMD64必须在/lib64中放置64位库，在/lib中放置32位（或s390上的31位）库。

The 64-bit architecture IA64 must place 64-bit libraries in /lib.

    Rationale: This is a refinement of the general rules for /lib<qual> and /

> 理由：这是对/lib<qual>和/

    usr/lib<qual>. The architectures PPC64, s390x, sparc64 and AMD64 support

> usr/lib＜qual＞。体系结构PPC64、s390x、sparc64和AMD64支持

    support both 32-bit (for s390 more precise 31-bit) and 64-bit programs.

> 支持32位（对于s390，更精确地说是31位）和64位程序。

    Using lib for 32-bit binaries allows existing binaries from the 32-bit

> 对32位二进制文件使用lib允许从
    systems to work without any changes: such binaries are expected to be

    numerous. IA-64 uses a different scheme, reflecting the deprecation of

> 很多的IA-64使用了不同的方案，反映了
    32-bit binaries (and hence libraries) on that architecture.

------------------------------------------------------------------------

/proc : Kernel and process information virtual filesystem

The proc filesystem is the de-facto standard Linux method for handling process and system information, rather than /dev/kmem and other similar methods. We strongly encourage this for the storage and retrieval of process information as well as other kernel and memory information.

> proc文件系统是处理进程和系统信息的事实上的标准Linux方法，而不是/dev/kmem和其他类似的方法。我们强烈鼓励将其用于进程信息以及其他内核和内存信息的存储和检索。

------------------------------------------------------------------------

/sbin : Essential system binaries

Linux systems place these additional files into /sbin.

-   Second extended filesystem commands (optional):

    -   badblocks

    -   dumpe2fs

    -   e2fsck

    -   mke2fs

    -   mklost+found

    -   tune2fs

-   Boot-loader map installer (optional):

    -   lilo

Optional files for /sbin:

-   Static binaries:

    -   ldconfig

    -   sln

    -   ssync

    Static ln (sln) and static sync (ssync) are useful when things go wrong. The primary use of sln (to repair incorrect symlinks in /lib after a poorly orchestrated upgrade) is no longer a major concern now that the ldconfig program (usually located in /usr/sbin) exists and can act as a guiding hand in upgrading the dynamic libraries. Static sync is useful in some emergency situations. Note that these need not be statically linked versions of the standard ln and sync, but may be.

> 当出现问题时，静态ln（sln）和静态同步（ssync）非常有用。由于ldconfig程序（通常位于/usr/sbin中）已经存在，并且可以作为升级动态库的向导，因此sln的主要用途（在精心安排的升级后修复/lib中不正确的符号链接）不再是主要问题。静态同步在某些紧急情况下很有用。请注意，这些不需要是标准ln和sync的静态链接版本，但可能是。

    The ldconfig binary is optional for /sbin since a site may choose to run ldconfig at boot time, rather than only when upgrading the shared libraries. (It's not clear whether or not it is advantageous to run ldconfig on each boot.) Even so, some people like ldconfig around for the following (all too common) situation:

> ldconfig二进制文件对于/sbin是可选的，因为站点可以选择在启动时运行ldconfig，而不是仅在升级共享库时运行。（目前还不清楚在每次启动时运行ldconfig是否有利。）尽管如此，有些人还是喜欢ldconfig，因为它适用于以下情况（太常见了）：

    1.  I've just removed /lib/`<file>`{=html}.

    2.  I can't find out the name of the library because ls is dynamically linked, I'm using a shell that doesn't have ls built-in, and I don't know about using "echo \*" as a replacement.

> 2.我找不到库的名称，因为ls是动态链接的，我使用的是一个没有内置ls的shell，我不知道是否使用“echo\*”作为替换。

    3.  I have a static sln, but I don't know what to call the link.

-   Miscellaneous:

    -   ctrlaltdel

    -   kbdrate

    So as to cope with the fact that some keyboards come up with such a high repeat rate as to be unusable, kbdrate may be installed in /sbin on some systems.

> 为了应对一些键盘出现如此高的重复率以至于无法使用的事实，kbdrate可能会安装在一些系统的/sbin中。

    Since the default action in the kernel for the Ctrl-Alt-Del key combination is an instant hard reboot, it is generally advisable to disable the behavior before mounting the root filesystem in read-write mode. Some init suites are able to disable Ctrl-Alt-Del, but others may require the ctrlaltdel program, which may be installed in /sbin on those systems.

> 由于内核中Ctrl-Alt-Del键组合的默认操作是即时硬重新启动，因此通常建议在以读写模式安装根文件系统之前禁用该行为。一些init套件可以禁用Ctrl-Alt-Del，但其他套件可能需要ctrlaltdel程序，该程序可能安装在这些系统的/sbin中。

------------------------------------------------------------------------

/usr/include : Header files included by C programs

These symbolic links are required if a C or C++ compiler is installed and only for systems not based on glibc.

> 如果安装了C或C++编译器，并且仅适用于不基于glibc的系统，则需要这些符号链接。

    /usr/include/asm -> /usr/src/linux/include/asm-<arch>
    /usr/include/linux -> /usr/src/linux/include/linux

------------------------------------------------------------------------

/usr/src : Source code

For systems based on glibc, there are no specific guidelines for this directory. For systems based on Linux libc revisions prior to glibc, the following guidelines and rationale apply:

> 对于基于glibc的系统，没有针对该目录的特定指南。对于基于glibc之前的Linux libc修订版的系统，适用以下指导原则和基本原理：

The only source code that should be placed in a specific location is the Linux kernel source code. It is located in /usr/src/linux.

> 唯一应该放在特定位置的源代码是Linux内核源代码。它位于/usr/src/linux中。

If a C or C++ compiler is installed, but the complete Linux kernel source code is not installed, then the include files from the kernel source code must be located in these directories:

> 如果安装了C或C++编译器，但没有安装完整的Linux内核源代码，则内核源代码中的include文件必须位于以下目录中：

    /usr/src/linux/include/asm-<arch>
    /usr/src/linux/include/linux

`<arch>`{=html} is the name of the system architecture.

    Note: /usr/src/linux may be a symbolic link to a kernel source code tree.

> 注意：/usr/src/linux可能是指向内核源代码树的符号链接。

    Rationale: It is important that the kernel include files be located in /usr

> 理由：内核包含文件位于/usr/

    /src/linux and not in /usr/include so there are no problems when system

> /src/linux，不在/usr/include中，所以当系统
    administrators upgrade their kernel version for the first time.

------------------------------------------------------------------------

/var/spool/cron : cron and at jobs

This directory contains the variable data for the cron and at programs.

------------------------------------------------------------------------

Chapter 7. Appendix

The FHS mailing list

The FHS mailing list is located at <freestandards-fhs-discuss@lists.sourceforge.net>. You can subscribe to the mailing list at this page http://sourceforge.net/projects/freestandards/.

> FHS邮件列表位于<freestandards-fhs-discuss@lists.sourceforge.net>。您可以在此页面订阅邮件列表http://sourceforge.net/projects/freestandards/.

Thanks to Network Operations at the University of California at San Diego who allowed us to use their excellent mailing list server.

> 感谢加州大学圣地亚哥分校的网络运营部门，他们允许我们使用他们出色的邮件列表服务器。

As noted in the introduction, please do not send mail to the mailing list without first contacting the FHS editor or a listed contributor.

> 正如简介中所指出的，在没有首先联系FHS编辑或列出的投稿人的情况下，请不要向邮件列表发送邮件。

------------------------------------------------------------------------

Background of the FHS

The process of developing a standard filesystem hierarchy began in August 1993 with an effort to restructure the file and directory structure of Linux. The FSSTND, a filesystem hierarchy standard specific to the Linux operating system, was released on February 14, 1994. Subsequent revisions were released on October 9, 1994 and March 28, 1995.

> 开发标准文件系统层次结构的过程始于1993年8月，旨在重组Linux的文件和目录结构。FSSTND是一个特定于Linux操作系统的文件系统层次结构标准，于1994年2月14日发布。随后的修订于1994年10月9日和1995年3月28日发布。

In early 1995, the goal of developing a more comprehensive version of FSSTND to address not only Linux, but other UNIX-like systems was adopted with the help of members of the BSD development community. As a result, a concerted effort was made to focus on issues that were general to UNIX-like systems. In recognition of this widening of scope, the name of the standard was changed to Filesystem Hierarchy Standard or FHS for short.

> 1995年初，在BSD开发社区成员的帮助下，实现了开发一个更全面的FSSTND版本的目标，该版本不仅适用于Linux，还适用于其他类UNIX系统。结果，大家齐心协力，把重点放在类UNIX系统的通用问题上。由于认识到范围的扩大，该标准的名称被更改为文件系统层次结构标准（简称FHS）。

Volunteers who have contributed extensively to this standard are listed at the end of this document. This standard represents a consensus view of those and other contributors.

> 本文件末尾列出了为本标准做出广泛贡献的志愿者。该标准代表了这些贡献者和其他贡献者的共识。

------------------------------------------------------------------------

General Guidelines

Here are some of the guidelines that have been used in the development of this standard:

> 以下是本标准制定过程中使用的一些指南：

-   Solve technical problems while limiting transitional difficulties.

-   Make the specification reasonably stable.

-   Gain the approval of distributors, developers, and other decision-makers in relevant development groups and encourage their participation.

> -获得分销商、开发商和相关开发小组其他决策者的批准，并鼓励他们参与。

-   Provide a standard that is attractive to the implementors of different UNIX-like systems.

------------------------------------------------------------------------

Scope

This document specifies a standard filesystem hierarchy for FHS filesystems by specifying the location of files and directories, and the contents of some system files.

> 本文档通过指定文件和目录的位置以及一些系统文件的内容，为FHS文件系统指定了标准的文件系统层次结构。

This standard has been designed to be used by system integrators, package developers, and system administrators in the construction and maintenance of FHS compliant filesystems. It is primarily intended to be a reference and is not a tutorial on how to manage a conforming filesystem hierarchy.

> 本标准旨在供系统集成商、软件包开发人员和系统管理员在构建和维护符合FHS的文件系统时使用。它主要是作为参考，而不是关于如何管理一致的文件系统层次结构的教程。

The FHS grew out of earlier work on FSSTND, a filesystem organization standard for the Linux operating system. It builds on FSSTND to address interoperability issues not just in the Linux community but in a wider arena including 4.4BSD-based operating systems. It incorporates lessons learned in the BSD world and elsewhere about multi-architecture support and the demands of heterogeneous networking.

> FHS源于FSSTND的早期工作，FSSTND是Linux操作系统的文件系统组织标准。它建立在FSSTND的基础上，以解决互操作性问题，不仅在Linux社区，而且在更广泛的领域，包括基于4.4BSD的操作系统。它结合了在BSD世界和其他地方学到的关于多体系结构支持和异构网络需求的经验教训。

Although this standard is more comprehensive than previous attempts at filesystem hierarchy standardization, periodic updates may become necessary as requirements change in relation to emerging technology. It is also possible that better solutions to the problems addressed here will be discovered so that our solutions will no longer be the best possible solutions. Supplementary drafts may be released in addition to periodic updates to this document. However, a specific goal is backwards compatibility from one release of this document to the next.

> 尽管此标准比以前尝试的文件系统层次结构标准化更全面，但随着需求相对于新兴技术的变化，定期更新可能变得必要。也有可能会发现更好的解决方案来解决这里解决的问题，这样我们的解决方案就不再是最好的解决方案。除了定期更新本文件外，还可发布补充草案。然而，一个特定的目标是从本文档的一个版本向后兼容到下一个版本。

Comments related to this standard are welcome. Any comments or suggestions for changes may be directed to the FHS editor (Daniel Quinlan <quinlan@pathname.com>) or the FHS mailing list. Typographical or grammatical comments should be directed to the FHS editor.

> 欢迎对本标准提出意见。任何修改意见或建议可直接向FHS编辑（Daniel Quinlan<quinlan@pathname.com>)或FHS邮件列表。打字或语法注释应直接提交给FHS编辑。

Before sending mail to the mailing list it is requested that you first contact the FHS editor in order to avoid excessive re-discussion of old topics.

> 在将邮件发送到邮件列表之前，请您首先联系FHS编辑，以避免对旧主题进行过多的重新讨论。

Questions about how to interpret items in this document may occasionally arise. If you have need for a clarification, please contact the FHS editor. Since this standard represents a consensus of many participants, it is important to make certain that any interpretation also represents their collective opinion. For this reason it may not be possible to provide an immediate response unless the inquiry has been the subject of previous discussion.

> 关于如何解释本文件中的项目的问题偶尔会出现。如果您需要澄清，请联系FHS编辑。由于这一标准代表了许多参与者的共识，因此必须确保任何解释也代表了他们的集体意见。因此，除非调查是之前讨论的主题，否则可能无法立即做出回应。

------------------------------------------------------------------------

Acknowledgments

The developers of the FHS wish to thank the developers, system administrators, and users whose input was essential to this standard. We wish to thank each of the contributors who helped to write, compile, and compose this standard.

> FHS的开发人员希望感谢开发人员、系统管理员和用户，他们的投入对本标准至关重要。我们要感谢每一位帮助编写、编译和撰写本标准的贡献者。

The FHS Group also wishes to thank those Linux developers who supported the FSSTND, the predecessor to this standard. If they hadn't demonstrated that the FSSTND was beneficial, the FHS could never have evolved.

> FHS集团还要感谢那些支持FSSTND的Linux开发人员，FSSTND是本标准的前身。如果他们没有证明FSSTND是有益的，FHS就永远不会进化。

------------------------------------------------------------------------

Contributors

Brandon S. Allbery <bsa@kf8nh.wariat.org> Keith Bostic <bostic@cs.berkeley.edu> Drew Eckhardt <drew@colorado.edu> Rik Faith <faith@cs.unc.edu> Stephen Harris <sweh@spuddy.mew.co.uk> Ian Jackson <ijackson@cus.cam.ac.uk> Andreas Jaeger <aj@suse.de> John A. Martin <jmartin@acm.org> Ian McCloghrie <ian@ucsd.edu> Chris Metcalf <metcalf@lcs.mit.edu> Ian Murdock <imurdock@debian.org> David C. Niemi <niemidc@clark.net> Daniel Quinlan <quinlan@pathname.com> Eric S. Raymond <esr@thyrsus.com> Rusty Russell <rusty@rustcorp.com.au> Mike Sangrey <mike@sojurn.lns.pa.us> David H. Silber <dhs@glowworm.firefly.com> Thomas Sippel-Dau <t.sippel-dau@ic.ac.uk> Theodore Ts'o <tytso@athena.mit.edu> Stephen Tweedie <sct@dcs.ed.ac.uk> Fred N. van Kempen <waltje@infomagic.com> Bernd Warken <bwarken@mayn.de> Christopher Yeoh <cyeoh@samba.org>

> Brandon S.Allbery<bsa@kf8nh.wariat.org>Keith Bostic<bostic@cs.berkeley.edu>德鲁·埃克哈特<drew@colorado.edu>Rik Faith<faith@cs.unc.edu>斯蒂芬·哈里斯<sweh@spuddy.mew.co.uk>伊恩·杰克逊<ijackson@cus.cam.ac.uk>Andreas Jaeger<aj@suse.de>约翰·A·马丁<jmartin@acm.org>伊恩·麦克洛格里<ian@ucsd.edu>Chris Metcalf<metcalf@lcs.mit.edu>伊恩·默多克<imurdock@debian.org>David C.Niemi<niemidc@clark.net>丹尼尔·昆兰<quinlan@pathname.com>Eric S.Raymond<esr@thyrsus.com>鲁斯蒂·拉塞尔<rusty@rustcorp.com.au>Mike Sangrey<mike@sojurn.lns.pa.us>David H.Silber<dhs@glowworm.firefly.com>Thomas Sippel Dau<t.sippel-dau@ic.ac.uk>西奥多·措<tytso@athena.mit.edu>斯蒂芬·特威迪<sct@dcs.ed.ac.uk>Fred N.van Kempen<waltje@infomagic.com>伯恩德·沃肯<bwarken@mayn.de>Christopher Yeoh<cyeoh@samba.org>

Notes

\[1\] Command binaries that are not essential enough to place into /bin must be placed in /usr/bin, instead. Items that are required only by non-root users (the X Window System, chsh, etc.) are generally not essential enough to be placed into the root partition.

\[2\] Programs necessary to arrange for the boot loader to be able to boot a file must be placed in /sbin. Configuration files for boot loaders must be placed in /etc.

     The GRUB bootloader reads its configurations file before booting, so that

> GRUB引导加载程序在引导之前读取其配置文件，以便

     must be placed in /boot. However, it is a configuration file, so should be

> 必须放置在/boot中。但是，它是一个配置文件，因此应该

     in /etc. The answer here is a symbolic link such as /etc/grub/menu.lst ->

> in等。这里的答案是一个符号链接，例如/etc/grub/menu.lst->
     /boot/menu.lst.

\[3\] On some i386 machines, it may be necessary for /boot to be located on a separate partition located completely below cylinder 1024 of the boot device due to hardware constraints.

     Certain MIPS systems require a /boot partition that is a mounted MS-DOS

> 某些MIPS系统需要安装MS-DOS的/boot分区
     filesystem or whatever other filesystem type is accessible for the

     firmware. This may result in restrictions with respect to usable filenames

> 固件。这可能会导致对可用文件名的限制
     within /boot (only for affected systems).

\[4\] The setup of command scripts invoked at boot time may resemble System V, BSD or other models. Further specification in this area may be added to a future version of this standard.

\[5\] It is recommended that files be stored in subdirectories of /etc rather than directly in /etc.

\[6\] Systems that use the shadow password suite will have additional configuration files in /etc (/etc/shadow and others) and programs in /usr/ sbin (useradd, usermod, and others).

\[7\] On some Linux systems, this may be a symbolic link to /proc/mounts, in which case this exception is not required.

\[8\] /etc/X11/xdm holds the configuration files for xdm. These are most of the files previously found in /usr/lib/X11/xdm. Some local variable data for xdm is stored in /var/lib/xdm.

\[9\] Different people prefer to place user accounts in a variety of places. This section describes only a suggested placement for user home directories; nevertheless we recommend that all FHS-compliant distributions use this as the default location for home directories.

     On small systems, each user's directory is typically one of the many
     subdirectories of /home such as /home/smith, /home/torvalds, /home/

     operator, etc. On large systems (especially when the /home directories are

> 操作员等。在大型系统上（尤其是当/home目录

     shared amongst many hosts using NFS) it is useful to subdivide user home

> 在使用NFS的许多主机之间共享）细分用户主页是有用的

     directories. Subdivision may be accomplished by using subdirectories such

> 目录。细分可以通过使用子目录来完成，例如
     as /home/staff, /home/guests, /home/students, etc.

\[10\] If you want to find out a user's home directory, you should use the getpwent(3) library function rather than relying on /etc/passwd because user information may be stored remotely using systems such as NIS.

\[11\] It is recommended that apart from autosave and lock files programs should refrain from creating non dot files or directories in a home directory without user intervention.

\[12\] Shared libraries that are only necessary for binaries in /usr (such as any X Window binaries) must not be in /lib. Only the shared libraries required to run binaries in /bin and /sbin may be here. In particular, the library libm.so.\* may also be placed in /usr/lib if it is not required by anything in /bin or /sbin.

\[13\] The usual placement of this binary is /usr/bin/cpp.

\[14\] This is commonly used for 64-bit or 32-bit support on systems which support multiple binary formats, but require libraries of the same name. In this case, /lib32 and /lib64 might be the library directories, and /lib a symlink to one of them.

\[15\] /lib`<qual>`{=html}/cpp is still permitted: this allows the case where /lib and / lib`<qual>`{=html} are the same (one is a symbolic link to the other).

\[16\] A compliant implementation with two CDROM drives might have /media/cdrom0 and /media/cdrom1 with /media/cdrom a symlink to either of these.

\[17\] If the home directory of the root account is not stored on the root partition it will be necessary to make certain it will default to / if it can not be located.

     We recommend against using the root account for tasks that can be

     performed as an unprivileged user, and that it be used solely for system

> 以无特权用户身份执行，并且仅用于系统

     administration. For this reason, we recommend that subdirectories for mail

> 管理因此，我们建议邮件的子目录

     and other applications not appear in the root account's home directory,

> 并且其他应用程序没有出现在根帐户的主目录中，
     and that mail for administration roles such as root, postmaster, and
     webmaster be forwarded to an appropriate user.

\[18\] Originally, /sbin binaries were kept in /etc.

\[19\] Deciding what things go into "sbin" directories is simple: if a normal (not a system administrator) user will ever run it directly, then it must be placed in one of the "bin" directories. Ordinary users should not have to place any of the sbin directories in their path.

     For example, files such as chfn which users only occasionally use must

> 例如，用户偶尔使用的chfn等文件必须

     still be placed in /usr/bin. ping, although it is absolutely necessary for

> 仍然放在/usr/bin中。ping，尽管这是绝对必要的

     root (network recovery and diagnosis) is often used by users and must live

> root（网络恢复和诊断）经常被用户使用，并且必须存在
     in /bin for that reason.

     We recommend that users have read and execute permission for everything in

> 我们建议用户对中的所有内容都具有读取和执行权限

     /sbin except, perhaps, certain setuid and setgid programs. The division

> /sbin，除了某些setuid和setgid程序。分区

     between /bin and /sbin was not created for security reasons or to prevent

> 由于安全原因或为了防止

     users from seeing the operating system, but to provide a good partition

> 用户看不到操作系统，但要提供一个好的分区

     between binaries that everyone uses and ones that are primarily used for

> 每个人都使用的二进制文件和主要用于

     administration tasks. There is no inherent security advantage in making /

> 管理任务。制作没有固有的安全优势/
     sbin off-limits for users.

\[20\] This is particularly important as these areas will often contain both files initially installed by the distributor, and those added by the administrator.

\[21\] Examples of such configuration files include Xconfig, XF86Config, or system.twmrc)

\[22\] Miscellaneous architecture-independent application-specific static files and subdirectories must be placed in /usr/share.

\[23\] For example, the perl5 subdirectory for Perl 5 modules and libraries.

\[24\] Some executable commands such as makewhatis and sendmail have also been traditionally placed in /usr/lib. makewhatis is an internal binary and must be placed in a binary directory; users access only catman. Newer sendmail binaries are now placed by default in /usr/sbin. Additionally, systems using a sendmail-compatible mail transfer agent must provide /usr/ sbin/sendmail as a symbolic link to the appropriate executable.

\[25\] Host-specific data for the X Window System must not be stored in /usr/lib/ X11. Host-specific configuration files such as Xconfig or XF86Config must be stored in /etc/X11. This includes configuration data such as system.twmrc even if it is only made a symbolic link to a more global configuration file (probably in /usr/X11R6/lib/X11).

\[26\] The case where /usr/lib and /usr/lib`<qual>`{=html} are the same (one is a symbolic link to the other) these files and the per-application subdirectories will exist.

\[27\] Software placed in / or /usr may be overwritten by system upgrades (though we recommend that distributions do not overwrite data in /etc under these circumstances). For this reason, local software must not be placed outside of /usr/local without good reason.

\[28\] /usr/local/man may be deprecated in future FHS releases, so if all else is equal, making that one a symlink seems sensible.

\[29\] Locally installed system administration programs should be placed in /usr/ local/sbin.

\[30\] Much of this data originally lived in /usr (man, doc) or /usr/lib (dict, terminfo, zoneinfo).

\[31\] Obviously, there are no manual pages in / because they are not required at boot time nor are they required in emergencies. Really.

\[32\] For example, if /usr/local/man has no manual pages in section 4 (Devices), then /usr/local/man/man4 may be omitted.

\[33\] A major exception to this rule is the United Kingdom, which is `GB' in the      ISO 3166, but`UK' for most email addresses.

\[34\] Some such files include: airport, birthtoken, eqnchar, getopt, gprof.callg, gprof.flat, inter.phone, ipfw.samp.filters, ipfw.samp.scripts, keycap.pcvt, mail.help, mail.tildehelp, man.template, map3270, mdoc.template, more.help, na.phone, nslookup.help, operator, scsi_modes, sendmail.hf, style, units.lib, vgrindefs, vgrindefs.db, zipcodes

\[35\] Generally, source should not be built within this hierarchy.

\[36\] This standard does not currently incorporate the TeX Directory Structure (a document that describes the layout TeX files and directories), but it may be useful reading. It is located at ftp://ctan.tug.org/tex/
 to a more global configuration file (probably in /usr/X11R6/lib/X11).

\[26\] The case where /usr/lib and /usr/lib`<qual>`{=html} are the same (one is a symbolic link to the other) these files and the per-application subdirectories will exist.

\[27\] Software placed in / or /usr may be overwritten by system upgrades (though we recommend that distributions do not overwrite data in /etc under these circumstances). For this reason, local software must not be placed outside of /usr/local without good reason.

\[28\] /usr/local/man may be deprecated in future FHS releases, so if all else is equal, making that one a symlink seems sensible.

\[29\] Locally installed system administration programs should be placed in /usr/ local/sbin.

\[30\] Much of this data originally lived in /usr (man, doc) or /usr/lib (dict, terminfo, zoneinfo).

\[31\] Obviously, there are no manual pages in / because they are not required at boot time nor are they required in emergencies. Really.

\[32\] For example, if /usr/local/man has no manual pages in section 4 (Devices), then /usr/local/man/man4 may be omitted.

\[33\] A major exception to this rule is the United Kingdom, which is `GB' in the      ISO 3166, but`UK' for most email addresses.

\[34\] Some such files include: airport, birthtoken, eqnchar, getopt, gprof.callg, gprof.flat, inter.phone, ipfw.samp.filters, ipfw.samp.scripts, keycap.pcvt, mail.help, mail.tildehelp, man.template, map3270, mdoc.template, more.help, na.phone, nslookup.help, operator, scsi_modes, sendmail.hf, style, units.lib, vgrindefs, vgrindefs.db, zipcodes

\[35\] Generally, source should not be built within this hierarchy.

\[36\] This standard does not currently incorporate the TeX Directory Structure (a document that describes the layout TeX files and directories), but it may be useful reading. It is located at ftp://ctan.tug.org/tex/

\[37\] For example, /usr/share/man/man1/ls.1 is formatted into /var/cache/man/ cat1/ls.1, and /usr/X11R6/man/`<locale>`{=html}/man3/XtClass.3x into /var/cache/man /X11R6/`<locale>`{=html}/cat3/XtClass.3x.

\[38\] An important difference between this version of this standard and previous ones is that applications are now required to use a subdirectory of /var/ lib.

\[39\] This hierarchy should contain files stored in /var/db in current BSD releases. These include locate.database and mountdtab, and the kernel symbol database(s).

\[40\] Then, anything wishing to use /dev/ttyS0 can read the lock file and act accordingly (all locks in /var/lock should be world-readable).

\[41\] Note that /var/mail may be a symbolic link to another directory.

\[42\] /var/run should be unwritable for unprivileged users (root or users running daemons); it is a major security problem if any user can write in this directory.

\[43\] UUCP lock files must be placed in /var/lock. See the above section on /var /lock.

\[44\] NIS should not be confused with Sun NIS+, which uses a different directory, /var/nis.

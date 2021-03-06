---
title: /kernel
description: The /kernel parameter directs the boot loader to load an alternate kernel file for the operating system.
ms.assetid: 052c8426-3ce1-4868-9efd-5480c18f46e9
keywords: ["/kernel Driver Development Tools"]
topic_type:
- apiref
api_name:
- /kernel
api_type:
- NA
---

/kernel
=======

The **/kernel** parameter directs the boot loader to load an alternate kernel file for the operating system.

``` syntax
    /kernel=KernelFile 

   
```

## Subparameters


<a href="" id="-------kernelfile------"></a> *KernelFile*   
Specifies a kernel file. The specified file must be located in the %SystemRoot%\\system32 directory, and its file name must conform to 8.3−character format.

### Comments

The **/execute** option is supported only on Windows Server 2003 with SP1 and Windows XP with SP2. On Windows Vista and later versions of Windows, use the **Kernel** element in BCDEdit.

For computers with less than 4 GB of memory, the default kernel file is ntoskrnl.exe. For computers with 4 GB or more of memory, the default kernel file is ntkrnlpa.exe.

Do not use this parameter unless you have deliberately installed a different kernel. You can use this parameter to test a kernel update, or use it with the [**/hal**](-hal.md) parameter to load a [partial checked build](https://msdn.microsoft.com/library/windows/hardware/ff547196) installation.

### Example

```
multi(0)disk(0)rdisk(0)partition(1)\WINDOWS="Microsoft Windows XP Professional" /fastdetect /hal=KRNLtest.dll
```

### Bootcfg Command

```
bootcfg /raw "/kernel=KRNLtest.dll" /A /ID 1
```

 

 

[Send comments about this topic to Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bdevtest\devtest%5D:%20/kernel%20%20RELEASE:%20%281/17/2018%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "Send comments about this topic to Microsoft")





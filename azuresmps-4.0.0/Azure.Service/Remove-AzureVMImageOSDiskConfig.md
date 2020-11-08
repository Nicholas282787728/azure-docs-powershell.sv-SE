---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1E1F98E9-FC45-4BEF-90F6-A21D7DB7C82F
online version: ''
schema: 2.0.0
ms.openlocfilehash: eac6db4400e5c51f295e0bbf549117ffdbc97644
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099675"
---
# <span data-ttu-id="83298-101">Remove-AzureVMImageOSDiskConfig</span><span class="sxs-lookup"><span data-stu-id="83298-101">Remove-AzureVMImageOSDiskConfig</span></span>

## <span data-ttu-id="83298-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="83298-102">SYNOPSIS</span></span>
<span data-ttu-id="83298-103">Tar bort disk konfigurationen för operativ systemet från DiskConfigSet-objektet.</span><span class="sxs-lookup"><span data-stu-id="83298-103">Removes the operating system disk configuration from the DiskConfigSet object.</span></span>

## <span data-ttu-id="83298-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="83298-104">SYNTAX</span></span>

```
Remove-AzureVMImageOSDiskConfig [-DiskConfig] <VirtualMachineImageDiskConfigSet>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="83298-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="83298-105">DESCRIPTION</span></span>
<span data-ttu-id="83298-106">Cmdleten **Remove-AzureVMImageOSDiskConfig** tar bort datorns disk konfiguration från DiskConfigSet-objektet.</span><span class="sxs-lookup"><span data-stu-id="83298-106">The **Remove-AzureVMImageOSDiskConfig** cmdlet removes the operating system disk configuration from the DiskConfigSet object.</span></span>

## <span data-ttu-id="83298-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="83298-107">EXAMPLES</span></span>

### <span data-ttu-id="83298-108">Exempel 1: ta bort operativ systemets disk konfiguration från en DiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="83298-108">Example 1: Remove the operating system disk configuration from a DiskConfigSet</span></span>
```
PS C:\> $Disk = New-AzureDiskConfigSet
PS C:\> $Disk = Set-AzureOSDiskConfig -DiskConfig $Disk -HostCaching ReadWrite
PS C:\> Remove-AzureVMImageOSDiskConfig -DiskConfig $Disk
```

<span data-ttu-id="83298-109">Det här kommandot tar bort disk konfigurationen för operativ systemet från DiskConfigSet-objektet</span><span class="sxs-lookup"><span data-stu-id="83298-109">This command removes the operating system disk configuration from the DiskConfigSet object</span></span>

## <span data-ttu-id="83298-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="83298-110">PARAMETERS</span></span>

### <span data-ttu-id="83298-111">-DiskConfig</span><span class="sxs-lookup"><span data-stu-id="83298-111">-DiskConfig</span></span>
<span data-ttu-id="83298-112">Anger det disk konfigurations objekt som kapslar in operativ system disken och data disk objekt.</span><span class="sxs-lookup"><span data-stu-id="83298-112">Specifies the disk configuration object that encapsulates the operating system disk and Data Disk objects.</span></span>

```yaml
Type: VirtualMachineImageDiskConfigSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="83298-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="83298-113">-InformationAction</span></span>
<span data-ttu-id="83298-114">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="83298-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="83298-115">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="83298-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="83298-116">Vidare</span><span class="sxs-lookup"><span data-stu-id="83298-116">Continue</span></span>
- <span data-ttu-id="83298-117">Över</span><span class="sxs-lookup"><span data-stu-id="83298-117">Ignore</span></span>
- <span data-ttu-id="83298-118">Inquire</span><span class="sxs-lookup"><span data-stu-id="83298-118">Inquire</span></span>
- <span data-ttu-id="83298-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="83298-119">SilentlyContinue</span></span>
- <span data-ttu-id="83298-120">Stanna</span><span class="sxs-lookup"><span data-stu-id="83298-120">Stop</span></span>
- <span data-ttu-id="83298-121">Avbryt</span><span class="sxs-lookup"><span data-stu-id="83298-121">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83298-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="83298-122">-InformationVariable</span></span>
<span data-ttu-id="83298-123">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="83298-123">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83298-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83298-124">CommonParameters</span></span>
<span data-ttu-id="83298-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83298-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83298-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83298-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83298-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="83298-127">INPUTS</span></span>

## <span data-ttu-id="83298-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="83298-128">OUTPUTS</span></span>

### <span data-ttu-id="83298-129">Microsoft. WindowsAzure. kommandon. ServiceManagement. Model. VirtualMachineImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="83298-129">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.VirtualMachineImageDiskConfigSet</span></span>

## <span data-ttu-id="83298-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="83298-130">NOTES</span></span>

## <span data-ttu-id="83298-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="83298-131">RELATED LINKS</span></span>

[<span data-ttu-id="83298-132">Set-AzureVMImageOSDiskConfig</span><span class="sxs-lookup"><span data-stu-id="83298-132">Set-AzureVMImageOSDiskConfig</span></span>](./Set-AzureVMImageOSDiskConfig.md)



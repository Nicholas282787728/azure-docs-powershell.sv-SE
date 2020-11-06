---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 473C71A8-1DF7-487A-B239-B80E2BB63B82
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMChefExtension.md
ms.openlocfilehash: dc2e22acf8efd18a565c1ede7ff22aeb21679a47
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576595"
---
# <span data-ttu-id="d46ed-101">Remove-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="d46ed-101">Remove-AzureRmVMChefExtension</span></span>

## <span data-ttu-id="d46ed-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d46ed-102">SYNOPSIS</span></span>
<span data-ttu-id="d46ed-103">Tar bort kock-tillägget från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="d46ed-103">Removes the Chef extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d46ed-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d46ed-104">SYNTAX</span></span>

### <span data-ttu-id="d46ed-105">Linux</span><span class="sxs-lookup"><span data-stu-id="d46ed-105">Linux</span></span>
```
Remove-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Linux]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d46ed-106">Windows</span><span class="sxs-lookup"><span data-stu-id="d46ed-106">Windows</span></span>
```
Remove-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Windows]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d46ed-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d46ed-107">DESCRIPTION</span></span>
<span data-ttu-id="d46ed-108">Cmdleten **Remove-AzureVMChefExtension** tar bort kock-tillägget från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="d46ed-108">The **Remove-AzureVMChefExtension** cmdlet removes the Chef extension from a virtual machine.</span></span>

## <span data-ttu-id="d46ed-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d46ed-109">EXAMPLES</span></span>

### <span data-ttu-id="d46ed-110">Exempel 1: ta bort en kock-anknytning från en virtuell Windows-dator</span><span class="sxs-lookup"><span data-stu-id="d46ed-110">Example 1: Remove a Chef extension from a Windows virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="d46ed-111">Det här kommandot tar bort en kock-anknytning från en Windows-baserad virtuell dator med namnet WindowsVM001 som tillhör resurs gruppen med namnet ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="d46ed-111">This command removes a Chef extension from a Windows based virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="d46ed-112">Exempel 2: ta bort en kock-anknytning från en virtuell dator i Linux</span><span class="sxs-lookup"><span data-stu-id="d46ed-112">Example 2: Remove a Chef extension from a Linux virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="d46ed-113">Det här kommandot tar bort en kock-anknytning från en Linux-baserad virtuell dator med namnet LinuxVM001 som tillhör resurs gruppen med namnet ResourceGroup002.</span><span class="sxs-lookup"><span data-stu-id="d46ed-113">This command removes a Chef extension from a Linux based virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="d46ed-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d46ed-114">PARAMETERS</span></span>

### <span data-ttu-id="d46ed-115">-Linux</span><span class="sxs-lookup"><span data-stu-id="d46ed-115">-Linux</span></span>
<span data-ttu-id="d46ed-116">Anger att denna cmdlet riktar sig till en virtuell Linux-dator.</span><span class="sxs-lookup"><span data-stu-id="d46ed-116">Indicates that this cmdlet targets a Linux virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d46ed-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="d46ed-117">-Name</span></span>
<span data-ttu-id="d46ed-118">Anger namnet på det chefs tillägg som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="d46ed-118">Specifies the name of the Chef extension that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d46ed-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d46ed-119">-ResourceGroupName</span></span>
<span data-ttu-id="d46ed-120">Anger namnet på den resurs grupp som innehåller den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="d46ed-120">Specifies the name of the resource group that contains the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d46ed-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="d46ed-121">-VMName</span></span>
<span data-ttu-id="d46ed-122">Anger namnet på en virtuell dator för vilken denna cmdlet tar bort kock-tillägget.</span><span class="sxs-lookup"><span data-stu-id="d46ed-122">Specifies the name of a virtual machine for which this cmdlet removes the Chef extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d46ed-123">-Windows</span><span class="sxs-lookup"><span data-stu-id="d46ed-123">-Windows</span></span>
<span data-ttu-id="d46ed-124">Anger att denna cmdlet riktar sig till en Windows-dator.</span><span class="sxs-lookup"><span data-stu-id="d46ed-124">Indicates that this cmdlet targets a Windows virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d46ed-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d46ed-125">-Confirm</span></span>
<span data-ttu-id="d46ed-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d46ed-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d46ed-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d46ed-127">-WhatIf</span></span>
<span data-ttu-id="d46ed-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d46ed-128">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="d46ed-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d46ed-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d46ed-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d46ed-130">CommonParameters</span></span>
<span data-ttu-id="d46ed-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d46ed-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d46ed-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d46ed-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d46ed-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d46ed-133">INPUTS</span></span>

### <span data-ttu-id="d46ed-134">Ingen</span><span class="sxs-lookup"><span data-stu-id="d46ed-134">None</span></span>
<span data-ttu-id="d46ed-135">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="d46ed-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d46ed-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d46ed-136">OUTPUTS</span></span>

## <span data-ttu-id="d46ed-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d46ed-137">NOTES</span></span>

## <span data-ttu-id="d46ed-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d46ed-138">RELATED LINKS</span></span>

[<span data-ttu-id="d46ed-139">Get-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="d46ed-139">Get-AzureRmVMChefExtension</span></span>](./Get-AzureRmVMChefExtension.md)

[<span data-ttu-id="d46ed-140">Set-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="d46ed-140">Set-AzureRmVMChefExtension</span></span>](./Set-AzureRmVMChefExtension.md)

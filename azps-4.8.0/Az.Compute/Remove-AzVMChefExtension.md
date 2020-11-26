---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 473C71A8-1DF7-487A-B239-B80E2BB63B82
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmchefextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMChefExtension.md
ms.openlocfilehash: 79b16afbd6188682ff68ba5b2f2d9ccae67ff630
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94103256"
---
# <span data-ttu-id="b5e47-101">Remove-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="b5e47-101">Remove-AzVMChefExtension</span></span>

## <span data-ttu-id="b5e47-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b5e47-102">SYNOPSIS</span></span>
<span data-ttu-id="b5e47-103">Tar bort kock-tillägget från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="b5e47-103">Removes the Chef extension from a virtual machine.</span></span>

## <span data-ttu-id="b5e47-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b5e47-104">SYNTAX</span></span>

### <span data-ttu-id="b5e47-105">Linux</span><span class="sxs-lookup"><span data-stu-id="b5e47-105">Linux</span></span>
```
Remove-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Linux] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5e47-106">Windows</span><span class="sxs-lookup"><span data-stu-id="b5e47-106">Windows</span></span>
```
Remove-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Windows]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5e47-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b5e47-107">DESCRIPTION</span></span>
<span data-ttu-id="b5e47-108">Cmdleten **Remove-AzVMChefExtension** tar bort kock-tillägget från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="b5e47-108">The **Remove-AzVMChefExtension** cmdlet removes the Chef extension from a virtual machine.</span></span>

## <span data-ttu-id="b5e47-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b5e47-109">EXAMPLES</span></span>

### <span data-ttu-id="b5e47-110">Exempel 1: ta bort en kock-anknytning från en virtuell Windows-dator</span><span class="sxs-lookup"><span data-stu-id="b5e47-110">Example 1: Remove a Chef extension from a Windows virtual machine</span></span>
```
PS C:\> Remove-AzVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="b5e47-111">Det här kommandot tar bort en kock-anknytning från en Windows-baserad virtuell dator med namnet WindowsVM001 som tillhör resurs gruppen med namnet ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="b5e47-111">This command removes a Chef extension from a Windows based virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="b5e47-112">Exempel 2: ta bort en kock-anknytning från en virtuell dator i Linux</span><span class="sxs-lookup"><span data-stu-id="b5e47-112">Example 2: Remove a Chef extension from a Linux virtual machine</span></span>
```
PS C:\> Remove-AzVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="b5e47-113">Det här kommandot tar bort en kock-anknytning från en Linux-baserad virtuell dator med namnet LinuxVM001 som tillhör resurs gruppen med namnet ResourceGroup002.</span><span class="sxs-lookup"><span data-stu-id="b5e47-113">This command removes a Chef extension from a Linux based virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="b5e47-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b5e47-114">PARAMETERS</span></span>

### <span data-ttu-id="b5e47-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5e47-115">-DefaultProfile</span></span>
<span data-ttu-id="b5e47-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b5e47-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5e47-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="b5e47-117">-Linux</span></span>
<span data-ttu-id="b5e47-118">Anger att denna cmdlet riktar sig till en virtuell Linux-dator.</span><span class="sxs-lookup"><span data-stu-id="b5e47-118">Indicates that this cmdlet targets a Linux virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5e47-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="b5e47-119">-Name</span></span>
<span data-ttu-id="b5e47-120">Anger namnet på det chefs tillägg som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="b5e47-120">Specifies the name of the Chef extension that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5e47-121">-Nowait</span><span class="sxs-lookup"><span data-stu-id="b5e47-121">-NoWait</span></span>
<span data-ttu-id="b5e47-122">Startar operationen och returnerar omedelbart innan operationen är slutförd.</span><span class="sxs-lookup"><span data-stu-id="b5e47-122">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="b5e47-123">Använd en annan mekanism för att avgöra om åtgärden har slutförts.</span><span class="sxs-lookup"><span data-stu-id="b5e47-123">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5e47-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5e47-124">-ResourceGroupName</span></span>
<span data-ttu-id="b5e47-125">Anger namnet på den resurs grupp som innehåller den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="b5e47-125">Specifies the name of the resource group that contains the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5e47-126">-VMName</span><span class="sxs-lookup"><span data-stu-id="b5e47-126">-VMName</span></span>
<span data-ttu-id="b5e47-127">Anger namnet på en virtuell dator för vilken denna cmdlet tar bort kock-tillägget.</span><span class="sxs-lookup"><span data-stu-id="b5e47-127">Specifies the name of a virtual machine for which this cmdlet removes the Chef extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5e47-128">-Windows</span><span class="sxs-lookup"><span data-stu-id="b5e47-128">-Windows</span></span>
<span data-ttu-id="b5e47-129">Anger att denna cmdlet riktar sig till en Windows-dator.</span><span class="sxs-lookup"><span data-stu-id="b5e47-129">Indicates that this cmdlet targets a Windows virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5e47-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b5e47-130">-Confirm</span></span>
<span data-ttu-id="b5e47-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b5e47-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5e47-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5e47-132">-WhatIf</span></span>
<span data-ttu-id="b5e47-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b5e47-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5e47-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b5e47-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5e47-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5e47-135">CommonParameters</span></span>
<span data-ttu-id="b5e47-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5e47-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5e47-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b5e47-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5e47-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b5e47-138">INPUTS</span></span>

### <span data-ttu-id="b5e47-139">System. String</span><span class="sxs-lookup"><span data-stu-id="b5e47-139">System.String</span></span>

## <span data-ttu-id="b5e47-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b5e47-140">OUTPUTS</span></span>

### <span data-ttu-id="b5e47-141">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="b5e47-141">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="b5e47-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b5e47-142">NOTES</span></span>

## <span data-ttu-id="b5e47-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b5e47-143">RELATED LINKS</span></span>

[<span data-ttu-id="b5e47-144">Get-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="b5e47-144">Get-AzVMChefExtension</span></span>](./Get-AzVMChefExtension.md)

[<span data-ttu-id="b5e47-145">Set-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="b5e47-145">Set-AzVMChefExtension</span></span>](./Set-AzVMChefExtension.md)
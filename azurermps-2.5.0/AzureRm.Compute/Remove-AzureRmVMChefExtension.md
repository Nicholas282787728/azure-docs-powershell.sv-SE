---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 473C71A8-1DF7-487A-B239-B80E2BB63B82
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmchefextension
schema: 2.0.0
ms.openlocfilehash: bc8dbd023d8730922614f749f540d182c63237a4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930633"
---
# <span data-ttu-id="cbe3c-101">Remove-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="cbe3c-101">Remove-AzureRmVMChefExtension</span></span>

## <span data-ttu-id="cbe3c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cbe3c-102">SYNOPSIS</span></span>
<span data-ttu-id="cbe3c-103">Tar bort kock-tillägget från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="cbe3c-103">Removes the Chef extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cbe3c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cbe3c-104">SYNTAX</span></span>

### <span data-ttu-id="cbe3c-105">Linux</span><span class="sxs-lookup"><span data-stu-id="cbe3c-105">Linux</span></span>
```
Remove-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Linux]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbe3c-106">Windows</span><span class="sxs-lookup"><span data-stu-id="cbe3c-106">Windows</span></span>
```
Remove-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Windows]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cbe3c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cbe3c-107">DESCRIPTION</span></span>
<span data-ttu-id="cbe3c-108">Cmdleten **Remove-AzureVMChefExtension** tar bort kock-tillägget från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="cbe3c-108">The **Remove-AzureVMChefExtension** cmdlet removes the Chef extension from a virtual machine.</span></span>

## <span data-ttu-id="cbe3c-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cbe3c-109">EXAMPLES</span></span>

### <span data-ttu-id="cbe3c-110">Exempel 1: ta bort en kock-anknytning från en virtuell Windows-dator</span><span class="sxs-lookup"><span data-stu-id="cbe3c-110">Example 1: Remove a Chef extension from a Windows virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="cbe3c-111">Det här kommandot tar bort en kock-anknytning från en Windows-baserad virtuell dator med namnet WindowsVM001 som tillhör resurs gruppen med namnet ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="cbe3c-111">This command removes a Chef extension from a Windows based virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="cbe3c-112">Exempel 2: ta bort en kock-anknytning från en virtuell dator i Linux</span><span class="sxs-lookup"><span data-stu-id="cbe3c-112">Example 2: Remove a Chef extension from a Linux virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="cbe3c-113">Det här kommandot tar bort en kock-anknytning från en Linux-baserad virtuell dator med namnet LinuxVM001 som tillhör resurs gruppen med namnet ResourceGroup002.</span><span class="sxs-lookup"><span data-stu-id="cbe3c-113">This command removes a Chef extension from a Linux based virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="cbe3c-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cbe3c-114">PARAMETERS</span></span>

### <span data-ttu-id="cbe3c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbe3c-115">-DefaultProfile</span></span>
<span data-ttu-id="cbe3c-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cbe3c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbe3c-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="cbe3c-117">-Linux</span></span>
<span data-ttu-id="cbe3c-118">Anger att denna cmdlet riktar sig till en virtuell Linux-dator.</span><span class="sxs-lookup"><span data-stu-id="cbe3c-118">Indicates that this cmdlet targets a Linux virtual machine.</span></span>

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

### <span data-ttu-id="cbe3c-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="cbe3c-119">-Name</span></span>
<span data-ttu-id="cbe3c-120">Anger namnet på det chefs tillägg som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="cbe3c-120">Specifies the name of the Chef extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="cbe3c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbe3c-121">-ResourceGroupName</span></span>
<span data-ttu-id="cbe3c-122">Anger namnet på den resurs grupp som innehåller den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="cbe3c-122">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="cbe3c-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="cbe3c-123">-VMName</span></span>
<span data-ttu-id="cbe3c-124">Anger namnet på en virtuell dator för vilken denna cmdlet tar bort kock-tillägget.</span><span class="sxs-lookup"><span data-stu-id="cbe3c-124">Specifies the name of a virtual machine for which this cmdlet removes the Chef extension.</span></span>

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

### <span data-ttu-id="cbe3c-125">-Windows</span><span class="sxs-lookup"><span data-stu-id="cbe3c-125">-Windows</span></span>
<span data-ttu-id="cbe3c-126">Anger att denna cmdlet riktar sig till en Windows-dator.</span><span class="sxs-lookup"><span data-stu-id="cbe3c-126">Indicates that this cmdlet targets a Windows virtual machine.</span></span>

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

### <span data-ttu-id="cbe3c-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cbe3c-127">-Confirm</span></span>
<span data-ttu-id="cbe3c-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cbe3c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cbe3c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbe3c-129">-WhatIf</span></span>
<span data-ttu-id="cbe3c-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cbe3c-130">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="cbe3c-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cbe3c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cbe3c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbe3c-132">CommonParameters</span></span>
<span data-ttu-id="cbe3c-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbe3c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbe3c-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbe3c-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbe3c-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cbe3c-135">INPUTS</span></span>

### <span data-ttu-id="cbe3c-136">Ingen</span><span class="sxs-lookup"><span data-stu-id="cbe3c-136">None</span></span>
<span data-ttu-id="cbe3c-137">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="cbe3c-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cbe3c-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cbe3c-138">OUTPUTS</span></span>

### <span data-ttu-id="cbe3c-139">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="cbe3c-139">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="cbe3c-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cbe3c-140">NOTES</span></span>

## <span data-ttu-id="cbe3c-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cbe3c-141">RELATED LINKS</span></span>

[<span data-ttu-id="cbe3c-142">Get-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="cbe3c-142">Get-AzureRmVMChefExtension</span></span>](./Get-AzureRmVMChefExtension.md)

[<span data-ttu-id="cbe3c-143">Set-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="cbe3c-143">Set-AzureRmVMChefExtension</span></span>](./Set-AzureRmVMChefExtension.md)

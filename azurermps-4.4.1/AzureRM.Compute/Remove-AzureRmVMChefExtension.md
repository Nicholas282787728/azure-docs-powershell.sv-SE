---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 473C71A8-1DF7-487A-B239-B80E2BB63B82
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMChefExtension.md
ms.openlocfilehash: df38df4da3fada0e89f527e7655c5c62c0df2602
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573713"
---
# <span data-ttu-id="49bc4-101">Remove-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="49bc4-101">Remove-AzureRmVMChefExtension</span></span>

## <span data-ttu-id="49bc4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="49bc4-102">SYNOPSIS</span></span>
<span data-ttu-id="49bc4-103">Tar bort kock-tillägget från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="49bc4-103">Removes the Chef extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49bc4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="49bc4-104">SYNTAX</span></span>

### <span data-ttu-id="49bc4-105">Linux</span><span class="sxs-lookup"><span data-stu-id="49bc4-105">Linux</span></span>
```
Remove-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Linux]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49bc4-106">Windows</span><span class="sxs-lookup"><span data-stu-id="49bc4-106">Windows</span></span>
```
Remove-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Windows]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49bc4-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="49bc4-107">DESCRIPTION</span></span>
<span data-ttu-id="49bc4-108">Cmdleten **Remove-AzureVMChefExtension** tar bort kock-tillägget från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="49bc4-108">The **Remove-AzureVMChefExtension** cmdlet removes the Chef extension from a virtual machine.</span></span>

## <span data-ttu-id="49bc4-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="49bc4-109">EXAMPLES</span></span>

### <span data-ttu-id="49bc4-110">Exempel 1: ta bort en kock-anknytning från en virtuell Windows-dator</span><span class="sxs-lookup"><span data-stu-id="49bc4-110">Example 1: Remove a Chef extension from a Windows virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="49bc4-111">Det här kommandot tar bort en kock-anknytning från en Windows-baserad virtuell dator med namnet WindowsVM001 som tillhör resurs gruppen med namnet ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="49bc4-111">This command removes a Chef extension from a Windows based virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="49bc4-112">Exempel 2: ta bort en kock-anknytning från en virtuell dator i Linux</span><span class="sxs-lookup"><span data-stu-id="49bc4-112">Example 2: Remove a Chef extension from a Linux virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="49bc4-113">Det här kommandot tar bort en kock-anknytning från en Linux-baserad virtuell dator med namnet LinuxVM001 som tillhör resurs gruppen med namnet ResourceGroup002.</span><span class="sxs-lookup"><span data-stu-id="49bc4-113">This command removes a Chef extension from a Linux based virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="49bc4-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="49bc4-114">PARAMETERS</span></span>

### <span data-ttu-id="49bc4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49bc4-115">-DefaultProfile</span></span>
<span data-ttu-id="49bc4-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="49bc4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49bc4-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="49bc4-117">-Linux</span></span>
<span data-ttu-id="49bc4-118">Anger att denna cmdlet riktar sig till en virtuell Linux-dator.</span><span class="sxs-lookup"><span data-stu-id="49bc4-118">Indicates that this cmdlet targets a Linux virtual machine.</span></span>

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

### <span data-ttu-id="49bc4-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="49bc4-119">-Name</span></span>
<span data-ttu-id="49bc4-120">Anger namnet på det chefs tillägg som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="49bc4-120">Specifies the name of the Chef extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="49bc4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49bc4-121">-ResourceGroupName</span></span>
<span data-ttu-id="49bc4-122">Anger namnet på den resurs grupp som innehåller den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="49bc4-122">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="49bc4-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="49bc4-123">-VMName</span></span>
<span data-ttu-id="49bc4-124">Anger namnet på en virtuell dator för vilken denna cmdlet tar bort kock-tillägget.</span><span class="sxs-lookup"><span data-stu-id="49bc4-124">Specifies the name of a virtual machine for which this cmdlet removes the Chef extension.</span></span>

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

### <span data-ttu-id="49bc4-125">-Windows</span><span class="sxs-lookup"><span data-stu-id="49bc4-125">-Windows</span></span>
<span data-ttu-id="49bc4-126">Anger att denna cmdlet riktar sig till en Windows-dator.</span><span class="sxs-lookup"><span data-stu-id="49bc4-126">Indicates that this cmdlet targets a Windows virtual machine.</span></span>

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

### <span data-ttu-id="49bc4-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="49bc4-127">-Confirm</span></span>
<span data-ttu-id="49bc4-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="49bc4-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49bc4-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49bc4-129">-WhatIf</span></span>
<span data-ttu-id="49bc4-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="49bc4-130">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="49bc4-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="49bc4-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49bc4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49bc4-132">CommonParameters</span></span>
<span data-ttu-id="49bc4-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49bc4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49bc4-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49bc4-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49bc4-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="49bc4-135">INPUTS</span></span>

## <span data-ttu-id="49bc4-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="49bc4-136">OUTPUTS</span></span>

## <span data-ttu-id="49bc4-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="49bc4-137">NOTES</span></span>

## <span data-ttu-id="49bc4-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="49bc4-138">RELATED LINKS</span></span>

[<span data-ttu-id="49bc4-139">Get-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="49bc4-139">Get-AzureRmVMChefExtension</span></span>](./Get-AzureRmVMChefExtension.md)

[<span data-ttu-id="49bc4-140">Set-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="49bc4-140">Set-AzureRmVMChefExtension</span></span>](./Set-AzureRmVMChefExtension.md)
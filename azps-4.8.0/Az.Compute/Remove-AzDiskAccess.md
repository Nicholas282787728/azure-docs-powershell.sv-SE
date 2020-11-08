---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskAccess.md
ms.openlocfilehash: 4b67364f0d079c7cd5fbbdd89b1a84b4dc6fee0e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94103029"
---
# <span data-ttu-id="cd886-101">Remove-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="cd886-101">Remove-AzDiskAccess</span></span>

## <span data-ttu-id="cd886-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cd886-102">SYNOPSIS</span></span>
<span data-ttu-id="cd886-103">Tar bort en disk åtkomst resurs.</span><span class="sxs-lookup"><span data-stu-id="cd886-103">Removes a disk access resource.</span></span>

## <span data-ttu-id="cd886-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cd886-104">SYNTAX</span></span>

### <span data-ttu-id="cd886-105">DefaultParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="cd886-105">DefaultParameterSet (Default)</span></span>
```
Remove-AzDiskAccess [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd886-106">ResourceIDParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd886-106">ResourceIDParameterSet</span></span>
```
Remove-AzDiskAccess [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd886-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd886-107">InputObjectParameterSet</span></span>
```
Remove-AzDiskAccess [-InputObject] <PSDiskAccess> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd886-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cd886-108">DESCRIPTION</span></span>
<span data-ttu-id="cd886-109">Cmdleten **Remove-AzDiskAccess** tar bort en disk åtkomst resurs.</span><span class="sxs-lookup"><span data-stu-id="cd886-109">The **Remove-AzDiskAccess** cmdlet removes a disk access resource.</span></span>

## <span data-ttu-id="cd886-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cd886-110">EXAMPLES</span></span>

### <span data-ttu-id="cd886-111">Exempel 1: ta bort disk åtkomst med standard parameter uppsättning</span><span class="sxs-lookup"><span data-stu-id="cd886-111">Example 1: Remove Disk Access using Default Parameter Set</span></span>
```
PS C:\> Remove-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01"
```

<span data-ttu-id="cd886-112">Det här kommandot tar bort disk åtkomsten med namnet "DiskAccess01" i resurs gruppen "ResourceGroup01"</span><span class="sxs-lookup"><span data-stu-id="cd886-112">This command removes the disk access named "DiskAccess01" in resource group "ResourceGroup01"</span></span>

### <span data-ttu-id="cd886-113">Exempel 2: ta bort disk åtkomst med resurs-ID</span><span class="sxs-lookup"><span data-stu-id="cd886-113">Example 2: Remove Disk Access using Resource ID</span></span>
```
PS C:\> $myDiskAccess = Get-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01"
PS C:\> Remove-AzDiskAccess -ResourceId $myDiskAccess.id
```

<span data-ttu-id="cd886-114">Det här kommandot tar bort disk åtkomst via resurs-ID</span><span class="sxs-lookup"><span data-stu-id="cd886-114">This command removes the disk access by Resource ID</span></span>

### <span data-ttu-id="cd886-115">Exempel 3: ta bort disk åtkomst med hjälp av indata</span><span class="sxs-lookup"><span data-stu-id="cd886-115">Example 3: Remove Disk Access using Input Object</span></span>
```
PS C:\> $myDiskAccess = Get-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01"
PS C:\> Remove-AzDiskAccess -InputObject $myDiskAccess
```

<span data-ttu-id="cd886-116">Det här kommandot tar bort disk åtkomst via InputObject</span><span class="sxs-lookup"><span data-stu-id="cd886-116">This command removes the disk access by InputObject</span></span>

### <span data-ttu-id="cd886-117">Exempel 4: ta bort disk åtkomst efter indatamängds objekt</span><span class="sxs-lookup"><span data-stu-id="cd886-117">Example 4: Remove Disk Access by piping Input Object</span></span>
```
PS C:\> Get-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01" | Remove-AzDiskAccess 
```

<span data-ttu-id="cd886-118">Det här kommandot tar bort disk åtkomst genom rör InputObject</span><span class="sxs-lookup"><span data-stu-id="cd886-118">This command removes the disk access by piping the InputObject</span></span>

## <span data-ttu-id="cd886-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cd886-119">PARAMETERS</span></span>

### <span data-ttu-id="cd886-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cd886-120">-AsJob</span></span>
<span data-ttu-id="cd886-121">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="cd886-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cd886-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd886-122">-DefaultProfile</span></span>
<span data-ttu-id="cd886-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cd886-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd886-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd886-124">-InputObject</span></span>
<span data-ttu-id="cd886-125">PowerShell-textobjekt</span><span class="sxs-lookup"><span data-stu-id="cd886-125">PowerShell Disk Access Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess
Parameter Sets: InputObjectParameterSet
Aliases: DiskAccess

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd886-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="cd886-126">-Name</span></span>
<span data-ttu-id="cd886-127">Anger namnet på en disk åtkomst.</span><span class="sxs-lookup"><span data-stu-id="cd886-127">Specifies the name of a disk access.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases: DiskAccessName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd886-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd886-128">-ResourceGroupName</span></span>
<span data-ttu-id="cd886-129">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="cd886-129">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd886-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd886-130">-ResourceId</span></span>
<span data-ttu-id="cd886-131">Resurs-ID för disk åtkomst.</span><span class="sxs-lookup"><span data-stu-id="cd886-131">Resource ID for your disk access.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIDParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd886-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cd886-132">-Confirm</span></span>
<span data-ttu-id="cd886-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cd886-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd886-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd886-134">-WhatIf</span></span>
<span data-ttu-id="cd886-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cd886-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd886-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cd886-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd886-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd886-137">CommonParameters</span></span>
<span data-ttu-id="cd886-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd886-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd886-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cd886-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd886-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cd886-140">INPUTS</span></span>

### <span data-ttu-id="cd886-141">System. String</span><span class="sxs-lookup"><span data-stu-id="cd886-141">System.String</span></span>

### <span data-ttu-id="cd886-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span><span class="sxs-lookup"><span data-stu-id="cd886-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span></span>

## <span data-ttu-id="cd886-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cd886-143">OUTPUTS</span></span>

### <span data-ttu-id="cd886-144">Microsoft. Azure. commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="cd886-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="cd886-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cd886-145">NOTES</span></span>

## <span data-ttu-id="cd886-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cd886-146">RELATED LINKS</span></span>

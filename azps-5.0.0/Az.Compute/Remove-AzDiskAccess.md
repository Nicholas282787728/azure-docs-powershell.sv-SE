---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskAccess.md
ms.openlocfilehash: 4b67364f0d079c7cd5fbbdd89b1a84b4dc6fee0e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94263448"
---
# <span data-ttu-id="54875-101">Remove-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="54875-101">Remove-AzDiskAccess</span></span>

## <span data-ttu-id="54875-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="54875-102">SYNOPSIS</span></span>
<span data-ttu-id="54875-103">Tar bort en disk åtkomst resurs.</span><span class="sxs-lookup"><span data-stu-id="54875-103">Removes a disk access resource.</span></span>

## <span data-ttu-id="54875-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="54875-104">SYNTAX</span></span>

### <span data-ttu-id="54875-105">DefaultParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="54875-105">DefaultParameterSet (Default)</span></span>
```
Remove-AzDiskAccess [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54875-106">ResourceIDParameterSet</span><span class="sxs-lookup"><span data-stu-id="54875-106">ResourceIDParameterSet</span></span>
```
Remove-AzDiskAccess [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54875-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="54875-107">InputObjectParameterSet</span></span>
```
Remove-AzDiskAccess [-InputObject] <PSDiskAccess> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54875-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="54875-108">DESCRIPTION</span></span>
<span data-ttu-id="54875-109">Cmdleten **Remove-AzDiskAccess** tar bort en disk åtkomst resurs.</span><span class="sxs-lookup"><span data-stu-id="54875-109">The **Remove-AzDiskAccess** cmdlet removes a disk access resource.</span></span>

## <span data-ttu-id="54875-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="54875-110">EXAMPLES</span></span>

### <span data-ttu-id="54875-111">Exempel 1: ta bort disk åtkomst med standard parameter uppsättning</span><span class="sxs-lookup"><span data-stu-id="54875-111">Example 1: Remove Disk Access using Default Parameter Set</span></span>
```
PS C:\> Remove-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01"
```

<span data-ttu-id="54875-112">Det här kommandot tar bort disk åtkomsten med namnet "DiskAccess01" i resurs gruppen "ResourceGroup01"</span><span class="sxs-lookup"><span data-stu-id="54875-112">This command removes the disk access named "DiskAccess01" in resource group "ResourceGroup01"</span></span>

### <span data-ttu-id="54875-113">Exempel 2: ta bort disk åtkomst med resurs-ID</span><span class="sxs-lookup"><span data-stu-id="54875-113">Example 2: Remove Disk Access using Resource ID</span></span>
```
PS C:\> $myDiskAccess = Get-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01"
PS C:\> Remove-AzDiskAccess -ResourceId $myDiskAccess.id
```

<span data-ttu-id="54875-114">Det här kommandot tar bort disk åtkomst via resurs-ID</span><span class="sxs-lookup"><span data-stu-id="54875-114">This command removes the disk access by Resource ID</span></span>

### <span data-ttu-id="54875-115">Exempel 3: ta bort disk åtkomst med hjälp av indata</span><span class="sxs-lookup"><span data-stu-id="54875-115">Example 3: Remove Disk Access using Input Object</span></span>
```
PS C:\> $myDiskAccess = Get-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01"
PS C:\> Remove-AzDiskAccess -InputObject $myDiskAccess
```

<span data-ttu-id="54875-116">Det här kommandot tar bort disk åtkomst via InputObject</span><span class="sxs-lookup"><span data-stu-id="54875-116">This command removes the disk access by InputObject</span></span>

### <span data-ttu-id="54875-117">Exempel 4: ta bort disk åtkomst efter indatamängds objekt</span><span class="sxs-lookup"><span data-stu-id="54875-117">Example 4: Remove Disk Access by piping Input Object</span></span>
```
PS C:\> Get-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01" | Remove-AzDiskAccess 
```

<span data-ttu-id="54875-118">Det här kommandot tar bort disk åtkomst genom rör InputObject</span><span class="sxs-lookup"><span data-stu-id="54875-118">This command removes the disk access by piping the InputObject</span></span>

## <span data-ttu-id="54875-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="54875-119">PARAMETERS</span></span>

### <span data-ttu-id="54875-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="54875-120">-AsJob</span></span>
<span data-ttu-id="54875-121">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="54875-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="54875-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54875-122">-DefaultProfile</span></span>
<span data-ttu-id="54875-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="54875-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54875-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="54875-124">-InputObject</span></span>
<span data-ttu-id="54875-125">PowerShell-textobjekt</span><span class="sxs-lookup"><span data-stu-id="54875-125">PowerShell Disk Access Object</span></span>

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

### <span data-ttu-id="54875-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="54875-126">-Name</span></span>
<span data-ttu-id="54875-127">Anger namnet på en disk åtkomst.</span><span class="sxs-lookup"><span data-stu-id="54875-127">Specifies the name of a disk access.</span></span>

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

### <span data-ttu-id="54875-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54875-128">-ResourceGroupName</span></span>
<span data-ttu-id="54875-129">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="54875-129">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="54875-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="54875-130">-ResourceId</span></span>
<span data-ttu-id="54875-131">Resurs-ID för disk åtkomst.</span><span class="sxs-lookup"><span data-stu-id="54875-131">Resource ID for your disk access.</span></span>

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

### <span data-ttu-id="54875-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="54875-132">-Confirm</span></span>
<span data-ttu-id="54875-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="54875-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54875-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54875-134">-WhatIf</span></span>
<span data-ttu-id="54875-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="54875-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54875-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="54875-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54875-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54875-137">CommonParameters</span></span>
<span data-ttu-id="54875-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54875-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54875-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="54875-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54875-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="54875-140">INPUTS</span></span>

### <span data-ttu-id="54875-141">System. String</span><span class="sxs-lookup"><span data-stu-id="54875-141">System.String</span></span>

### <span data-ttu-id="54875-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span><span class="sxs-lookup"><span data-stu-id="54875-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span></span>

## <span data-ttu-id="54875-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="54875-143">OUTPUTS</span></span>

### <span data-ttu-id="54875-144">Microsoft. Azure. commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="54875-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="54875-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="54875-145">NOTES</span></span>

## <span data-ttu-id="54875-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="54875-146">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageContainer.md
ms.openlocfilehash: c1e76da1fc01ea1698c56e40fd3bd46f6378ea07
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269858"
---
# <span data-ttu-id="c2b2b-101">Remove-AzStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="c2b2b-101">Remove-AzStackEdgeStorageContainer</span></span>

## <span data-ttu-id="c2b2b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c2b2b-102">SYNOPSIS</span></span>
<span data-ttu-id="c2b2b-103">Tar bort en lagrings behållare för Edge Storage-kontot på en enhet.</span><span class="sxs-lookup"><span data-stu-id="c2b2b-103">Removes a storage container for the Edge Storage account on a device.</span></span>

## <span data-ttu-id="c2b2b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c2b2b-104">SYNTAX</span></span>

### <span data-ttu-id="c2b2b-105">DeleteByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="c2b2b-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2b2b-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2b2b-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeStorageContainer -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2b2b-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2b2b-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeStorageContainer -InputObject <PSStackEdgeStorageContainer> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2b2b-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c2b2b-108">DESCRIPTION</span></span>
<span data-ttu-id="c2b2b-109">Cmdleten **Remove-AzStackEdgeStorageContainer** tar bort en tillhör ande lagrings behållare för Edge Storage-kontot på en stack Edge-enhet.</span><span class="sxs-lookup"><span data-stu-id="c2b2b-109">The **Remove-AzStackEdgeStorageContainer** cmdlet removes an associated storage container for the Edge Storage account on a Stack Edge device.</span></span> <span data-ttu-id="c2b2b-110">Du kan ange namnet på den lagrings enhet som ska tas bort som en parameter.</span><span class="sxs-lookup"><span data-stu-id="c2b2b-110">You can specify the name of the storage container to be removed as a parameter.</span></span>

## <span data-ttu-id="c2b2b-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c2b2b-111">EXAMPLES</span></span>

### <span data-ttu-id="c2b2b-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c2b2b-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccountname -Name container1
```

## <span data-ttu-id="c2b2b-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c2b2b-113">PARAMETERS</span></span>

### <span data-ttu-id="c2b2b-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c2b2b-114">-AsJob</span></span>
<span data-ttu-id="c2b2b-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="c2b2b-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c2b2b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2b2b-116">-DefaultProfile</span></span>
<span data-ttu-id="c2b2b-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c2b2b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2b2b-118">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="c2b2b-118">-DeviceName</span></span>
<span data-ttu-id="c2b2b-119">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="c2b2b-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2b2b-120">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c2b2b-120">-EdgeStorageAccountName</span></span>
<span data-ttu-id="c2b2b-121">Ange befintliga EdgeStorageAccount namn</span><span class="sxs-lookup"><span data-stu-id="c2b2b-121">Provide existing EdgeStorageAccount's Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2b2b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c2b2b-122">-InputObject</span></span>
<span data-ttu-id="c2b2b-123">Infoga objekt</span><span class="sxs-lookup"><span data-stu-id="c2b2b-123">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: EdgeStorageContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2b2b-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="c2b2b-124">-Name</span></span>
<span data-ttu-id="c2b2b-125">Resurs namn</span><span class="sxs-lookup"><span data-stu-id="c2b2b-125">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: EdgeContainerName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2b2b-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c2b2b-126">-PassThru</span></span>
<span data-ttu-id="c2b2b-127">Returnerar sant om det lyckas</span><span class="sxs-lookup"><span data-stu-id="c2b2b-127">returns true if successful</span></span>

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

### <span data-ttu-id="c2b2b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2b2b-128">-ResourceGroupName</span></span>
<span data-ttu-id="c2b2b-129">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="c2b2b-129">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2b2b-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c2b2b-130">-ResourceId</span></span>
<span data-ttu-id="c2b2b-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="c2b2b-131">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2b2b-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c2b2b-132">-Confirm</span></span>
<span data-ttu-id="c2b2b-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c2b2b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2b2b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2b2b-134">-WhatIf</span></span>
<span data-ttu-id="c2b2b-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c2b2b-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c2b2b-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c2b2b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2b2b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2b2b-137">CommonParameters</span></span>
<span data-ttu-id="c2b2b-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2b2b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2b2b-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c2b2b-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2b2b-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c2b2b-140">INPUTS</span></span>

### <span data-ttu-id="c2b2b-141">System. String</span><span class="sxs-lookup"><span data-stu-id="c2b2b-141">System.String</span></span>

### <span data-ttu-id="c2b2b-142">Microsoft. Azure. PowerShell. cmdletar. StackEdge. Models. PSStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="c2b2b-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span></span>

## <span data-ttu-id="c2b2b-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c2b2b-143">OUTPUTS</span></span>

### <span data-ttu-id="c2b2b-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c2b2b-144">System.Boolean</span></span>

## <span data-ttu-id="c2b2b-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c2b2b-145">NOTES</span></span>

## <span data-ttu-id="c2b2b-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c2b2b-146">RELATED LINKS</span></span>

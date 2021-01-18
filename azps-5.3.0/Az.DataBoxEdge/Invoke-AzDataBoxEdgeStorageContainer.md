---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/invoke-azdataboxedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeStorageContainer.md
ms.openlocfilehash: f897c2adfe4154aeff5bd370437ea8b23e4efd36
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524246"
---
# <span data-ttu-id="cba8c-101">Invoke-AzDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="cba8c-101">Invoke-AzDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="cba8c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cba8c-102">SYNOPSIS</span></span>
<span data-ttu-id="cba8c-103">Anropar specifika åtgärder på en lagrings behållare</span><span class="sxs-lookup"><span data-stu-id="cba8c-103">Invokes specific actions on a storage container</span></span>

## <span data-ttu-id="cba8c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cba8c-104">SYNTAX</span></span>

### <span data-ttu-id="cba8c-105">InvokeByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="cba8c-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-RefreshData] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cba8c-106">InvokeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cba8c-106">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeStorageContainer [-ResourceId] <String> [-RefreshData] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cba8c-107">InvokeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cba8c-107">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeStorageContainer [-RefreshData] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 -InputObject <PSDataBoxEdgeStorageContainer> [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cba8c-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cba8c-108">DESCRIPTION</span></span>
<span data-ttu-id="cba8c-109">Cmdleten **Invoke-AzDataBoxEdgeStorageContainer** anropar åtgärder för att uppdatera data i en lagrings behållare på en Edge-enhet.</span><span class="sxs-lookup"><span data-stu-id="cba8c-109">The **Invoke-AzDataBoxEdgeStorageContainer** cmdlet invokes actions to refresh the data on a storage container on a Data Box Edge device.</span></span> 

## <span data-ttu-id="cba8c-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cba8c-110">EXAMPLES</span></span>

### <span data-ttu-id="cba8c-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="cba8c-111">Example 1</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccount1 -Name container1 -PassThru
PS C:\> true
```

### <span data-ttu-id="cba8c-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="cba8c-112">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccount1 -Name container1 | Invoke-AzDataBoxEdgeStorageContainer
```

## <span data-ttu-id="cba8c-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cba8c-113">PARAMETERS</span></span>

### <span data-ttu-id="cba8c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cba8c-114">-AsJob</span></span>
<span data-ttu-id="cba8c-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="cba8c-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cba8c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cba8c-116">-DefaultProfile</span></span>
<span data-ttu-id="cba8c-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cba8c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cba8c-118">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="cba8c-118">-DeviceName</span></span>
<span data-ttu-id="cba8c-119">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="cba8c-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cba8c-120">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="cba8c-120">-EdgeStorageAccountName</span></span>
<span data-ttu-id="cba8c-121">Resurs namn</span><span class="sxs-lookup"><span data-stu-id="cba8c-121">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cba8c-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cba8c-122">-InputObject</span></span>
<span data-ttu-id="cba8c-123">Ange befintligt EdgeStorageAccount-objekt</span><span class="sxs-lookup"><span data-stu-id="cba8c-123">Provide existing EdgeStorageAccount Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer
Parameter Sets: InvokeByInputObjectParameterSet
Aliases: EdgeContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cba8c-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="cba8c-124">-Name</span></span>
<span data-ttu-id="cba8c-125">Resurs namn</span><span class="sxs-lookup"><span data-stu-id="cba8c-125">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases: EdgeContainerName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cba8c-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cba8c-126">-PassThru</span></span>
<span data-ttu-id="cba8c-127">Returnerar sant om det lyckas</span><span class="sxs-lookup"><span data-stu-id="cba8c-127">returns true if successful</span></span>

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

### <span data-ttu-id="cba8c-128">-RefreshData</span><span class="sxs-lookup"><span data-stu-id="cba8c-128">-RefreshData</span></span>
<span data-ttu-id="cba8c-129">Uppdatera metadata för en container med data från molnet</span><span class="sxs-lookup"><span data-stu-id="cba8c-129">Refresh Container Metadata with the data from the cloud</span></span>

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

### <span data-ttu-id="cba8c-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cba8c-130">-ResourceGroupName</span></span>
<span data-ttu-id="cba8c-131">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="cba8c-131">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cba8c-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cba8c-132">-ResourceId</span></span>
<span data-ttu-id="cba8c-133">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="cba8c-133">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cba8c-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cba8c-134">-Confirm</span></span>
<span data-ttu-id="cba8c-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cba8c-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cba8c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cba8c-136">-WhatIf</span></span>
<span data-ttu-id="cba8c-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cba8c-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cba8c-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cba8c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cba8c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cba8c-139">CommonParameters</span></span>
<span data-ttu-id="cba8c-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cba8c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cba8c-141">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cba8c-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cba8c-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cba8c-142">INPUTS</span></span>

### <span data-ttu-id="cba8c-143">System. String</span><span class="sxs-lookup"><span data-stu-id="cba8c-143">System.String</span></span>

### <span data-ttu-id="cba8c-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="cba8c-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="cba8c-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cba8c-145">OUTPUTS</span></span>

### <span data-ttu-id="cba8c-146">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="cba8c-146">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="cba8c-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cba8c-147">NOTES</span></span>

## <span data-ttu-id="cba8c-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cba8c-148">RELATED LINKS</span></span>

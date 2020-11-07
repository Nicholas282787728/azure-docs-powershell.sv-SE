---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/invoke-azdataboxedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeStorageContainer.md
ms.openlocfilehash: c228b00cb8d0d1e8f238e0b2e75427e0d623490f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924678"
---
# <span data-ttu-id="d8d82-101">Invoke-AzDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="d8d82-101">Invoke-AzDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="d8d82-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d8d82-102">SYNOPSIS</span></span>
<span data-ttu-id="d8d82-103">Anropar specifika åtgärder på en lagrings behållare</span><span class="sxs-lookup"><span data-stu-id="d8d82-103">Invokes specific actions on a storage container</span></span>

## <span data-ttu-id="d8d82-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d8d82-104">SYNTAX</span></span>

### <span data-ttu-id="d8d82-105">InvokeByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="d8d82-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-RefreshData] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8d82-106">InvokeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8d82-106">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeStorageContainer [-ResourceId] <String> [-RefreshData] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8d82-107">InvokeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8d82-107">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeStorageContainer [-RefreshData] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 -InputObject <PSDataBoxEdgeStorageContainer> [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8d82-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d8d82-108">DESCRIPTION</span></span>
<span data-ttu-id="d8d82-109">Cmdleten **Invoke-AzDataBoxEdgeStorageContainer** anropar åtgärder för att uppdatera data i en lagrings behållare på en Edge-enhet.</span><span class="sxs-lookup"><span data-stu-id="d8d82-109">The **Invoke-AzDataBoxEdgeStorageContainer** cmdlet invokes actions to refresh the data on a storage container on a Data Box Edge device.</span></span> 

## <span data-ttu-id="d8d82-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d8d82-110">EXAMPLES</span></span>

### <span data-ttu-id="d8d82-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d8d82-111">Example 1</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccount1 -Name container1 -PassThru
PS C:\> true
```

### <span data-ttu-id="d8d82-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="d8d82-112">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccount1 -Name container1 | Invoke-AzDataBoxEdgeStorageContainer
```

## <span data-ttu-id="d8d82-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d8d82-113">PARAMETERS</span></span>

### <span data-ttu-id="d8d82-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d8d82-114">-AsJob</span></span>
<span data-ttu-id="d8d82-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="d8d82-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d8d82-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8d82-116">-DefaultProfile</span></span>
<span data-ttu-id="d8d82-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d8d82-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8d82-118">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="d8d82-118">-DeviceName</span></span>
<span data-ttu-id="d8d82-119">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="d8d82-119">Device Name</span></span>

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

### <span data-ttu-id="d8d82-120">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d8d82-120">-EdgeStorageAccountName</span></span>
<span data-ttu-id="d8d82-121">Resurs namn</span><span class="sxs-lookup"><span data-stu-id="d8d82-121">Resource Name</span></span>

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

### <span data-ttu-id="d8d82-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d8d82-122">-InputObject</span></span>
<span data-ttu-id="d8d82-123">Ange befintligt EdgeStorageAccount-objekt</span><span class="sxs-lookup"><span data-stu-id="d8d82-123">Provide existing EdgeStorageAccount Object</span></span>

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

### <span data-ttu-id="d8d82-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="d8d82-124">-Name</span></span>
<span data-ttu-id="d8d82-125">Resurs namn</span><span class="sxs-lookup"><span data-stu-id="d8d82-125">Resource Name</span></span>

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

### <span data-ttu-id="d8d82-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d8d82-126">-PassThru</span></span>
<span data-ttu-id="d8d82-127">Returnerar sant om det lyckas</span><span class="sxs-lookup"><span data-stu-id="d8d82-127">returns true if successful</span></span>

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

### <span data-ttu-id="d8d82-128">-RefreshData</span><span class="sxs-lookup"><span data-stu-id="d8d82-128">-RefreshData</span></span>
<span data-ttu-id="d8d82-129">Uppdatera metadata för en container med data från molnet</span><span class="sxs-lookup"><span data-stu-id="d8d82-129">Refresh Container Metadata with the data from the cloud</span></span>

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

### <span data-ttu-id="d8d82-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8d82-130">-ResourceGroupName</span></span>
<span data-ttu-id="d8d82-131">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="d8d82-131">Resource Group Name</span></span>

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

### <span data-ttu-id="d8d82-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d8d82-132">-ResourceId</span></span>
<span data-ttu-id="d8d82-133">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="d8d82-133">Azure ResourceId</span></span>

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

### <span data-ttu-id="d8d82-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d8d82-134">-Confirm</span></span>
<span data-ttu-id="d8d82-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d8d82-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8d82-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8d82-136">-WhatIf</span></span>
<span data-ttu-id="d8d82-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d8d82-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d8d82-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d8d82-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8d82-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8d82-139">CommonParameters</span></span>
<span data-ttu-id="d8d82-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8d82-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8d82-141">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d8d82-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8d82-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d8d82-142">INPUTS</span></span>

### <span data-ttu-id="d8d82-143">System. String</span><span class="sxs-lookup"><span data-stu-id="d8d82-143">System.String</span></span>

### <span data-ttu-id="d8d82-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="d8d82-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="d8d82-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d8d82-145">OUTPUTS</span></span>

### <span data-ttu-id="d8d82-146">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="d8d82-146">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="d8d82-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d8d82-147">NOTES</span></span>

## <span data-ttu-id="d8d82-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d8d82-148">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageContainer.md
ms.openlocfilehash: 0e952ba845398fcd221ca7e5f4177a103b1f6155
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092297"
---
# <span data-ttu-id="04ac4-101">Remove-AzDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="04ac4-101">Remove-AzDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="04ac4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="04ac4-102">SYNOPSIS</span></span>
<span data-ttu-id="04ac4-103">Tar bort en lagrings behållare för Edge Storage-kontot på en enhet.</span><span class="sxs-lookup"><span data-stu-id="04ac4-103">Removes a storage container for the Edge Storage account on a device.</span></span>

## <span data-ttu-id="04ac4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="04ac4-104">SYNTAX</span></span>

### <span data-ttu-id="04ac4-105">DeleteByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="04ac4-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04ac4-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="04ac4-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageContainer -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04ac4-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="04ac4-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageContainer -InputObject <PSDataBoxEdgeStorageContainer> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04ac4-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="04ac4-108">DESCRIPTION</span></span>
<span data-ttu-id="04ac4-109">Cmdleten **Remove-AzDataBoxEdgeStorageContainer** tar bort en tillhör ande lagrings behållare för Edge Storage-kontot på en Edge-enhet.</span><span class="sxs-lookup"><span data-stu-id="04ac4-109">The **Remove-AzDataBoxEdgeStorageContainer** cmdlet removes an associated storage container for the Edge Storage account on a Data Box Edge device.</span></span> <span data-ttu-id="04ac4-110">Du kan ange namnet på den lagrings enhet som ska tas bort som en parameter.</span><span class="sxs-lookup"><span data-stu-id="04ac4-110">You can specify the name of the storage container to be removed as a parameter.</span></span>

## <span data-ttu-id="04ac4-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="04ac4-111">EXAMPLES</span></span>

### <span data-ttu-id="04ac4-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="04ac4-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccountname -Name container1
```

## <span data-ttu-id="04ac4-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="04ac4-113">PARAMETERS</span></span>

### <span data-ttu-id="04ac4-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="04ac4-114">-AsJob</span></span>
<span data-ttu-id="04ac4-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="04ac4-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="04ac4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04ac4-116">-DefaultProfile</span></span>
<span data-ttu-id="04ac4-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="04ac4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04ac4-118">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="04ac4-118">-DeviceName</span></span>
<span data-ttu-id="04ac4-119">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="04ac4-119">Device Name</span></span>

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

### <span data-ttu-id="04ac4-120">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="04ac4-120">-EdgeStorageAccountName</span></span>
<span data-ttu-id="04ac4-121">Ange befintliga EdgeStorageAccount namn</span><span class="sxs-lookup"><span data-stu-id="04ac4-121">Provide existing EdgeStorageAccount's Name</span></span>

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

### <span data-ttu-id="04ac4-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="04ac4-122">-InputObject</span></span>
<span data-ttu-id="04ac4-123">Infoga objekt</span><span class="sxs-lookup"><span data-stu-id="04ac4-123">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="04ac4-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="04ac4-124">-Name</span></span>
<span data-ttu-id="04ac4-125">Resurs namn</span><span class="sxs-lookup"><span data-stu-id="04ac4-125">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04ac4-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="04ac4-126">-PassThru</span></span>
<span data-ttu-id="04ac4-127">Returnerar sant om det lyckas</span><span class="sxs-lookup"><span data-stu-id="04ac4-127">returns true if successful</span></span>

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

### <span data-ttu-id="04ac4-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04ac4-128">-ResourceGroupName</span></span>
<span data-ttu-id="04ac4-129">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="04ac4-129">Resource Group Name</span></span>

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

### <span data-ttu-id="04ac4-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="04ac4-130">-ResourceId</span></span>
<span data-ttu-id="04ac4-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="04ac4-131">Azure ResourceId</span></span>

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

### <span data-ttu-id="04ac4-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="04ac4-132">-Confirm</span></span>
<span data-ttu-id="04ac4-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="04ac4-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04ac4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04ac4-134">-WhatIf</span></span>
<span data-ttu-id="04ac4-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="04ac4-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="04ac4-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="04ac4-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04ac4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04ac4-137">CommonParameters</span></span>
<span data-ttu-id="04ac4-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04ac4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04ac4-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="04ac4-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04ac4-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="04ac4-140">INPUTS</span></span>

### <span data-ttu-id="04ac4-141">System. String</span><span class="sxs-lookup"><span data-stu-id="04ac4-141">System.String</span></span>

### <span data-ttu-id="04ac4-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="04ac4-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="04ac4-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="04ac4-143">OUTPUTS</span></span>

### <span data-ttu-id="04ac4-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="04ac4-144">System.Boolean</span></span>

## <span data-ttu-id="04ac4-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="04ac4-145">NOTES</span></span>

## <span data-ttu-id="04ac4-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="04ac4-146">RELATED LINKS</span></span>

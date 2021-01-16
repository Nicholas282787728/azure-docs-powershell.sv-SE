---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageContainer.md
ms.openlocfilehash: 0e952ba845398fcd221ca7e5f4177a103b1f6155
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98411795"
---
# <span data-ttu-id="89ce8-101">Remove-AzDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="89ce8-101">Remove-AzDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="89ce8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="89ce8-102">SYNOPSIS</span></span>
<span data-ttu-id="89ce8-103">Tar bort en lagrings behållare för Edge Storage-kontot på en enhet.</span><span class="sxs-lookup"><span data-stu-id="89ce8-103">Removes a storage container for the Edge Storage account on a device.</span></span>

## <span data-ttu-id="89ce8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="89ce8-104">SYNTAX</span></span>

### <span data-ttu-id="89ce8-105">DeleteByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="89ce8-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89ce8-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="89ce8-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageContainer -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89ce8-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="89ce8-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageContainer -InputObject <PSDataBoxEdgeStorageContainer> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89ce8-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="89ce8-108">DESCRIPTION</span></span>
<span data-ttu-id="89ce8-109">Cmdleten **Remove-AzDataBoxEdgeStorageContainer** tar bort en tillhör ande lagrings behållare för Edge Storage-kontot på en Edge-enhet.</span><span class="sxs-lookup"><span data-stu-id="89ce8-109">The **Remove-AzDataBoxEdgeStorageContainer** cmdlet removes an associated storage container for the Edge Storage account on a Data Box Edge device.</span></span> <span data-ttu-id="89ce8-110">Du kan ange namnet på den lagrings enhet som ska tas bort som en parameter.</span><span class="sxs-lookup"><span data-stu-id="89ce8-110">You can specify the name of the storage container to be removed as a parameter.</span></span>

## <span data-ttu-id="89ce8-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="89ce8-111">EXAMPLES</span></span>

### <span data-ttu-id="89ce8-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="89ce8-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccountname -Name container1
```

## <span data-ttu-id="89ce8-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="89ce8-113">PARAMETERS</span></span>

### <span data-ttu-id="89ce8-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="89ce8-114">-AsJob</span></span>
<span data-ttu-id="89ce8-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="89ce8-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="89ce8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89ce8-116">-DefaultProfile</span></span>
<span data-ttu-id="89ce8-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="89ce8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89ce8-118">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="89ce8-118">-DeviceName</span></span>
<span data-ttu-id="89ce8-119">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="89ce8-119">Device Name</span></span>

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

### <span data-ttu-id="89ce8-120">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="89ce8-120">-EdgeStorageAccountName</span></span>
<span data-ttu-id="89ce8-121">Ange befintliga EdgeStorageAccount namn</span><span class="sxs-lookup"><span data-stu-id="89ce8-121">Provide existing EdgeStorageAccount's Name</span></span>

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

### <span data-ttu-id="89ce8-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="89ce8-122">-InputObject</span></span>
<span data-ttu-id="89ce8-123">Infoga objekt</span><span class="sxs-lookup"><span data-stu-id="89ce8-123">Input Object</span></span>

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

### <span data-ttu-id="89ce8-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="89ce8-124">-Name</span></span>
<span data-ttu-id="89ce8-125">Resurs namn</span><span class="sxs-lookup"><span data-stu-id="89ce8-125">Resource Name</span></span>

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

### <span data-ttu-id="89ce8-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="89ce8-126">-PassThru</span></span>
<span data-ttu-id="89ce8-127">Returnerar sant om det lyckas</span><span class="sxs-lookup"><span data-stu-id="89ce8-127">returns true if successful</span></span>

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

### <span data-ttu-id="89ce8-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89ce8-128">-ResourceGroupName</span></span>
<span data-ttu-id="89ce8-129">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="89ce8-129">Resource Group Name</span></span>

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

### <span data-ttu-id="89ce8-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="89ce8-130">-ResourceId</span></span>
<span data-ttu-id="89ce8-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="89ce8-131">Azure ResourceId</span></span>

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

### <span data-ttu-id="89ce8-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="89ce8-132">-Confirm</span></span>
<span data-ttu-id="89ce8-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="89ce8-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89ce8-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89ce8-134">-WhatIf</span></span>
<span data-ttu-id="89ce8-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="89ce8-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="89ce8-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="89ce8-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89ce8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89ce8-137">CommonParameters</span></span>
<span data-ttu-id="89ce8-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89ce8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89ce8-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="89ce8-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89ce8-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="89ce8-140">INPUTS</span></span>

### <span data-ttu-id="89ce8-141">System. String</span><span class="sxs-lookup"><span data-stu-id="89ce8-141">System.String</span></span>

### <span data-ttu-id="89ce8-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="89ce8-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="89ce8-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="89ce8-143">OUTPUTS</span></span>

### <span data-ttu-id="89ce8-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="89ce8-144">System.Boolean</span></span>

## <span data-ttu-id="89ce8-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="89ce8-145">NOTES</span></span>

## <span data-ttu-id="89ce8-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="89ce8-146">RELATED LINKS</span></span>

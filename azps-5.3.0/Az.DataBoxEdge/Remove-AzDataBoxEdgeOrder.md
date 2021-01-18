---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeOrder.md
ms.openlocfilehash: 84e17ac36e446d784715c2de38944f7b44d1337d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98526328"
---
# <span data-ttu-id="1e77c-101">Remove-AzDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="1e77c-101">Remove-AzDataBoxEdgeOrder</span></span>

## <span data-ttu-id="1e77c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1e77c-102">SYNOPSIS</span></span>
<span data-ttu-id="1e77c-103">Tar bort en enhets ordning.</span><span class="sxs-lookup"><span data-stu-id="1e77c-103">Removes the order for a device.</span></span>

## <span data-ttu-id="1e77c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1e77c-104">SYNTAX</span></span>

### <span data-ttu-id="1e77c-105">DeleteByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="1e77c-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e77c-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1e77c-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeOrder -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e77c-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1e77c-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeOrder -InputObject <PSDataBoxEdgeOrder> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e77c-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1e77c-108">DESCRIPTION</span></span>
<span data-ttu-id="1e77c-109">Cmdleten **Remove-AzDataBoxEdgeOrder** tar bort en befintlig order för Edge-enheten.</span><span class="sxs-lookup"><span data-stu-id="1e77c-109">The **Remove-AzDataBoxEdgeOrder** cmdlet deletes an existing order for a Data Box Edge device.</span></span>

## <span data-ttu-id="1e77c-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1e77c-110">EXAMPLES</span></span>

### <span data-ttu-id="1e77c-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1e77c-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeOrder -ResourceGroupName resourceGroupName -DeviceName deviceName
```

## <span data-ttu-id="1e77c-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1e77c-112">PARAMETERS</span></span>

### <span data-ttu-id="1e77c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1e77c-113">-AsJob</span></span>
<span data-ttu-id="1e77c-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="1e77c-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1e77c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e77c-115">-DefaultProfile</span></span>
<span data-ttu-id="1e77c-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1e77c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e77c-117">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="1e77c-117">-DeviceName</span></span>
<span data-ttu-id="1e77c-118">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="1e77c-118">Device Name</span></span>

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

### <span data-ttu-id="1e77c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1e77c-119">-InputObject</span></span>
<span data-ttu-id="1e77c-120">Infoga objekt</span><span class="sxs-lookup"><span data-stu-id="1e77c-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1e77c-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1e77c-121">-PassThru</span></span>
<span data-ttu-id="1e77c-122">Returnerar sant om det lyckas</span><span class="sxs-lookup"><span data-stu-id="1e77c-122">returns true if successful</span></span>

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

### <span data-ttu-id="1e77c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e77c-123">-ResourceGroupName</span></span>
<span data-ttu-id="1e77c-124">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="1e77c-124">Resource Group Name</span></span>

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

### <span data-ttu-id="1e77c-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1e77c-125">-ResourceId</span></span>
<span data-ttu-id="1e77c-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="1e77c-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="1e77c-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1e77c-127">-Confirm</span></span>
<span data-ttu-id="1e77c-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1e77c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e77c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e77c-129">-WhatIf</span></span>
<span data-ttu-id="1e77c-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1e77c-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1e77c-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1e77c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e77c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e77c-132">CommonParameters</span></span>
<span data-ttu-id="1e77c-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e77c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e77c-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1e77c-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e77c-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1e77c-135">INPUTS</span></span>

### <span data-ttu-id="1e77c-136">System. String</span><span class="sxs-lookup"><span data-stu-id="1e77c-136">System.String</span></span>

### <span data-ttu-id="1e77c-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="1e77c-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span></span>

## <span data-ttu-id="1e77c-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1e77c-138">OUTPUTS</span></span>

### <span data-ttu-id="1e77c-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="1e77c-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span></span>

## <span data-ttu-id="1e77c-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1e77c-140">NOTES</span></span>

## <span data-ttu-id="1e77c-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1e77c-141">RELATED LINKS</span></span>

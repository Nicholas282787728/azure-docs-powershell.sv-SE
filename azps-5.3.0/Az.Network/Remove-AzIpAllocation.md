---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpAllocation.md
ms.openlocfilehash: 7a81ce555ed99de1504dc0625c0c83cdab6ab881
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523223"
---
# <span data-ttu-id="9a43a-101">Remove-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="9a43a-101">Remove-AzIpAllocation</span></span>

## <span data-ttu-id="9a43a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9a43a-102">SYNOPSIS</span></span>
<span data-ttu-id="9a43a-103">Tar bort en Azure-IpAllocation.</span><span class="sxs-lookup"><span data-stu-id="9a43a-103">Deletes an Azure IpAllocation.</span></span>

## <span data-ttu-id="9a43a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9a43a-104">SYNTAX</span></span>

### <span data-ttu-id="9a43a-105">DeleteByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a43a-105">DeleteByNameParameterSet</span></span>
```
Remove-AzIpAllocation [-Name] <String> [-ResourceGroupName] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a43a-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a43a-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzIpAllocation [-InputObject] <PSTopLevelResource> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a43a-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a43a-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzIpAllocation [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a43a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9a43a-108">DESCRIPTION</span></span>
<span data-ttu-id="9a43a-109">Cmdleten **Remove-AzIpAllocation** tar bort en Azure-IpAllocation</span><span class="sxs-lookup"><span data-stu-id="9a43a-109">The **Remove-AzIpAllocation** cmdlet deletes an Azure IpAllocation</span></span>

## <span data-ttu-id="9a43a-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9a43a-110">EXAMPLES</span></span>

### <span data-ttu-id="9a43a-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9a43a-111">Example 1</span></span>
```powershell
Remove-AzIpAllocation -ResourceGroupName 'TestResourceGroup' -Name 'TestIpAllocation'
```

## <span data-ttu-id="9a43a-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9a43a-112">PARAMETERS</span></span>

### <span data-ttu-id="9a43a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9a43a-113">-AsJob</span></span>
<span data-ttu-id="9a43a-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="9a43a-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9a43a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a43a-115">-DefaultProfile</span></span>
<span data-ttu-id="9a43a-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9a43a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a43a-117">-Force</span><span class="sxs-lookup"><span data-stu-id="9a43a-117">-Force</span></span>
<span data-ttu-id="9a43a-118">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="9a43a-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="9a43a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9a43a-119">-InputObject</span></span>
<span data-ttu-id="9a43a-120">{{Fill InputObject Description}}</span><span class="sxs-lookup"><span data-stu-id="9a43a-120">{{ Fill InputObject Description }}</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSTopLevelResource
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a43a-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="9a43a-121">-Name</span></span>
<span data-ttu-id="9a43a-122">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="9a43a-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a43a-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9a43a-123">-PassThru</span></span>
<span data-ttu-id="9a43a-124">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="9a43a-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9a43a-125">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="9a43a-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9a43a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a43a-126">-ResourceGroupName</span></span>
<span data-ttu-id="9a43a-127">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="9a43a-127">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a43a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9a43a-128">-ResourceId</span></span>
<span data-ttu-id="9a43a-129">IpAllocation resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="9a43a-129">IpAllocation resource id.</span></span>

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

### <span data-ttu-id="9a43a-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9a43a-130">-Confirm</span></span>
<span data-ttu-id="9a43a-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9a43a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a43a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a43a-132">-WhatIf</span></span>
<span data-ttu-id="9a43a-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9a43a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a43a-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9a43a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a43a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a43a-135">CommonParameters</span></span>
<span data-ttu-id="9a43a-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a43a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a43a-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9a43a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a43a-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9a43a-138">INPUTS</span></span>

### <span data-ttu-id="9a43a-139">System. String</span><span class="sxs-lookup"><span data-stu-id="9a43a-139">System.String</span></span>

## <span data-ttu-id="9a43a-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9a43a-140">OUTPUTS</span></span>

### <span data-ttu-id="9a43a-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9a43a-141">System.Boolean</span></span>

## <span data-ttu-id="9a43a-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9a43a-142">NOTES</span></span>

## <span data-ttu-id="9a43a-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9a43a-143">RELATED LINKS</span></span>

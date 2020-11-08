---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgriddomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomain.md
ms.openlocfilehash: 2eb9fc2575af16f6f0bc2d6e239f63d95a0c27d7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089155"
---
# <span data-ttu-id="718c7-101">Remove-AzEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="718c7-101">Remove-AzEventGridDomain</span></span>

## <span data-ttu-id="718c7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="718c7-102">SYNOPSIS</span></span>
<span data-ttu-id="718c7-103">Tar bort en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="718c7-103">Removes an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="718c7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="718c7-104">SYNTAX</span></span>

### <span data-ttu-id="718c7-105">DomainNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="718c7-105">DomainNameParameterSet (Default)</span></span>
```
Remove-AzEventGridDomain [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="718c7-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="718c7-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridDomain [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="718c7-107">DomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="718c7-107">DomainInputObjectParameterSet</span></span>
```
Remove-AzEventGridDomain [-InputObject] <PSDomain> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="718c7-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="718c7-108">DESCRIPTION</span></span>
<span data-ttu-id="718c7-109">Tar bort en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="718c7-109">Removes an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="718c7-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="718c7-110">EXAMPLES</span></span>

### <span data-ttu-id="718c7-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="718c7-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridDomain -ResourceGroupName MyResourceGroupName -Name Domain1
```

<span data-ttu-id="718c7-112">Tar bort händelse rutnäts domänen \` domain1 \` i resurs gruppen \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="718c7-112">Removes the Event Grid Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="718c7-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="718c7-113">Example 2</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/Domains/Domain1" | Remove-AzEventGridDomain
```

<span data-ttu-id="718c7-114">Tar bort händelse rutnäts domänen \` domain1 \` i resurs gruppen \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="718c7-114">Removes the Event Grid Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="718c7-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="718c7-115">PARAMETERS</span></span>

### <span data-ttu-id="718c7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="718c7-116">-DefaultProfile</span></span>
<span data-ttu-id="718c7-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="718c7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="718c7-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="718c7-118">-InputObject</span></span>
<span data-ttu-id="718c7-119">EventGrid.</span><span class="sxs-lookup"><span data-stu-id="718c7-119">EventGrid Domain object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomain
Parameter Sets: DomainInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="718c7-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="718c7-120">-Name</span></span>
<span data-ttu-id="718c7-121">EventGrid domän namn.</span><span class="sxs-lookup"><span data-stu-id="718c7-121">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: DomainName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="718c7-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="718c7-122">-PassThru</span></span>
<span data-ttu-id="718c7-123">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="718c7-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="718c7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="718c7-124">-ResourceGroupName</span></span>
<span data-ttu-id="718c7-125">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="718c7-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="718c7-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="718c7-126">-ResourceId</span></span>
<span data-ttu-id="718c7-127">Resurs-ID som representerar händelse rutnäts domänen.</span><span class="sxs-lookup"><span data-stu-id="718c7-127">Resource Identifier representing the Event Grid Domain.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="718c7-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="718c7-128">-Confirm</span></span>
<span data-ttu-id="718c7-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="718c7-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="718c7-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="718c7-130">-WhatIf</span></span>
<span data-ttu-id="718c7-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="718c7-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="718c7-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="718c7-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="718c7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="718c7-133">CommonParameters</span></span>
<span data-ttu-id="718c7-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="718c7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="718c7-135">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="718c7-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="718c7-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="718c7-136">INPUTS</span></span>

### <span data-ttu-id="718c7-137">System. String</span><span class="sxs-lookup"><span data-stu-id="718c7-137">System.String</span></span>

### <span data-ttu-id="718c7-138">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="718c7-138">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="718c7-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="718c7-139">OUTPUTS</span></span>

### <span data-ttu-id="718c7-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="718c7-140">System.Boolean</span></span>

## <span data-ttu-id="718c7-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="718c7-141">NOTES</span></span>

## <span data-ttu-id="718c7-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="718c7-142">RELATED LINKS</span></span>

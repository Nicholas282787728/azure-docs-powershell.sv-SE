---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgriddomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomain.md
ms.openlocfilehash: 88d5e0baadaa625a2cd33a795b66d7484d496330
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98520803"
---
# <span data-ttu-id="dc274-101">Remove-AzEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="dc274-101">Remove-AzEventGridDomain</span></span>

## <span data-ttu-id="dc274-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dc274-102">SYNOPSIS</span></span>
<span data-ttu-id="dc274-103">Tar bort en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="dc274-103">Removes an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="dc274-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dc274-104">SYNTAX</span></span>

### <span data-ttu-id="dc274-105">DomainNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="dc274-105">DomainNameParameterSet (Default)</span></span>
```
Remove-AzEventGridDomain [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc274-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc274-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridDomain [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc274-107">DomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc274-107">DomainInputObjectParameterSet</span></span>
```
Remove-AzEventGridDomain [-InputObject] <PSDomain> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc274-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dc274-108">DESCRIPTION</span></span>
<span data-ttu-id="dc274-109">Tar bort en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="dc274-109">Removes an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="dc274-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dc274-110">EXAMPLES</span></span>

### <span data-ttu-id="dc274-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="dc274-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridDomain -ResourceGroupName MyResourceGroupName -Name Domain1
```

<span data-ttu-id="dc274-112">Tar bort händelse rutnäts domänen \` domain1 \` i resurs gruppen \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="dc274-112">Removes the Event Grid Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="dc274-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="dc274-113">Example 2</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/Domains/Domain1" | Remove-AzEventGridDomain
```

<span data-ttu-id="dc274-114">Tar bort händelse rutnäts domänen \` domain1 \` i resurs gruppen \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="dc274-114">Removes the Event Grid Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="dc274-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dc274-115">PARAMETERS</span></span>

### <span data-ttu-id="dc274-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc274-116">-DefaultProfile</span></span>
<span data-ttu-id="dc274-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dc274-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc274-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dc274-118">-InputObject</span></span>
<span data-ttu-id="dc274-119">EventGrid.</span><span class="sxs-lookup"><span data-stu-id="dc274-119">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="dc274-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="dc274-120">-Name</span></span>
<span data-ttu-id="dc274-121">EventGrid domän namn.</span><span class="sxs-lookup"><span data-stu-id="dc274-121">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: DomainName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc274-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dc274-122">-PassThru</span></span>
<span data-ttu-id="dc274-123">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="dc274-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="dc274-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc274-124">-ResourceGroupName</span></span>
<span data-ttu-id="dc274-125">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="dc274-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc274-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dc274-126">-ResourceId</span></span>
<span data-ttu-id="dc274-127">Resurs-ID som representerar händelse rutnäts domänen.</span><span class="sxs-lookup"><span data-stu-id="dc274-127">Resource Identifier representing the Event Grid Domain.</span></span>

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

### <span data-ttu-id="dc274-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="dc274-128">-Confirm</span></span>
<span data-ttu-id="dc274-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="dc274-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc274-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc274-130">-WhatIf</span></span>
<span data-ttu-id="dc274-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="dc274-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc274-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="dc274-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc274-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc274-133">CommonParameters</span></span>
<span data-ttu-id="dc274-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc274-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc274-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dc274-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc274-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dc274-136">INPUTS</span></span>

### <span data-ttu-id="dc274-137">System. String</span><span class="sxs-lookup"><span data-stu-id="dc274-137">System.String</span></span>

### <span data-ttu-id="dc274-138">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="dc274-138">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="dc274-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dc274-139">OUTPUTS</span></span>

### <span data-ttu-id="dc274-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dc274-140">System.Boolean</span></span>

## <span data-ttu-id="dc274-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dc274-141">NOTES</span></span>

## <span data-ttu-id="dc274-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dc274-142">RELATED LINKS</span></span>

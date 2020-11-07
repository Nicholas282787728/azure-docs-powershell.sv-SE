---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNamespace.md
ms.openlocfilehash: bb5f6b57b83bfc2642ab01abb277c86b6e1f4984
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93926173"
---
# <span data-ttu-id="80c8f-101">Remove-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="80c8f-101">Remove-AzEventHubNamespace</span></span>

## <span data-ttu-id="80c8f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="80c8f-102">SYNOPSIS</span></span>
<span data-ttu-id="80c8f-103">Tar bort det angivna namn området för Event Hubs.</span><span class="sxs-lookup"><span data-stu-id="80c8f-103">Removes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="80c8f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="80c8f-104">SYNTAX</span></span>

### <span data-ttu-id="80c8f-105">NamespaceParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="80c8f-105">NamespaceParameterSet (Default)</span></span>
```
Remove-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80c8f-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="80c8f-106">NamespaceInputObjectSet</span></span>
```
Remove-AzEventHubNamespace [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80c8f-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="80c8f-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzEventHubNamespace [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80c8f-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="80c8f-108">DESCRIPTION</span></span>
<span data-ttu-id="80c8f-109">Remove-AzEventHubNamespace-cmdleten tar bort och tar bort det angivna namn området för Event Hub.</span><span class="sxs-lookup"><span data-stu-id="80c8f-109">The Remove-AzEventHubNamespace cmdlet removes and deletes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="80c8f-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="80c8f-110">EXAMPLES</span></span>

### <span data-ttu-id="80c8f-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="80c8f-111">Example 1</span></span>
```
PS C:\> Remove-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName
```

<span data-ttu-id="80c8f-112">Tar bort namn områdes \` MyNamespaceName \` för Event Hub i resurs gruppen \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="80c8f-112">Removes the Event Hubs namespace \`MyNamespaceName\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="80c8f-113">Exempel 2,1 – InputObject – använder variabel:</span><span class="sxs-lookup"><span data-stu-id="80c8f-113">Example 2.1 - InputObject - Using Variable:</span></span>
```
PS C:\> $inputObject = Get-AzEventHubNamespace <params> 
PS C:\> Remove-AzEventHubNamespace -InputObject $inputObject
```

### <span data-ttu-id="80c8f-114">Exempel 2,1 – InputObject-med rör dragning:</span><span class="sxs-lookup"><span data-stu-id="80c8f-114">Example 2.1 - InputObject - Using Piping:</span></span>
```
PS C:\> Get-AzEventHubNamespace <params> | Remove-AzEventHubNamespace
```

### <span data-ttu-id="80c8f-115">Exempel 3,1-ResourceId-använder variabel</span><span class="sxs-lookup"><span data-stu-id="80c8f-115">Example 3.1 - ResourceId - Using Variable</span></span>
```
PS C:\> $resourceid = Get-AzEventHubNamespace <params>
PS C:\> Remove-AzEventHubNamespace -ResourceId $resourceid.Id
```

### <span data-ttu-id="80c8f-116">Exempel 3,2-ResourceId-använder rör:</span><span class="sxs-lookup"><span data-stu-id="80c8f-116">Example 3.2 - ResourceId - Using Piping:</span></span>
```
PS C:\> Get-AzResource -ResourceType Microsoft.EventHub/Namespaces | Remove-AzEventHubNamespace
```

### <span data-ttu-id="80c8f-117">Exempel 3,3-ResourceId-använder sträng:</span><span class="sxs-lookup"><span data-stu-id="80c8f-117">Example 3.3 - ResourceId - Using String:</span></span>
```
PS C:\> Remove-AzEventHubNamespace -ResourceId "/subscriptions/xxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName"
```

## <span data-ttu-id="80c8f-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="80c8f-118">PARAMETERS</span></span>

### <span data-ttu-id="80c8f-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="80c8f-119">-AsJob</span></span>
<span data-ttu-id="80c8f-120">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="80c8f-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="80c8f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80c8f-121">-DefaultProfile</span></span>
<span data-ttu-id="80c8f-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="80c8f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80c8f-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="80c8f-123">-InputObject</span></span>
<span data-ttu-id="80c8f-124">EventHubs</span><span class="sxs-lookup"><span data-stu-id="80c8f-124">EventHubs Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="80c8f-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="80c8f-125">-Name</span></span>
<span data-ttu-id="80c8f-126">Namn område för EventHub</span><span class="sxs-lookup"><span data-stu-id="80c8f-126">EventHub Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceParameterSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80c8f-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="80c8f-127">-PassThru</span></span>
<span data-ttu-id="80c8f-128">Om du anger detta returneras sant om kommandot lyckades.</span><span class="sxs-lookup"><span data-stu-id="80c8f-128">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="80c8f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80c8f-129">-ResourceGroupName</span></span>
<span data-ttu-id="80c8f-130">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="80c8f-130">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80c8f-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="80c8f-131">-ResourceId</span></span>
<span data-ttu-id="80c8f-132">Resurs-ID för EventHubs</span><span class="sxs-lookup"><span data-stu-id="80c8f-132">EventHubs Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80c8f-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="80c8f-133">-Confirm</span></span>
<span data-ttu-id="80c8f-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="80c8f-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80c8f-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80c8f-135">-WhatIf</span></span>
<span data-ttu-id="80c8f-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="80c8f-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80c8f-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="80c8f-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80c8f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80c8f-138">CommonParameters</span></span>
<span data-ttu-id="80c8f-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80c8f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80c8f-140">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80c8f-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80c8f-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="80c8f-141">INPUTS</span></span>

### <span data-ttu-id="80c8f-142">System. String</span><span class="sxs-lookup"><span data-stu-id="80c8f-142">System.String</span></span>

### <span data-ttu-id="80c8f-143">Microsoft. Azure. commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="80c8f-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="80c8f-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="80c8f-144">OUTPUTS</span></span>

### <span data-ttu-id="80c8f-145">System. Void</span><span class="sxs-lookup"><span data-stu-id="80c8f-145">System.Void</span></span>

## <span data-ttu-id="80c8f-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="80c8f-146">NOTES</span></span>

## <span data-ttu-id="80c8f-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="80c8f-147">RELATED LINKS</span></span>

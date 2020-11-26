---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNamespace.md
ms.openlocfilehash: 29f2b961637a398470f6455d0d2330ce5fd863a6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270676"
---
# <span data-ttu-id="85da4-101">Remove-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="85da4-101">Remove-AzEventHubNamespace</span></span>

## <span data-ttu-id="85da4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="85da4-102">SYNOPSIS</span></span>
<span data-ttu-id="85da4-103">Tar bort det angivna namn området för Event Hubs.</span><span class="sxs-lookup"><span data-stu-id="85da4-103">Removes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="85da4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="85da4-104">SYNTAX</span></span>

### <span data-ttu-id="85da4-105">NamespaceParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="85da4-105">NamespaceParameterSet (Default)</span></span>
```
Remove-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85da4-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="85da4-106">NamespaceInputObjectSet</span></span>
```
Remove-AzEventHubNamespace [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85da4-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="85da4-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzEventHubNamespace [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85da4-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="85da4-108">DESCRIPTION</span></span>
<span data-ttu-id="85da4-109">Remove-AzEventHubNamespace-cmdleten tar bort och tar bort det angivna namn området för Event Hub.</span><span class="sxs-lookup"><span data-stu-id="85da4-109">The Remove-AzEventHubNamespace cmdlet removes and deletes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="85da4-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="85da4-110">EXAMPLES</span></span>

### <span data-ttu-id="85da4-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="85da4-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName
```

<span data-ttu-id="85da4-112">Tar bort namn områdes \` MyNamespaceName \` för Event Hub i resurs gruppen \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="85da4-112">Removes the Event Hubs namespace \`MyNamespaceName\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="85da4-113">Exempel 2: InputObject – använder variabel:</span><span class="sxs-lookup"><span data-stu-id="85da4-113">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputObject = Get-AzEventHubNamespace <params> 
PS C:\> Remove-AzEventHubNamespace -InputObject $inputObject
```

### <span data-ttu-id="85da4-114">Exempel 3: InputObject-använder rör:</span><span class="sxs-lookup"><span data-stu-id="85da4-114">Example 3: InputObject - Using Piping:</span></span>
```powershell
PS C:\> Get-AzEventHubNamespace <params> | Remove-AzEventHubNamespace
```

### <span data-ttu-id="85da4-115">Exempel 4: ResourceId-använder variabel</span><span class="sxs-lookup"><span data-stu-id="85da4-115">Example 4: ResourceId - Using Variable</span></span>
```powershell
PS C:\> $resourceid = Get-AzEventHubNamespace <params>
PS C:\> Remove-AzEventHubNamespace -ResourceId $resourceid.Id
```

### <span data-ttu-id="85da4-116">Exempel 5: ResourceId-använder rör:</span><span class="sxs-lookup"><span data-stu-id="85da4-116">Example 5: ResourceId - Using Piping:</span></span>
```powershell
PS C:\> Get-AzResource -ResourceType Microsoft.EventHub/Namespaces | Remove-AzEventHubNamespace
```

### <span data-ttu-id="85da4-117">Exempel 6: ResourceId-använder sträng:</span><span class="sxs-lookup"><span data-stu-id="85da4-117">Example 6: ResourceId - Using String:</span></span>
```powershell
PS C:\> Remove-AzEventHubNamespace -ResourceId "/subscriptions/xxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName"
```

## <span data-ttu-id="85da4-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="85da4-118">PARAMETERS</span></span>

### <span data-ttu-id="85da4-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="85da4-119">-AsJob</span></span>
<span data-ttu-id="85da4-120">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="85da4-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="85da4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85da4-121">-DefaultProfile</span></span>
<span data-ttu-id="85da4-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="85da4-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85da4-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="85da4-123">-InputObject</span></span>
<span data-ttu-id="85da4-124">EventHubs</span><span class="sxs-lookup"><span data-stu-id="85da4-124">EventHubs Namespace Object</span></span>

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

### <span data-ttu-id="85da4-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="85da4-125">-Name</span></span>
<span data-ttu-id="85da4-126">Namn område för EventHub</span><span class="sxs-lookup"><span data-stu-id="85da4-126">EventHub Namespace Name</span></span>

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

### <span data-ttu-id="85da4-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="85da4-127">-PassThru</span></span>
<span data-ttu-id="85da4-128">Om du anger detta returneras sant om kommandot lyckades.</span><span class="sxs-lookup"><span data-stu-id="85da4-128">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="85da4-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85da4-129">-ResourceGroupName</span></span>
<span data-ttu-id="85da4-130">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="85da4-130">Resource Group Name</span></span>

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

### <span data-ttu-id="85da4-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="85da4-131">-ResourceId</span></span>
<span data-ttu-id="85da4-132">Resurs-ID för EventHubs</span><span class="sxs-lookup"><span data-stu-id="85da4-132">EventHubs Namespace Resource Id</span></span>

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

### <span data-ttu-id="85da4-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="85da4-133">-Confirm</span></span>
<span data-ttu-id="85da4-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="85da4-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85da4-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85da4-135">-WhatIf</span></span>
<span data-ttu-id="85da4-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="85da4-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85da4-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="85da4-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85da4-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85da4-138">CommonParameters</span></span>
<span data-ttu-id="85da4-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85da4-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85da4-140">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85da4-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85da4-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="85da4-141">INPUTS</span></span>

### <span data-ttu-id="85da4-142">System. String</span><span class="sxs-lookup"><span data-stu-id="85da4-142">System.String</span></span>

### <span data-ttu-id="85da4-143">Microsoft. Azure. commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="85da4-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="85da4-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="85da4-144">OUTPUTS</span></span>

### <span data-ttu-id="85da4-145">System. Void</span><span class="sxs-lookup"><span data-stu-id="85da4-145">System.Void</span></span>

## <span data-ttu-id="85da4-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="85da4-146">NOTES</span></span>

## <span data-ttu-id="85da4-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="85da4-147">RELATED LINKS</span></span>
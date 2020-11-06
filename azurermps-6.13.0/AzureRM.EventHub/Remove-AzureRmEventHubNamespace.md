---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespace.md
ms.openlocfilehash: 6df8d5539bf340df5e00ad69ac557bc2cbb8ccaa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577038"
---
# <span data-ttu-id="20fce-101">Remove-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="20fce-101">Remove-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="20fce-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="20fce-102">SYNOPSIS</span></span>
<span data-ttu-id="20fce-103">Tar bort det angivna namn området för Event Hubs.</span><span class="sxs-lookup"><span data-stu-id="20fce-103">Removes the specified Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="20fce-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="20fce-104">SYNTAX</span></span>

### <span data-ttu-id="20fce-105">NamespaceParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="20fce-105">NamespaceParameterSet (Default)</span></span>
```
Remove-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20fce-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="20fce-106">NamespaceInputObjectSet</span></span>
```
Remove-AzureRmEventHubNamespace [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20fce-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="20fce-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzureRmEventHubNamespace [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20fce-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="20fce-108">DESCRIPTION</span></span>
<span data-ttu-id="20fce-109">Remove-AzureRmEventHubNamespace-cmdleten tar bort och tar bort det angivna namn området för Event Hub.</span><span class="sxs-lookup"><span data-stu-id="20fce-109">The Remove-AzureRmEventHubNamespace cmdlet removes and deletes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="20fce-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="20fce-110">EXAMPLES</span></span>

### <span data-ttu-id="20fce-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="20fce-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName
```

<span data-ttu-id="20fce-112">Tar bort namn områdes \` MyNamespaceName \` för Event Hub i resurs gruppen \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="20fce-112">Removes the Event Hubs namespace \`MyNamespaceName\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="20fce-113">Exempel 2,1 – InputObject – använder variabel:</span><span class="sxs-lookup"><span data-stu-id="20fce-113">Example 2.1 - InputObject - Using Variable:</span></span>
```
PS C:\> $inputObject = Get-AzureRmEventHubNamespace <params> 
PS C:\> Remove-AzureRmEventHubNamespace -InputObject $inputObject
```

### <span data-ttu-id="20fce-114">Exempel 2,1 – InputObject-med rör dragning:</span><span class="sxs-lookup"><span data-stu-id="20fce-114">Example 2.1 - InputObject - Using Piping:</span></span>
```
PS C:\> Get-AzureRmEventHubNamespace <params> | Remove-AzureRmEventHubNamespace
```

### <span data-ttu-id="20fce-115">Exempel 3,1-ResourceId-använder variabel</span><span class="sxs-lookup"><span data-stu-id="20fce-115">Example 3.1 - ResourceId - Using Variable</span></span>
```
PS C:\> $resourceid = Get-AzureRmEventHubNamespace <params>
PS C:\> Remove-AzureRmEventHubNamespace -ResourceId $resourceid.Id
```

### <span data-ttu-id="20fce-116">Exempel 3,2-ResourceId-använder rör:</span><span class="sxs-lookup"><span data-stu-id="20fce-116">Example 3.2 - ResourceId - Using Piping:</span></span>
```
PS C:\> Get-AzureRmResource -ResourceType Microsoft.EventHub/Namespaces | Remove-AzureRmEventHubNamespace
```

### <span data-ttu-id="20fce-117">Exempel 3,3-ResourceId-använder sträng:</span><span class="sxs-lookup"><span data-stu-id="20fce-117">Example 3.3 - ResourceId - Using String:</span></span>
```
PS C:\> Remove-AzureRmEventHubNamespace -ResourceId "/subscriptions/xxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName"
```

## <span data-ttu-id="20fce-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="20fce-118">PARAMETERS</span></span>

### <span data-ttu-id="20fce-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="20fce-119">-AsJob</span></span>
<span data-ttu-id="20fce-120">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="20fce-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="20fce-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20fce-121">-DefaultProfile</span></span>
<span data-ttu-id="20fce-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="20fce-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20fce-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="20fce-123">-InputObject</span></span>
<span data-ttu-id="20fce-124">EventHubs</span><span class="sxs-lookup"><span data-stu-id="20fce-124">EventHubs Namespace Object</span></span>

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

### <span data-ttu-id="20fce-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="20fce-125">-Name</span></span>
<span data-ttu-id="20fce-126">Namn område för EventHub</span><span class="sxs-lookup"><span data-stu-id="20fce-126">EventHub Namespace Name</span></span>

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

### <span data-ttu-id="20fce-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="20fce-127">-PassThru</span></span>
<span data-ttu-id="20fce-128">Om du anger detta returneras sant om kommandot lyckades.</span><span class="sxs-lookup"><span data-stu-id="20fce-128">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="20fce-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20fce-129">-ResourceGroupName</span></span>
<span data-ttu-id="20fce-130">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="20fce-130">Resource Group Name</span></span>

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

### <span data-ttu-id="20fce-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="20fce-131">-ResourceId</span></span>
<span data-ttu-id="20fce-132">Resurs-ID för EventHubs</span><span class="sxs-lookup"><span data-stu-id="20fce-132">EventHubs Namespace Resource Id</span></span>

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

### <span data-ttu-id="20fce-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="20fce-133">-Confirm</span></span>
<span data-ttu-id="20fce-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="20fce-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20fce-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20fce-135">-WhatIf</span></span>
<span data-ttu-id="20fce-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="20fce-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20fce-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="20fce-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20fce-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20fce-138">CommonParameters</span></span>
<span data-ttu-id="20fce-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20fce-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20fce-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20fce-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20fce-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="20fce-141">INPUTS</span></span>

### <span data-ttu-id="20fce-142">System. String</span><span class="sxs-lookup"><span data-stu-id="20fce-142">System.String</span></span>

### <span data-ttu-id="20fce-143">Microsoft. Azure. commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="20fce-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>
<span data-ttu-id="20fce-144">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="20fce-144">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="20fce-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="20fce-145">OUTPUTS</span></span>

### <span data-ttu-id="20fce-146">System. Void</span><span class="sxs-lookup"><span data-stu-id="20fce-146">System.Void</span></span>

## <span data-ttu-id="20fce-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="20fce-147">NOTES</span></span>

## <span data-ttu-id="20fce-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="20fce-148">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Remove-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Remove-AzEventHub.md
ms.openlocfilehash: c67793371b6842e4aa8190055580b0cdfefd3e08
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922889"
---
# <span data-ttu-id="42064-101">Remove-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="42064-101">Remove-AzEventHub</span></span>

## <span data-ttu-id="42064-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="42064-102">SYNOPSIS</span></span>
<span data-ttu-id="42064-103">Tar bort den angivna händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="42064-103">Removes the specified Event Hub.</span></span>

## <span data-ttu-id="42064-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="42064-104">SYNTAX</span></span>

### <span data-ttu-id="42064-105">EventhubDefaultSet (standard)</span><span class="sxs-lookup"><span data-stu-id="42064-105">EventhubDefaultSet (Default)</span></span>
```
Remove-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42064-106">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="42064-106">EventhubInputObjectSet</span></span>
```
Remove-AzEventHub [-InputObject] <PSEventHubAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42064-107">EventhubResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="42064-107">EventhubResourceIdParameterSet</span></span>
```
Remove-AzEventHub [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42064-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="42064-108">DESCRIPTION</span></span>
<span data-ttu-id="42064-109">Remove-AzEventHub cmdlet tar bort och tar bort den angivna händelsehubben från det angivna namn området.</span><span class="sxs-lookup"><span data-stu-id="42064-109">The Remove-AzEventHub cmdlet removes and deletes the specified Event Hub from the given namespace.</span></span>

## <span data-ttu-id="42064-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="42064-110">EXAMPLES</span></span>

### <span data-ttu-id="42064-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="42064-111">Example 1</span></span>
```
PS C:\> Remove-AzEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName
```

<span data-ttu-id="42064-112">Tar bort Händelsehubben \` MyEventHubName \` .</span><span class="sxs-lookup"><span data-stu-id="42064-112">Removes the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="42064-113">Exempel 2,1 – InputObject – använder variabel:</span><span class="sxs-lookup"><span data-stu-id="42064-113">Example 2.1 - InputObject - Using Variable:</span></span>
```
PS C:\> $inputobject = Get-AzEventHub <params>
PS C:\> Remove-AzEventHub -InputObject $inputobject
```

### <span data-ttu-id="42064-114">Exempel 2,2-InputObject med rör:</span><span class="sxs-lookup"><span data-stu-id="42064-114">Example 2.2 - InputObject Using Piping:</span></span>
```
PS C:\> Get-AzEventHub <params> | Remove-AzEventHub
```

### <span data-ttu-id="42064-115">Exempel 3,1-ResourceId-använder variabel:</span><span class="sxs-lookup"><span data-stu-id="42064-115">Example 3.1 - ResourceId - Using Variable:</span></span>
```
PS C:\> $resourceid = Get-AzEventHub <params>
PS C:\> Remove-AzEventHub -ResourceId $resourceid.Id
```

### <span data-ttu-id="42064-116">Exempel 3,1-ResourceId-använder sträng:</span><span class="sxs-lookup"><span data-stu-id="42064-116">Example 3.1 - ResourceId - Using string:</span></span>
```
PS C:\> Remove-AzEventHub -ResourceId "/subscriptions/xxxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName/eventhubs/EventHubName"
```

## <span data-ttu-id="42064-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="42064-117">PARAMETERS</span></span>

### <span data-ttu-id="42064-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="42064-118">-AsJob</span></span>
<span data-ttu-id="42064-119">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="42064-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="42064-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42064-120">-DefaultProfile</span></span>
<span data-ttu-id="42064-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="42064-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42064-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="42064-122">-InputObject</span></span>
<span data-ttu-id="42064-123">Eventhub-objekt</span><span class="sxs-lookup"><span data-stu-id="42064-123">Eventhub Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes
Parameter Sets: EventhubInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="42064-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="42064-124">-Name</span></span>
<span data-ttu-id="42064-125">Namn på EventHub</span><span class="sxs-lookup"><span data-stu-id="42064-125">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubDefaultSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42064-126">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="42064-126">-Namespace</span></span>
<span data-ttu-id="42064-127">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="42064-127">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubDefaultSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42064-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="42064-128">-PassThru</span></span>
<span data-ttu-id="42064-129">Om du anger detta returneras sant om kommandot lyckades.</span><span class="sxs-lookup"><span data-stu-id="42064-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="42064-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42064-130">-ResourceGroupName</span></span>
<span data-ttu-id="42064-131">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="42064-131">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubDefaultSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42064-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="42064-132">-ResourceId</span></span>
<span data-ttu-id="42064-133">ID för Eventhub-resurs</span><span class="sxs-lookup"><span data-stu-id="42064-133">Eventhub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42064-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="42064-134">-Confirm</span></span>
<span data-ttu-id="42064-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="42064-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42064-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42064-136">-WhatIf</span></span>
<span data-ttu-id="42064-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="42064-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42064-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="42064-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42064-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42064-139">CommonParameters</span></span>
<span data-ttu-id="42064-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42064-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42064-141">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42064-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42064-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="42064-142">INPUTS</span></span>

### <span data-ttu-id="42064-143">System. String</span><span class="sxs-lookup"><span data-stu-id="42064-143">System.String</span></span>

### <span data-ttu-id="42064-144">Microsoft. Azure. commands. EventHub. Models. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="42064-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="42064-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="42064-145">OUTPUTS</span></span>

### <span data-ttu-id="42064-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="42064-146">System.Boolean</span></span>

## <span data-ttu-id="42064-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="42064-147">NOTES</span></span>

## <span data-ttu-id="42064-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="42064-148">RELATED LINKS</span></span>

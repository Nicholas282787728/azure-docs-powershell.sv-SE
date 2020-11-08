---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHub.md
ms.openlocfilehash: daa63859c9649d9467f750f77d5b0e466d03ff56
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94263186"
---
# <span data-ttu-id="aab9e-101">Remove-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="aab9e-101">Remove-AzEventHub</span></span>

## <span data-ttu-id="aab9e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="aab9e-102">SYNOPSIS</span></span>
<span data-ttu-id="aab9e-103">Tar bort den angivna händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="aab9e-103">Removes the specified Event Hub.</span></span>

## <span data-ttu-id="aab9e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="aab9e-104">SYNTAX</span></span>

### <span data-ttu-id="aab9e-105">EventhubDefaultSet (standard)</span><span class="sxs-lookup"><span data-stu-id="aab9e-105">EventhubDefaultSet (Default)</span></span>
```
Remove-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aab9e-106">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="aab9e-106">EventhubInputObjectSet</span></span>
```
Remove-AzEventHub [-InputObject] <PSEventHubAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aab9e-107">EventhubResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="aab9e-107">EventhubResourceIdParameterSet</span></span>
```
Remove-AzEventHub [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aab9e-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="aab9e-108">DESCRIPTION</span></span>
<span data-ttu-id="aab9e-109">Remove-AzEventHub cmdlet tar bort och tar bort den angivna händelsehubben från det angivna namn området.</span><span class="sxs-lookup"><span data-stu-id="aab9e-109">The Remove-AzEventHub cmdlet removes and deletes the specified Event Hub from the given namespace.</span></span>

## <span data-ttu-id="aab9e-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="aab9e-110">EXAMPLES</span></span>

### <span data-ttu-id="aab9e-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="aab9e-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName
```

<span data-ttu-id="aab9e-112">Tar bort Händelsehubben \` MyEventHubName \` .</span><span class="sxs-lookup"><span data-stu-id="aab9e-112">Removes the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="aab9e-113">Exempel 2: InputObject – använder variabel:</span><span class="sxs-lookup"><span data-stu-id="aab9e-113">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputobject = Get-AzEventHub <params>
PS C:\> Remove-AzEventHub -InputObject $inputobject
```

### <span data-ttu-id="aab9e-114">Exempel 3: InputObject med rör:</span><span class="sxs-lookup"><span data-stu-id="aab9e-114">Example 3: InputObject Using Piping:</span></span>
```powershell
PS C:\> Get-AzEventHub <params> | Remove-AzEventHub
```

### <span data-ttu-id="aab9e-115">Exempel 4: ResourceId-använder variabel:</span><span class="sxs-lookup"><span data-stu-id="aab9e-115">Example 4: ResourceId - Using Variable:</span></span>
```powershell
PS C:\> $resourceid = Get-AzEventHub <params>
PS C:\> Remove-AzEventHub -ResourceId $resourceid.Id
```

### <span data-ttu-id="aab9e-116">Exempel 5: ResourceId-använder sträng:</span><span class="sxs-lookup"><span data-stu-id="aab9e-116">Example 5: ResourceId - Using string:</span></span>
```powershell
PS C:\> Remove-AzEventHub -ResourceId "/subscriptions/xxxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName/eventhubs/EventHubName"
```

## <span data-ttu-id="aab9e-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="aab9e-117">PARAMETERS</span></span>

### <span data-ttu-id="aab9e-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aab9e-118">-AsJob</span></span>
<span data-ttu-id="aab9e-119">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="aab9e-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="aab9e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aab9e-120">-DefaultProfile</span></span>
<span data-ttu-id="aab9e-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="aab9e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aab9e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aab9e-122">-InputObject</span></span>
<span data-ttu-id="aab9e-123">Eventhub-objekt</span><span class="sxs-lookup"><span data-stu-id="aab9e-123">Eventhub Object</span></span>

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

### <span data-ttu-id="aab9e-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="aab9e-124">-Name</span></span>
<span data-ttu-id="aab9e-125">Namn på EventHub</span><span class="sxs-lookup"><span data-stu-id="aab9e-125">EventHub Name</span></span>

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

### <span data-ttu-id="aab9e-126">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="aab9e-126">-Namespace</span></span>
<span data-ttu-id="aab9e-127">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="aab9e-127">Namespace Name</span></span>

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

### <span data-ttu-id="aab9e-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aab9e-128">-PassThru</span></span>
<span data-ttu-id="aab9e-129">Om du anger detta returneras sant om kommandot lyckades.</span><span class="sxs-lookup"><span data-stu-id="aab9e-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="aab9e-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aab9e-130">-ResourceGroupName</span></span>
<span data-ttu-id="aab9e-131">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="aab9e-131">Resource Group Name</span></span>

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

### <span data-ttu-id="aab9e-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aab9e-132">-ResourceId</span></span>
<span data-ttu-id="aab9e-133">ID för Eventhub-resurs</span><span class="sxs-lookup"><span data-stu-id="aab9e-133">Eventhub Resource Id</span></span>

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

### <span data-ttu-id="aab9e-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="aab9e-134">-Confirm</span></span>
<span data-ttu-id="aab9e-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="aab9e-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aab9e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aab9e-136">-WhatIf</span></span>
<span data-ttu-id="aab9e-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="aab9e-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aab9e-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="aab9e-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aab9e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aab9e-139">CommonParameters</span></span>
<span data-ttu-id="aab9e-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aab9e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aab9e-141">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aab9e-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aab9e-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="aab9e-142">INPUTS</span></span>

### <span data-ttu-id="aab9e-143">System. String</span><span class="sxs-lookup"><span data-stu-id="aab9e-143">System.String</span></span>

### <span data-ttu-id="aab9e-144">Microsoft. Azure. commands. EventHub. Models. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="aab9e-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="aab9e-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="aab9e-145">OUTPUTS</span></span>

### <span data-ttu-id="aab9e-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="aab9e-146">System.Boolean</span></span>

## <span data-ttu-id="aab9e-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="aab9e-147">NOTES</span></span>

## <span data-ttu-id="aab9e-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="aab9e-148">RELATED LINKS</span></span>

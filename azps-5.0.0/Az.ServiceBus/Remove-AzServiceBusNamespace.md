---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNamespace.md
ms.openlocfilehash: 49b6a29410bd6c670e74b072a48b6f2a79e8fd0f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319840"
---
# <span data-ttu-id="809b1-101">Remove-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="809b1-101">Remove-AzServiceBusNamespace</span></span>

## <span data-ttu-id="809b1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="809b1-102">SYNOPSIS</span></span>
<span data-ttu-id="809b1-103">Tar bort namn området från den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="809b1-103">Removes the namespace from the specified resource group.</span></span> 

## <span data-ttu-id="809b1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="809b1-104">SYNTAX</span></span>

### <span data-ttu-id="809b1-105">NamespacePropertiesSet (standard)</span><span class="sxs-lookup"><span data-stu-id="809b1-105">NamespacePropertiesSet (Default)</span></span>
```
Remove-AzServiceBusNamespace [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="809b1-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="809b1-106">NamespaceInputObjectSet</span></span>
```
Remove-AzServiceBusNamespace [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="809b1-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="809b1-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzServiceBusNamespace [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="809b1-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="809b1-108">DESCRIPTION</span></span>
<span data-ttu-id="809b1-109">Cmdleten **Remove-AzServiceBusNamespace** tar bort namn området från den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="809b1-109">The **Remove-AzServiceBusNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="809b1-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="809b1-110">EXAMPLES</span></span>

### <span data-ttu-id="809b1-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="809b1-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="809b1-112">Tar bort Service Bus-namnområdet `SB-Example1` från den angivna resurs gruppen `Default-ServiceBus-WestUS` .</span><span class="sxs-lookup"><span data-stu-id="809b1-112">Removes the Service Bus namespace `SB-Example1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

### <span data-ttu-id="809b1-113">Exempel 2,1 – InputObject – använder variabel:</span><span class="sxs-lookup"><span data-stu-id="809b1-113">Example 2.1 - InputObject - Using variable:</span></span>
```
PS C:\> $inputobject = Get-AzServiceBusNamespace <params>
PS C:\> Remove-AzServiceBusNamespace -InputObject $inputobject
```

<span data-ttu-id="809b1-114">Tar bort Service Bus-namnområdet som tillhandahålls via $inputobject.</span><span class="sxs-lookup"><span data-stu-id="809b1-114">Removes the Service Bus namespace provided through the $inputobject.</span></span>

### <span data-ttu-id="809b1-115">Exempel 2,2 – InputObject-med rör dragning:</span><span class="sxs-lookup"><span data-stu-id="809b1-115">Example 2.2 - InputObject - Using Piping:</span></span>
```
PS C:\> Get-AzServiceBusNamespace <params> | Remove-AzServiceBusNamespace
```

<span data-ttu-id="809b1-116">Tar bort Service Bus-namnområdet med rör.</span><span class="sxs-lookup"><span data-stu-id="809b1-116">Removes the Service Bus namespace using Piping.</span></span>

### <span data-ttu-id="809b1-117">Exempel 3 – ResourceId</span><span class="sxs-lookup"><span data-stu-id="809b1-117">Example 3 - ResourceId</span></span>
```
PS c:\> $ResourceId = (Get-AzResource -ResourceType Microsoft.ServiceBus/namespaces).ResourceId
PS C:\> Remove-AzServiceBusNamespace -ResourceId $resourceid
```

<span data-ttu-id="809b1-118">Tar bort namn området för Service Bus som tillhandahålls med ARM-ID i $resourceid för parametern-ResourceId eller genom rör.</span><span class="sxs-lookup"><span data-stu-id="809b1-118">Removes the Service Bus namespace provided through ARM id in $resourceid for -ResourceId parameter or through piping.</span></span>

## <span data-ttu-id="809b1-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="809b1-119">PARAMETERS</span></span>

### <span data-ttu-id="809b1-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="809b1-120">-AsJob</span></span>
<span data-ttu-id="809b1-121">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="809b1-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="809b1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="809b1-122">-DefaultProfile</span></span>
<span data-ttu-id="809b1-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="809b1-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="809b1-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="809b1-124">-InputObject</span></span>
<span data-ttu-id="809b1-125">Service Bus namespace-objekt</span><span class="sxs-lookup"><span data-stu-id="809b1-125">Service Bus Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="809b1-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="809b1-126">-Name</span></span>
<span data-ttu-id="809b1-127">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="809b1-127">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NamespacePropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="809b1-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="809b1-128">-PassThru</span></span>
<span data-ttu-id="809b1-129">Om du anger detta returneras sant om kommandot lyckades.</span><span class="sxs-lookup"><span data-stu-id="809b1-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="809b1-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="809b1-130">-ResourceGroupName</span></span>
<span data-ttu-id="809b1-131">Namnet på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="809b1-131">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: NamespacePropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="809b1-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="809b1-132">-ResourceId</span></span>
<span data-ttu-id="809b1-133">Resurs-ID för Service Bus-namnrymd</span><span class="sxs-lookup"><span data-stu-id="809b1-133">Service Bus Namespace Resource Id</span></span>

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

### <span data-ttu-id="809b1-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="809b1-134">-Confirm</span></span>
<span data-ttu-id="809b1-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="809b1-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="809b1-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="809b1-136">-WhatIf</span></span>
<span data-ttu-id="809b1-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="809b1-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="809b1-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="809b1-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="809b1-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="809b1-139">CommonParameters</span></span>
<span data-ttu-id="809b1-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="809b1-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="809b1-141">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="809b1-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="809b1-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="809b1-142">INPUTS</span></span>

### <span data-ttu-id="809b1-143">System. String</span><span class="sxs-lookup"><span data-stu-id="809b1-143">System.String</span></span>

### <span data-ttu-id="809b1-144">Microsoft. Azure. commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="809b1-144">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="809b1-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="809b1-145">OUTPUTS</span></span>

### <span data-ttu-id="809b1-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="809b1-146">System.Boolean</span></span>

## <span data-ttu-id="809b1-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="809b1-147">NOTES</span></span>

## <span data-ttu-id="809b1-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="809b1-148">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusIPRule.md
ms.openlocfilehash: 90c832d36017aa02a05d972a7b6e26fffd93937e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089023"
---
# <span data-ttu-id="0156d-101">Remove-AzServiceBusIPRule</span><span class="sxs-lookup"><span data-stu-id="0156d-101">Remove-AzServiceBusIPRule</span></span>

## <span data-ttu-id="0156d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0156d-102">SYNOPSIS</span></span>
<span data-ttu-id="0156d-103">Ta bort en enskild IP-regel till NetworkRuleSet för det angivna namn området</span><span class="sxs-lookup"><span data-stu-id="0156d-103">Remove a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="0156d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0156d-104">SYNTAX</span></span>

### <span data-ttu-id="0156d-105">IPRulePropertiesParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="0156d-105">IPRulePropertiesParameterSet (Default)</span></span>
```
Remove-AzServiceBusIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0156d-106">IPRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0156d-106">IPRuleInputObjectParameterSet</span></span>
```
Remove-AzServiceBusIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0156d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0156d-107">DESCRIPTION</span></span>
<span data-ttu-id="0156d-108">Ta bort en enskild IP-regel till NetworkRuleSet för det angivna namn området</span><span class="sxs-lookup"><span data-stu-id="0156d-108">Remove a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="0156d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0156d-109">EXAMPLES</span></span>

### <span data-ttu-id="0156d-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0156d-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusIPRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -IpMask "11.22.33.44"
```

<span data-ttu-id="0156d-111">Tar bort IpMask för NetworkRuleSet för det givna namn området</span><span class="sxs-lookup"><span data-stu-id="0156d-111">Removes IpMask of the NetworkRuleSet of the given namespace</span></span>

## <span data-ttu-id="0156d-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0156d-112">PARAMETERS</span></span>

### <span data-ttu-id="0156d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0156d-113">-AsJob</span></span>
<span data-ttu-id="0156d-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="0156d-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0156d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0156d-115">-DefaultProfile</span></span>
<span data-ttu-id="0156d-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0156d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0156d-117">-IpMask</span><span class="sxs-lookup"><span data-stu-id="0156d-117">-IpMask</span></span>
<span data-ttu-id="0156d-118">ID för under nätet</span><span class="sxs-lookup"><span data-stu-id="0156d-118">Subnet Resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: IPRulePropertiesParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0156d-119">-IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="0156d-119">-IpRuleObject</span></span>
<span data-ttu-id="0156d-120">IPRule-konfigurations objekt</span><span class="sxs-lookup"><span data-stu-id="0156d-120">IPRule Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes
Parameter Sets: IPRuleInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0156d-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="0156d-121">-Name</span></span>
<span data-ttu-id="0156d-122">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="0156d-122">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0156d-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0156d-123">-PassThru</span></span>
<span data-ttu-id="0156d-124">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="0156d-124">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="0156d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0156d-125">-ResourceGroupName</span></span>
<span data-ttu-id="0156d-126">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="0156d-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0156d-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0156d-127">-Confirm</span></span>
<span data-ttu-id="0156d-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0156d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0156d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0156d-129">-WhatIf</span></span>
<span data-ttu-id="0156d-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0156d-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0156d-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0156d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0156d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0156d-132">CommonParameters</span></span>
<span data-ttu-id="0156d-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0156d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="0156d-134">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0156d-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0156d-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0156d-135">INPUTS</span></span>

### <span data-ttu-id="0156d-136">System. String</span><span class="sxs-lookup"><span data-stu-id="0156d-136">System.String</span></span>

### <span data-ttu-id="0156d-137">Microsoft. Azure. commands. ServiceBus. Models. PSNWRuleSetIpRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="0156d-137">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes</span></span>

## <span data-ttu-id="0156d-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0156d-138">OUTPUTS</span></span>

### <span data-ttu-id="0156d-139">Microsoft. Azure. commands. ServiceBus. Models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="0156d-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="0156d-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0156d-140">NOTES</span></span>

## <span data-ttu-id="0156d-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0156d-141">RELATED LINKS</span></span>

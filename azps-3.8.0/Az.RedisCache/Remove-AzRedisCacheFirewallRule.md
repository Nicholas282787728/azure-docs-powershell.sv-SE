---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheFirewallRule.md
ms.openlocfilehash: c19be1f524519a55a5a95a575e97cfd250952570
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93927509"
---
# <span data-ttu-id="e4722-101">Remove-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e4722-101">Remove-AzRedisCacheFirewallRule</span></span>

## <span data-ttu-id="e4722-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e4722-102">SYNOPSIS</span></span>
<span data-ttu-id="e4722-103">Ta bort en brand Väggs regel från en Redis cache.</span><span class="sxs-lookup"><span data-stu-id="e4722-103">Remove a firewall rule from a Redis Cache.</span></span>

## <span data-ttu-id="e4722-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e4722-104">SYNTAX</span></span>

### <span data-ttu-id="e4722-105">NormalParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="e4722-105">NormalParameterSet (Default)</span></span>
```
Remove-AzRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> -RuleName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4722-106">PSRedisFirewallRuleObject</span><span class="sxs-lookup"><span data-stu-id="e4722-106">PSRedisFirewallRuleObject</span></span>
```
Remove-AzRedisCacheFirewallRule -InputObject <PSRedisFirewallRule> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4722-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e4722-107">DESCRIPTION</span></span>
<span data-ttu-id="e4722-108">Ta bort en brand Väggs regel från en Redis cache.</span><span class="sxs-lookup"><span data-stu-id="e4722-108">Remove a firewall rule from a Redis Cache.</span></span>

## <span data-ttu-id="e4722-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e4722-109">EXAMPLES</span></span>

### <span data-ttu-id="e4722-110">Exempel 1: ta bort en enskild brand Väggs regel</span><span class="sxs-lookup"><span data-stu-id="e4722-110">Example 1: Remove a single firewall rule</span></span>
```
PS C:\>Remove-AzRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone" -PassThru
True
```

<span data-ttu-id="e4722-111">Det här kommandot tar bort en brand Väggs regel med namnet ruleone från Redis cacheminne.</span><span class="sxs-lookup"><span data-stu-id="e4722-111">This command removes a firewall rule named ruleone from Redis Cache named mycache.</span></span> 

## <span data-ttu-id="e4722-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e4722-112">PARAMETERS</span></span>

### <span data-ttu-id="e4722-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4722-113">-DefaultProfile</span></span>
<span data-ttu-id="e4722-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e4722-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4722-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e4722-115">-InputObject</span></span>
<span data-ttu-id="e4722-116">objekt av typen PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e4722-116">object of type PSRedisFirewallRule</span></span>

```yaml
Type: Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule
Parameter Sets: PSRedisFirewallRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4722-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="e4722-117">-Name</span></span>
<span data-ttu-id="e4722-118">Namn på Redis cache.</span><span class="sxs-lookup"><span data-stu-id="e4722-118">Name of redis cache.</span></span>

```yaml
Type: System.String
Parameter Sets: NormalParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4722-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e4722-119">-PassThru</span></span>
<span data-ttu-id="e4722-120">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="e4722-120">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="e4722-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4722-121">-ResourceGroupName</span></span>
<span data-ttu-id="e4722-122">Namn på resurs gruppen där cacheminnet finns.</span><span class="sxs-lookup"><span data-stu-id="e4722-122">Name of resource group in which cache exists.</span></span>

```yaml
Type: System.String
Parameter Sets: NormalParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4722-123">-RuleName</span><span class="sxs-lookup"><span data-stu-id="e4722-123">-RuleName</span></span>
<span data-ttu-id="e4722-124">Namn på brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="e4722-124">Name of firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: NormalParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4722-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e4722-125">-Confirm</span></span>
<span data-ttu-id="e4722-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e4722-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4722-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4722-127">-WhatIf</span></span>
<span data-ttu-id="e4722-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e4722-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4722-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e4722-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4722-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4722-130">CommonParameters</span></span>
<span data-ttu-id="e4722-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4722-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4722-132">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4722-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4722-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e4722-133">INPUTS</span></span>

### <span data-ttu-id="e4722-134">System. String</span><span class="sxs-lookup"><span data-stu-id="e4722-134">System.String</span></span>

### <span data-ttu-id="e4722-135">Microsoft. Azure. commands. RedisCache. Models. PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e4722-135">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="e4722-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e4722-136">OUTPUTS</span></span>

### <span data-ttu-id="e4722-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e4722-137">System.Boolean</span></span>

## <span data-ttu-id="e4722-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e4722-138">NOTES</span></span>

## <span data-ttu-id="e4722-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e4722-139">RELATED LINKS</span></span>

[<span data-ttu-id="e4722-140">New-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e4722-140">New-AzRedisCacheFirewallRule</span></span>](./New-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="e4722-141">Get-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e4722-141">Get-AzRedisCacheFirewallRule</span></span>](./Get-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="e4722-142">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="e4722-142">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="e4722-143">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="e4722-143">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="e4722-144">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="e4722-144">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="e4722-145">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="e4722-145">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)
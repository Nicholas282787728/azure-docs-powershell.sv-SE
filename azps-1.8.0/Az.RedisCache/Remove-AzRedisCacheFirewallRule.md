---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheFirewallRule.md
ms.openlocfilehash: e24ea6e0b5bf88b17a6209f2ea69634200a10a62
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747257"
---
# <span data-ttu-id="f5262-101">Remove-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f5262-101">Remove-AzRedisCacheFirewallRule</span></span>

## <span data-ttu-id="f5262-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f5262-102">SYNOPSIS</span></span>
<span data-ttu-id="f5262-103">Ta bort en brand Väggs regel från en Redis cache.</span><span class="sxs-lookup"><span data-stu-id="f5262-103">Remove a firewall rule from a Redis Cache.</span></span>

## <span data-ttu-id="f5262-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f5262-104">SYNTAX</span></span>

### <span data-ttu-id="f5262-105">NormalParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="f5262-105">NormalParameterSet (Default)</span></span>
```
Remove-AzRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> -RuleName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5262-106">PSRedisFirewallRuleObject</span><span class="sxs-lookup"><span data-stu-id="f5262-106">PSRedisFirewallRuleObject</span></span>
```
Remove-AzRedisCacheFirewallRule -InputObject <PSRedisFirewallRule> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5262-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f5262-107">DESCRIPTION</span></span>
<span data-ttu-id="f5262-108">Ta bort en brand Väggs regel från en Redis cache.</span><span class="sxs-lookup"><span data-stu-id="f5262-108">Remove a firewall rule from a Redis Cache.</span></span>

## <span data-ttu-id="f5262-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f5262-109">EXAMPLES</span></span>

### <span data-ttu-id="f5262-110">Exempel 1: ta bort en enskild brand Väggs regel</span><span class="sxs-lookup"><span data-stu-id="f5262-110">Example 1: Remove a single firewall rule</span></span>
```
PS C:\>Remove-AzRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone" -PassThru
True
```

<span data-ttu-id="f5262-111">Det här kommandot tar bort en brand Väggs regel med namnet ruleone från Redis cacheminne.</span><span class="sxs-lookup"><span data-stu-id="f5262-111">This command removes a firewall rule named ruleone from Redis Cache named mycache.</span></span> 

## <span data-ttu-id="f5262-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f5262-112">PARAMETERS</span></span>

### <span data-ttu-id="f5262-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5262-113">-DefaultProfile</span></span>
<span data-ttu-id="f5262-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f5262-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5262-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f5262-115">-InputObject</span></span>
<span data-ttu-id="f5262-116">objekt av typen PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f5262-116">object of type PSRedisFirewallRule</span></span>

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

### <span data-ttu-id="f5262-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="f5262-117">-Name</span></span>
<span data-ttu-id="f5262-118">Namn på Redis cache.</span><span class="sxs-lookup"><span data-stu-id="f5262-118">Name of redis cache.</span></span>

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

### <span data-ttu-id="f5262-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f5262-119">-PassThru</span></span>
<span data-ttu-id="f5262-120">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="f5262-120">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="f5262-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5262-121">-ResourceGroupName</span></span>
<span data-ttu-id="f5262-122">Namn på resurs gruppen där cacheminnet finns.</span><span class="sxs-lookup"><span data-stu-id="f5262-122">Name of resource group in which cache exists.</span></span>

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

### <span data-ttu-id="f5262-123">-RuleName</span><span class="sxs-lookup"><span data-stu-id="f5262-123">-RuleName</span></span>
<span data-ttu-id="f5262-124">Namn på brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="f5262-124">Name of firewall rule.</span></span>

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

### <span data-ttu-id="f5262-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f5262-125">-Confirm</span></span>
<span data-ttu-id="f5262-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f5262-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5262-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5262-127">-WhatIf</span></span>
<span data-ttu-id="f5262-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f5262-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5262-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f5262-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5262-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5262-130">CommonParameters</span></span>
<span data-ttu-id="f5262-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5262-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5262-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5262-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5262-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f5262-133">INPUTS</span></span>

### <span data-ttu-id="f5262-134">System. String</span><span class="sxs-lookup"><span data-stu-id="f5262-134">System.String</span></span>

### <span data-ttu-id="f5262-135">Microsoft. Azure. commands. RedisCache. Models. PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f5262-135">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="f5262-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f5262-136">OUTPUTS</span></span>

### <span data-ttu-id="f5262-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f5262-137">System.Boolean</span></span>

## <span data-ttu-id="f5262-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f5262-138">NOTES</span></span>

## <span data-ttu-id="f5262-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f5262-139">RELATED LINKS</span></span>

[<span data-ttu-id="f5262-140">New-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f5262-140">New-AzRedisCacheFirewallRule</span></span>](./New-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="f5262-141">Get-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f5262-141">Get-AzRedisCacheFirewallRule</span></span>](./Get-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="f5262-142">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="f5262-142">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="f5262-143">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="f5262-143">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="f5262-144">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="f5262-144">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="f5262-145">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="f5262-145">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)
---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheFirewallRule.md
ms.openlocfilehash: dc52668a7d0f17d9cdbf9221a174228be1fa0f5f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920155"
---
# <span data-ttu-id="fdb2b-101">New-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="fdb2b-101">New-AzRedisCacheFirewallRule</span></span>

## <span data-ttu-id="fdb2b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fdb2b-102">SYNOPSIS</span></span>
<span data-ttu-id="fdb2b-103">Skapa en brand Väggs regel i en Redis cache.</span><span class="sxs-lookup"><span data-stu-id="fdb2b-103">Create a firewall rule on a Redis Cache.</span></span>

## <span data-ttu-id="fdb2b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fdb2b-104">SYNTAX</span></span>

### <span data-ttu-id="fdb2b-105">NormalParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="fdb2b-105">NormalParameterSet (Default)</span></span>
```
New-AzRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> -RuleName <String> -StartIP <String>
 -EndIP <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdb2b-106">RedisCacheAttributesObject</span><span class="sxs-lookup"><span data-stu-id="fdb2b-106">RedisCacheAttributesObject</span></span>
```
New-AzRedisCacheFirewallRule -InputObject <RedisCacheAttributes> -RuleName <String> -StartIP <String>
 -EndIP <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdb2b-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fdb2b-107">ResourceIdParameterSet</span></span>
```
New-AzRedisCacheFirewallRule -ResourceId <String> -RuleName <String> -StartIP <String> -EndIP <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fdb2b-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fdb2b-108">DESCRIPTION</span></span>
<span data-ttu-id="fdb2b-109">Skapa en brand Väggs regel i en Redis cache.</span><span class="sxs-lookup"><span data-stu-id="fdb2b-109">Create a firewall rule on a Redis Cache.</span></span>

## <span data-ttu-id="fdb2b-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fdb2b-110">EXAMPLES</span></span>

### <span data-ttu-id="fdb2b-111">Exempel 1: skapa en brand Väggs regel</span><span class="sxs-lookup"><span data-stu-id="fdb2b-111">Example 1: Create a firewall rule</span></span>
```
PS C:\>New-AzRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone" -StartIP "10.0.0.1" -EndIP "10.0.0.32"

        ResourceGroupName : myGroup
        Name              : mycache
        FirewallRuleId    : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/mycache/firewallRules/ruleone
        RuleName          : ruleone
        Type              : Microsoft.Cache/Redis/firewallRules
        StartIP           : 10.0.0.1
        EndIP             : 10.0.0.32
```

<span data-ttu-id="fdb2b-112">Det här kommandot skapar en brand Väggs regel med namnet ruleone i Redis cache med namnet noncache.</span><span class="sxs-lookup"><span data-stu-id="fdb2b-112">This command creates firewall rule named ruleone on Redis Cache named mycache.</span></span>

## <span data-ttu-id="fdb2b-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fdb2b-113">PARAMETERS</span></span>

### <span data-ttu-id="fdb2b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdb2b-114">-DefaultProfile</span></span>
<span data-ttu-id="fdb2b-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fdb2b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fdb2b-116">-EndIP</span><span class="sxs-lookup"><span data-stu-id="fdb2b-116">-EndIP</span></span>
<span data-ttu-id="fdb2b-117">Sista IP-adress.</span><span class="sxs-lookup"><span data-stu-id="fdb2b-117">Ending IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdb2b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fdb2b-118">-InputObject</span></span>
<span data-ttu-id="fdb2b-119">objekt av typen RedisCacheAttributes</span><span class="sxs-lookup"><span data-stu-id="fdb2b-119">object of type RedisCacheAttributes</span></span>

```yaml
Type: Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes
Parameter Sets: RedisCacheAttributesObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fdb2b-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="fdb2b-120">-Name</span></span>
<span data-ttu-id="fdb2b-121">Namn på Redis cache.</span><span class="sxs-lookup"><span data-stu-id="fdb2b-121">Name of redis cache.</span></span>

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

### <span data-ttu-id="fdb2b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdb2b-122">-ResourceGroupName</span></span>
<span data-ttu-id="fdb2b-123">Namn på resurs gruppen där cacheminnet finns.</span><span class="sxs-lookup"><span data-stu-id="fdb2b-123">Name of resource group in which cache exists.</span></span>

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

### <span data-ttu-id="fdb2b-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fdb2b-124">-ResourceId</span></span>
<span data-ttu-id="fdb2b-125">ARM-ID för Redis cache.</span><span class="sxs-lookup"><span data-stu-id="fdb2b-125">ARM Id of Redis Cache.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdb2b-126">-RuleName</span><span class="sxs-lookup"><span data-stu-id="fdb2b-126">-RuleName</span></span>
<span data-ttu-id="fdb2b-127">Namn på brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="fdb2b-127">Name of firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdb2b-128">-StartIP</span><span class="sxs-lookup"><span data-stu-id="fdb2b-128">-StartIP</span></span>
<span data-ttu-id="fdb2b-129">Inledande IP-adress.</span><span class="sxs-lookup"><span data-stu-id="fdb2b-129">Starting IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdb2b-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fdb2b-130">-Confirm</span></span>
<span data-ttu-id="fdb2b-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fdb2b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fdb2b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fdb2b-132">-WhatIf</span></span>
<span data-ttu-id="fdb2b-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fdb2b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fdb2b-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fdb2b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fdb2b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdb2b-135">CommonParameters</span></span>
<span data-ttu-id="fdb2b-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdb2b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdb2b-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdb2b-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdb2b-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fdb2b-138">INPUTS</span></span>

### <span data-ttu-id="fdb2b-139">System. String</span><span class="sxs-lookup"><span data-stu-id="fdb2b-139">System.String</span></span>

### <span data-ttu-id="fdb2b-140">Microsoft. Azure. commands. RedisCache. Models. RedisCacheAttributes</span><span class="sxs-lookup"><span data-stu-id="fdb2b-140">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span></span>

## <span data-ttu-id="fdb2b-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fdb2b-141">OUTPUTS</span></span>

### <span data-ttu-id="fdb2b-142">Microsoft. Azure. commands. RedisCache. Models. PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="fdb2b-142">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="fdb2b-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fdb2b-143">NOTES</span></span>

## <span data-ttu-id="fdb2b-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fdb2b-144">RELATED LINKS</span></span>

[<span data-ttu-id="fdb2b-145">Get-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="fdb2b-145">Get-AzRedisCacheFirewallRule</span></span>](./Get-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="fdb2b-146">Remove-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="fdb2b-146">Remove-AzRedisCacheFirewallRule</span></span>](./Remove-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="fdb2b-147">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="fdb2b-147">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="fdb2b-148">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="fdb2b-148">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="fdb2b-149">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="fdb2b-149">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="fdb2b-150">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="fdb2b-150">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)
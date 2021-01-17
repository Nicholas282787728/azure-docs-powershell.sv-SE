---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheFirewallRule.md
ms.openlocfilehash: 50a2df73d6cfa1e9d34f2c5c4b426f601c9d9309
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98395427"
---
# <span data-ttu-id="5afaf-101">New-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5afaf-101">New-AzRedisCacheFirewallRule</span></span>

## <span data-ttu-id="5afaf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5afaf-102">SYNOPSIS</span></span>
<span data-ttu-id="5afaf-103">Skapa en brand Väggs regel i en Redis cache.</span><span class="sxs-lookup"><span data-stu-id="5afaf-103">Create a firewall rule on a Redis Cache.</span></span>

## <span data-ttu-id="5afaf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5afaf-104">SYNTAX</span></span>

### <span data-ttu-id="5afaf-105">NormalParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="5afaf-105">NormalParameterSet (Default)</span></span>
```
New-AzRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> -RuleName <String> -StartIP <String>
 -EndIP <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5afaf-106">RedisCacheAttributesObject</span><span class="sxs-lookup"><span data-stu-id="5afaf-106">RedisCacheAttributesObject</span></span>
```
New-AzRedisCacheFirewallRule -InputObject <RedisCacheAttributes> -RuleName <String> -StartIP <String>
 -EndIP <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5afaf-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5afaf-107">ResourceIdParameterSet</span></span>
```
New-AzRedisCacheFirewallRule -ResourceId <String> -RuleName <String> -StartIP <String> -EndIP <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5afaf-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5afaf-108">DESCRIPTION</span></span>
<span data-ttu-id="5afaf-109">Skapa en brand Väggs regel i en Redis cache.</span><span class="sxs-lookup"><span data-stu-id="5afaf-109">Create a firewall rule on a Redis Cache.</span></span>

## <span data-ttu-id="5afaf-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5afaf-110">EXAMPLES</span></span>

### <span data-ttu-id="5afaf-111">Exempel 1: skapa en brand Väggs regel</span><span class="sxs-lookup"><span data-stu-id="5afaf-111">Example 1: Create a firewall rule</span></span>
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

<span data-ttu-id="5afaf-112">Det här kommandot skapar en brand Väggs regel med namnet ruleone i Redis cache med namnet noncache.</span><span class="sxs-lookup"><span data-stu-id="5afaf-112">This command creates firewall rule named ruleone on Redis Cache named mycache.</span></span>

## <span data-ttu-id="5afaf-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5afaf-113">PARAMETERS</span></span>

### <span data-ttu-id="5afaf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5afaf-114">-DefaultProfile</span></span>
<span data-ttu-id="5afaf-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5afaf-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5afaf-116">-EndIP</span><span class="sxs-lookup"><span data-stu-id="5afaf-116">-EndIP</span></span>
<span data-ttu-id="5afaf-117">Sista IP-adress.</span><span class="sxs-lookup"><span data-stu-id="5afaf-117">Ending IP address.</span></span>

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

### <span data-ttu-id="5afaf-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5afaf-118">-InputObject</span></span>
<span data-ttu-id="5afaf-119">objekt av typen RedisCacheAttributes</span><span class="sxs-lookup"><span data-stu-id="5afaf-119">object of type RedisCacheAttributes</span></span>

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

### <span data-ttu-id="5afaf-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="5afaf-120">-Name</span></span>
<span data-ttu-id="5afaf-121">Namn på Redis cache.</span><span class="sxs-lookup"><span data-stu-id="5afaf-121">Name of redis cache.</span></span>

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

### <span data-ttu-id="5afaf-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5afaf-122">-ResourceGroupName</span></span>
<span data-ttu-id="5afaf-123">Namn på resurs gruppen där cacheminnet finns.</span><span class="sxs-lookup"><span data-stu-id="5afaf-123">Name of resource group in which cache exists.</span></span>

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

### <span data-ttu-id="5afaf-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5afaf-124">-ResourceId</span></span>
<span data-ttu-id="5afaf-125">ARM-ID för Redis cache.</span><span class="sxs-lookup"><span data-stu-id="5afaf-125">ARM Id of Redis Cache.</span></span>

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

### <span data-ttu-id="5afaf-126">-RuleName</span><span class="sxs-lookup"><span data-stu-id="5afaf-126">-RuleName</span></span>
<span data-ttu-id="5afaf-127">Namn på brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="5afaf-127">Name of firewall rule.</span></span>

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

### <span data-ttu-id="5afaf-128">-StartIP</span><span class="sxs-lookup"><span data-stu-id="5afaf-128">-StartIP</span></span>
<span data-ttu-id="5afaf-129">Inledande IP-adress.</span><span class="sxs-lookup"><span data-stu-id="5afaf-129">Starting IP address.</span></span>

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

### <span data-ttu-id="5afaf-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5afaf-130">-Confirm</span></span>
<span data-ttu-id="5afaf-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5afaf-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5afaf-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5afaf-132">-WhatIf</span></span>
<span data-ttu-id="5afaf-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5afaf-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5afaf-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5afaf-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5afaf-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5afaf-135">CommonParameters</span></span>
<span data-ttu-id="5afaf-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5afaf-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5afaf-137">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5afaf-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5afaf-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5afaf-138">INPUTS</span></span>

### <span data-ttu-id="5afaf-139">System. String</span><span class="sxs-lookup"><span data-stu-id="5afaf-139">System.String</span></span>

### <span data-ttu-id="5afaf-140">Microsoft. Azure. commands. RedisCache. Models. RedisCacheAttributes</span><span class="sxs-lookup"><span data-stu-id="5afaf-140">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span></span>

## <span data-ttu-id="5afaf-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5afaf-141">OUTPUTS</span></span>

### <span data-ttu-id="5afaf-142">Microsoft. Azure. commands. RedisCache. Models. PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5afaf-142">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="5afaf-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5afaf-143">NOTES</span></span>

## <span data-ttu-id="5afaf-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5afaf-144">RELATED LINKS</span></span>

[<span data-ttu-id="5afaf-145">Get-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5afaf-145">Get-AzRedisCacheFirewallRule</span></span>](./Get-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="5afaf-146">Remove-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5afaf-146">Remove-AzRedisCacheFirewallRule</span></span>](./Remove-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="5afaf-147">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="5afaf-147">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="5afaf-148">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="5afaf-148">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="5afaf-149">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="5afaf-149">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="5afaf-150">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="5afaf-150">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)
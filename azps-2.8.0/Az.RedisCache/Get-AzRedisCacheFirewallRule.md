---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheFirewallRule.md
ms.openlocfilehash: 1bf6394621435293be1d00d4a9e9f435c160e668
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919681"
---
# <span data-ttu-id="1c88a-101">Get-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="1c88a-101">Get-AzRedisCacheFirewallRule</span></span>

## <span data-ttu-id="1c88a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1c88a-102">SYNOPSIS</span></span>
<span data-ttu-id="1c88a-103">Skaffa brand Väggs regler som är inställda på Redis cache.</span><span class="sxs-lookup"><span data-stu-id="1c88a-103">Get firewall rules set on Redis Cache.</span></span>

## <span data-ttu-id="1c88a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1c88a-104">SYNTAX</span></span>

```
Get-AzRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> [-RuleName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c88a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1c88a-105">DESCRIPTION</span></span>
<span data-ttu-id="1c88a-106">Om **RuleName** parameter anges får cmdleten **Get-AzRedisCacheFirewallRule** information om den angivna brand Väggs regeln i Azure Redis-cachen.</span><span class="sxs-lookup"><span data-stu-id="1c88a-106">If **RuleName** parameter if provided, **Get-AzRedisCacheFirewallRule** cmdlet gets detail about the specified firewall rule on Azure Redis Cache.</span></span> <span data-ttu-id="1c88a-107">Om det bara finns **ett namn** hämtas alla brand Väggs regler som är tillgängliga för det Redis cacheminnet.</span><span class="sxs-lookup"><span data-stu-id="1c88a-107">If only **Name** is specified this operation gets all firewall rules available on that Redis Cache.</span></span>

## <span data-ttu-id="1c88a-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1c88a-108">EXAMPLES</span></span>

### <span data-ttu-id="1c88a-109">Exempel 1: skaffa en enda brand Väggs regel</span><span class="sxs-lookup"><span data-stu-id="1c88a-109">Example 1: Get a single firewall rule</span></span>
```
PS C:\>Get-AzRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone"

        ResourceGroupName : myGroup
        Name              : mycache
        FirewallRuleId    : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/mycache/firewallRules/ruleone
        RuleName          : ruleone
        Type              : Microsoft.Cache/Redis/firewallRules
        StartIP           : 10.0.0.1
        EndIP             : 10.0.0.32
```

<span data-ttu-id="1c88a-110">Det här kommandot får brand Väggs regeln som heter ruleone från Redis cacheminne.</span><span class="sxs-lookup"><span data-stu-id="1c88a-110">This command gets firewall rule named ruleone from Redis Cache named mycache.</span></span>

### <span data-ttu-id="1c88a-111">Exempel 2: Hämta alla brand Väggs regler</span><span class="sxs-lookup"><span data-stu-id="1c88a-111">Example 2: Get all firewall rules</span></span>
```
PS C:\>Get-AzRedisCacheFirewallRule -Name "mycache"

        ResourceGroupName : myGroup
        Name              : mycache
        FirewallRuleId    : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/mycache/firewallRules/ruleone
        RuleName          : ruleone
        Type              : Microsoft.Cache/Redis/firewallRules
        StartIP           : 10.0.0.1
        EndIP             : 10.0.0.32

        ResourceGroupName : myGroup
        Name              : mycache
        FirewallRuleId    : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/mycache/firewallRules/ruletwo
        RuleName          : ruletwo
        Type              : Microsoft.Cache/Redis/firewallRules
        StartIP           : 10.0.0.33
        EndIP             : 10.0.0.64
```

<span data-ttu-id="1c88a-112">Det här kommandot får alla brand Väggs regler från Redis cachelagrade.</span><span class="sxs-lookup"><span data-stu-id="1c88a-112">This command gets all firewall rules from Redis Cache named mycache.</span></span>

## <span data-ttu-id="1c88a-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1c88a-113">PARAMETERS</span></span>

### <span data-ttu-id="1c88a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c88a-114">-DefaultProfile</span></span>
<span data-ttu-id="1c88a-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1c88a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c88a-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="1c88a-116">-Name</span></span>
<span data-ttu-id="1c88a-117">Namn på Redis cache.</span><span class="sxs-lookup"><span data-stu-id="1c88a-117">Name of redis cache.</span></span>

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

### <span data-ttu-id="1c88a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c88a-118">-ResourceGroupName</span></span>
<span data-ttu-id="1c88a-119">Namn på resurs gruppen där cacheminnet finns.</span><span class="sxs-lookup"><span data-stu-id="1c88a-119">Name of resource group in which cache exists.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c88a-120">-RuleName</span><span class="sxs-lookup"><span data-stu-id="1c88a-120">-RuleName</span></span>
<span data-ttu-id="1c88a-121">Namn på brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="1c88a-121">Name of firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c88a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c88a-122">CommonParameters</span></span>
<span data-ttu-id="1c88a-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c88a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c88a-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c88a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c88a-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1c88a-125">INPUTS</span></span>

### <span data-ttu-id="1c88a-126">System. String</span><span class="sxs-lookup"><span data-stu-id="1c88a-126">System.String</span></span>

## <span data-ttu-id="1c88a-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1c88a-127">OUTPUTS</span></span>

### <span data-ttu-id="1c88a-128">Microsoft. Azure. commands. RedisCache. Models. PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="1c88a-128">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="1c88a-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1c88a-129">NOTES</span></span>

## <span data-ttu-id="1c88a-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1c88a-130">RELATED LINKS</span></span>

[<span data-ttu-id="1c88a-131">New-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="1c88a-131">New-AzRedisCacheFirewallRule</span></span>](./New-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="1c88a-132">Remove-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="1c88a-132">Remove-AzRedisCacheFirewallRule</span></span>](./Remove-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="1c88a-133">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="1c88a-133">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="1c88a-134">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="1c88a-134">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="1c88a-135">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="1c88a-135">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="1c88a-136">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="1c88a-136">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)
---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheFirewallRule.md
ms.openlocfilehash: 8e28951f826c5a049f345bb3182bda10e7de82fb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102584"
---
# <span data-ttu-id="c0bdf-101">Get-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c0bdf-101">Get-AzRedisCacheFirewallRule</span></span>

## <span data-ttu-id="c0bdf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c0bdf-102">SYNOPSIS</span></span>
<span data-ttu-id="c0bdf-103">Skaffa brand Väggs regler som är inställda på Redis cache.</span><span class="sxs-lookup"><span data-stu-id="c0bdf-103">Get firewall rules set on Redis Cache.</span></span>

## <span data-ttu-id="c0bdf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c0bdf-104">SYNTAX</span></span>

```
Get-AzRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> [-RuleName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c0bdf-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c0bdf-105">DESCRIPTION</span></span>
<span data-ttu-id="c0bdf-106">Om **RuleName** parameter anges får cmdleten **Get-AzRedisCacheFirewallRule** information om den angivna brand Väggs regeln i Azure Redis-cachen.</span><span class="sxs-lookup"><span data-stu-id="c0bdf-106">If **RuleName** parameter if provided, **Get-AzRedisCacheFirewallRule** cmdlet gets detail about the specified firewall rule on Azure Redis Cache.</span></span> <span data-ttu-id="c0bdf-107">Om det bara finns **ett namn** hämtas alla brand Väggs regler som är tillgängliga för det Redis cacheminnet.</span><span class="sxs-lookup"><span data-stu-id="c0bdf-107">If only **Name** is specified this operation gets all firewall rules available on that Redis Cache.</span></span>

## <span data-ttu-id="c0bdf-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c0bdf-108">EXAMPLES</span></span>

### <span data-ttu-id="c0bdf-109">Exempel 1: skaffa en enda brand Väggs regel</span><span class="sxs-lookup"><span data-stu-id="c0bdf-109">Example 1: Get a single firewall rule</span></span>
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

<span data-ttu-id="c0bdf-110">Det här kommandot får brand Väggs regeln som heter ruleone från Redis cacheminne.</span><span class="sxs-lookup"><span data-stu-id="c0bdf-110">This command gets firewall rule named ruleone from Redis Cache named mycache.</span></span>

### <span data-ttu-id="c0bdf-111">Exempel 2: Hämta alla brand Väggs regler</span><span class="sxs-lookup"><span data-stu-id="c0bdf-111">Example 2: Get all firewall rules</span></span>
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

<span data-ttu-id="c0bdf-112">Det här kommandot får alla brand Väggs regler från Redis cachelagrade.</span><span class="sxs-lookup"><span data-stu-id="c0bdf-112">This command gets all firewall rules from Redis Cache named mycache.</span></span>

## <span data-ttu-id="c0bdf-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c0bdf-113">PARAMETERS</span></span>

### <span data-ttu-id="c0bdf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0bdf-114">-DefaultProfile</span></span>
<span data-ttu-id="c0bdf-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c0bdf-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0bdf-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="c0bdf-116">-Name</span></span>
<span data-ttu-id="c0bdf-117">Namn på Redis cache.</span><span class="sxs-lookup"><span data-stu-id="c0bdf-117">Name of redis cache.</span></span>

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

### <span data-ttu-id="c0bdf-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0bdf-118">-ResourceGroupName</span></span>
<span data-ttu-id="c0bdf-119">Namn på resurs gruppen där cacheminnet finns.</span><span class="sxs-lookup"><span data-stu-id="c0bdf-119">Name of resource group in which cache exists.</span></span>

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

### <span data-ttu-id="c0bdf-120">-RuleName</span><span class="sxs-lookup"><span data-stu-id="c0bdf-120">-RuleName</span></span>
<span data-ttu-id="c0bdf-121">Namn på brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="c0bdf-121">Name of firewall rule.</span></span>

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

### <span data-ttu-id="c0bdf-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0bdf-122">CommonParameters</span></span>
<span data-ttu-id="c0bdf-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0bdf-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0bdf-124">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0bdf-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0bdf-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c0bdf-125">INPUTS</span></span>

### <span data-ttu-id="c0bdf-126">System. String</span><span class="sxs-lookup"><span data-stu-id="c0bdf-126">System.String</span></span>

## <span data-ttu-id="c0bdf-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c0bdf-127">OUTPUTS</span></span>

### <span data-ttu-id="c0bdf-128">Microsoft. Azure. commands. RedisCache. Models. PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c0bdf-128">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="c0bdf-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c0bdf-129">NOTES</span></span>

## <span data-ttu-id="c0bdf-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c0bdf-130">RELATED LINKS</span></span>

[<span data-ttu-id="c0bdf-131">New-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c0bdf-131">New-AzRedisCacheFirewallRule</span></span>](./New-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="c0bdf-132">Remove-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c0bdf-132">Remove-AzRedisCacheFirewallRule</span></span>](./Remove-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="c0bdf-133">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="c0bdf-133">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="c0bdf-134">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="c0bdf-134">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="c0bdf-135">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="c0bdf-135">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="c0bdf-136">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="c0bdf-136">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)
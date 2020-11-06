---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/get-azurermrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheFirewallRule.md
ms.openlocfilehash: 91eff9b6a096263b96ecae0cf9901f6dbce26c68
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581696"
---
# <span data-ttu-id="6d449-101">Get-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6d449-101">Get-AzureRmRedisCacheFirewallRule</span></span>

## <span data-ttu-id="6d449-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6d449-102">SYNOPSIS</span></span>
<span data-ttu-id="6d449-103">Skaffa brand Väggs regler som är inställda på Redis cache.</span><span class="sxs-lookup"><span data-stu-id="6d449-103">Get firewall rules set on Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d449-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6d449-104">SYNTAX</span></span>

```
Get-AzureRmRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> [-RuleName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d449-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6d449-105">DESCRIPTION</span></span>
<span data-ttu-id="6d449-106">Om **RuleName** parameter anges får cmdleten **Get-AzureRmRedisCacheFirewallRule** information om den angivna brand Väggs regeln i Azure Redis-cachen.</span><span class="sxs-lookup"><span data-stu-id="6d449-106">If **RuleName** parameter if provided, **Get-AzureRmRedisCacheFirewallRule** cmdlet gets detail about the specified firewall rule on Azure Redis Cache.</span></span> <span data-ttu-id="6d449-107">Om det bara finns **ett namn** hämtas alla brand Väggs regler som är tillgängliga för det Redis cacheminnet.</span><span class="sxs-lookup"><span data-stu-id="6d449-107">If only **Name** is specified this operation gets all firewall rules available on that Redis Cache.</span></span>

## <span data-ttu-id="6d449-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6d449-108">EXAMPLES</span></span>

### <span data-ttu-id="6d449-109">Exempel 1: skaffa en enda brand Väggs regel</span><span class="sxs-lookup"><span data-stu-id="6d449-109">Example 1: Get a single firewall rule</span></span>
```
PS C:\>Get-AzureRmRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone"

        ResourceGroupName : myGroup
        Name              : mycache
        FirewallRuleId    : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/mycache/firewallRules/ruleone
        RuleName          : ruleone
        Type              : Microsoft.Cache/Redis/firewallRules
        StartIP           : 10.0.0.1
        EndIP             : 10.0.0.32
```

<span data-ttu-id="6d449-110">Det här kommandot får brand Väggs regeln som heter ruleone från Redis cacheminne.</span><span class="sxs-lookup"><span data-stu-id="6d449-110">This command gets firewall rule named ruleone from Redis Cache named mycache.</span></span>

### <span data-ttu-id="6d449-111">Exempel 2: Hämta alla brand Väggs regler</span><span class="sxs-lookup"><span data-stu-id="6d449-111">Example 2: Get all firewall rules</span></span>
```
PS C:\>Get-AzureRmRedisCacheFirewallRule -Name "mycache"

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

<span data-ttu-id="6d449-112">Det här kommandot får alla brand Väggs regler från Redis cachelagrade.</span><span class="sxs-lookup"><span data-stu-id="6d449-112">This command gets all firewall rules from Redis Cache named mycache.</span></span>

## <span data-ttu-id="6d449-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6d449-113">PARAMETERS</span></span>

### <span data-ttu-id="6d449-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d449-114">-DefaultProfile</span></span>
<span data-ttu-id="6d449-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6d449-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d449-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="6d449-116">-Name</span></span>
<span data-ttu-id="6d449-117">Namn på Redis cache.</span><span class="sxs-lookup"><span data-stu-id="6d449-117">Name of redis cache.</span></span>

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

### <span data-ttu-id="6d449-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d449-118">-ResourceGroupName</span></span>
<span data-ttu-id="6d449-119">Namn på resurs gruppen där cacheminnet finns.</span><span class="sxs-lookup"><span data-stu-id="6d449-119">Name of resource group in which cache exists.</span></span>

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

### <span data-ttu-id="6d449-120">-RuleName</span><span class="sxs-lookup"><span data-stu-id="6d449-120">-RuleName</span></span>
<span data-ttu-id="6d449-121">Namn på brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="6d449-121">Name of firewall rule.</span></span>

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

### <span data-ttu-id="6d449-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d449-122">CommonParameters</span></span>
<span data-ttu-id="6d449-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d449-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d449-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d449-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d449-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6d449-125">INPUTS</span></span>

### <span data-ttu-id="6d449-126">System. String</span><span class="sxs-lookup"><span data-stu-id="6d449-126">System.String</span></span>

## <span data-ttu-id="6d449-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6d449-127">OUTPUTS</span></span>

### <span data-ttu-id="6d449-128">Microsoft. Azure. commands. RedisCache. Models. PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6d449-128">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="6d449-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6d449-129">NOTES</span></span>

## <span data-ttu-id="6d449-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6d449-130">RELATED LINKS</span></span>

[<span data-ttu-id="6d449-131">New-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6d449-131">New-AzureRmRedisCacheFirewallRule</span></span>](./New-AzureRmRedisCacheFirewallRule.md)

[<span data-ttu-id="6d449-132">Remove-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6d449-132">Remove-AzureRmRedisCacheFirewallRule</span></span>](./Remove-AzureRmRedisCacheFirewallRule.md)

[<span data-ttu-id="6d449-133">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="6d449-133">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="6d449-134">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="6d449-134">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="6d449-135">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="6d449-135">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="6d449-136">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="6d449-136">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)

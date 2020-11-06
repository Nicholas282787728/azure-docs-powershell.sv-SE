---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/get-azurermrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheFirewallRule.md
ms.openlocfilehash: 231787f57061ff4e118510c3dc166915b39da436
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576452"
---
# <span data-ttu-id="b4da5-101">Get-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b4da5-101">Get-AzureRmRedisCacheFirewallRule</span></span>

## <span data-ttu-id="b4da5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b4da5-102">SYNOPSIS</span></span>
<span data-ttu-id="b4da5-103">Skaffa brand Väggs regler som är inställda på Redis cache.</span><span class="sxs-lookup"><span data-stu-id="b4da5-103">Get firewall rules set on Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4da5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b4da5-104">SYNTAX</span></span>

```
Get-AzureRmRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> [-RuleName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4da5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b4da5-105">DESCRIPTION</span></span>
<span data-ttu-id="b4da5-106">Om **RuleName** parameter anges får cmdleten **Get-AzureRmRedisCacheFirewallRule** information om den angivna brand Väggs regeln i Azure Redis-cachen.</span><span class="sxs-lookup"><span data-stu-id="b4da5-106">If **RuleName** parameter if provided, **Get-AzureRmRedisCacheFirewallRule** cmdlet gets detail about the specified firewall rule on Azure Redis Cache.</span></span> <span data-ttu-id="b4da5-107">Om det bara finns **ett namn** hämtas alla brand Väggs regler som är tillgängliga för det Redis cacheminnet.</span><span class="sxs-lookup"><span data-stu-id="b4da5-107">If only **Name** is specified this operation gets all firewall rules available on that Redis Cache.</span></span>

## <span data-ttu-id="b4da5-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b4da5-108">EXAMPLES</span></span>

### <span data-ttu-id="b4da5-109">Exempel 1: skaffa en enda brand Väggs regel</span><span class="sxs-lookup"><span data-stu-id="b4da5-109">Example 1: Get a single firewall rule</span></span>
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

<span data-ttu-id="b4da5-110">Det här kommandot får brand Väggs regeln som heter ruleone från Redis cacheminne.</span><span class="sxs-lookup"><span data-stu-id="b4da5-110">This command gets firewall rule named ruleone from Redis Cache named mycache.</span></span>

### <span data-ttu-id="b4da5-111">Exempel 2: Hämta alla brand Väggs regler</span><span class="sxs-lookup"><span data-stu-id="b4da5-111">Example 2: Get all firewall rules</span></span>
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

<span data-ttu-id="b4da5-112">Det här kommandot får alla brand Väggs regler från Redis cachelagrade.</span><span class="sxs-lookup"><span data-stu-id="b4da5-112">This command gets all firewall rules from Redis Cache named mycache.</span></span>

## <span data-ttu-id="b4da5-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b4da5-113">PARAMETERS</span></span>

### <span data-ttu-id="b4da5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4da5-114">-DefaultProfile</span></span>
<span data-ttu-id="b4da5-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b4da5-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4da5-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="b4da5-116">-Name</span></span>
<span data-ttu-id="b4da5-117">Namn på Redis cache.</span><span class="sxs-lookup"><span data-stu-id="b4da5-117">Name of redis cache.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4da5-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4da5-118">-ResourceGroupName</span></span>
<span data-ttu-id="b4da5-119">Namn på resurs gruppen där cacheminnet finns.</span><span class="sxs-lookup"><span data-stu-id="b4da5-119">Name of resource group in which cache exists.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4da5-120">-RuleName</span><span class="sxs-lookup"><span data-stu-id="b4da5-120">-RuleName</span></span>
<span data-ttu-id="b4da5-121">Namn på brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="b4da5-121">Name of firewall rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4da5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4da5-122">CommonParameters</span></span>
<span data-ttu-id="b4da5-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4da5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4da5-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4da5-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4da5-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b4da5-125">INPUTS</span></span>

### <span data-ttu-id="b4da5-126">System. String</span><span class="sxs-lookup"><span data-stu-id="b4da5-126">System.String</span></span>
<span data-ttu-id="b4da5-127">Du kan pipes in i denna cmdlet efter namn men inte efter värde.</span><span class="sxs-lookup"><span data-stu-id="b4da5-127">You can pipe input to this cmdlet by name, but not by value.</span></span>

## <span data-ttu-id="b4da5-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b4da5-128">OUTPUTS</span></span>

### <span data-ttu-id="b4da5-129">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. RedisCache. Models. PSRedisFirewallRule, Microsoft. Azure. commands. RedisCache, version = 4.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="b4da5-129">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule, Microsoft.Azure.Commands.RedisCache, Version=4.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="b4da5-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b4da5-130">NOTES</span></span>

## <span data-ttu-id="b4da5-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b4da5-131">RELATED LINKS</span></span>

[<span data-ttu-id="b4da5-132">New-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b4da5-132">New-AzureRmRedisCacheFirewallRule</span></span>](./New-AzureRmRedisCacheFirewallRule.md)

[<span data-ttu-id="b4da5-133">Remove-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b4da5-133">Remove-AzureRmRedisCacheFirewallRule</span></span>](./Remove-AzureRmRedisCacheFirewallRule.md)

[<span data-ttu-id="b4da5-134">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="b4da5-134">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="b4da5-135">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="b4da5-135">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="b4da5-136">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="b4da5-136">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="b4da5-137">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="b4da5-137">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)

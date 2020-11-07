---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/remove-azurermrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCacheFirewallRule.md
ms.openlocfilehash: 25c3d0c72539ecd74e25ed455b4afcf4211c0718
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756668"
---
# <span data-ttu-id="1859d-101">Remove-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="1859d-101">Remove-AzureRmRedisCacheFirewallRule</span></span>

## <span data-ttu-id="1859d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1859d-102">SYNOPSIS</span></span>
<span data-ttu-id="1859d-103">Ta bort en brand Väggs regel från en Redis cache.</span><span class="sxs-lookup"><span data-stu-id="1859d-103">Remove a firewall rule from a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1859d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1859d-104">SYNTAX</span></span>

### <span data-ttu-id="1859d-105">NormalParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="1859d-105">NormalParameterSet (Default)</span></span>
```
Remove-AzureRmRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> -RuleName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1859d-106">PSRedisFirewallRuleObject</span><span class="sxs-lookup"><span data-stu-id="1859d-106">PSRedisFirewallRuleObject</span></span>
```
Remove-AzureRmRedisCacheFirewallRule -InputObject <PSRedisFirewallRule> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1859d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1859d-107">DESCRIPTION</span></span>
<span data-ttu-id="1859d-108">Ta bort en brand Väggs regel från en Redis cache.</span><span class="sxs-lookup"><span data-stu-id="1859d-108">Remove a firewall rule from a Redis Cache.</span></span>

## <span data-ttu-id="1859d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1859d-109">EXAMPLES</span></span>

### <span data-ttu-id="1859d-110">Exempel 1: ta bort en enskild brand Väggs regel</span><span class="sxs-lookup"><span data-stu-id="1859d-110">Example 1: Remove a single firewall rule</span></span>
```
PS C:\>Remove-AzureRmRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone" -PassThru
True
```

<span data-ttu-id="1859d-111">Det här kommandot tar bort en brand Väggs regel med namnet ruleone från Redis cacheminne.</span><span class="sxs-lookup"><span data-stu-id="1859d-111">This command removes a firewall rule named ruleone from Redis Cache named mycache.</span></span> 

## <span data-ttu-id="1859d-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1859d-112">PARAMETERS</span></span>

### <span data-ttu-id="1859d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1859d-113">-DefaultProfile</span></span>
<span data-ttu-id="1859d-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1859d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1859d-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1859d-115">-InputObject</span></span>
<span data-ttu-id="1859d-116">objekt av typen PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="1859d-116">object of type PSRedisFirewallRule</span></span>

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

### <span data-ttu-id="1859d-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="1859d-117">-Name</span></span>
<span data-ttu-id="1859d-118">Namn på Redis cache.</span><span class="sxs-lookup"><span data-stu-id="1859d-118">Name of redis cache.</span></span>

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

### <span data-ttu-id="1859d-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1859d-119">-PassThru</span></span>
<span data-ttu-id="1859d-120">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="1859d-120">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="1859d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1859d-121">-ResourceGroupName</span></span>
<span data-ttu-id="1859d-122">Namn på resurs gruppen där cacheminnet finns.</span><span class="sxs-lookup"><span data-stu-id="1859d-122">Name of resource group in which cache exists.</span></span>

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

### <span data-ttu-id="1859d-123">-RuleName</span><span class="sxs-lookup"><span data-stu-id="1859d-123">-RuleName</span></span>
<span data-ttu-id="1859d-124">Namn på brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="1859d-124">Name of firewall rule.</span></span>

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

### <span data-ttu-id="1859d-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1859d-125">-Confirm</span></span>
<span data-ttu-id="1859d-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1859d-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1859d-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1859d-127">-WhatIf</span></span>
<span data-ttu-id="1859d-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1859d-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1859d-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1859d-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1859d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1859d-130">CommonParameters</span></span>
<span data-ttu-id="1859d-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1859d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1859d-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1859d-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1859d-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1859d-133">INPUTS</span></span>

### <span data-ttu-id="1859d-134">System. String</span><span class="sxs-lookup"><span data-stu-id="1859d-134">System.String</span></span>

### <span data-ttu-id="1859d-135">Microsoft. Azure. commands. RedisCache. Models. PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="1859d-135">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>
<span data-ttu-id="1859d-136">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1859d-136">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="1859d-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1859d-137">OUTPUTS</span></span>

### <span data-ttu-id="1859d-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1859d-138">System.Boolean</span></span>

## <span data-ttu-id="1859d-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1859d-139">NOTES</span></span>

## <span data-ttu-id="1859d-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1859d-140">RELATED LINKS</span></span>

[<span data-ttu-id="1859d-141">New-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="1859d-141">New-AzureRmRedisCacheFirewallRule</span></span>](./New-AzureRmRedisCacheFirewallRule.md)

[<span data-ttu-id="1859d-142">Get-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="1859d-142">Get-AzureRmRedisCacheFirewallRule</span></span>](./Get-AzureRmRedisCacheFirewallRule.md)

[<span data-ttu-id="1859d-143">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="1859d-143">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="1859d-144">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="1859d-144">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="1859d-145">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="1859d-145">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="1859d-146">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="1859d-146">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)

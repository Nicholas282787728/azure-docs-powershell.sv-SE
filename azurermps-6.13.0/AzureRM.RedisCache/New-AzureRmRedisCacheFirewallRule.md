---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/new-azurermrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheFirewallRule.md
ms.openlocfilehash: e5e909107d740f67e3407347625270226c87839d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581684"
---
# <span data-ttu-id="1eb12-101">New-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="1eb12-101">New-AzureRmRedisCacheFirewallRule</span></span>

## <span data-ttu-id="1eb12-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1eb12-102">SYNOPSIS</span></span>
<span data-ttu-id="1eb12-103">Skapa en brand Väggs regel i en Redis cache.</span><span class="sxs-lookup"><span data-stu-id="1eb12-103">Create a firewall rule on a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1eb12-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1eb12-104">SYNTAX</span></span>

### <span data-ttu-id="1eb12-105">NormalParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="1eb12-105">NormalParameterSet (Default)</span></span>
```
New-AzureRmRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> -RuleName <String>
 -StartIP <String> -EndIP <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1eb12-106">RedisCacheAttributesObject</span><span class="sxs-lookup"><span data-stu-id="1eb12-106">RedisCacheAttributesObject</span></span>
```
New-AzureRmRedisCacheFirewallRule -InputObject <RedisCacheAttributes> -RuleName <String> -StartIP <String>
 -EndIP <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1eb12-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1eb12-107">ResourceIdParameterSet</span></span>
```
New-AzureRmRedisCacheFirewallRule -ResourceId <String> -RuleName <String> -StartIP <String> -EndIP <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1eb12-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1eb12-108">DESCRIPTION</span></span>
<span data-ttu-id="1eb12-109">Skapa en brand Väggs regel i en Redis cache.</span><span class="sxs-lookup"><span data-stu-id="1eb12-109">Create a firewall rule on a Redis Cache.</span></span>

## <span data-ttu-id="1eb12-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1eb12-110">EXAMPLES</span></span>

### <span data-ttu-id="1eb12-111">Exempel 1: skapa en brand Väggs regel</span><span class="sxs-lookup"><span data-stu-id="1eb12-111">Example 1: Create a firewall rule</span></span>
```
PS C:\>New-AzureRmRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone" -StartIP "10.0.0.1" -EndIP "10.0.0.32"

        ResourceGroupName : myGroup
        Name              : mycache
        FirewallRuleId    : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/mycache/firewallRules/ruleone
        RuleName          : ruleone
        Type              : Microsoft.Cache/Redis/firewallRules
        StartIP           : 10.0.0.1
        EndIP             : 10.0.0.32
```

<span data-ttu-id="1eb12-112">Det här kommandot skapar en brand Väggs regel med namnet ruleone i Redis cache med namnet noncache.</span><span class="sxs-lookup"><span data-stu-id="1eb12-112">This command creates firewall rule named ruleone on Redis Cache named mycache.</span></span>

## <span data-ttu-id="1eb12-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1eb12-113">PARAMETERS</span></span>

### <span data-ttu-id="1eb12-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1eb12-114">-DefaultProfile</span></span>
<span data-ttu-id="1eb12-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1eb12-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1eb12-116">-EndIP</span><span class="sxs-lookup"><span data-stu-id="1eb12-116">-EndIP</span></span>
<span data-ttu-id="1eb12-117">Sista IP-adress.</span><span class="sxs-lookup"><span data-stu-id="1eb12-117">Ending IP address.</span></span>

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

### <span data-ttu-id="1eb12-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1eb12-118">-InputObject</span></span>
<span data-ttu-id="1eb12-119">objekt av typen RedisCacheAttributes</span><span class="sxs-lookup"><span data-stu-id="1eb12-119">object of type RedisCacheAttributes</span></span>

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

### <span data-ttu-id="1eb12-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="1eb12-120">-Name</span></span>
<span data-ttu-id="1eb12-121">Namn på Redis cache.</span><span class="sxs-lookup"><span data-stu-id="1eb12-121">Name of redis cache.</span></span>

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

### <span data-ttu-id="1eb12-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1eb12-122">-ResourceGroupName</span></span>
<span data-ttu-id="1eb12-123">Namn på resurs gruppen där cacheminnet finns.</span><span class="sxs-lookup"><span data-stu-id="1eb12-123">Name of resource group in which cache exists.</span></span>

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

### <span data-ttu-id="1eb12-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1eb12-124">-ResourceId</span></span>
<span data-ttu-id="1eb12-125">ARM-ID för Redis cache.</span><span class="sxs-lookup"><span data-stu-id="1eb12-125">ARM Id of Redis Cache.</span></span>

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

### <span data-ttu-id="1eb12-126">-RuleName</span><span class="sxs-lookup"><span data-stu-id="1eb12-126">-RuleName</span></span>
<span data-ttu-id="1eb12-127">Namn på brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="1eb12-127">Name of firewall rule.</span></span>

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

### <span data-ttu-id="1eb12-128">-StartIP</span><span class="sxs-lookup"><span data-stu-id="1eb12-128">-StartIP</span></span>
<span data-ttu-id="1eb12-129">Inledande IP-adress.</span><span class="sxs-lookup"><span data-stu-id="1eb12-129">Starting IP address.</span></span>

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

### <span data-ttu-id="1eb12-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1eb12-130">-Confirm</span></span>
<span data-ttu-id="1eb12-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1eb12-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1eb12-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1eb12-132">-WhatIf</span></span>
<span data-ttu-id="1eb12-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1eb12-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1eb12-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1eb12-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1eb12-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1eb12-135">CommonParameters</span></span>
<span data-ttu-id="1eb12-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1eb12-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1eb12-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1eb12-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1eb12-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1eb12-138">INPUTS</span></span>

### <span data-ttu-id="1eb12-139">System. String</span><span class="sxs-lookup"><span data-stu-id="1eb12-139">System.String</span></span>

### <span data-ttu-id="1eb12-140">Microsoft. Azure. commands. RedisCache. Models. RedisCacheAttributes</span><span class="sxs-lookup"><span data-stu-id="1eb12-140">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span></span>
<span data-ttu-id="1eb12-141">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1eb12-141">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="1eb12-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1eb12-142">OUTPUTS</span></span>

### <span data-ttu-id="1eb12-143">Microsoft. Azure. commands. RedisCache. Models. PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="1eb12-143">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="1eb12-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1eb12-144">NOTES</span></span>

## <span data-ttu-id="1eb12-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1eb12-145">RELATED LINKS</span></span>

[<span data-ttu-id="1eb12-146">Get-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="1eb12-146">Get-AzureRmRedisCacheFirewallRule</span></span>](./Get-AzureRmRedisCacheFirewallRule.md)

[<span data-ttu-id="1eb12-147">Remove-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="1eb12-147">Remove-AzureRmRedisCacheFirewallRule</span></span>](./Remove-AzureRmRedisCacheFirewallRule.md)

[<span data-ttu-id="1eb12-148">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="1eb12-148">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="1eb12-149">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="1eb12-149">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="1eb12-150">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="1eb12-150">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="1eb12-151">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="1eb12-151">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)

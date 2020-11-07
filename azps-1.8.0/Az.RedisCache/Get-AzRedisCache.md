---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 8EF45FCE-5475-4A18-BFB0-C016E239612E
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCache.md
ms.openlocfilehash: 1e7f57ce251c6f95a74b2ca0a55aa1caa92349a7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747288"
---
# <span data-ttu-id="2e34f-101">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="2e34f-101">Get-AzRedisCache</span></span>

## <span data-ttu-id="2e34f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2e34f-102">SYNOPSIS</span></span>
<span data-ttu-id="2e34f-103">Hämtar en Redis cache.</span><span class="sxs-lookup"><span data-stu-id="2e34f-103">Gets a Redis Cache.</span></span>

## <span data-ttu-id="2e34f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2e34f-104">SYNTAX</span></span>

```
Get-AzRedisCache [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2e34f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2e34f-105">DESCRIPTION</span></span>
<span data-ttu-id="2e34f-106">Cmdleten **Get-AzRedisCache** hämtar det angivna Azure Redis-cacheminnet.</span><span class="sxs-lookup"><span data-stu-id="2e34f-106">The **Get-AzRedisCache** cmdlet gets the specified Azure Redis Cache.</span></span>
<span data-ttu-id="2e34f-107">Om du inte anger några parametrar får den här åtgärden alla Redis-cachen för det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="2e34f-107">If you specify no parameters, this operation gets every Redis Cache for the current subscription.</span></span>

## <span data-ttu-id="2e34f-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2e34f-108">EXAMPLES</span></span>

### <span data-ttu-id="2e34f-109">Exempel 1: Hämta en Redis-cache efter namn</span><span class="sxs-lookup"><span data-stu-id="2e34f-109">Example 1: Get a Redis Cache by name</span></span>
```
PS C:\>Get-AzRedisCache -Name "myexists"

        ResourceGroupName  : myGroup
        Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/myexists
        Location           : North Central US
        Name               : myexists
        Type               : Microsoft.Cache/Redis
        HostName           : myexists.redis.cache.windows.net
        Port               : 6379
        ProvisioningState  : succeeded
        SslPort            : 6380
        RedisConfiguration : {}
        EnableNonSslPort   : False
        RedisVersion       : 2.8
        Size               : 1GB
        Sku                : Basic
        Tag                : {}
        Zone               : []
```

<span data-ttu-id="2e34f-110">Det här kommandot får Redis cacheminnet som heter exist.</span><span class="sxs-lookup"><span data-stu-id="2e34f-110">This command gets the Redis Cache named myexists.</span></span>

### <span data-ttu-id="2e34f-111">Exempel 2: Hämta alla Redis-cachen i en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="2e34f-111">Example 2: Get every Redis Cache in a resource group</span></span>
```
PS C:\>Get-AzRedisCache -ResourceGroupName "myGroup"

        ResourceGroupName  : myGroup
        Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/myexists
        Location           : North Central US
        Name               : myexists
        Type               : Microsoft.Cache/Redis
        HostName           : myexists.redis.cache.windows.net
        Port               : 6379
        ProvisioningState  : succeeded
        SslPort            : 6380
        RedisConfiguration : {}
        EnableNonSslPort   : False
        RedisVersion       : 2.8
        Size               : 1GB
        Sku                : Basic
        Tag                : {}
        Zone               : []

        ResourceGroupName  : myGroup
        Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/myearlier
        Location           : North Central US
        Name               : myearlier
        Type               : Microsoft.Cache/Redis
        HostName           : myearlier.redis.cache.windows.net
        Port               : 6379
        ProvisioningState  : succeeded
        SslPort            : 6380
        RedisConfiguration : {}
        EnableNonSslPort   : True
        RedisVersion       : 2.8
        Size               : 250MB
        Sku                : Standard
        Tag                : {}
        Zone               : []
```

<span data-ttu-id="2e34f-112">Det här kommandot får alla Redis-cache i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="2e34f-112">This command gets every Redis Cache in the specified resource group.</span></span>

### <span data-ttu-id="2e34f-113">Exempel 3: Hämta alla Redis-cachen i det aktuella abonnemanget</span><span class="sxs-lookup"><span data-stu-id="2e34f-113">Example 3: Get every Redis Cache in the current subscription</span></span>
```
PS C:\>Get-AzRedisCache

        ResourceGroupName  : myGroup
        Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/myexists
        Location           : North Central US
        Name               : myexists
        Type               : Microsoft.Cache/Redis
        HostName           : myexists.redis.cache.windows.net
        Port               : 6379
        ProvisioningState  : succeeded
        SslPort            : 6380
        RedisConfiguration : {}
        EnableNonSslPort   : False
        RedisVersion       : 2.8
        Size               : 1GB
        Sku                : Basic
        Tag                : {}
        Zone               : []

        ResourceGroupName  : myGroup
        Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/myearlier
        Location           : North Central US
        Name               : myearlier
        Type               : Microsoft.Cache/Redis
        HostName           : myearlier.redis.cache.windows.net
        Port               : 6379
        ProvisioningState  : succeeded
        SslPort            : 6380
        RedisConfiguration : {}
        EnableNonSslPort   : True
        RedisVersion       : 2.8
        Size               : 250MB
        Sku                : Standard
        Tag                : {}
        Zone               : []

        ResourceGroupName  : myGroup2
        Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup2/providers/Microsoft.Cache/Redis/myearlier2
        Location           : North Central US
        Name               : myearlier2
        Type               : Microsoft.Cache/Redis
        HostName           : myearlier2.redis.cache.windows.net
        Port               : 6379
        ProvisioningState  : succeeded
        SslPort            : 6380
        RedisConfiguration : {}
        EnableNonSslPort   : False
        RedisVersion       : 2.8
        Size               : 250MB
        Sku                : Basic
        Tag                : {}
        Zone               : []
```

<span data-ttu-id="2e34f-114">Det här kommandot får alla Redis-cachen i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="2e34f-114">This command gets every Redis Cache in the current subscription.</span></span>

## <span data-ttu-id="2e34f-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2e34f-115">PARAMETERS</span></span>

### <span data-ttu-id="2e34f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e34f-116">-DefaultProfile</span></span>
<span data-ttu-id="2e34f-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2e34f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e34f-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="2e34f-118">-Name</span></span>
<span data-ttu-id="2e34f-119">Anger namnet på den Redis-cache som ska visas.</span><span class="sxs-lookup"><span data-stu-id="2e34f-119">Specifies the name of the Redis Cache to get.</span></span>
<span data-ttu-id="2e34f-120">Använd med parametern *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="2e34f-120">Use with the *ResourceGroupName* parameter.</span></span>

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

### <span data-ttu-id="2e34f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e34f-121">-ResourceGroupName</span></span>
<span data-ttu-id="2e34f-122">Anger namnet på den resurs grupp som innehåller det Redis-cacheminne som ska visas.</span><span class="sxs-lookup"><span data-stu-id="2e34f-122">Specifies the name of the resource group that contains the Redis Cache to get.</span></span>
<span data-ttu-id="2e34f-123">Om du bara anger parametern *ResourceGroupName* får den här åtgärden alla Redis-cachen i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="2e34f-123">If you specify only the *ResourceGroupName* parameter, this operation gets every Redis Cache in the specified resource group.</span></span>

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

### <span data-ttu-id="2e34f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e34f-124">CommonParameters</span></span>
<span data-ttu-id="2e34f-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e34f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e34f-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e34f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e34f-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2e34f-127">INPUTS</span></span>

### <span data-ttu-id="2e34f-128">System. String</span><span class="sxs-lookup"><span data-stu-id="2e34f-128">System.String</span></span>

## <span data-ttu-id="2e34f-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2e34f-129">OUTPUTS</span></span>

### <span data-ttu-id="2e34f-130">Microsoft. Azure. commands. RedisCache. Models. RedisCacheAttributes</span><span class="sxs-lookup"><span data-stu-id="2e34f-130">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span></span>

## <span data-ttu-id="2e34f-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2e34f-131">NOTES</span></span>

## <span data-ttu-id="2e34f-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2e34f-132">RELATED LINKS</span></span>

[<span data-ttu-id="2e34f-133">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="2e34f-133">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="2e34f-134">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="2e34f-134">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="2e34f-135">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="2e34f-135">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


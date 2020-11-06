---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 8EF45FCE-5475-4A18-BFB0-C016E239612E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/get-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCache.md
ms.openlocfilehash: 1e91aa946e89b8231ea2c58b28c686d603855ada
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576454"
---
# <span data-ttu-id="d0d85-101">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="d0d85-101">Get-AzureRmRedisCache</span></span>

## <span data-ttu-id="d0d85-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d0d85-102">SYNOPSIS</span></span>
<span data-ttu-id="d0d85-103">Hämtar en Redis cache.</span><span class="sxs-lookup"><span data-stu-id="d0d85-103">Gets a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d0d85-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d0d85-104">SYNTAX</span></span>

```
Get-AzureRmRedisCache [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d0d85-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d0d85-105">DESCRIPTION</span></span>
<span data-ttu-id="d0d85-106">Cmdleten **Get-AzureRmRedisCache** hämtar det angivna Azure Redis-cacheminnet.</span><span class="sxs-lookup"><span data-stu-id="d0d85-106">The **Get-AzureRmRedisCache** cmdlet gets the specified Azure Redis Cache.</span></span>
<span data-ttu-id="d0d85-107">Om du inte anger några parametrar får den här åtgärden alla Redis-cachen för det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="d0d85-107">If you specify no parameters, this operation gets every Redis Cache for the current subscription.</span></span>

## <span data-ttu-id="d0d85-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d0d85-108">EXAMPLES</span></span>

### <span data-ttu-id="d0d85-109">Exempel 1: Hämta en Redis-cache efter namn</span><span class="sxs-lookup"><span data-stu-id="d0d85-109">Example 1: Get a Redis Cache by name</span></span>
```
PS C:\>Get-AzureRmRedisCache -Name "myexists"

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

<span data-ttu-id="d0d85-110">Det här kommandot får Redis cacheminnet som heter exist.</span><span class="sxs-lookup"><span data-stu-id="d0d85-110">This command gets the Redis Cache named myexists.</span></span>

### <span data-ttu-id="d0d85-111">Exempel 2: Hämta alla Redis-cachen i en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="d0d85-111">Example 2: Get every Redis Cache in a resource group</span></span>
```
PS C:\>Get-AzureRmRedisCache -ResourceGroupName "myGroup"

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

<span data-ttu-id="d0d85-112">Det här kommandot får alla Redis-cache i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="d0d85-112">This command gets every Redis Cache in the specified resource group.</span></span>

### <span data-ttu-id="d0d85-113">Exempel 3: Hämta alla Redis-cachen i det aktuella abonnemanget</span><span class="sxs-lookup"><span data-stu-id="d0d85-113">Example 3: Get every Redis Cache in the current subscription</span></span>
```
PS C:\>Get-AzureRmRedisCache

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

<span data-ttu-id="d0d85-114">Det här kommandot får alla Redis-cachen i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="d0d85-114">This command gets every Redis Cache in the current subscription.</span></span>

## <span data-ttu-id="d0d85-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d0d85-115">PARAMETERS</span></span>

### <span data-ttu-id="d0d85-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0d85-116">-DefaultProfile</span></span>
<span data-ttu-id="d0d85-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d0d85-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0d85-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="d0d85-118">-Name</span></span>
<span data-ttu-id="d0d85-119">Anger namnet på den Redis-cache som ska visas.</span><span class="sxs-lookup"><span data-stu-id="d0d85-119">Specifies the name of the Redis Cache to get.</span></span>
<span data-ttu-id="d0d85-120">Använd med parametern *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="d0d85-120">Use with the *ResourceGroupName* parameter.</span></span>

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

### <span data-ttu-id="d0d85-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0d85-121">-ResourceGroupName</span></span>
<span data-ttu-id="d0d85-122">Anger namnet på den resurs grupp som innehåller det Redis-cacheminne som ska visas.</span><span class="sxs-lookup"><span data-stu-id="d0d85-122">Specifies the name of the resource group that contains the Redis Cache to get.</span></span>

<span data-ttu-id="d0d85-123">Om du bara anger parametern *ResourceGroupName* får den här åtgärden alla Redis-cachen i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="d0d85-123">If you specify only the *ResourceGroupName* parameter, this operation gets every Redis Cache in the specified resource group.</span></span>

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

### <span data-ttu-id="d0d85-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0d85-124">CommonParameters</span></span>
<span data-ttu-id="d0d85-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0d85-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0d85-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0d85-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0d85-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d0d85-127">INPUTS</span></span>

### <span data-ttu-id="d0d85-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="d0d85-128">None</span></span>
<span data-ttu-id="d0d85-129">Du kan pipes in i denna cmdlet efter namn men inte efter värde.</span><span class="sxs-lookup"><span data-stu-id="d0d85-129">You can pipe input to this cmdlet by name, but not by value.</span></span>

## <span data-ttu-id="d0d85-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d0d85-130">OUTPUTS</span></span>

### <span data-ttu-id="d0d85-131">Microsoft. Azure. commands. RedisCache. Models. RedisCacheAttributes</span><span class="sxs-lookup"><span data-stu-id="d0d85-131">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span></span>
<span data-ttu-id="d0d85-132">Returnerar en matris med **RedisCacheAttributes** -objekt.</span><span class="sxs-lookup"><span data-stu-id="d0d85-132">Returns an array of **RedisCacheAttributes** objects.</span></span>

## <span data-ttu-id="d0d85-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d0d85-133">NOTES</span></span>

## <span data-ttu-id="d0d85-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d0d85-134">RELATED LINKS</span></span>

[<span data-ttu-id="d0d85-135">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="d0d85-135">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="d0d85-136">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="d0d85-136">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="d0d85-137">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="d0d85-137">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)



---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 8EF45FCE-5475-4A18-BFB0-C016E239612E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCache.md
ms.openlocfilehash: 4cdd81b0cf9f83482192fbe6f484fb0b0d1beaf6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584548"
---
# <span data-ttu-id="0fbd5-101">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="0fbd5-101">Get-AzureRmRedisCache</span></span>

## <span data-ttu-id="0fbd5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0fbd5-102">SYNOPSIS</span></span>
<span data-ttu-id="0fbd5-103">Hämtar en Redis cache.</span><span class="sxs-lookup"><span data-stu-id="0fbd5-103">Gets a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0fbd5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0fbd5-104">SYNTAX</span></span>

### <span data-ttu-id="0fbd5-105">Allt i abonnemanget (standard)</span><span class="sxs-lookup"><span data-stu-id="0fbd5-105">All In Subscription (Default)</span></span>
```
Get-AzureRmRedisCache [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0fbd5-106">Alla i resurs grupp</span><span class="sxs-lookup"><span data-stu-id="0fbd5-106">All In Resource Group</span></span>
```
Get-AzureRmRedisCache -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0fbd5-107">Specifik Redis-cache</span><span class="sxs-lookup"><span data-stu-id="0fbd5-107">Specific Redis Cache</span></span>
```
Get-AzureRmRedisCache -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0fbd5-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0fbd5-108">DESCRIPTION</span></span>
<span data-ttu-id="0fbd5-109">Cmdleten **Get-AzureRmRedisCache** hämtar det angivna Azure Redis-cacheminnet.</span><span class="sxs-lookup"><span data-stu-id="0fbd5-109">The **Get-AzureRmRedisCache** cmdlet gets the specified Azure Redis Cache.</span></span>
<span data-ttu-id="0fbd5-110">Om du inte anger några parametrar får den här åtgärden alla Redis-cachen för det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="0fbd5-110">If you specify no parameters, this operation gets every Redis Cache for the current subscription.</span></span>

## <span data-ttu-id="0fbd5-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0fbd5-111">EXAMPLES</span></span>

### <span data-ttu-id="0fbd5-112">Exempel 1: Hämta en Redis-cache efter namn</span><span class="sxs-lookup"><span data-stu-id="0fbd5-112">Example 1: Get a Redis Cache by name</span></span>
```
PS C:\>Get-AzureRmRedisCache -ResourceGroupName "myGroup" -Name "myexists"

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
```

<span data-ttu-id="0fbd5-113">Det här kommandot får Redis cacheminnet som heter exist.</span><span class="sxs-lookup"><span data-stu-id="0fbd5-113">This command gets the Redis Cache named myexists.</span></span>

### <span data-ttu-id="0fbd5-114">Exempel 2: Hämta alla Redis-cachen i en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="0fbd5-114">Example 2: Get every Redis Cache in a resource group</span></span>
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
```

<span data-ttu-id="0fbd5-115">Det här kommandot får alla Redis-cache i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="0fbd5-115">This command gets every Redis Cache in the specified resource group.</span></span>

### <span data-ttu-id="0fbd5-116">Exempel 3: Hämta alla Redis-cachen i det aktuella abonnemanget</span><span class="sxs-lookup"><span data-stu-id="0fbd5-116">Example 3: Get every Redis Cache in the current subscription</span></span>
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
```

<span data-ttu-id="0fbd5-117">Det här kommandot får alla Redis-cachen i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="0fbd5-117">This command gets every Redis Cache in the current subscription.</span></span>

## <span data-ttu-id="0fbd5-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0fbd5-118">PARAMETERS</span></span>

### <span data-ttu-id="0fbd5-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="0fbd5-119">-Name</span></span>
<span data-ttu-id="0fbd5-120">Anger namnet på den Redis-cache som ska visas.</span><span class="sxs-lookup"><span data-stu-id="0fbd5-120">Specifies the name of the Redis Cache to get.</span></span>
<span data-ttu-id="0fbd5-121">Använd med parametern *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="0fbd5-121">Use with the *ResourceGroupName* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Specific Redis Cache
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fbd5-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fbd5-122">-ResourceGroupName</span></span>
<span data-ttu-id="0fbd5-123">Anger namnet på den resurs grupp som innehåller det Redis-cacheminne som ska visas.</span><span class="sxs-lookup"><span data-stu-id="0fbd5-123">Specifies the name of the resource group that contains the Redis Cache to get.</span></span>

<span data-ttu-id="0fbd5-124">Om du bara anger parametern *ResourceGroupName* får den här åtgärden alla Redis-cachen i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="0fbd5-124">If you specify only the *ResourceGroupName* parameter, this operation gets every Redis Cache in the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: All In Resource Group, Specific Redis Cache
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fbd5-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fbd5-125">-DefaultProfile</span></span>
<span data-ttu-id="0fbd5-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0fbd5-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0fbd5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fbd5-127">CommonParameters</span></span>
<span data-ttu-id="0fbd5-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fbd5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fbd5-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0fbd5-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fbd5-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0fbd5-130">INPUTS</span></span>

### <span data-ttu-id="0fbd5-131">Ingen</span><span class="sxs-lookup"><span data-stu-id="0fbd5-131">None</span></span>
<span data-ttu-id="0fbd5-132">Du kan pipes in i denna cmdlet efter namn men inte efter värde.</span><span class="sxs-lookup"><span data-stu-id="0fbd5-132">You can pipe input to this cmdlet by name, but not by value.</span></span>

## <span data-ttu-id="0fbd5-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0fbd5-133">OUTPUTS</span></span>

### <span data-ttu-id="0fbd5-134">Microsoft. Azure. commands. RedisCache. Models. RedisCacheAttributes</span><span class="sxs-lookup"><span data-stu-id="0fbd5-134">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span></span>
<span data-ttu-id="0fbd5-135">Returnerar en matris med **RedisCacheAttributes** -objekt.</span><span class="sxs-lookup"><span data-stu-id="0fbd5-135">Returns an array of **RedisCacheAttributes** objects.</span></span>

## <span data-ttu-id="0fbd5-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0fbd5-136">NOTES</span></span>

## <span data-ttu-id="0fbd5-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0fbd5-137">RELATED LINKS</span></span>

[<span data-ttu-id="0fbd5-138">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="0fbd5-138">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="0fbd5-139">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="0fbd5-139">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="0fbd5-140">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="0fbd5-140">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)



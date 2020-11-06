---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: A73D4DDD-387A-4468-AC6E-F15BF473527E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/reset-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Reset-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Reset-AzureRmRedisCache.md
ms.openlocfilehash: 8aad14bde950a5e98d8d9331428a62e957cb0afe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584004"
---
# <span data-ttu-id="9d1d8-101">Reset-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="9d1d8-101">Reset-AzureRmRedisCache</span></span>

## <span data-ttu-id="9d1d8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9d1d8-102">SYNOPSIS</span></span>
<span data-ttu-id="9d1d8-103">Startar om noder i ett cacheminne.</span><span class="sxs-lookup"><span data-stu-id="9d1d8-103">Restarts nodes of a cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d1d8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9d1d8-104">SYNTAX</span></span>

```
Reset-AzureRmRedisCache [-ResourceGroupName <String>] -Name <String> -RebootType <String> [-ShardId <Int32>]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d1d8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9d1d8-105">DESCRIPTION</span></span>
<span data-ttu-id="9d1d8-106">Cmdleten **Reset-AzureRmRedisCache** startar om noder för en Azure Redis-cachepost.</span><span class="sxs-lookup"><span data-stu-id="9d1d8-106">The **Reset-AzureRmRedisCache** cmdlet restarts nodes of an Azure Redis Cache instance.</span></span>

## <span data-ttu-id="9d1d8-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9d1d8-107">EXAMPLES</span></span>

### <span data-ttu-id="9d1d8-108">Exempel 1: starta om båda noderna</span><span class="sxs-lookup"><span data-stu-id="9d1d8-108">Example 1: Restart both nodes</span></span>
```
PS C:\>Reset-AzureRmRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -RebootType "AllNodes" -Force
```

<span data-ttu-id="9d1d8-109">Med det här kommandot startas båda noderna för cacheminnet som heter RedisCache06.</span><span class="sxs-lookup"><span data-stu-id="9d1d8-109">This command restarts both nodes for the cache named RedisCache06.</span></span>

## <span data-ttu-id="9d1d8-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9d1d8-110">PARAMETERS</span></span>

### <span data-ttu-id="9d1d8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d1d8-111">-DefaultProfile</span></span>
<span data-ttu-id="9d1d8-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9d1d8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d1d8-113">-Force</span><span class="sxs-lookup"><span data-stu-id="9d1d8-113">-Force</span></span>
<span data-ttu-id="9d1d8-114">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="9d1d8-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9d1d8-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="9d1d8-115">-Name</span></span>
<span data-ttu-id="9d1d8-116">Anger namnet på en cache.</span><span class="sxs-lookup"><span data-stu-id="9d1d8-116">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="9d1d8-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9d1d8-117">-PassThru</span></span>
<span data-ttu-id="9d1d8-118">Anger att denna cmdlet returnerar ett booleskt värde som anger om åtgärden lyckades.</span><span class="sxs-lookup"><span data-stu-id="9d1d8-118">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="9d1d8-119">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="9d1d8-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9d1d8-120">-RebootType</span><span class="sxs-lookup"><span data-stu-id="9d1d8-120">-RebootType</span></span>
<span data-ttu-id="9d1d8-121">Anger vilken nod eller vilka noder som ska startas om.</span><span class="sxs-lookup"><span data-stu-id="9d1d8-121">Specifies which node or nodes to restart.</span></span>
<span data-ttu-id="9d1d8-122">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="9d1d8-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9d1d8-123">PrimaryNode</span><span class="sxs-lookup"><span data-stu-id="9d1d8-123">PrimaryNode</span></span> 
- <span data-ttu-id="9d1d8-124">SecondaryNode</span><span class="sxs-lookup"><span data-stu-id="9d1d8-124">SecondaryNode</span></span> 
- <span data-ttu-id="9d1d8-125">AllNodes</span><span class="sxs-lookup"><span data-stu-id="9d1d8-125">AllNodes</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryNode, SecondaryNode, AllNodes

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d1d8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d1d8-126">-ResourceGroupName</span></span>
<span data-ttu-id="9d1d8-127">Anger namnet på den resurs grupp som innehåller cacheminnet.</span><span class="sxs-lookup"><span data-stu-id="9d1d8-127">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="9d1d8-128">-ShardId</span><span class="sxs-lookup"><span data-stu-id="9d1d8-128">-ShardId</span></span>
<span data-ttu-id="9d1d8-129">Anger ID för den Shard som denna cmdlet startar om för en Premium-cache med kluster aktiverat.</span><span class="sxs-lookup"><span data-stu-id="9d1d8-129">Specifies the ID of the shard that this cmdlet restarts for a premium cache with clustering enabled.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d1d8-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9d1d8-130">-Confirm</span></span>
<span data-ttu-id="9d1d8-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9d1d8-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d1d8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d1d8-132">-WhatIf</span></span>
<span data-ttu-id="9d1d8-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9d1d8-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d1d8-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9d1d8-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d1d8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d1d8-135">CommonParameters</span></span>
<span data-ttu-id="9d1d8-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d1d8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d1d8-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d1d8-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d1d8-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9d1d8-138">INPUTS</span></span>

### <span data-ttu-id="9d1d8-139">System. String</span><span class="sxs-lookup"><span data-stu-id="9d1d8-139">System.String</span></span>

### <span data-ttu-id="9d1d8-140">System. Nullable ' 1 [[system. Int32, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="9d1d8-140">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="9d1d8-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9d1d8-141">OUTPUTS</span></span>

### <span data-ttu-id="9d1d8-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9d1d8-142">System.Boolean</span></span>

## <span data-ttu-id="9d1d8-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9d1d8-143">NOTES</span></span>
* <span data-ttu-id="9d1d8-144">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, Redis, cache, Web, webapp, webbplats</span><span class="sxs-lookup"><span data-stu-id="9d1d8-144">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="9d1d8-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9d1d8-145">RELATED LINKS</span></span>

[<span data-ttu-id="9d1d8-146">Exportera-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="9d1d8-146">Export-AzureRmRedisCache</span></span>](./Export-AzureRmRedisCache.md)

[<span data-ttu-id="9d1d8-147">Import-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="9d1d8-147">Import-AzureRmRedisCache</span></span>](./Import-AzureRmRedisCache.md)

[<span data-ttu-id="9d1d8-148">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="9d1d8-148">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="9d1d8-149">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="9d1d8-149">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="9d1d8-150">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="9d1d8-150">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)



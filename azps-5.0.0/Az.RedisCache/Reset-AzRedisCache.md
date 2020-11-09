---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: A73D4DDD-387A-4468-AC6E-F15BF473527E
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/reset-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Reset-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Reset-AzRedisCache.md
ms.openlocfilehash: c2373bb4ef093a35abc12b14f55f4c977fc54d64
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324504"
---
# <span data-ttu-id="96da0-101">Reset-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="96da0-101">Reset-AzRedisCache</span></span>

## <span data-ttu-id="96da0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="96da0-102">SYNOPSIS</span></span>
<span data-ttu-id="96da0-103">Startar om noder i ett cacheminne.</span><span class="sxs-lookup"><span data-stu-id="96da0-103">Restarts nodes of a cache.</span></span>

## <span data-ttu-id="96da0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="96da0-104">SYNTAX</span></span>

```
Reset-AzRedisCache [-ResourceGroupName <String>] -Name <String> -RebootType <String> [-ShardId <Int32>]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96da0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="96da0-105">DESCRIPTION</span></span>
<span data-ttu-id="96da0-106">Cmdleten **Reset-AzRedisCache** startar om noder för en Azure Redis-cachepost.</span><span class="sxs-lookup"><span data-stu-id="96da0-106">The **Reset-AzRedisCache** cmdlet restarts nodes of an Azure Redis Cache instance.</span></span>

## <span data-ttu-id="96da0-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="96da0-107">EXAMPLES</span></span>

### <span data-ttu-id="96da0-108">Exempel 1: starta om båda noderna</span><span class="sxs-lookup"><span data-stu-id="96da0-108">Example 1: Restart both nodes</span></span>
```
PS C:\>Reset-AzRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -RebootType "AllNodes" -Force
```

<span data-ttu-id="96da0-109">Med det här kommandot startas båda noderna för cacheminnet som heter RedisCache06.</span><span class="sxs-lookup"><span data-stu-id="96da0-109">This command restarts both nodes for the cache named RedisCache06.</span></span>

## <span data-ttu-id="96da0-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="96da0-110">PARAMETERS</span></span>

### <span data-ttu-id="96da0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96da0-111">-DefaultProfile</span></span>
<span data-ttu-id="96da0-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="96da0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96da0-113">-Force</span><span class="sxs-lookup"><span data-stu-id="96da0-113">-Force</span></span>
<span data-ttu-id="96da0-114">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="96da0-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="96da0-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="96da0-115">-Name</span></span>
<span data-ttu-id="96da0-116">Anger namnet på en cache.</span><span class="sxs-lookup"><span data-stu-id="96da0-116">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="96da0-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="96da0-117">-PassThru</span></span>
<span data-ttu-id="96da0-118">Anger att denna cmdlet returnerar ett booleskt värde som anger om åtgärden lyckades.</span><span class="sxs-lookup"><span data-stu-id="96da0-118">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="96da0-119">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="96da0-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="96da0-120">-RebootType</span><span class="sxs-lookup"><span data-stu-id="96da0-120">-RebootType</span></span>
<span data-ttu-id="96da0-121">Anger vilken nod eller vilka noder som ska startas om.</span><span class="sxs-lookup"><span data-stu-id="96da0-121">Specifies which node or nodes to restart.</span></span>
<span data-ttu-id="96da0-122">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="96da0-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="96da0-123">PrimaryNode</span><span class="sxs-lookup"><span data-stu-id="96da0-123">PrimaryNode</span></span> 
- <span data-ttu-id="96da0-124">SecondaryNode</span><span class="sxs-lookup"><span data-stu-id="96da0-124">SecondaryNode</span></span> 
- <span data-ttu-id="96da0-125">AllNodes</span><span class="sxs-lookup"><span data-stu-id="96da0-125">AllNodes</span></span>

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

### <span data-ttu-id="96da0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96da0-126">-ResourceGroupName</span></span>
<span data-ttu-id="96da0-127">Anger namnet på den resurs grupp som innehåller cacheminnet.</span><span class="sxs-lookup"><span data-stu-id="96da0-127">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="96da0-128">-ShardId</span><span class="sxs-lookup"><span data-stu-id="96da0-128">-ShardId</span></span>
<span data-ttu-id="96da0-129">Anger ID för den Shard som denna cmdlet startar om för en Premium-cache med kluster aktiverat.</span><span class="sxs-lookup"><span data-stu-id="96da0-129">Specifies the ID of the shard that this cmdlet restarts for a premium cache with clustering enabled.</span></span>

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

### <span data-ttu-id="96da0-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="96da0-130">-Confirm</span></span>
<span data-ttu-id="96da0-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="96da0-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96da0-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96da0-132">-WhatIf</span></span>
<span data-ttu-id="96da0-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="96da0-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96da0-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="96da0-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96da0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96da0-135">CommonParameters</span></span>
<span data-ttu-id="96da0-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96da0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96da0-137">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96da0-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96da0-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="96da0-138">INPUTS</span></span>

### <span data-ttu-id="96da0-139">System. String</span><span class="sxs-lookup"><span data-stu-id="96da0-139">System.String</span></span>

### <span data-ttu-id="96da0-140">System. Nullable ' 1 [[system. Int32, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="96da0-140">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="96da0-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="96da0-141">OUTPUTS</span></span>

### <span data-ttu-id="96da0-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="96da0-142">System.Boolean</span></span>

## <span data-ttu-id="96da0-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="96da0-143">NOTES</span></span>
* <span data-ttu-id="96da0-144">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, Redis, cache, Web, webapp, webbplats</span><span class="sxs-lookup"><span data-stu-id="96da0-144">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="96da0-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="96da0-145">RELATED LINKS</span></span>

[<span data-ttu-id="96da0-146">Exportera-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="96da0-146">Export-AzRedisCache</span></span>](./Export-AzRedisCache.md)

[<span data-ttu-id="96da0-147">Import-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="96da0-147">Import-AzRedisCache</span></span>](./Import-AzRedisCache.md)

[<span data-ttu-id="96da0-148">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="96da0-148">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="96da0-149">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="96da0-149">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="96da0-150">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="96da0-150">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)



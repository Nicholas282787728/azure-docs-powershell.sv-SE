---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: A73D4DDD-387A-4468-AC6E-F15BF473527E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Reset-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Reset-AzureRmRedisCache.md
ms.openlocfilehash: 2b352c649d01e2fceb42f99a6c4dad20859a2adc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755646"
---
# <span data-ttu-id="23237-101">Reset-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="23237-101">Reset-AzureRmRedisCache</span></span>

## <span data-ttu-id="23237-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="23237-102">SYNOPSIS</span></span>
<span data-ttu-id="23237-103">Startar om noder i ett cacheminne.</span><span class="sxs-lookup"><span data-stu-id="23237-103">Restarts nodes of a cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23237-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="23237-104">SYNTAX</span></span>

```
Reset-AzureRmRedisCache -ResourceGroupName <String> -Name <String> -RebootType <String> [-ShardId <Int32>]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23237-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="23237-105">DESCRIPTION</span></span>
<span data-ttu-id="23237-106">Cmdleten **Reset-AzureRmRedisCache** startar om noder för en Azure Redis-cachepost.</span><span class="sxs-lookup"><span data-stu-id="23237-106">The **Reset-AzureRmRedisCache** cmdlet restarts nodes of an Azure Redis Cache instance.</span></span>

## <span data-ttu-id="23237-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="23237-107">EXAMPLES</span></span>

### <span data-ttu-id="23237-108">Exempel 1: starta om båda noderna</span><span class="sxs-lookup"><span data-stu-id="23237-108">Example 1: Restart both nodes</span></span>
```
PS C:\>Reset-AzureRmRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -RebootType "AllNodes" -Force
```

<span data-ttu-id="23237-109">Med det här kommandot startas båda noderna för cacheminnet som heter RedisCache06.</span><span class="sxs-lookup"><span data-stu-id="23237-109">This command restarts both nodes for the cache named RedisCache06.</span></span>

## <span data-ttu-id="23237-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="23237-110">PARAMETERS</span></span>

### <span data-ttu-id="23237-111">-Force</span><span class="sxs-lookup"><span data-stu-id="23237-111">-Force</span></span>
<span data-ttu-id="23237-112">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="23237-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="23237-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="23237-113">-Name</span></span>
<span data-ttu-id="23237-114">Anger namnet på en cache.</span><span class="sxs-lookup"><span data-stu-id="23237-114">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="23237-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="23237-115">-PassThru</span></span>
<span data-ttu-id="23237-116">Anger att denna cmdlet returnerar ett booleskt värde som anger om åtgärden lyckades.</span><span class="sxs-lookup"><span data-stu-id="23237-116">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="23237-117">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="23237-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="23237-118">-RebootType</span><span class="sxs-lookup"><span data-stu-id="23237-118">-RebootType</span></span>
<span data-ttu-id="23237-119">Anger vilken nod eller vilka noder som ska startas om.</span><span class="sxs-lookup"><span data-stu-id="23237-119">Specifies which node or nodes to restart.</span></span>
<span data-ttu-id="23237-120">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="23237-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="23237-121">PrimaryNode</span><span class="sxs-lookup"><span data-stu-id="23237-121">PrimaryNode</span></span> 
- <span data-ttu-id="23237-122">SecondaryNode</span><span class="sxs-lookup"><span data-stu-id="23237-122">SecondaryNode</span></span> 
- <span data-ttu-id="23237-123">AllNodes</span><span class="sxs-lookup"><span data-stu-id="23237-123">AllNodes</span></span>

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

### <span data-ttu-id="23237-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23237-124">-ResourceGroupName</span></span>
<span data-ttu-id="23237-125">Anger namnet på den resurs grupp som innehåller cacheminnet.</span><span class="sxs-lookup"><span data-stu-id="23237-125">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="23237-126">-ShardId</span><span class="sxs-lookup"><span data-stu-id="23237-126">-ShardId</span></span>
<span data-ttu-id="23237-127">Anger ID för den Shard som denna cmdlet startar om för en Premium-cache med kluster aktiverat.</span><span class="sxs-lookup"><span data-stu-id="23237-127">Specifies the ID of the shard that this cmdlet restarts for a premium cache with clustering enabled.</span></span>

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

### <span data-ttu-id="23237-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="23237-128">-Confirm</span></span>
<span data-ttu-id="23237-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="23237-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23237-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23237-130">-WhatIf</span></span>
<span data-ttu-id="23237-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="23237-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23237-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="23237-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23237-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23237-133">-DefaultProfile</span></span>
<span data-ttu-id="23237-134">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="23237-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23237-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23237-135">CommonParameters</span></span>
<span data-ttu-id="23237-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23237-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23237-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23237-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23237-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="23237-138">INPUTS</span></span>

### <span data-ttu-id="23237-139">Ingen</span><span class="sxs-lookup"><span data-stu-id="23237-139">None</span></span>
<span data-ttu-id="23237-140">Du kan ange indata för denna cmdlet efter egenskaps namn, men inte efter värde.</span><span class="sxs-lookup"><span data-stu-id="23237-140">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="23237-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="23237-141">OUTPUTS</span></span>

### <span data-ttu-id="23237-142">Ingen</span><span class="sxs-lookup"><span data-stu-id="23237-142">None</span></span>

## <span data-ttu-id="23237-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="23237-143">NOTES</span></span>
* <span data-ttu-id="23237-144">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, Redis, cache, Web, webapp, webbplats</span><span class="sxs-lookup"><span data-stu-id="23237-144">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="23237-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="23237-145">RELATED LINKS</span></span>

[<span data-ttu-id="23237-146">Exportera-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="23237-146">Export-AzureRmRedisCache</span></span>](./Export-AzureRmRedisCache.md)

[<span data-ttu-id="23237-147">Import-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="23237-147">Import-AzureRmRedisCache</span></span>](./Import-AzureRmRedisCache.md)

[<span data-ttu-id="23237-148">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="23237-148">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="23237-149">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="23237-149">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="23237-150">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="23237-150">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)



---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/remove-azurermrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCacheLink.md
ms.openlocfilehash: e4c45095dba8ec72e00fa26eee2d8a3fb6f029fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757354"
---
# <span data-ttu-id="3af11-101">Remove-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="3af11-101">Remove-AzureRmRedisCacheLink</span></span>

## <span data-ttu-id="3af11-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3af11-102">SYNOPSIS</span></span>
<span data-ttu-id="3af11-103">Ta bort en geo-replikeringslänk mellan två Redis cacheminnen.</span><span class="sxs-lookup"><span data-stu-id="3af11-103">Remove a geo replication link between two Redis Caches.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3af11-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3af11-104">SYNTAX</span></span>

```
Remove-AzureRmRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3af11-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3af11-105">DESCRIPTION</span></span>
<span data-ttu-id="3af11-106">Ta bort en geo-replikeringslänk mellan två Redis cacheminnen.</span><span class="sxs-lookup"><span data-stu-id="3af11-106">Remove a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="3af11-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3af11-107">EXAMPLES</span></span>

### <span data-ttu-id="3af11-108">Exempel 1: ta bort en geo-replikeringslänk</span><span class="sxs-lookup"><span data-stu-id="3af11-108">Example 1: Remove a geo replication link</span></span>
```
PS C:\>Remove-AzureRmRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"
```

<span data-ttu-id="3af11-109">Det här kommandot tar bort en geo-replikeringslänk där Redis cache-namnet mycache1 är primärt och Redis cache med namnet mycache2 är sekundärt.</span><span class="sxs-lookup"><span data-stu-id="3af11-109">This command removes a geo-replication links where Redis Cache named mycache1 is primary and Redis Cache named mycache2 is secondary.</span></span>

## <span data-ttu-id="3af11-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3af11-110">PARAMETERS</span></span>

### <span data-ttu-id="3af11-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3af11-111">-DefaultProfile</span></span>
<span data-ttu-id="3af11-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3af11-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3af11-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3af11-113">-PassThru</span></span>
<span data-ttu-id="3af11-114">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="3af11-114">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="3af11-115">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="3af11-115">-PrimaryServerName</span></span>
<span data-ttu-id="3af11-116">Namn på primär Redis cache i länken.</span><span class="sxs-lookup"><span data-stu-id="3af11-116">Name of primary redis cache in link.</span></span>

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

### <span data-ttu-id="3af11-117">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="3af11-117">-SecondaryServerName</span></span>
<span data-ttu-id="3af11-118">Namnet på den sekundära Redis-cachen i länken.</span><span class="sxs-lookup"><span data-stu-id="3af11-118">Name of secondary redis cache in link.</span></span>

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

### <span data-ttu-id="3af11-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3af11-119">-Confirm</span></span>
<span data-ttu-id="3af11-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3af11-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3af11-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3af11-121">-WhatIf</span></span>
<span data-ttu-id="3af11-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3af11-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3af11-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3af11-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3af11-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3af11-124">CommonParameters</span></span>
<span data-ttu-id="3af11-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3af11-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3af11-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3af11-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3af11-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3af11-127">INPUTS</span></span>

### <span data-ttu-id="3af11-128">System. String</span><span class="sxs-lookup"><span data-stu-id="3af11-128">System.String</span></span>

## <span data-ttu-id="3af11-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3af11-129">OUTPUTS</span></span>

### <span data-ttu-id="3af11-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3af11-130">System.Boolean</span></span>

## <span data-ttu-id="3af11-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3af11-131">NOTES</span></span>

## <span data-ttu-id="3af11-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3af11-132">RELATED LINKS</span></span>

[<span data-ttu-id="3af11-133">New-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="3af11-133">New-AzureRmRedisCacheLink</span></span>](./New-AzureRmRedisCacheLink.md)

[<span data-ttu-id="3af11-134">Get-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="3af11-134">Get-AzureRmRedisCacheLink</span></span>](./Get-AzureRmRedisCacheLink.md)

[<span data-ttu-id="3af11-135">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="3af11-135">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="3af11-136">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="3af11-136">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="3af11-137">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="3af11-137">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="3af11-138">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="3af11-138">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)

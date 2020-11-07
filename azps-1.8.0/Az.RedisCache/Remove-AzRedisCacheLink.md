---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheLink.md
ms.openlocfilehash: e4f4dd72104b4a57823c54e6cf56f531f48e610d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747258"
---
# <span data-ttu-id="d387c-101">Remove-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="d387c-101">Remove-AzRedisCacheLink</span></span>

## <span data-ttu-id="d387c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d387c-102">SYNOPSIS</span></span>
<span data-ttu-id="d387c-103">Ta bort en geo-replikeringslänk mellan två Redis cacheminnen.</span><span class="sxs-lookup"><span data-stu-id="d387c-103">Remove a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="d387c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d387c-104">SYNTAX</span></span>

```
Remove-AzRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d387c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d387c-105">DESCRIPTION</span></span>
<span data-ttu-id="d387c-106">Ta bort en geo-replikeringslänk mellan två Redis cacheminnen.</span><span class="sxs-lookup"><span data-stu-id="d387c-106">Remove a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="d387c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d387c-107">EXAMPLES</span></span>

### <span data-ttu-id="d387c-108">Exempel 1: ta bort en geo-replikeringslänk</span><span class="sxs-lookup"><span data-stu-id="d387c-108">Example 1: Remove a geo replication link</span></span>
```
PS C:\>Remove-AzRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"
```

<span data-ttu-id="d387c-109">Det här kommandot tar bort en geo-replikeringslänk där Redis cache-namnet mycache1 är primärt och Redis cache med namnet mycache2 är sekundärt.</span><span class="sxs-lookup"><span data-stu-id="d387c-109">This command removes a geo-replication links where Redis Cache named mycache1 is primary and Redis Cache named mycache2 is secondary.</span></span>

## <span data-ttu-id="d387c-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d387c-110">PARAMETERS</span></span>

### <span data-ttu-id="d387c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d387c-111">-DefaultProfile</span></span>
<span data-ttu-id="d387c-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d387c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d387c-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d387c-113">-PassThru</span></span>
<span data-ttu-id="d387c-114">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="d387c-114">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="d387c-115">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="d387c-115">-PrimaryServerName</span></span>
<span data-ttu-id="d387c-116">Namn på primär Redis cache i länken.</span><span class="sxs-lookup"><span data-stu-id="d387c-116">Name of primary redis cache in link.</span></span>

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

### <span data-ttu-id="d387c-117">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="d387c-117">-SecondaryServerName</span></span>
<span data-ttu-id="d387c-118">Namnet på den sekundära Redis-cachen i länken.</span><span class="sxs-lookup"><span data-stu-id="d387c-118">Name of secondary redis cache in link.</span></span>

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

### <span data-ttu-id="d387c-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d387c-119">-Confirm</span></span>
<span data-ttu-id="d387c-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d387c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d387c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d387c-121">-WhatIf</span></span>
<span data-ttu-id="d387c-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d387c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d387c-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d387c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d387c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d387c-124">CommonParameters</span></span>
<span data-ttu-id="d387c-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d387c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d387c-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d387c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d387c-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d387c-127">INPUTS</span></span>

### <span data-ttu-id="d387c-128">System. String</span><span class="sxs-lookup"><span data-stu-id="d387c-128">System.String</span></span>

## <span data-ttu-id="d387c-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d387c-129">OUTPUTS</span></span>

### <span data-ttu-id="d387c-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d387c-130">System.Boolean</span></span>

## <span data-ttu-id="d387c-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d387c-131">NOTES</span></span>

## <span data-ttu-id="d387c-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d387c-132">RELATED LINKS</span></span>

[<span data-ttu-id="d387c-133">New-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="d387c-133">New-AzRedisCacheLink</span></span>](./New-AzRedisCacheLink.md)

[<span data-ttu-id="d387c-134">Get-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="d387c-134">Get-AzRedisCacheLink</span></span>](./Get-AzRedisCacheLink.md)

[<span data-ttu-id="d387c-135">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="d387c-135">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="d387c-136">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="d387c-136">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="d387c-137">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="d387c-137">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="d387c-138">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="d387c-138">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)
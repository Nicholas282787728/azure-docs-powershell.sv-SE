---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheLink.md
ms.openlocfilehash: 157490da6abeae7e947c22e88301d29043722a86
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920154"
---
# <span data-ttu-id="5a7a1-101">New-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="5a7a1-101">New-AzRedisCacheLink</span></span>

## <span data-ttu-id="5a7a1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5a7a1-102">SYNOPSIS</span></span>
<span data-ttu-id="5a7a1-103">Skapa en geo-replikeringslänk mellan två Redis cacheminnen.</span><span class="sxs-lookup"><span data-stu-id="5a7a1-103">Create a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="5a7a1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5a7a1-104">SYNTAX</span></span>

```
New-AzRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a7a1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5a7a1-105">DESCRIPTION</span></span>
<span data-ttu-id="5a7a1-106">Skapa en geo-replikeringslänk mellan två Redis cacheminnen.</span><span class="sxs-lookup"><span data-stu-id="5a7a1-106">Create a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="5a7a1-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5a7a1-107">EXAMPLES</span></span>

### <span data-ttu-id="5a7a1-108">Exempel 1: skapa en länk mellan två cacheminnen</span><span class="sxs-lookup"><span data-stu-id="5a7a1-108">Example 1: Create a link between two caches</span></span>
```
PS C:\>New-AzRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Creating
```

<span data-ttu-id="5a7a1-109">Det här kommandot skapar geo-replikeringslänk mellan Redis cache mycache1 och mycache2.</span><span class="sxs-lookup"><span data-stu-id="5a7a1-109">This command creates geo-replication link between Redis Cache mycache1 and mycache2.</span></span>

## <span data-ttu-id="5a7a1-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5a7a1-110">PARAMETERS</span></span>

### <span data-ttu-id="5a7a1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a7a1-111">-DefaultProfile</span></span>
<span data-ttu-id="5a7a1-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5a7a1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a7a1-113">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="5a7a1-113">-PrimaryServerName</span></span>
<span data-ttu-id="5a7a1-114">Namn på primär Redis cache i länken.</span><span class="sxs-lookup"><span data-stu-id="5a7a1-114">Name of primary redis cache in link.</span></span>

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

### <span data-ttu-id="5a7a1-115">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="5a7a1-115">-SecondaryServerName</span></span>
<span data-ttu-id="5a7a1-116">Namnet på den sekundära Redis-cachen i länken.</span><span class="sxs-lookup"><span data-stu-id="5a7a1-116">Name of secondary redis cache in link.</span></span>

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

### <span data-ttu-id="5a7a1-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5a7a1-117">-Confirm</span></span>
<span data-ttu-id="5a7a1-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5a7a1-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a7a1-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a7a1-119">-WhatIf</span></span>
<span data-ttu-id="5a7a1-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5a7a1-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a7a1-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5a7a1-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a7a1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a7a1-122">CommonParameters</span></span>
<span data-ttu-id="5a7a1-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a7a1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a7a1-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a7a1-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a7a1-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5a7a1-125">INPUTS</span></span>

### <span data-ttu-id="5a7a1-126">System. String</span><span class="sxs-lookup"><span data-stu-id="5a7a1-126">System.String</span></span>

## <span data-ttu-id="5a7a1-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5a7a1-127">OUTPUTS</span></span>

### <span data-ttu-id="5a7a1-128">Microsoft. Azure. commands. RedisCache. Models. PSRedisLinkedServer</span><span class="sxs-lookup"><span data-stu-id="5a7a1-128">Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer</span></span>

## <span data-ttu-id="5a7a1-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5a7a1-129">NOTES</span></span>

## <span data-ttu-id="5a7a1-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5a7a1-130">RELATED LINKS</span></span>

[<span data-ttu-id="5a7a1-131">Get-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="5a7a1-131">Get-AzRedisCacheLink</span></span>](./Get-AzRedisCacheLink.md)

[<span data-ttu-id="5a7a1-132">Remove-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="5a7a1-132">Remove-AzRedisCacheLink</span></span>](./Remove-AzRedisCacheLink.md)

[<span data-ttu-id="5a7a1-133">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="5a7a1-133">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="5a7a1-134">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="5a7a1-134">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="5a7a1-135">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="5a7a1-135">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="5a7a1-136">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="5a7a1-136">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)
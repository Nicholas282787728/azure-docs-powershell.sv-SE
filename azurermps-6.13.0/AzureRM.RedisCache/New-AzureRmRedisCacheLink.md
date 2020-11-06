---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/new-azurermrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheLink.md
ms.openlocfilehash: f625c9180287166b01607c468c44b5e0623c11cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572652"
---
# <span data-ttu-id="fb269-101">New-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="fb269-101">New-AzureRmRedisCacheLink</span></span>

## <span data-ttu-id="fb269-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fb269-102">SYNOPSIS</span></span>
<span data-ttu-id="fb269-103">Skapa en geo-replikeringslänk mellan två Redis cacheminnen.</span><span class="sxs-lookup"><span data-stu-id="fb269-103">Create a geo replication link between two Redis Caches.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb269-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fb269-104">SYNTAX</span></span>

```
New-AzureRmRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb269-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fb269-105">DESCRIPTION</span></span>
<span data-ttu-id="fb269-106">Skapa en geo-replikeringslänk mellan två Redis cacheminnen.</span><span class="sxs-lookup"><span data-stu-id="fb269-106">Create a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="fb269-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fb269-107">EXAMPLES</span></span>

### <span data-ttu-id="fb269-108">Exempel 1: skapa en länk mellan två cacheminnen</span><span class="sxs-lookup"><span data-stu-id="fb269-108">Example 1: Create a link between two caches</span></span>
```
PS C:\>New-AzureRmRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Creating
```

<span data-ttu-id="fb269-109">Det här kommandot skapar geo-replikeringslänk mellan Redis cache mycache1 och mycache2.</span><span class="sxs-lookup"><span data-stu-id="fb269-109">This command creates geo-replication link between Redis Cache mycache1 and mycache2.</span></span>

## <span data-ttu-id="fb269-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fb269-110">PARAMETERS</span></span>

### <span data-ttu-id="fb269-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb269-111">-DefaultProfile</span></span>
<span data-ttu-id="fb269-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fb269-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb269-113">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="fb269-113">-PrimaryServerName</span></span>
<span data-ttu-id="fb269-114">Namn på primär Redis cache i länken.</span><span class="sxs-lookup"><span data-stu-id="fb269-114">Name of primary redis cache in link.</span></span>

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

### <span data-ttu-id="fb269-115">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="fb269-115">-SecondaryServerName</span></span>
<span data-ttu-id="fb269-116">Namnet på den sekundära Redis-cachen i länken.</span><span class="sxs-lookup"><span data-stu-id="fb269-116">Name of secondary redis cache in link.</span></span>

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

### <span data-ttu-id="fb269-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fb269-117">-Confirm</span></span>
<span data-ttu-id="fb269-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fb269-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb269-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb269-119">-WhatIf</span></span>
<span data-ttu-id="fb269-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fb269-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb269-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fb269-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb269-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb269-122">CommonParameters</span></span>
<span data-ttu-id="fb269-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb269-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb269-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb269-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb269-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fb269-125">INPUTS</span></span>

### <span data-ttu-id="fb269-126">System. String</span><span class="sxs-lookup"><span data-stu-id="fb269-126">System.String</span></span>

## <span data-ttu-id="fb269-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fb269-127">OUTPUTS</span></span>

### <span data-ttu-id="fb269-128">Microsoft. Azure. commands. RedisCache. Models. PSRedisLinkedServer</span><span class="sxs-lookup"><span data-stu-id="fb269-128">Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer</span></span>

## <span data-ttu-id="fb269-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fb269-129">NOTES</span></span>

## <span data-ttu-id="fb269-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fb269-130">RELATED LINKS</span></span>

[<span data-ttu-id="fb269-131">Get-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="fb269-131">Get-AzureRmRedisCacheLink</span></span>](./Get-AzureRmRedisCacheLink.md)

[<span data-ttu-id="fb269-132">Remove-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="fb269-132">Remove-AzureRmRedisCacheLink</span></span>](./Remove-AzureRmRedisCacheLink.md)

[<span data-ttu-id="fb269-133">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="fb269-133">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="fb269-134">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="fb269-134">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="fb269-135">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="fb269-135">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="fb269-136">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="fb269-136">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)

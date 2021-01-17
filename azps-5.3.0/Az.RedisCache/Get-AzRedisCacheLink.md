---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheLink.md
ms.openlocfilehash: 58c52e30270af309eb5104bbc0a9308f83df91ea
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98421208"
---
# <span data-ttu-id="45a3f-101">Get-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="45a3f-101">Get-AzRedisCacheLink</span></span>

## <span data-ttu-id="45a3f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="45a3f-102">SYNOPSIS</span></span>
<span data-ttu-id="45a3f-103">Länken Hämta geo-replikering för Redis cache.</span><span class="sxs-lookup"><span data-stu-id="45a3f-103">Get geo replication link for Redis Cache.</span></span>

## <span data-ttu-id="45a3f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="45a3f-104">SYNTAX</span></span>

### <span data-ttu-id="45a3f-105">AllLinksForCache (standard)</span><span class="sxs-lookup"><span data-stu-id="45a3f-105">AllLinksForCache (Default)</span></span>
```
Get-AzRedisCacheLink -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45a3f-106">AllLinksForPrimaryCache</span><span class="sxs-lookup"><span data-stu-id="45a3f-106">AllLinksForPrimaryCache</span></span>
```
Get-AzRedisCacheLink -PrimaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="45a3f-107">SingleLink</span><span class="sxs-lookup"><span data-stu-id="45a3f-107">SingleLink</span></span>
```
Get-AzRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45a3f-108">AllLinksForSecondaryCache</span><span class="sxs-lookup"><span data-stu-id="45a3f-108">AllLinksForSecondaryCache</span></span>
```
Get-AzRedisCacheLink -SecondaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="45a3f-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="45a3f-109">DESCRIPTION</span></span>
<span data-ttu-id="45a3f-110">Det finns fyra olika sätt att få till gång till geo-Replication.</span><span class="sxs-lookup"><span data-stu-id="45a3f-110">There are four different ways to get geo-replication link detail.</span></span> <span data-ttu-id="45a3f-111">Ange antingen parameter namn eller PrimaryServerName och/eller SecondaryServerName.</span><span class="sxs-lookup"><span data-stu-id="45a3f-111">Either provide parameter Name or PrimaryServerName and/or SecondaryServerName.</span></span> <span data-ttu-id="45a3f-112">Namnet ges och alla länkar där cache finns returneras.</span><span class="sxs-lookup"><span data-stu-id="45a3f-112">Name is given then all link where cache exists will be returned.</span></span> <span data-ttu-id="45a3f-113">Om endast PrimaryServerName ges returneras alla länkar där cache är primärt.</span><span class="sxs-lookup"><span data-stu-id="45a3f-113">If only PrimaryServerName is given then all links where cache is primary will be returned.</span></span> <span data-ttu-id="45a3f-114">Om endast SecondaryServerName ges returneras alla länkar där cache är sekundärt.</span><span class="sxs-lookup"><span data-stu-id="45a3f-114">If only SecondaryServerName is given then all links where cache is secondary will be returned.</span></span> <span data-ttu-id="45a3f-115">Om PrimaryServerName och SecondaryServerName båda anges returneras specifik länk med rätt roll.</span><span class="sxs-lookup"><span data-stu-id="45a3f-115">If PrimaryServerName and SecondaryServerName both are given then specific link with correct role will be returned.</span></span> 

## <span data-ttu-id="45a3f-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="45a3f-116">EXAMPLES</span></span>

### <span data-ttu-id="45a3f-117">Exempel 1: använda parameter uppsättning AllLinksForCache</span><span class="sxs-lookup"><span data-stu-id="45a3f-117">Example 1: Get using parameter set AllLinksForCache</span></span>
```
PS C:\>Get-AzRedisCacheLink -Name "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="45a3f-118">Det här kommandot får alla geo-replikeringslänk för Redis cache som heter mycache1.</span><span class="sxs-lookup"><span data-stu-id="45a3f-118">This command gets all geo-replication links for Redis Cache named mycache1.</span></span>

### <span data-ttu-id="45a3f-119">Exempel 2: använda parameter uppsättning AllLinksForPrimaryCache</span><span class="sxs-lookup"><span data-stu-id="45a3f-119">Example 2: Get using parameter set AllLinksForPrimaryCache</span></span>
```
PS C:\>Get-AzRedisCacheLink -PrimaryServerName "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="45a3f-120">Det här kommandot får geo-replikeringslänken-länkar där Redis cache-namnet mycache1 är primärt.</span><span class="sxs-lookup"><span data-stu-id="45a3f-120">This command gets geo-replication links where Redis Cache named mycache1 is primary.</span></span>

### <span data-ttu-id="45a3f-121">Exempel 3: använda parameter uppsättning AllLinksForSecondaryCache</span><span class="sxs-lookup"><span data-stu-id="45a3f-121">Example 3: Get using parameter set AllLinksForSecondaryCache</span></span>
```
PS C:\>Get-AzRedisCacheLink -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="45a3f-122">Det här kommandot får geo-replikeringslänken-länkar där Redis cache med namnet mycache2 är sekundärt.</span><span class="sxs-lookup"><span data-stu-id="45a3f-122">This command gets geo-replication links where Redis Cache named mycache2 is secondary.</span></span>

### <span data-ttu-id="45a3f-123">Exempel 4: använda parameter uppsättning SingleLink</span><span class="sxs-lookup"><span data-stu-id="45a3f-123">Example 4: Get using parameter set SingleLink</span></span>
```
PS C:\>Get-AzRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="45a3f-124">Det här kommandot får du en enda geo-replikeringslänk där Redis cache med namnet mycache1 är primär och Redis cache med namnet mycache2 är sekundär.</span><span class="sxs-lookup"><span data-stu-id="45a3f-124">This command gets a single geo-replication links where Redis Cache named mycache1 is primary and Redis Cache named mycache2 is secondary.</span></span>

## <span data-ttu-id="45a3f-125">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="45a3f-125">PARAMETERS</span></span>

### <span data-ttu-id="45a3f-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45a3f-126">-DefaultProfile</span></span>
<span data-ttu-id="45a3f-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="45a3f-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45a3f-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="45a3f-128">-Name</span></span>
<span data-ttu-id="45a3f-129">Namn på Redis cache.</span><span class="sxs-lookup"><span data-stu-id="45a3f-129">Name of redis cache.</span></span>

```yaml
Type: System.String
Parameter Sets: AllLinksForCache
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45a3f-130">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="45a3f-130">-PrimaryServerName</span></span>
<span data-ttu-id="45a3f-131">Namn på primär Redis cache i länken.</span><span class="sxs-lookup"><span data-stu-id="45a3f-131">Name of primary redis cache in link.</span></span>

```yaml
Type: System.String
Parameter Sets: AllLinksForPrimaryCache, SingleLink
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45a3f-132">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="45a3f-132">-SecondaryServerName</span></span>
<span data-ttu-id="45a3f-133">Namnet på den sekundära Redis-cachen i länken.</span><span class="sxs-lookup"><span data-stu-id="45a3f-133">Name of secondary redis cache in link.</span></span>

```yaml
Type: System.String
Parameter Sets: SingleLink, AllLinksForSecondaryCache
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45a3f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45a3f-134">CommonParameters</span></span>
<span data-ttu-id="45a3f-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45a3f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45a3f-136">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45a3f-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45a3f-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="45a3f-137">INPUTS</span></span>

### <span data-ttu-id="45a3f-138">System. String</span><span class="sxs-lookup"><span data-stu-id="45a3f-138">System.String</span></span>

## <span data-ttu-id="45a3f-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="45a3f-139">OUTPUTS</span></span>

### <span data-ttu-id="45a3f-140">Microsoft. Azure. commands. RedisCache. Models. PSRedisLinkedServer</span><span class="sxs-lookup"><span data-stu-id="45a3f-140">Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer</span></span>

## <span data-ttu-id="45a3f-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="45a3f-141">NOTES</span></span>

## <span data-ttu-id="45a3f-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="45a3f-142">RELATED LINKS</span></span>

[<span data-ttu-id="45a3f-143">New-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="45a3f-143">New-AzRedisCacheLink</span></span>](./New-AzRedisCacheLink.md)

[<span data-ttu-id="45a3f-144">Remove-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="45a3f-144">Remove-AzRedisCacheLink</span></span>](./Remove-AzRedisCacheLink.md)

[<span data-ttu-id="45a3f-145">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="45a3f-145">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="45a3f-146">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="45a3f-146">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="45a3f-147">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="45a3f-147">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="45a3f-148">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="45a3f-148">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)
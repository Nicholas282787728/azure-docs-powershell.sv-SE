---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/get-azurermrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheLink.md
ms.openlocfilehash: dff5f565e27f89360465ede3eb8fbe2c3d5620a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575555"
---
# <span data-ttu-id="9dc72-101">Get-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="9dc72-101">Get-AzureRmRedisCacheLink</span></span>

## <span data-ttu-id="9dc72-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9dc72-102">SYNOPSIS</span></span>
<span data-ttu-id="9dc72-103">Länken Hämta geo-replikering för Redis cache.</span><span class="sxs-lookup"><span data-stu-id="9dc72-103">Get geo replication link for Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9dc72-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9dc72-104">SYNTAX</span></span>

### <span data-ttu-id="9dc72-105">AllLinksForCache (standard)</span><span class="sxs-lookup"><span data-stu-id="9dc72-105">AllLinksForCache (Default)</span></span>
```
Get-AzureRmRedisCacheLink -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9dc72-106">AllLinksForPrimaryCache</span><span class="sxs-lookup"><span data-stu-id="9dc72-106">AllLinksForPrimaryCache</span></span>
```
Get-AzureRmRedisCacheLink -PrimaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9dc72-107">SingleLink</span><span class="sxs-lookup"><span data-stu-id="9dc72-107">SingleLink</span></span>
```
Get-AzureRmRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9dc72-108">AllLinksForSecondaryCache</span><span class="sxs-lookup"><span data-stu-id="9dc72-108">AllLinksForSecondaryCache</span></span>
```
Get-AzureRmRedisCacheLink -SecondaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9dc72-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9dc72-109">DESCRIPTION</span></span>
<span data-ttu-id="9dc72-110">Det finns fyra olika sätt att få till gång till geo-Replication.</span><span class="sxs-lookup"><span data-stu-id="9dc72-110">There are four different ways to get geo-replication link detail.</span></span> <span data-ttu-id="9dc72-111">Ange antingen parameter namn eller PrimaryServerName och/eller SecondaryServerName.</span><span class="sxs-lookup"><span data-stu-id="9dc72-111">Either provide parameter Name or PrimaryServerName and/or SecondaryServerName.</span></span> <span data-ttu-id="9dc72-112">Namnet ges och alla länkar där cache finns returneras.</span><span class="sxs-lookup"><span data-stu-id="9dc72-112">Name is given then all link where cache exists will be returned.</span></span> <span data-ttu-id="9dc72-113">Om endast PrimaryServerName ges returneras alla länkar där cache är primärt.</span><span class="sxs-lookup"><span data-stu-id="9dc72-113">If only PrimaryServerName is given then all links where cache is primary will be returned.</span></span> <span data-ttu-id="9dc72-114">Om endast SecondaryServerName ges returneras alla länkar där cache är sekundärt.</span><span class="sxs-lookup"><span data-stu-id="9dc72-114">If only SecondaryServerName is given then all links where cache is secondary will be returned.</span></span> <span data-ttu-id="9dc72-115">Om PrimaryServerName och SecondaryServerName båda anges returneras specifik länk med rätt roll.</span><span class="sxs-lookup"><span data-stu-id="9dc72-115">If PrimaryServerName and SecondaryServerName both are given then specific link with correct role will be returned.</span></span> 

## <span data-ttu-id="9dc72-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9dc72-116">EXAMPLES</span></span>

### <span data-ttu-id="9dc72-117">Exempel 1: använda parameter uppsättning AllLinksForCache</span><span class="sxs-lookup"><span data-stu-id="9dc72-117">Example 1: Get using parameter set AllLinksForCache</span></span>
```
PS C:\>Get-AzureRmRedisCacheLink -Name "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="9dc72-118">Det här kommandot får alla geo-replikeringslänk för Redis cache som heter mycache1.</span><span class="sxs-lookup"><span data-stu-id="9dc72-118">This command gets all geo-replication links for Redis Cache named mycache1.</span></span>

### <span data-ttu-id="9dc72-119">Exempel 2: använda parameter uppsättning AllLinksForPrimaryCache</span><span class="sxs-lookup"><span data-stu-id="9dc72-119">Example 2: Get using parameter set AllLinksForPrimaryCache</span></span>
```
PS C:\>Get-AzureRmRedisCacheLink -PrimaryServerName "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="9dc72-120">Det här kommandot får geo-replikeringslänken-länkar där Redis cache-namnet mycache1 är primärt.</span><span class="sxs-lookup"><span data-stu-id="9dc72-120">This command gets geo-replication links where Redis Cache named mycache1 is primary.</span></span>

### <span data-ttu-id="9dc72-121">Exempel 3: använda parameter uppsättning AllLinksForSecondaryCache</span><span class="sxs-lookup"><span data-stu-id="9dc72-121">Example 3: Get using parameter set AllLinksForSecondaryCache</span></span>
```
PS C:\>Get-AzureRmRedisCacheLink -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="9dc72-122">Det här kommandot får geo-replikeringslänken-länkar där Redis cache med namnet mycache2 är sekundärt.</span><span class="sxs-lookup"><span data-stu-id="9dc72-122">This command gets geo-replication links where Redis Cache named mycache2 is secondary.</span></span>

### <span data-ttu-id="9dc72-123">Exempel 4: använda parameter uppsättning SingleLink</span><span class="sxs-lookup"><span data-stu-id="9dc72-123">Example 4: Get using parameter set SingleLink</span></span>
```
PS C:\>Get-AzureRmRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="9dc72-124">Det här kommandot får du en enda geo-replikeringslänk där Redis cache med namnet mycache1 är primär och Redis cache med namnet mycache2 är sekundär.</span><span class="sxs-lookup"><span data-stu-id="9dc72-124">This command gets a single geo-replication links where Redis Cache named mycache1 is primary and Redis Cache named mycache2 is secondary.</span></span>

## <span data-ttu-id="9dc72-125">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9dc72-125">PARAMETERS</span></span>

### <span data-ttu-id="9dc72-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dc72-126">-DefaultProfile</span></span>
<span data-ttu-id="9dc72-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9dc72-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9dc72-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="9dc72-128">-Name</span></span>
<span data-ttu-id="9dc72-129">Namn på Redis cache.</span><span class="sxs-lookup"><span data-stu-id="9dc72-129">Name of redis cache.</span></span>

```yaml
Type: String
Parameter Sets: AllLinksForCache
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9dc72-130">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="9dc72-130">-PrimaryServerName</span></span>
<span data-ttu-id="9dc72-131">Namn på primär Redis cache i länken.</span><span class="sxs-lookup"><span data-stu-id="9dc72-131">Name of primary redis cache in link.</span></span>

```yaml
Type: String
Parameter Sets: AllLinksForPrimaryCache, SingleLink
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9dc72-132">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="9dc72-132">-SecondaryServerName</span></span>
<span data-ttu-id="9dc72-133">Namnet på den sekundära Redis-cachen i länken.</span><span class="sxs-lookup"><span data-stu-id="9dc72-133">Name of secondary redis cache in link.</span></span>

```yaml
Type: String
Parameter Sets: SingleLink, AllLinksForSecondaryCache
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9dc72-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dc72-134">CommonParameters</span></span>
<span data-ttu-id="9dc72-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9dc72-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dc72-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9dc72-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dc72-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9dc72-137">INPUTS</span></span>

### <span data-ttu-id="9dc72-138">System. String</span><span class="sxs-lookup"><span data-stu-id="9dc72-138">System.String</span></span>
<span data-ttu-id="9dc72-139">Du kan pipes in i denna cmdlet efter namn men inte efter värde.</span><span class="sxs-lookup"><span data-stu-id="9dc72-139">You can pipe input to this cmdlet by name, but not by value.</span></span>

## <span data-ttu-id="9dc72-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9dc72-140">OUTPUTS</span></span>

### <span data-ttu-id="9dc72-141">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. RedisCache. Models. PSRedisLinkedServer, Microsoft. Azure. commands. RedisCache, version = 4.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="9dc72-141">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer, Microsoft.Azure.Commands.RedisCache, Version=4.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="9dc72-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9dc72-142">NOTES</span></span>

## <span data-ttu-id="9dc72-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9dc72-143">RELATED LINKS</span></span>

[<span data-ttu-id="9dc72-144">New-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="9dc72-144">New-AzureRmRedisCacheLink</span></span>](./New-AzureRmRedisCacheLink.md)

[<span data-ttu-id="9dc72-145">Remove-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="9dc72-145">Remove-AzureRmRedisCacheLink</span></span>](./Remove-AzureRmRedisCacheLink.md)

[<span data-ttu-id="9dc72-146">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="9dc72-146">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="9dc72-147">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="9dc72-147">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="9dc72-148">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="9dc72-148">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="9dc72-149">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="9dc72-149">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)

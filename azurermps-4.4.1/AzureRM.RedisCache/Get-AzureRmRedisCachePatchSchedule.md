---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: DA180A4A-88B6-4359-94E0-CF72F66D1FE4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCachePatchSchedule.md
ms.openlocfilehash: 1899a35f183f66fb938abe0c6492e826ad661e43
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585352"
---
# <span data-ttu-id="72455-101">Get-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="72455-101">Get-AzureRmRedisCachePatchSchedule</span></span>

## <span data-ttu-id="72455-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="72455-102">SYNOPSIS</span></span>
<span data-ttu-id="72455-103">Får ett uppdaterings schema.</span><span class="sxs-lookup"><span data-stu-id="72455-103">Gets a patch schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72455-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="72455-104">SYNTAX</span></span>

```
Get-AzureRmRedisCachePatchSchedule -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72455-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="72455-105">DESCRIPTION</span></span>
<span data-ttu-id="72455-106">Cmdleten **Get-AzureRmRedisCachePatchSchedule** får ett uppdaterings schema för ett cacheminne i Azure Redis-cachen.</span><span class="sxs-lookup"><span data-stu-id="72455-106">The **Get-AzureRmRedisCachePatchSchedule** cmdlet gets a patch schedule for a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="72455-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="72455-107">EXAMPLES</span></span>

### <span data-ttu-id="72455-108">Exempel 1: få uppdaterings schema</span><span class="sxs-lookup"><span data-stu-id="72455-108">Example 1: Get the patch schedule</span></span>
```
PS C:\>Get-AzureRmRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="72455-109">Det här kommandot får ett uppdaterings schema från cachen som heter RedisCache06.</span><span class="sxs-lookup"><span data-stu-id="72455-109">This command gets the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="72455-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="72455-110">PARAMETERS</span></span>

### <span data-ttu-id="72455-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="72455-111">-Name</span></span>
<span data-ttu-id="72455-112">Anger namnet på en cache.</span><span class="sxs-lookup"><span data-stu-id="72455-112">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="72455-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72455-113">-ResourceGroupName</span></span>
<span data-ttu-id="72455-114">Anger namnet på den resurs grupp som innehåller cacheminnet.</span><span class="sxs-lookup"><span data-stu-id="72455-114">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="72455-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72455-115">-DefaultProfile</span></span>
<span data-ttu-id="72455-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="72455-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72455-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72455-117">CommonParameters</span></span>
<span data-ttu-id="72455-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72455-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72455-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72455-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72455-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="72455-120">INPUTS</span></span>

### <span data-ttu-id="72455-121">Ingen</span><span class="sxs-lookup"><span data-stu-id="72455-121">None</span></span>
<span data-ttu-id="72455-122">Du kan ange indata för denna cmdlet efter egenskaps namn, men inte efter värde.</span><span class="sxs-lookup"><span data-stu-id="72455-122">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="72455-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="72455-123">OUTPUTS</span></span>

### <span data-ttu-id="72455-124">Microsoft. Azure. commands. RedisCache. Models. PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="72455-124">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>
<span data-ttu-id="72455-125">Den här cmdleten returnerar de ändrings schema poster som är inställda i cacheminnet.</span><span class="sxs-lookup"><span data-stu-id="72455-125">This cmdlet returns the of patch schedule entries set on the cache.</span></span>

## <span data-ttu-id="72455-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="72455-126">NOTES</span></span>
* <span data-ttu-id="72455-127">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, Redis, cache, Web, webapp, webbplats</span><span class="sxs-lookup"><span data-stu-id="72455-127">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="72455-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="72455-128">RELATED LINKS</span></span>

[<span data-ttu-id="72455-129">New-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="72455-129">New-AzureRmRedisCachePatchSchedule</span></span>](./New-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="72455-130">New-AzureRmRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="72455-130">New-AzureRmRedisCacheScheduleEntry</span></span>](./New-AzureRmRedisCacheScheduleEntry.md)

[<span data-ttu-id="72455-131">Remove-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="72455-131">Remove-AzureRmRedisCachePatchSchedule</span></span>](./Remove-AzureRmRedisCachePatchSchedule.md)



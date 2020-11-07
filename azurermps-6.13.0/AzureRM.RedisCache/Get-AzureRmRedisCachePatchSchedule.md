---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: DA180A4A-88B6-4359-94E0-CF72F66D1FE4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/get-azurermrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCachePatchSchedule.md
ms.openlocfilehash: ac1184dcdcc55a0b5cac28f996c29c3476ba3613
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757043"
---
# <span data-ttu-id="31cc4-101">Get-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="31cc4-101">Get-AzureRmRedisCachePatchSchedule</span></span>

## <span data-ttu-id="31cc4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="31cc4-102">SYNOPSIS</span></span>
<span data-ttu-id="31cc4-103">Får ett uppdaterings schema.</span><span class="sxs-lookup"><span data-stu-id="31cc4-103">Gets a patch schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31cc4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="31cc4-104">SYNTAX</span></span>

```
Get-AzureRmRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31cc4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="31cc4-105">DESCRIPTION</span></span>
<span data-ttu-id="31cc4-106">Cmdleten **Get-AzureRmRedisCachePatchSchedule** får ett uppdaterings schema för ett cacheminne i Azure Redis-cachen.</span><span class="sxs-lookup"><span data-stu-id="31cc4-106">The **Get-AzureRmRedisCachePatchSchedule** cmdlet gets a patch schedule for a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="31cc4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="31cc4-107">EXAMPLES</span></span>

### <span data-ttu-id="31cc4-108">Exempel 1: få uppdaterings schema</span><span class="sxs-lookup"><span data-stu-id="31cc4-108">Example 1: Get the patch schedule</span></span>
```
PS C:\>Get-AzureRmRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="31cc4-109">Det här kommandot får ett uppdaterings schema från cachen som heter RedisCache06.</span><span class="sxs-lookup"><span data-stu-id="31cc4-109">This command gets the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="31cc4-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="31cc4-110">PARAMETERS</span></span>

### <span data-ttu-id="31cc4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31cc4-111">-DefaultProfile</span></span>
<span data-ttu-id="31cc4-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="31cc4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31cc4-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="31cc4-113">-Name</span></span>
<span data-ttu-id="31cc4-114">Anger namnet på en cache.</span><span class="sxs-lookup"><span data-stu-id="31cc4-114">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="31cc4-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31cc4-115">-ResourceGroupName</span></span>
<span data-ttu-id="31cc4-116">Anger namnet på den resurs grupp som innehåller cacheminnet.</span><span class="sxs-lookup"><span data-stu-id="31cc4-116">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="31cc4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31cc4-117">CommonParameters</span></span>
<span data-ttu-id="31cc4-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31cc4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31cc4-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31cc4-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31cc4-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="31cc4-120">INPUTS</span></span>

### <span data-ttu-id="31cc4-121">System. String</span><span class="sxs-lookup"><span data-stu-id="31cc4-121">System.String</span></span>

## <span data-ttu-id="31cc4-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="31cc4-122">OUTPUTS</span></span>

### <span data-ttu-id="31cc4-123">Microsoft. Azure. commands. RedisCache. Models. PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="31cc4-123">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>

## <span data-ttu-id="31cc4-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="31cc4-124">NOTES</span></span>
* <span data-ttu-id="31cc4-125">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, Redis, cache, Web, webapp, webbplats</span><span class="sxs-lookup"><span data-stu-id="31cc4-125">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="31cc4-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="31cc4-126">RELATED LINKS</span></span>

[<span data-ttu-id="31cc4-127">New-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="31cc4-127">New-AzureRmRedisCachePatchSchedule</span></span>](./New-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="31cc4-128">New-AzureRmRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="31cc4-128">New-AzureRmRedisCacheScheduleEntry</span></span>](./New-AzureRmRedisCacheScheduleEntry.md)

[<span data-ttu-id="31cc4-129">Remove-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="31cc4-129">Remove-AzureRmRedisCachePatchSchedule</span></span>](./Remove-AzureRmRedisCachePatchSchedule.md)



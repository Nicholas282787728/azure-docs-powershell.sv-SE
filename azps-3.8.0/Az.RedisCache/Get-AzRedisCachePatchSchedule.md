---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: DA180A4A-88B6-4359-94E0-CF72F66D1FE4
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCachePatchSchedule.md
ms.openlocfilehash: 0e63f8e5f427a251db13c76f915dc615f259defc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091290"
---
# <span data-ttu-id="c6769-101">Get-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="c6769-101">Get-AzRedisCachePatchSchedule</span></span>

## <span data-ttu-id="c6769-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c6769-102">SYNOPSIS</span></span>
<span data-ttu-id="c6769-103">Får ett uppdaterings schema.</span><span class="sxs-lookup"><span data-stu-id="c6769-103">Gets a patch schedule.</span></span>

## <span data-ttu-id="c6769-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c6769-104">SYNTAX</span></span>

```
Get-AzRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6769-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c6769-105">DESCRIPTION</span></span>
<span data-ttu-id="c6769-106">Cmdleten **Get-AzRedisCachePatchSchedule** får ett uppdaterings schema för ett cacheminne i Azure Redis-cachen.</span><span class="sxs-lookup"><span data-stu-id="c6769-106">The **Get-AzRedisCachePatchSchedule** cmdlet gets a patch schedule for a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="c6769-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c6769-107">EXAMPLES</span></span>

### <span data-ttu-id="c6769-108">Exempel 1: få uppdaterings schema</span><span class="sxs-lookup"><span data-stu-id="c6769-108">Example 1: Get the patch schedule</span></span>
```
PS C:\>Get-AzRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="c6769-109">Det här kommandot får ett uppdaterings schema från cachen som heter RedisCache06.</span><span class="sxs-lookup"><span data-stu-id="c6769-109">This command gets the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="c6769-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c6769-110">PARAMETERS</span></span>

### <span data-ttu-id="c6769-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6769-111">-DefaultProfile</span></span>
<span data-ttu-id="c6769-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c6769-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6769-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="c6769-113">-Name</span></span>
<span data-ttu-id="c6769-114">Anger namnet på en cache.</span><span class="sxs-lookup"><span data-stu-id="c6769-114">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="c6769-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6769-115">-ResourceGroupName</span></span>
<span data-ttu-id="c6769-116">Anger namnet på den resurs grupp som innehåller cacheminnet.</span><span class="sxs-lookup"><span data-stu-id="c6769-116">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="c6769-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6769-117">CommonParameters</span></span>
<span data-ttu-id="c6769-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6769-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6769-119">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6769-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6769-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c6769-120">INPUTS</span></span>

### <span data-ttu-id="c6769-121">System. String</span><span class="sxs-lookup"><span data-stu-id="c6769-121">System.String</span></span>

## <span data-ttu-id="c6769-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c6769-122">OUTPUTS</span></span>

### <span data-ttu-id="c6769-123">Microsoft. Azure. commands. RedisCache. Models. PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="c6769-123">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>

## <span data-ttu-id="c6769-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c6769-124">NOTES</span></span>
* <span data-ttu-id="c6769-125">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, Redis, cache, Web, webapp, webbplats</span><span class="sxs-lookup"><span data-stu-id="c6769-125">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="c6769-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c6769-126">RELATED LINKS</span></span>

[<span data-ttu-id="c6769-127">New-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="c6769-127">New-AzRedisCachePatchSchedule</span></span>](./New-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="c6769-128">New-AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="c6769-128">New-AzRedisCacheScheduleEntry</span></span>](./New-AzRedisCacheScheduleEntry.md)

[<span data-ttu-id="c6769-129">Remove-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="c6769-129">Remove-AzRedisCachePatchSchedule</span></span>](./Remove-AzRedisCachePatchSchedule.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: DA180A4A-88B6-4359-94E0-CF72F66D1FE4
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCachePatchSchedule.md
ms.openlocfilehash: 0e63f8e5f427a251db13c76f915dc615f259defc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98395435"
---
# <span data-ttu-id="59a98-101">Get-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="59a98-101">Get-AzRedisCachePatchSchedule</span></span>

## <span data-ttu-id="59a98-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="59a98-102">SYNOPSIS</span></span>
<span data-ttu-id="59a98-103">Får ett uppdaterings schema.</span><span class="sxs-lookup"><span data-stu-id="59a98-103">Gets a patch schedule.</span></span>

## <span data-ttu-id="59a98-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="59a98-104">SYNTAX</span></span>

```
Get-AzRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59a98-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="59a98-105">DESCRIPTION</span></span>
<span data-ttu-id="59a98-106">Cmdleten **Get-AzRedisCachePatchSchedule** får ett uppdaterings schema för ett cacheminne i Azure Redis-cachen.</span><span class="sxs-lookup"><span data-stu-id="59a98-106">The **Get-AzRedisCachePatchSchedule** cmdlet gets a patch schedule for a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="59a98-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="59a98-107">EXAMPLES</span></span>

### <span data-ttu-id="59a98-108">Exempel 1: få uppdaterings schema</span><span class="sxs-lookup"><span data-stu-id="59a98-108">Example 1: Get the patch schedule</span></span>
```
PS C:\>Get-AzRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="59a98-109">Det här kommandot får ett uppdaterings schema från cachen som heter RedisCache06.</span><span class="sxs-lookup"><span data-stu-id="59a98-109">This command gets the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="59a98-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="59a98-110">PARAMETERS</span></span>

### <span data-ttu-id="59a98-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59a98-111">-DefaultProfile</span></span>
<span data-ttu-id="59a98-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="59a98-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59a98-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="59a98-113">-Name</span></span>
<span data-ttu-id="59a98-114">Anger namnet på en cache.</span><span class="sxs-lookup"><span data-stu-id="59a98-114">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="59a98-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59a98-115">-ResourceGroupName</span></span>
<span data-ttu-id="59a98-116">Anger namnet på den resurs grupp som innehåller cacheminnet.</span><span class="sxs-lookup"><span data-stu-id="59a98-116">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="59a98-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59a98-117">CommonParameters</span></span>
<span data-ttu-id="59a98-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59a98-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59a98-119">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59a98-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59a98-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="59a98-120">INPUTS</span></span>

### <span data-ttu-id="59a98-121">System. String</span><span class="sxs-lookup"><span data-stu-id="59a98-121">System.String</span></span>

## <span data-ttu-id="59a98-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="59a98-122">OUTPUTS</span></span>

### <span data-ttu-id="59a98-123">Microsoft. Azure. commands. RedisCache. Models. PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="59a98-123">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>

## <span data-ttu-id="59a98-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="59a98-124">NOTES</span></span>
* <span data-ttu-id="59a98-125">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, Redis, cache, Web, webapp, webbplats</span><span class="sxs-lookup"><span data-stu-id="59a98-125">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="59a98-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="59a98-126">RELATED LINKS</span></span>

[<span data-ttu-id="59a98-127">New-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="59a98-127">New-AzRedisCachePatchSchedule</span></span>](./New-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="59a98-128">New-AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="59a98-128">New-AzRedisCacheScheduleEntry</span></span>](./New-AzRedisCacheScheduleEntry.md)

[<span data-ttu-id="59a98-129">Remove-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="59a98-129">Remove-AzRedisCachePatchSchedule</span></span>](./Remove-AzRedisCachePatchSchedule.md)



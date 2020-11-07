---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 2EA765B8-D82B-4789-8F10-88F79BDF44D0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/remove-azurermrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCachePatchSchedule.md
ms.openlocfilehash: 7224e83333b281fac849ee9e5d99a0691aba3ccc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756667"
---
# <span data-ttu-id="70e87-101">Remove-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="70e87-101">Remove-AzureRmRedisCachePatchSchedule</span></span>

## <span data-ttu-id="70e87-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="70e87-102">SYNOPSIS</span></span>
<span data-ttu-id="70e87-103">Tar bort uppdaterings schema.</span><span class="sxs-lookup"><span data-stu-id="70e87-103">Removes the patch schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="70e87-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="70e87-104">SYNTAX</span></span>

```
Remove-AzureRmRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70e87-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="70e87-105">DESCRIPTION</span></span>
<span data-ttu-id="70e87-106">Cmdleten **Remove-AzureRmRedisCachePatchSchedule** tar bort uppdaterings schema från cachen i Azure Redis-cachen.</span><span class="sxs-lookup"><span data-stu-id="70e87-106">The **Remove-AzureRmRedisCachePatchSchedule** cmdlet removes the patch schedule from a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="70e87-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="70e87-107">EXAMPLES</span></span>

### <span data-ttu-id="70e87-108">Exempel 1: ta bort uppdaterings schema</span><span class="sxs-lookup"><span data-stu-id="70e87-108">Example 1: Remove the patch schedule</span></span>
```
PS C:\>Remove-AzureRmRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="70e87-109">Det här kommandot tar bort uppdaterings schema från cachen som heter RedisCache06.</span><span class="sxs-lookup"><span data-stu-id="70e87-109">This command removes the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="70e87-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="70e87-110">PARAMETERS</span></span>

### <span data-ttu-id="70e87-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70e87-111">-DefaultProfile</span></span>
<span data-ttu-id="70e87-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="70e87-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70e87-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="70e87-113">-Name</span></span>
<span data-ttu-id="70e87-114">Anger namnet på en cache.</span><span class="sxs-lookup"><span data-stu-id="70e87-114">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="70e87-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="70e87-115">-PassThru</span></span>
<span data-ttu-id="70e87-116">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="70e87-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="70e87-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70e87-117">-ResourceGroupName</span></span>
<span data-ttu-id="70e87-118">Anger namnet på den resurs grupp som innehåller cacheminnet.</span><span class="sxs-lookup"><span data-stu-id="70e87-118">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="70e87-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="70e87-119">-Confirm</span></span>
<span data-ttu-id="70e87-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="70e87-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70e87-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70e87-121">-WhatIf</span></span>
<span data-ttu-id="70e87-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="70e87-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70e87-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="70e87-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70e87-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70e87-124">CommonParameters</span></span>
<span data-ttu-id="70e87-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70e87-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70e87-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70e87-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70e87-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="70e87-127">INPUTS</span></span>

### <span data-ttu-id="70e87-128">System. String</span><span class="sxs-lookup"><span data-stu-id="70e87-128">System.String</span></span>

## <span data-ttu-id="70e87-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="70e87-129">OUTPUTS</span></span>

### <span data-ttu-id="70e87-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="70e87-130">System.Boolean</span></span>

## <span data-ttu-id="70e87-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="70e87-131">NOTES</span></span>
* <span data-ttu-id="70e87-132">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, Redis, cache, Web, webapp, webbplats</span><span class="sxs-lookup"><span data-stu-id="70e87-132">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="70e87-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="70e87-133">RELATED LINKS</span></span>

[<span data-ttu-id="70e87-134">Get-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="70e87-134">Get-AzureRmRedisCachePatchSchedule</span></span>](./Get-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="70e87-135">New-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="70e87-135">New-AzureRmRedisCachePatchSchedule</span></span>](./New-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="70e87-136">New-AzureRmRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="70e87-136">New-AzureRmRedisCacheScheduleEntry</span></span>](./New-AzureRmRedisCacheScheduleEntry.md)



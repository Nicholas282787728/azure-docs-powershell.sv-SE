---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 1F86CE62-AA01-44FB-A935-484EC51DDE5A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/new-azurermrediscachekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheKey.md
ms.openlocfilehash: 51fff2f79435c6806b126fbc0a9c120ee8b8842e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573328"
---
# <span data-ttu-id="87ac3-101">New-AzureRmRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="87ac3-101">New-AzureRmRedisCacheKey</span></span>

## <span data-ttu-id="87ac3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="87ac3-102">SYNOPSIS</span></span>
<span data-ttu-id="87ac3-103">Återskapar åtkomst nyckeln för en Redis-cache.</span><span class="sxs-lookup"><span data-stu-id="87ac3-103">Regenerates the access key of a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87ac3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="87ac3-104">SYNTAX</span></span>

```
New-AzureRmRedisCacheKey [-ResourceGroupName <String>] -Name <String> -KeyType <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87ac3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="87ac3-105">DESCRIPTION</span></span>
<span data-ttu-id="87ac3-106">Cmdleten **New-AzureRmRedisCacheKey** återskapar Access-nyckeln för Azure Redis-cachen.</span><span class="sxs-lookup"><span data-stu-id="87ac3-106">The **New-AzureRmRedisCacheKey** cmdlet regenerates the access key of an Azure Redis Cache.</span></span>

## <span data-ttu-id="87ac3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="87ac3-107">EXAMPLES</span></span>

### <span data-ttu-id="87ac3-108">Exempel 1: återskapa en primär nyckeln</span><span class="sxs-lookup"><span data-stu-id="87ac3-108">Example 1: Regenerate a primary key</span></span>
```
PS C:\>New-AzureRmRedisCacheKey -ResourceGroupName "ResourceGroup03" -Name "myCache" -KeyType "Primary" -Force

          PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=

          SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="87ac3-109">Det här kommandot återskapar primär nyckeln för en Redis-cache.</span><span class="sxs-lookup"><span data-stu-id="87ac3-109">This command regenerates the primary key of a Redis Cache.</span></span>

### <span data-ttu-id="87ac3-110">Exempel 2: återskapa en sekundär nyckeln</span><span class="sxs-lookup"><span data-stu-id="87ac3-110">Example 2: Regenerate a secondary key</span></span>
```
PS C:\>New-AzureRmRedisCacheKey -ResourceGroupName "ResourceGroup03" -Name "myCache" -KeyType "Secondary" -Force
          PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=

          SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="87ac3-111">Det här kommandot återskapar den sekundära nyckeln i en Redis-cache.</span><span class="sxs-lookup"><span data-stu-id="87ac3-111">This command regenerates the secondary key of a Redis Cache.</span></span>

## <span data-ttu-id="87ac3-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="87ac3-112">PARAMETERS</span></span>

### <span data-ttu-id="87ac3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87ac3-113">-DefaultProfile</span></span>
<span data-ttu-id="87ac3-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="87ac3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87ac3-115">-Force</span><span class="sxs-lookup"><span data-stu-id="87ac3-115">-Force</span></span>
<span data-ttu-id="87ac3-116">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="87ac3-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87ac3-117">-Värdetyp</span><span class="sxs-lookup"><span data-stu-id="87ac3-117">-KeyType</span></span>
<span data-ttu-id="87ac3-118">Anger om den primära eller sekundära åtkomst nyckeln ska återskapas.</span><span class="sxs-lookup"><span data-stu-id="87ac3-118">Specifies whether to regenerate the primary or secondary access key.</span></span>
<span data-ttu-id="87ac3-119">Giltiga värden är: primär, sekundär.</span><span class="sxs-lookup"><span data-stu-id="87ac3-119">Valid values are: Primary, Secondary.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87ac3-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="87ac3-120">-Name</span></span>
<span data-ttu-id="87ac3-121">Anger namnet på Redis cache.</span><span class="sxs-lookup"><span data-stu-id="87ac3-121">Specifies the name of the Redis Cache.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87ac3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87ac3-122">-ResourceGroupName</span></span>
<span data-ttu-id="87ac3-123">Anger namnet på den resurs grupp som innehåller Redis-cachen.</span><span class="sxs-lookup"><span data-stu-id="87ac3-123">Specifies the name of the resource group that contains the Redis Cache.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87ac3-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="87ac3-124">-Confirm</span></span>
<span data-ttu-id="87ac3-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="87ac3-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87ac3-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87ac3-126">-WhatIf</span></span>
<span data-ttu-id="87ac3-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="87ac3-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87ac3-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="87ac3-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87ac3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87ac3-129">CommonParameters</span></span>
<span data-ttu-id="87ac3-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87ac3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87ac3-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87ac3-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87ac3-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="87ac3-132">INPUTS</span></span>

### <span data-ttu-id="87ac3-133">Ingen</span><span class="sxs-lookup"><span data-stu-id="87ac3-133">None</span></span>
<span data-ttu-id="87ac3-134">Du kan pipes in i denna cmdlet efter namn men inte efter värde.</span><span class="sxs-lookup"><span data-stu-id="87ac3-134">You can pipe input to this cmdlet by name, but not by value.</span></span>

## <span data-ttu-id="87ac3-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="87ac3-135">OUTPUTS</span></span>

### <span data-ttu-id="87ac3-136">Microsoft. Azure. Management. Redis. Models. RedisAccessKeys</span><span class="sxs-lookup"><span data-stu-id="87ac3-136">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span></span>
<span data-ttu-id="87ac3-137">Denna cmdlet returnerar den primära och sekundära åtkomst knappen i en Redis cache.</span><span class="sxs-lookup"><span data-stu-id="87ac3-137">This cmdlet returns the primary and secondary access key of a Redis Cache.</span></span>

## <span data-ttu-id="87ac3-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="87ac3-138">NOTES</span></span>

## <span data-ttu-id="87ac3-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="87ac3-139">RELATED LINKS</span></span>

[<span data-ttu-id="87ac3-140">Get-AzureRmRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="87ac3-140">Get-AzureRmRedisCacheKey</span></span>](./Get-AzureRmRedisCacheKey.md)



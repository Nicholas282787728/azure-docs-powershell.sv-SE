---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 1F86CE62-AA01-44FB-A935-484EC51DDE5A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheKey.md
ms.openlocfilehash: b453b47da35addb8a04a19957c148c5ec1929e75
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575884"
---
# <span data-ttu-id="4ef0c-101">New-AzureRmRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="4ef0c-101">New-AzureRmRedisCacheKey</span></span>

## <span data-ttu-id="4ef0c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4ef0c-102">SYNOPSIS</span></span>
<span data-ttu-id="4ef0c-103">Återskapar åtkomst nyckeln för en Redis-cache.</span><span class="sxs-lookup"><span data-stu-id="4ef0c-103">Regenerates the access key of a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ef0c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4ef0c-104">SYNTAX</span></span>

```
New-AzureRmRedisCacheKey -ResourceGroupName <String> -Name <String> -KeyType <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ef0c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4ef0c-105">DESCRIPTION</span></span>
<span data-ttu-id="4ef0c-106">Cmdleten **New-AzureRmRedisCacheKey** återskapar Access-nyckeln för Azure Redis-cachen.</span><span class="sxs-lookup"><span data-stu-id="4ef0c-106">The **New-AzureRmRedisCacheKey** cmdlet regenerates the access key of an Azure Redis Cache.</span></span>

## <span data-ttu-id="4ef0c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4ef0c-107">EXAMPLES</span></span>

### <span data-ttu-id="4ef0c-108">Exempel 1: återskapa en primär nyckeln</span><span class="sxs-lookup"><span data-stu-id="4ef0c-108">Example 1: Regenerate a primary key</span></span>
```
PS C:\>New-AzureRmRedisCacheKey -ResourceGroupName "ResourceGroup03" -Name "myCache" -KeyType "Primary" -Force

          PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=

          SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="4ef0c-109">Det här kommandot återskapar primär nyckeln för en Redis-cache.</span><span class="sxs-lookup"><span data-stu-id="4ef0c-109">This command regenerates the primary key of a Redis Cache.</span></span>

### <span data-ttu-id="4ef0c-110">Exempel 2: återskapa en sekundär nyckeln</span><span class="sxs-lookup"><span data-stu-id="4ef0c-110">Example 2: Regenerate a secondary key</span></span>
```
PS C:\>New-AzureRmRedisCacheKey -ResourceGroupName "ResourceGroup03" -Name "myCache" -KeyType "Secondary" -Force
          PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=

          SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="4ef0c-111">Det här kommandot återskapar den sekundära nyckeln i en Redis-cache.</span><span class="sxs-lookup"><span data-stu-id="4ef0c-111">This command regenerates the secondary key of a Redis Cache.</span></span>

## <span data-ttu-id="4ef0c-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4ef0c-112">PARAMETERS</span></span>

### <span data-ttu-id="4ef0c-113">-Force</span><span class="sxs-lookup"><span data-stu-id="4ef0c-113">-Force</span></span>
<span data-ttu-id="4ef0c-114">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="4ef0c-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4ef0c-115">-Värdetyp</span><span class="sxs-lookup"><span data-stu-id="4ef0c-115">-KeyType</span></span>
<span data-ttu-id="4ef0c-116">Anger om den primära eller sekundära åtkomst nyckeln ska återskapas.</span><span class="sxs-lookup"><span data-stu-id="4ef0c-116">Specifies whether to regenerate the primary or secondary access key.</span></span>
<span data-ttu-id="4ef0c-117">Giltiga värden är: primär, sekundär.</span><span class="sxs-lookup"><span data-stu-id="4ef0c-117">Valid values are: Primary, Secondary.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ef0c-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="4ef0c-118">-Name</span></span>
<span data-ttu-id="4ef0c-119">Anger namnet på Redis cache.</span><span class="sxs-lookup"><span data-stu-id="4ef0c-119">Specifies the name of the Redis Cache.</span></span>

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

### <span data-ttu-id="4ef0c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ef0c-120">-ResourceGroupName</span></span>
<span data-ttu-id="4ef0c-121">Anger namnet på den resurs grupp som innehåller Redis-cachen.</span><span class="sxs-lookup"><span data-stu-id="4ef0c-121">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="4ef0c-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4ef0c-122">-Confirm</span></span>
<span data-ttu-id="4ef0c-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4ef0c-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ef0c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ef0c-124">-WhatIf</span></span>
<span data-ttu-id="4ef0c-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4ef0c-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ef0c-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4ef0c-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ef0c-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ef0c-127">-DefaultProfile</span></span>
<span data-ttu-id="4ef0c-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4ef0c-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ef0c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ef0c-129">CommonParameters</span></span>
<span data-ttu-id="4ef0c-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ef0c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ef0c-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ef0c-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ef0c-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4ef0c-132">INPUTS</span></span>

### <span data-ttu-id="4ef0c-133">Ingen</span><span class="sxs-lookup"><span data-stu-id="4ef0c-133">None</span></span>
<span data-ttu-id="4ef0c-134">Du kan pipes in i denna cmdlet efter namn men inte efter värde.</span><span class="sxs-lookup"><span data-stu-id="4ef0c-134">You can pipe input to this cmdlet by name, but not by value.</span></span>

## <span data-ttu-id="4ef0c-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4ef0c-135">OUTPUTS</span></span>

### <span data-ttu-id="4ef0c-136">Microsoft. Azure. Management. Redis. Models. RedisAccessKeys</span><span class="sxs-lookup"><span data-stu-id="4ef0c-136">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span></span>
<span data-ttu-id="4ef0c-137">Denna cmdlet returnerar den primära och sekundära åtkomst knappen i en Redis cache.</span><span class="sxs-lookup"><span data-stu-id="4ef0c-137">This cmdlet returns the primary and secondary access key of a Redis Cache.</span></span>

## <span data-ttu-id="4ef0c-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4ef0c-138">NOTES</span></span>

## <span data-ttu-id="4ef0c-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4ef0c-139">RELATED LINKS</span></span>

[<span data-ttu-id="4ef0c-140">Get-AzureRmRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="4ef0c-140">Get-AzureRmRedisCacheKey</span></span>](./Get-AzureRmRedisCacheKey.md)



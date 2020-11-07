---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: C0BEC701-8CE2-4B19-9F04-D32A42D9249E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheKey.md
ms.openlocfilehash: e7e50488f69adb2b168453fd18264bf25a69942d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758018"
---
# <span data-ttu-id="91fbe-101">Get-AzureRmRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="91fbe-101">Get-AzureRmRedisCacheKey</span></span>

## <span data-ttu-id="91fbe-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="91fbe-102">SYNOPSIS</span></span>
<span data-ttu-id="91fbe-103">Hämtar snabb tangenterna för en Redis cache.</span><span class="sxs-lookup"><span data-stu-id="91fbe-103">Gets the access keys for a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="91fbe-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="91fbe-104">SYNTAX</span></span>

```
Get-AzureRmRedisCacheKey -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="91fbe-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="91fbe-105">DESCRIPTION</span></span>
<span data-ttu-id="91fbe-106">Cmdleten **Get-AzureRmRedisCacheKey** hämtar snabb tangenterna för Azure Redis-cachen.</span><span class="sxs-lookup"><span data-stu-id="91fbe-106">The **Get-AzureRmRedisCacheKey** cmdlet gets the access keys for an Azure Redis Cache.</span></span>

## <span data-ttu-id="91fbe-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="91fbe-107">EXAMPLES</span></span>

### <span data-ttu-id="91fbe-108">Exempel 1: Hämta snabb tangenterna för en Redis cache</span><span class="sxs-lookup"><span data-stu-id="91fbe-108">Example 1: Get the access keys for a Redis Cache</span></span>
```
PS C:\>Get-AzureRmRedisCacheKey -ResourceGroupName "MyResourceGroup" -Name "MyCacheKey"
PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="91fbe-109">Det här kommandot får åtkomst nycklar som heter MyCacheKey.</span><span class="sxs-lookup"><span data-stu-id="91fbe-109">This command gets the access keys named MyCacheKey.</span></span>

## <span data-ttu-id="91fbe-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="91fbe-110">PARAMETERS</span></span>

### <span data-ttu-id="91fbe-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="91fbe-111">-Name</span></span>
<span data-ttu-id="91fbe-112">Anger namnet på en Redis-cache.</span><span class="sxs-lookup"><span data-stu-id="91fbe-112">Specifies the name of a Redis Cache.</span></span>

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

### <span data-ttu-id="91fbe-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91fbe-113">-ResourceGroupName</span></span>
<span data-ttu-id="91fbe-114">Anger namnet på den resurs grupp som innehåller Redis-cachen.</span><span class="sxs-lookup"><span data-stu-id="91fbe-114">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="91fbe-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91fbe-115">-DefaultProfile</span></span>
<span data-ttu-id="91fbe-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="91fbe-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91fbe-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91fbe-117">CommonParameters</span></span>
<span data-ttu-id="91fbe-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91fbe-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91fbe-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91fbe-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91fbe-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="91fbe-120">INPUTS</span></span>

### <span data-ttu-id="91fbe-121">Ingen</span><span class="sxs-lookup"><span data-stu-id="91fbe-121">None</span></span>
<span data-ttu-id="91fbe-122">Du kan ange indata för denna cmdlet efter egenskaps namn, men inte efter värde.</span><span class="sxs-lookup"><span data-stu-id="91fbe-122">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="91fbe-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="91fbe-123">OUTPUTS</span></span>

### <span data-ttu-id="91fbe-124">Microsoft. Azure. Management. Redis. Models. RedisAccessKeys</span><span class="sxs-lookup"><span data-stu-id="91fbe-124">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span></span>
<span data-ttu-id="91fbe-125">Denna cmdlet returnerar primära och sekundära åtkomst nycklar för en Redis cache.</span><span class="sxs-lookup"><span data-stu-id="91fbe-125">This cmdlet returns primary and secondary access keys for a Redis Cache.</span></span>

## <span data-ttu-id="91fbe-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="91fbe-126">NOTES</span></span>

## <span data-ttu-id="91fbe-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="91fbe-127">RELATED LINKS</span></span>

[<span data-ttu-id="91fbe-128">New-AzureRmRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="91fbe-128">New-AzureRmRedisCacheKey</span></span>](./New-AzureRmRedisCacheKey.md)



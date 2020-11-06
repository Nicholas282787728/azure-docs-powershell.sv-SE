---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: C0BEC701-8CE2-4B19-9F04-D32A42D9249E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/get-azurermrediscachekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheKey.md
ms.openlocfilehash: 297d02fcb77c8fc537831b2b1995bfe43ca90e73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576807"
---
# <span data-ttu-id="d4cf5-101">Get-AzureRmRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="d4cf5-101">Get-AzureRmRedisCacheKey</span></span>

## <span data-ttu-id="d4cf5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d4cf5-102">SYNOPSIS</span></span>
<span data-ttu-id="d4cf5-103">Hämtar snabb tangenterna för en Redis cache.</span><span class="sxs-lookup"><span data-stu-id="d4cf5-103">Gets the access keys for a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4cf5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d4cf5-104">SYNTAX</span></span>

```
Get-AzureRmRedisCacheKey [-ResourceGroupName <String>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d4cf5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d4cf5-105">DESCRIPTION</span></span>
<span data-ttu-id="d4cf5-106">Cmdleten **Get-AzureRmRedisCacheKey** hämtar snabb tangenterna för Azure Redis-cachen.</span><span class="sxs-lookup"><span data-stu-id="d4cf5-106">The **Get-AzureRmRedisCacheKey** cmdlet gets the access keys for an Azure Redis Cache.</span></span>

## <span data-ttu-id="d4cf5-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d4cf5-107">EXAMPLES</span></span>

### <span data-ttu-id="d4cf5-108">Exempel 1: Hämta snabb tangenterna för en Redis cache</span><span class="sxs-lookup"><span data-stu-id="d4cf5-108">Example 1: Get the access keys for a Redis Cache</span></span>
```
PS C:\>Get-AzureRmRedisCacheKey -ResourceGroupName "MyResourceGroup" -Name "MyCacheKey"
PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="d4cf5-109">Det här kommandot får åtkomst nycklar som heter MyCacheKey.</span><span class="sxs-lookup"><span data-stu-id="d4cf5-109">This command gets the access keys named MyCacheKey.</span></span>

## <span data-ttu-id="d4cf5-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d4cf5-110">PARAMETERS</span></span>

### <span data-ttu-id="d4cf5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4cf5-111">-DefaultProfile</span></span>
<span data-ttu-id="d4cf5-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d4cf5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4cf5-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="d4cf5-113">-Name</span></span>
<span data-ttu-id="d4cf5-114">Anger namnet på en Redis-cache.</span><span class="sxs-lookup"><span data-stu-id="d4cf5-114">Specifies the name of a Redis Cache.</span></span>

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

### <span data-ttu-id="d4cf5-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4cf5-115">-ResourceGroupName</span></span>
<span data-ttu-id="d4cf5-116">Anger namnet på den resurs grupp som innehåller Redis-cachen.</span><span class="sxs-lookup"><span data-stu-id="d4cf5-116">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="d4cf5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4cf5-117">CommonParameters</span></span>
<span data-ttu-id="d4cf5-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4cf5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4cf5-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4cf5-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4cf5-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d4cf5-120">INPUTS</span></span>

### <span data-ttu-id="d4cf5-121">System. String</span><span class="sxs-lookup"><span data-stu-id="d4cf5-121">System.String</span></span>

## <span data-ttu-id="d4cf5-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d4cf5-122">OUTPUTS</span></span>

### <span data-ttu-id="d4cf5-123">Microsoft. Azure. Management. Redis. Models. RedisAccessKeys</span><span class="sxs-lookup"><span data-stu-id="d4cf5-123">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span></span>

## <span data-ttu-id="d4cf5-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d4cf5-124">NOTES</span></span>

## <span data-ttu-id="d4cf5-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d4cf5-125">RELATED LINKS</span></span>

[<span data-ttu-id="d4cf5-126">New-AzureRmRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="d4cf5-126">New-AzureRmRedisCacheKey</span></span>](./New-AzureRmRedisCacheKey.md)



---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: FA99C137-68E3-47D3-A0AC-FE33A481BE66
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCacheDiagnostics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCacheDiagnostics.md
ms.openlocfilehash: 103567021d7317a6777ca5fdb01c53d1f9f023a4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584544"
---
# <span data-ttu-id="1d414-101">Set-AzureRmRedisCacheDiagnostics</span><span class="sxs-lookup"><span data-stu-id="1d414-101">Set-AzureRmRedisCacheDiagnostics</span></span>

## <span data-ttu-id="1d414-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1d414-102">SYNOPSIS</span></span>
<span data-ttu-id="1d414-103">Aktiverar diagnostik på en Azure Redis-cache.</span><span class="sxs-lookup"><span data-stu-id="1d414-103">Enables diagnostics on an Azure Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1d414-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1d414-104">SYNTAX</span></span>

```
Set-AzureRmRedisCacheDiagnostics -ResourceGroupName <String> -Name <String> -StorageAccountId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d414-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1d414-105">DESCRIPTION</span></span>
<span data-ttu-id="1d414-106">Cmdleten **set-AzureRmRedisCacheDiagnostics** aktiverar diagnostik för ett Azure Redis-cacheminne.</span><span class="sxs-lookup"><span data-stu-id="1d414-106">The **Set-AzureRmRedisCacheDiagnostics** cmdlet enables diagnostics for an Azure Redis Cache.</span></span>

## <span data-ttu-id="1d414-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1d414-107">EXAMPLES</span></span>

### <span data-ttu-id="1d414-108">Exempel 1: Aktivera diagnostik</span><span class="sxs-lookup"><span data-stu-id="1d414-108">Example 1: Enable diagnostics</span></span>
```
PS C:\>Set-AzureRmRedisCacheDiagnostics -ResourceGroupName "ContosoResourceGroup" -Name "PeakCache" -StorageAccountId "/subscriptions/fffff139-aaaa-bbbb-cccc-21f21f35806e/resourcegroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount"
```

<span data-ttu-id="1d414-109">Det här kommandot aktiverar diagnostik för ett Azure Redis-cacheminne.</span><span class="sxs-lookup"><span data-stu-id="1d414-109">This command enables diagnostics for an Azure Redis cache.</span></span>

<span data-ttu-id="1d414-110">Med det här kommandot kan du aktivera diagnostik eller uppdatera lagrings kontot för alla Azure Redis-cacheminnen i samma region för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="1d414-110">This command will enable diagnostics or update the storage account for all Azure Redis Caches in the same region for the subscription.</span></span>

## <span data-ttu-id="1d414-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1d414-111">PARAMETERS</span></span>

### <span data-ttu-id="1d414-112">-Namn</span><span class="sxs-lookup"><span data-stu-id="1d414-112">-Name</span></span>
<span data-ttu-id="1d414-113">Anger namnet på cachen.</span><span class="sxs-lookup"><span data-stu-id="1d414-113">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="1d414-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d414-114">-ResourceGroupName</span></span>
<span data-ttu-id="1d414-115">Anger namnet på den resurs grupp som innehåller cacheminnet.</span><span class="sxs-lookup"><span data-stu-id="1d414-115">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="1d414-116">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="1d414-116">-StorageAccountId</span></span>
<span data-ttu-id="1d414-117">Anger resurs-ID för det lagrings konto som används för att lagra diagnostikdata.</span><span class="sxs-lookup"><span data-stu-id="1d414-117">Specifies the resource ID of the storage account used to store the diagnostics data.</span></span>

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

### <span data-ttu-id="1d414-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d414-118">-DefaultProfile</span></span>
<span data-ttu-id="1d414-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1d414-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d414-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d414-120">CommonParameters</span></span>
<span data-ttu-id="1d414-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d414-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d414-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d414-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d414-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1d414-123">INPUTS</span></span>

### <span data-ttu-id="1d414-124">Ingen</span><span class="sxs-lookup"><span data-stu-id="1d414-124">None</span></span>

## <span data-ttu-id="1d414-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1d414-125">OUTPUTS</span></span>

### <span data-ttu-id="1d414-126">Tom</span><span class="sxs-lookup"><span data-stu-id="1d414-126">Void</span></span>

## <span data-ttu-id="1d414-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1d414-127">NOTES</span></span>
* <span data-ttu-id="1d414-128">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, Redis, cache, Web, webapp, webbplats</span><span class="sxs-lookup"><span data-stu-id="1d414-128">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="1d414-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1d414-129">RELATED LINKS</span></span>

[<span data-ttu-id="1d414-130">Remove-AzureRmRedisCacheDiagnostics</span><span class="sxs-lookup"><span data-stu-id="1d414-130">Remove-AzureRmRedisCacheDiagnostics</span></span>](./Remove-AzureRmRedisCacheDiagnostics.md)



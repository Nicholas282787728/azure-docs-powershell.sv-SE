---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: FA99C137-68E3-47D3-A0AC-FE33A481BE66
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/set-azrediscachediagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCacheDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCacheDiagnostic.md
ms.openlocfilehash: 60c552b0878907c7b2c4a56d8068968c3ace862a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324498"
---
# <span data-ttu-id="c595c-101">Set-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="c595c-101">Set-AzRedisCacheDiagnostic</span></span>

## <span data-ttu-id="c595c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c595c-102">SYNOPSIS</span></span>
<span data-ttu-id="c595c-103">Aktiverar diagnostik på en Azure Redis-cache.</span><span class="sxs-lookup"><span data-stu-id="c595c-103">Enables diagnostics on an Azure Redis Cache.</span></span>

## <span data-ttu-id="c595c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c595c-104">SYNTAX</span></span>

```
Set-AzRedisCacheDiagnostic [-ResourceGroupName <String>] -Name <String> -StorageAccountId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c595c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c595c-105">DESCRIPTION</span></span>
<span data-ttu-id="c595c-106">Cmdleten **set-AzRedisCacheDiagnostic** aktiverar diagnostik för ett Azure Redis-cacheminne.</span><span class="sxs-lookup"><span data-stu-id="c595c-106">The **Set-AzRedisCacheDiagnostic** cmdlet enables diagnostics for an Azure Redis Cache.</span></span>

## <span data-ttu-id="c595c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c595c-107">EXAMPLES</span></span>

### <span data-ttu-id="c595c-108">Exempel 1: Aktivera diagnostik</span><span class="sxs-lookup"><span data-stu-id="c595c-108">Example 1: Enable diagnostics</span></span>
```
PS C:\>Set-AzRedisCacheDiagnostic -ResourceGroupName "ContosoResourceGroup" -Name "PeakCache" -StorageAccountId "/subscriptions/fffff139-aaaa-bbbb-cccc-21f21f35806e/resourcegroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount"
```

<span data-ttu-id="c595c-109">Det här kommandot aktiverar diagnostik för ett Azure Redis-cacheminne.</span><span class="sxs-lookup"><span data-stu-id="c595c-109">This command enables diagnostics for an Azure Redis cache.</span></span>
<span data-ttu-id="c595c-110">Med det här kommandot kan du aktivera diagnostik eller uppdatera lagrings kontot för alla Azure Redis-cacheminnen i samma region för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="c595c-110">This command will enable diagnostics or update the storage account for all Azure Redis Caches in the same region for the subscription.</span></span>

## <span data-ttu-id="c595c-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c595c-111">PARAMETERS</span></span>

### <span data-ttu-id="c595c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c595c-112">-DefaultProfile</span></span>
<span data-ttu-id="c595c-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c595c-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c595c-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="c595c-114">-Name</span></span>
<span data-ttu-id="c595c-115">Anger namnet på cachen.</span><span class="sxs-lookup"><span data-stu-id="c595c-115">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="c595c-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c595c-116">-ResourceGroupName</span></span>
<span data-ttu-id="c595c-117">Anger namnet på den resurs grupp som innehåller cacheminnet.</span><span class="sxs-lookup"><span data-stu-id="c595c-117">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="c595c-118">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="c595c-118">-StorageAccountId</span></span>
<span data-ttu-id="c595c-119">Anger resurs-ID för det lagrings konto som används för att lagra diagnostikdata.</span><span class="sxs-lookup"><span data-stu-id="c595c-119">Specifies the resource ID of the storage account used to store the diagnostics data.</span></span>

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

### <span data-ttu-id="c595c-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c595c-120">-Confirm</span></span>
<span data-ttu-id="c595c-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c595c-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c595c-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c595c-122">-WhatIf</span></span>
<span data-ttu-id="c595c-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c595c-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c595c-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c595c-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c595c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c595c-125">CommonParameters</span></span>
<span data-ttu-id="c595c-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c595c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c595c-127">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c595c-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c595c-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c595c-128">INPUTS</span></span>

### <span data-ttu-id="c595c-129">System. String</span><span class="sxs-lookup"><span data-stu-id="c595c-129">System.String</span></span>

## <span data-ttu-id="c595c-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c595c-130">OUTPUTS</span></span>

### <span data-ttu-id="c595c-131">System. Void</span><span class="sxs-lookup"><span data-stu-id="c595c-131">System.Void</span></span>

## <span data-ttu-id="c595c-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c595c-132">NOTES</span></span>
* <span data-ttu-id="c595c-133">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, Redis, cache, Web, webapp, webbplats</span><span class="sxs-lookup"><span data-stu-id="c595c-133">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="c595c-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c595c-134">RELATED LINKS</span></span>

[<span data-ttu-id="c595c-135">Remove-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="c595c-135">Remove-AzRedisCacheDiagnostic</span></span>](./Remove-AzRedisCacheDiagnostic.md)


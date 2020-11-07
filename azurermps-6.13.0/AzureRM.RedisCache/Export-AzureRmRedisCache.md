---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: B447E492-D87E-4DA3-A8B0-0BAF603CCC26
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/export-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Export-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Export-AzureRmRedisCache.md
ms.openlocfilehash: ceba71f729de627e0e7231b9c295d0cad1ccc105
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756672"
---
# <span data-ttu-id="67a2e-101">Export-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="67a2e-101">Export-AzureRmRedisCache</span></span>

## <span data-ttu-id="67a2e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="67a2e-102">SYNOPSIS</span></span>
<span data-ttu-id="67a2e-103">Exporterar data från Azure Redis cacheminne till en behållare.</span><span class="sxs-lookup"><span data-stu-id="67a2e-103">Exports data from Azure Redis Cache to a container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67a2e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="67a2e-104">SYNTAX</span></span>

```
Export-AzureRmRedisCache [-ResourceGroupName <String>] -Name <String> -Prefix <String> -Container <String>
 [-Format <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="67a2e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="67a2e-105">DESCRIPTION</span></span>
<span data-ttu-id="67a2e-106">Cmdleten **export-AzureRmRedisCache** exporterar data från Azure Redis cache till en behållare.</span><span class="sxs-lookup"><span data-stu-id="67a2e-106">The **Export-AzureRmRedisCache** cmdlet exports data from Azure Redis Cache to a container.</span></span>

## <span data-ttu-id="67a2e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="67a2e-107">EXAMPLES</span></span>

### <span data-ttu-id="67a2e-108">Exempel 1: exportera data</span><span class="sxs-lookup"><span data-stu-id="67a2e-108">Example 1: Export data</span></span>
```
PS C:\>Export-AzureRmRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Prefix "blobprefix" -Container "https://mystorageaccount.blob.core.windows.net/container18?sv=2015-04-05&sr=c&sig=HezZtBZ3DURmEGDduauE7pvETY4kqlPI8JCNa8ATmaw%3D&st=2016-05-27T00%3A00%3A00Z&se=2016-05-28T00%3A00%3A00Z&sp=rwdl"
```

<span data-ttu-id="67a2e-109">Det här kommandot exporterar data från en Azure Redis-cachefil till behållaren som anges av SAS URL: en.</span><span class="sxs-lookup"><span data-stu-id="67a2e-109">This command exports data from an Azure Redis Cache instance into the container that is specified by the SAS URL.</span></span>

## <span data-ttu-id="67a2e-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="67a2e-110">PARAMETERS</span></span>

### <span data-ttu-id="67a2e-111">-Container</span><span class="sxs-lookup"><span data-stu-id="67a2e-111">-Container</span></span>
<span data-ttu-id="67a2e-112">Anger URL-adressen för tjänste-sa där denna cmdlet exporterar data.</span><span class="sxs-lookup"><span data-stu-id="67a2e-112">Specifies the Service SAS URL of container where this cmdlet exports data.</span></span> <span data-ttu-id="67a2e-113">Du kan generera en URL-adress för en tjänst genom att använda följande PowerShell-kommandon: $storageAccountContext = New-AzureStorageContext-StorageAccountName "storageName"-StorageAccountKey "Key" $sasKeyForContainer = New-AzureStorageContainerSASToken-namn "ContainerName"-permission "rwdl"-StartTime ([system. DateTime]:: nu). AddMinutes (-15)-ExpiryTime ([system. DateTime]:: nu). AddHours (5)-kontext $storageAccountContext-FullUri Export-AzureRmRedisCache-ResourceGroupName "ResourceGroupName"-name "cacheName"-prefix "blobprefix"-container ($sasKeyForContainer)</span><span class="sxs-lookup"><span data-stu-id="67a2e-113">You can generate a Service SAS URL using the following PowerShell commands: $storageAccountContext = New-AzureStorageContext -StorageAccountName "storageName" -StorageAccountKey "key" $sasKeyForContainer = New-AzureStorageContainerSASToken -Name "containername" -Permission "rwdl" -StartTime ([System.DateTime]::Now).AddMinutes(-15) -ExpiryTime ([System.DateTime]::Now).AddHours(5) -Context $storageAccountContext -FullUri Export-AzureRmRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Prefix "blobprefix" -Container ($sasKeyForContainer)</span></span>

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

### <span data-ttu-id="67a2e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67a2e-114">-DefaultProfile</span></span>
<span data-ttu-id="67a2e-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="67a2e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67a2e-116">-Format</span><span class="sxs-lookup"><span data-stu-id="67a2e-116">-Format</span></span>
<span data-ttu-id="67a2e-117">Anger ett format för blobben.</span><span class="sxs-lookup"><span data-stu-id="67a2e-117">Specifies a format for the blob.</span></span>
<span data-ttu-id="67a2e-118">För närvarande är RDB det enda format som stöds.</span><span class="sxs-lookup"><span data-stu-id="67a2e-118">Currently rdb is the only supported format.</span></span>

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

### <span data-ttu-id="67a2e-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="67a2e-119">-Name</span></span>
<span data-ttu-id="67a2e-120">Anger namnet på en cache.</span><span class="sxs-lookup"><span data-stu-id="67a2e-120">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="67a2e-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="67a2e-121">-PassThru</span></span>
<span data-ttu-id="67a2e-122">Anger att denna cmdlet returnerar ett booleskt värde som anger om åtgärden lyckades.</span><span class="sxs-lookup"><span data-stu-id="67a2e-122">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="67a2e-123">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="67a2e-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="67a2e-124">-Prefix</span><span class="sxs-lookup"><span data-stu-id="67a2e-124">-Prefix</span></span>
<span data-ttu-id="67a2e-125">Anger ett prefix som ska användas för BLOB-namn.</span><span class="sxs-lookup"><span data-stu-id="67a2e-125">Specifies a prefix to use for blob names.</span></span>

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

### <span data-ttu-id="67a2e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67a2e-126">-ResourceGroupName</span></span>
<span data-ttu-id="67a2e-127">Anger namnet på den resurs grupp som innehåller cacheminnet.</span><span class="sxs-lookup"><span data-stu-id="67a2e-127">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="67a2e-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="67a2e-128">-Confirm</span></span>
<span data-ttu-id="67a2e-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="67a2e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67a2e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67a2e-130">-WhatIf</span></span>
<span data-ttu-id="67a2e-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="67a2e-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="67a2e-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="67a2e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67a2e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67a2e-133">CommonParameters</span></span>
<span data-ttu-id="67a2e-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67a2e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67a2e-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67a2e-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67a2e-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="67a2e-136">INPUTS</span></span>

### <span data-ttu-id="67a2e-137">System. String</span><span class="sxs-lookup"><span data-stu-id="67a2e-137">System.String</span></span>

## <span data-ttu-id="67a2e-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="67a2e-138">OUTPUTS</span></span>

### <span data-ttu-id="67a2e-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="67a2e-139">System.Boolean</span></span>

## <span data-ttu-id="67a2e-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="67a2e-140">NOTES</span></span>
* <span data-ttu-id="67a2e-141">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, Redis, cache, Web, webapp, webbplats</span><span class="sxs-lookup"><span data-stu-id="67a2e-141">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="67a2e-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="67a2e-142">RELATED LINKS</span></span>

[<span data-ttu-id="67a2e-143">Import-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="67a2e-143">Import-AzureRmRedisCache</span></span>](./Import-AzureRmRedisCache.md)

[<span data-ttu-id="67a2e-144">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="67a2e-144">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="67a2e-145">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="67a2e-145">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="67a2e-146">Reset-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="67a2e-146">Reset-AzureRmRedisCache</span></span>](./Reset-AzureRmRedisCache.md)

[<span data-ttu-id="67a2e-147">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="67a2e-147">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)



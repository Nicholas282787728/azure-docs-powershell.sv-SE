---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: B447E492-D87E-4DA3-A8B0-0BAF603CCC26
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/export-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Export-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Export-AzureRmRedisCache.md
ms.openlocfilehash: cd19fe8052ae95f547971452f4364f279f365cac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575557"
---
# <span data-ttu-id="8468b-101">Export-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="8468b-101">Export-AzureRmRedisCache</span></span>

## <span data-ttu-id="8468b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8468b-102">SYNOPSIS</span></span>
<span data-ttu-id="8468b-103">Exporterar data från Azure Redis cacheminne till en behållare.</span><span class="sxs-lookup"><span data-stu-id="8468b-103">Exports data from Azure Redis Cache to a container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8468b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8468b-104">SYNTAX</span></span>

```
Export-AzureRmRedisCache [-ResourceGroupName <String>] -Name <String> -Prefix <String> -Container <String>
 [-Format <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8468b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8468b-105">DESCRIPTION</span></span>
<span data-ttu-id="8468b-106">Cmdleten **export-AzureRmRedisCache** exporterar data från Azure Redis cache till en behållare.</span><span class="sxs-lookup"><span data-stu-id="8468b-106">The **Export-AzureRmRedisCache** cmdlet exports data from Azure Redis Cache to a container.</span></span>

## <span data-ttu-id="8468b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8468b-107">EXAMPLES</span></span>

### <span data-ttu-id="8468b-108">Exempel 1: exportera data</span><span class="sxs-lookup"><span data-stu-id="8468b-108">Example 1: Export data</span></span>
```
PS C:\>Export-AzureRmRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Prefix "blobprefix" -Container "https://mystorageaccount.blob.core.windows.net/container18?sv=2015-04-05&sr=c&sig=HezZtBZ3DURmEGDduauE7pvETY4kqlPI8JCNa8ATmaw%3D&st=2016-05-27T00%3A00%3A00Z&se=2016-05-28T00%3A00%3A00Z&sp=rwdl"
```

<span data-ttu-id="8468b-109">Det här kommandot exporterar data från en Azure Redis-cachefil till behållaren som anges av SAS URL: en.</span><span class="sxs-lookup"><span data-stu-id="8468b-109">This command exports data from an Azure Redis Cache instance into the container that is specified by the SAS URL.</span></span>

## <span data-ttu-id="8468b-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8468b-110">PARAMETERS</span></span>

### <span data-ttu-id="8468b-111">-Container</span><span class="sxs-lookup"><span data-stu-id="8468b-111">-Container</span></span>
<span data-ttu-id="8468b-112">Anger URL-adressen för tjänste-sa där denna cmdlet exporterar data.</span><span class="sxs-lookup"><span data-stu-id="8468b-112">Specifies the Service SAS URL of container where this cmdlet exports data.</span></span> <span data-ttu-id="8468b-113">Du kan generera en URL-adress för en tjänst genom att använda följande PowerShell-kommandon:</span><span class="sxs-lookup"><span data-stu-id="8468b-113">You can generate a Service SAS URL using the following PowerShell commands:</span></span>

<span data-ttu-id="8468b-114">$storageAccountContext = New-AzureStorageContext-StorageAccountName "storageName"-StorageAccountKey "Key"</span><span class="sxs-lookup"><span data-stu-id="8468b-114">$storageAccountContext = New-AzureStorageContext -StorageAccountName "storageName" -StorageAccountKey "key"</span></span>

<span data-ttu-id="8468b-115">$sasKeyForContainer = New-AzureStorageContainerSASToken-namn "ContainerName"-permission "rwdl"-StartTime ([system. DateTime]:: nu). AddMinutes (-15)-ExpiryTime ([system. DateTime]:: nu). AddHours (5)-kontext $storageAccountContext-FullUri</span><span class="sxs-lookup"><span data-stu-id="8468b-115">$sasKeyForContainer = New-AzureStorageContainerSASToken -Name "containername" -Permission "rwdl" -StartTime ([System.DateTime]::Now).AddMinutes(-15) -ExpiryTime ([System.DateTime]::Now).AddHours(5) -Context $storageAccountContext -FullUri</span></span> 

<span data-ttu-id="8468b-116">Export-AzureRmRedisCache-ResourceGroupName "ResourceGroupName"-name "cacheName"-prefix "blobprefix"-container ($sasKeyForContainer)</span><span class="sxs-lookup"><span data-stu-id="8468b-116">Export-AzureRmRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Prefix "blobprefix" -Container ($sasKeyForContainer)</span></span>

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

### <span data-ttu-id="8468b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8468b-117">-DefaultProfile</span></span>
<span data-ttu-id="8468b-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8468b-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8468b-119">-Format</span><span class="sxs-lookup"><span data-stu-id="8468b-119">-Format</span></span>
<span data-ttu-id="8468b-120">Anger ett format för blobben.</span><span class="sxs-lookup"><span data-stu-id="8468b-120">Specifies a format for the blob.</span></span>
<span data-ttu-id="8468b-121">För närvarande är RDB det enda format som stöds.</span><span class="sxs-lookup"><span data-stu-id="8468b-121">Currently rdb is the only supported format.</span></span>

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

### <span data-ttu-id="8468b-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="8468b-122">-Name</span></span>
<span data-ttu-id="8468b-123">Anger namnet på en cache.</span><span class="sxs-lookup"><span data-stu-id="8468b-123">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="8468b-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8468b-124">-PassThru</span></span>
<span data-ttu-id="8468b-125">Anger att denna cmdlet returnerar ett booleskt värde som anger om åtgärden lyckades.</span><span class="sxs-lookup"><span data-stu-id="8468b-125">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="8468b-126">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="8468b-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8468b-127">-Prefix</span><span class="sxs-lookup"><span data-stu-id="8468b-127">-Prefix</span></span>
<span data-ttu-id="8468b-128">Anger ett prefix som ska användas för BLOB-namn.</span><span class="sxs-lookup"><span data-stu-id="8468b-128">Specifies a prefix to use for blob names.</span></span>

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

### <span data-ttu-id="8468b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8468b-129">-ResourceGroupName</span></span>
<span data-ttu-id="8468b-130">Anger namnet på den resurs grupp som innehåller cacheminnet.</span><span class="sxs-lookup"><span data-stu-id="8468b-130">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="8468b-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8468b-131">-Confirm</span></span>
<span data-ttu-id="8468b-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8468b-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8468b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8468b-133">-WhatIf</span></span>
<span data-ttu-id="8468b-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8468b-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8468b-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8468b-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8468b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8468b-136">CommonParameters</span></span>
<span data-ttu-id="8468b-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8468b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8468b-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8468b-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8468b-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8468b-139">INPUTS</span></span>

### <span data-ttu-id="8468b-140">Ingen</span><span class="sxs-lookup"><span data-stu-id="8468b-140">None</span></span>
<span data-ttu-id="8468b-141">Du kan ange indata för denna cmdlet efter egenskaps namn, men inte efter värde.</span><span class="sxs-lookup"><span data-stu-id="8468b-141">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="8468b-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8468b-142">OUTPUTS</span></span>

### <span data-ttu-id="8468b-143">Ingen</span><span class="sxs-lookup"><span data-stu-id="8468b-143">None</span></span>

## <span data-ttu-id="8468b-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8468b-144">NOTES</span></span>
* <span data-ttu-id="8468b-145">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, Redis, cache, Web, webapp, webbplats</span><span class="sxs-lookup"><span data-stu-id="8468b-145">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="8468b-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8468b-146">RELATED LINKS</span></span>

[<span data-ttu-id="8468b-147">Import-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="8468b-147">Import-AzureRmRedisCache</span></span>](./Import-AzureRmRedisCache.md)

[<span data-ttu-id="8468b-148">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="8468b-148">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="8468b-149">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="8468b-149">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="8468b-150">Reset-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="8468b-150">Reset-AzureRmRedisCache</span></span>](./Reset-AzureRmRedisCache.md)

[<span data-ttu-id="8468b-151">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="8468b-151">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)



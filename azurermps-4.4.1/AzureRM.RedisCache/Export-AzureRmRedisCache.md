---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: B447E492-D87E-4DA3-A8B0-0BAF603CCC26
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Export-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Export-AzureRmRedisCache.md
ms.openlocfilehash: 0edfec1d98423f444b2291d43e6f2a3489e20b29
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582232"
---
# <span data-ttu-id="52498-101">Export-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="52498-101">Export-AzureRmRedisCache</span></span>

## <span data-ttu-id="52498-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="52498-102">SYNOPSIS</span></span>
<span data-ttu-id="52498-103">Exporterar data från Azure Redis cacheminne till en behållare.</span><span class="sxs-lookup"><span data-stu-id="52498-103">Exports data from Azure Redis Cache to a container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52498-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="52498-104">SYNTAX</span></span>

```
Export-AzureRmRedisCache -ResourceGroupName <String> -Name <String> -Prefix <String> -Container <String>
 [-Format <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52498-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="52498-105">DESCRIPTION</span></span>
<span data-ttu-id="52498-106">Cmdleten **export-AzureRmRedisCache** exporterar data från Azure Redis cache till en behållare.</span><span class="sxs-lookup"><span data-stu-id="52498-106">The **Export-AzureRmRedisCache** cmdlet exports data from Azure Redis Cache to a container.</span></span>

## <span data-ttu-id="52498-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="52498-107">EXAMPLES</span></span>

### <span data-ttu-id="52498-108">Exempel 1: exportera data</span><span class="sxs-lookup"><span data-stu-id="52498-108">Example 1: Export data</span></span>
```
PS C:\>Export-AzureRmRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Prefix "blobprefix" -Container "https://mystorageaccount.blob.core.windows.net/container18?sv=2015-04-05&sr=c&sig=HezZtBZ3DURmEGDduauE7pvETY4kqlPI8JCNa8ATmaw%3D&st=2016-05-27T00%3A00%3A00Z&se=2016-05-28T00%3A00%3A00Z&sp=rwdl"
```

<span data-ttu-id="52498-109">Det här kommandot exporterar data från en Azure Redis-cachefil till behållaren som anges av SAS URL: en.</span><span class="sxs-lookup"><span data-stu-id="52498-109">This command exports data from an Azure Redis Cache instance into the container that is specified by the SAS URL.</span></span>

## <span data-ttu-id="52498-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="52498-110">PARAMETERS</span></span>

### <span data-ttu-id="52498-111">-Container</span><span class="sxs-lookup"><span data-stu-id="52498-111">-Container</span></span>
<span data-ttu-id="52498-112">Anger URL-adressen för tjänste-sa där denna cmdlet exporterar data.</span><span class="sxs-lookup"><span data-stu-id="52498-112">Specifies the Service SAS URL of container where this cmdlet exports data.</span></span> <span data-ttu-id="52498-113">Du kan generera en URL-adress för en tjänst genom att använda följande PowerShell-kommandon:</span><span class="sxs-lookup"><span data-stu-id="52498-113">You can generate a Service SAS URL using the following PowerShell commands:</span></span>

<span data-ttu-id="52498-114">$storageAccountContext = New-AzureStorageContext-StorageAccountName "storageName"-StorageAccountKey "Key"</span><span class="sxs-lookup"><span data-stu-id="52498-114">$storageAccountContext = New-AzureStorageContext -StorageAccountName "storageName" -StorageAccountKey "key"</span></span>

<span data-ttu-id="52498-115">$sasKeyForContainer = New-AzureStorageContainerSASToken-namn "ContainerName"-permission "rwdl"-StartTime ([system. DateTime]:: nu). AddMinutes (-15)-ExpiryTime ([system. DateTime]:: nu). AddHours (5)-kontext $storageAccountContext-FullUri</span><span class="sxs-lookup"><span data-stu-id="52498-115">$sasKeyForContainer = New-AzureStorageContainerSASToken -Name "containername" -Permission "rwdl" -StartTime ([System.DateTime]::Now).AddMinutes(-15) -ExpiryTime ([System.DateTime]::Now).AddHours(5) -Context $storageAccountContext -FullUri</span></span> 

<span data-ttu-id="52498-116">Export-AzureRmRedisCache-ResourceGroupName "ResourceGroupName"-name "cacheName"-prefix "blobprefix"-container ($sasKeyForContainer)</span><span class="sxs-lookup"><span data-stu-id="52498-116">Export-AzureRmRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Prefix "blobprefix" -Container ($sasKeyForContainer)</span></span>

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

### <span data-ttu-id="52498-117">-Format</span><span class="sxs-lookup"><span data-stu-id="52498-117">-Format</span></span>
<span data-ttu-id="52498-118">Anger ett format för blobben.</span><span class="sxs-lookup"><span data-stu-id="52498-118">Specifies a format for the blob.</span></span>
<span data-ttu-id="52498-119">För närvarande är RDB det enda format som stöds.</span><span class="sxs-lookup"><span data-stu-id="52498-119">Currently rdb is the only supported format.</span></span>

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

### <span data-ttu-id="52498-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="52498-120">-Name</span></span>
<span data-ttu-id="52498-121">Anger namnet på en cache.</span><span class="sxs-lookup"><span data-stu-id="52498-121">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="52498-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="52498-122">-PassThru</span></span>
<span data-ttu-id="52498-123">Anger att denna cmdlet returnerar ett booleskt värde som anger om åtgärden lyckades.</span><span class="sxs-lookup"><span data-stu-id="52498-123">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="52498-124">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="52498-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="52498-125">-Prefix</span><span class="sxs-lookup"><span data-stu-id="52498-125">-Prefix</span></span>
<span data-ttu-id="52498-126">Anger ett prefix som ska användas för BLOB-namn.</span><span class="sxs-lookup"><span data-stu-id="52498-126">Specifies a prefix to use for blob names.</span></span>

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

### <span data-ttu-id="52498-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52498-127">-ResourceGroupName</span></span>
<span data-ttu-id="52498-128">Anger namnet på den resurs grupp som innehåller cacheminnet.</span><span class="sxs-lookup"><span data-stu-id="52498-128">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="52498-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52498-129">-DefaultProfile</span></span>
<span data-ttu-id="52498-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="52498-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52498-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52498-131">CommonParameters</span></span>
<span data-ttu-id="52498-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52498-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52498-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52498-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52498-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="52498-134">INPUTS</span></span>

### <span data-ttu-id="52498-135">Ingen</span><span class="sxs-lookup"><span data-stu-id="52498-135">None</span></span>
<span data-ttu-id="52498-136">Du kan ange indata för denna cmdlet efter egenskaps namn, men inte efter värde.</span><span class="sxs-lookup"><span data-stu-id="52498-136">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="52498-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="52498-137">OUTPUTS</span></span>

### <span data-ttu-id="52498-138">Ingen</span><span class="sxs-lookup"><span data-stu-id="52498-138">None</span></span>

## <span data-ttu-id="52498-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="52498-139">NOTES</span></span>
* <span data-ttu-id="52498-140">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, Redis, cache, Web, webapp, webbplats</span><span class="sxs-lookup"><span data-stu-id="52498-140">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="52498-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="52498-141">RELATED LINKS</span></span>

[<span data-ttu-id="52498-142">Import-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="52498-142">Import-AzureRmRedisCache</span></span>](./Import-AzureRmRedisCache.md)

[<span data-ttu-id="52498-143">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="52498-143">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="52498-144">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="52498-144">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="52498-145">Reset-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="52498-145">Reset-AzureRmRedisCache</span></span>](./Reset-AzureRmRedisCache.md)

[<span data-ttu-id="52498-146">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="52498-146">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)



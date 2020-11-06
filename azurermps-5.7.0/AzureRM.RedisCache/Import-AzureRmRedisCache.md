---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: BC00DEF9-6A93-4DF5-8E5B-C488551BA1D1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/import-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Import-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Import-AzureRmRedisCache.md
ms.openlocfilehash: ff7ac13080d3d5cb717cf7efbff322cabf83cc3a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575554"
---
# <span data-ttu-id="ef044-101">Import-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="ef044-101">Import-AzureRmRedisCache</span></span>

## <span data-ttu-id="ef044-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ef044-102">SYNOPSIS</span></span>
<span data-ttu-id="ef044-103">Importerar data från blobbar till Azure Redis cache.</span><span class="sxs-lookup"><span data-stu-id="ef044-103">Imports data from blobs to Azure Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef044-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ef044-104">SYNTAX</span></span>

```
Import-AzureRmRedisCache [-ResourceGroupName <String>] -Name <String> -Files <String[]> [-Format <String>]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef044-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ef044-105">DESCRIPTION</span></span>
<span data-ttu-id="ef044-106">Cmdleten **import-AzureRmRedisCache** importerar data från blobbar till Azure Redis-cachen.</span><span class="sxs-lookup"><span data-stu-id="ef044-106">The **Import-AzureRmRedisCache** cmdlet imports data from blobs into Azure Redis Cache.</span></span>

## <span data-ttu-id="ef044-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ef044-107">EXAMPLES</span></span>

### <span data-ttu-id="ef044-108">Exempel 1: importera data</span><span class="sxs-lookup"><span data-stu-id="ef044-108">Example 1: Import data</span></span>
```
PS C:\>Import-AzureRmRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Files @("https://mystorageaccount.blob.core.windows.net/container22/blobname?sv=2015-04-05&sr=b&sig=caIwutG2uDa0NZ8mjdNJdgOY8%2F8mhwRuGNdICU%2B0pI4%3D&st=2016-05-27T00%3A00%3A00Z&se=2016-05-28T00%3A00%3A00Z&sp=rwd") -Force
```

<span data-ttu-id="ef044-109">Det här kommandot importerar data från blobben som anges av SAS URL: en till Azure Redis cache.</span><span class="sxs-lookup"><span data-stu-id="ef044-109">This command imports data from the blob that is specified by the SAS URL into Azure Redis Cache.</span></span>

## <span data-ttu-id="ef044-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ef044-110">PARAMETERS</span></span>

### <span data-ttu-id="ef044-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef044-111">-DefaultProfile</span></span>
<span data-ttu-id="ef044-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ef044-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef044-113">-Filer</span><span class="sxs-lookup"><span data-stu-id="ef044-113">-Files</span></span>
<span data-ttu-id="ef044-114">Anger SAS-URL: er för blobbar vars innehåll denna cmdlet importerar till cacheminnet.</span><span class="sxs-lookup"><span data-stu-id="ef044-114">Specifies the SAS URLs of blobs whose content this cmdlet imports into the cache.</span></span> <span data-ttu-id="ef044-115">Du kan skapa SAS-adresser med följande PowerShell-kommandon:</span><span class="sxs-lookup"><span data-stu-id="ef044-115">You can generate the SAS URLs using the following PowerShell commands:</span></span>

<span data-ttu-id="ef044-116">$storageAccountContext = New-AzureStorageContext-StorageAccountName "storageName"-StorageAccountKey "Key"</span><span class="sxs-lookup"><span data-stu-id="ef044-116">$storageAccountContext = New-AzureStorageContext -StorageAccountName "storageName" -StorageAccountKey "key"</span></span>

<span data-ttu-id="ef044-117">$sasKeyForBlob = New-AzureStorageBlobSASToken-container "containerName"-BLOB "blobName"-permission "rwdl"-StartTime ([system. DateTime]:: nu). AddMinutes (-15)-ExpiryTime ([system. DateTime]:: nu). AddHours (5)-kontext $storageAccountContext-FullUri</span><span class="sxs-lookup"><span data-stu-id="ef044-117">$sasKeyForBlob = New-AzureStorageBlobSASToken -Container "containerName" -blob "blobName" -Permission "rwdl" -StartTime ([System.DateTime]::Now).AddMinutes(-15) -ExpiryTime ([System.DateTime]::Now).AddHours(5) -Context $storageAccountContext -FullUri</span></span>

<span data-ttu-id="ef044-118">Import-AzureRmRedisCache-ResourceGroupName "ResourceGroupName"-name "cacheName"-filer ($sasKeyForBlob)-Force</span><span class="sxs-lookup"><span data-stu-id="ef044-118">Import-AzureRmRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Files ($sasKeyForBlob) -Force</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef044-119">-Force</span><span class="sxs-lookup"><span data-stu-id="ef044-119">-Force</span></span>
<span data-ttu-id="ef044-120">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="ef044-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ef044-121">-Format</span><span class="sxs-lookup"><span data-stu-id="ef044-121">-Format</span></span>
<span data-ttu-id="ef044-122">Anger formatet för blobben.</span><span class="sxs-lookup"><span data-stu-id="ef044-122">Specifies the format of the blob.</span></span>
<span data-ttu-id="ef044-123">För närvarande är RDB det enda format som stöds.</span><span class="sxs-lookup"><span data-stu-id="ef044-123">Currently rdb is the only supported format.</span></span>

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

### <span data-ttu-id="ef044-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="ef044-124">-Name</span></span>
<span data-ttu-id="ef044-125">Anger namnet på en cache.</span><span class="sxs-lookup"><span data-stu-id="ef044-125">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="ef044-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ef044-126">-PassThru</span></span>
<span data-ttu-id="ef044-127">Anger att denna cmdlet returnerar ett booleskt värde som anger om åtgärden lyckades.</span><span class="sxs-lookup"><span data-stu-id="ef044-127">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="ef044-128">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="ef044-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ef044-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef044-129">-ResourceGroupName</span></span>
<span data-ttu-id="ef044-130">Anger namnet på den resurs grupp som innehåller cacheminnet.</span><span class="sxs-lookup"><span data-stu-id="ef044-130">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="ef044-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ef044-131">-Confirm</span></span>
<span data-ttu-id="ef044-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ef044-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef044-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef044-133">-WhatIf</span></span>
<span data-ttu-id="ef044-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ef044-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef044-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ef044-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef044-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef044-136">CommonParameters</span></span>
<span data-ttu-id="ef044-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef044-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef044-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef044-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef044-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ef044-139">INPUTS</span></span>

### <span data-ttu-id="ef044-140">Ingen</span><span class="sxs-lookup"><span data-stu-id="ef044-140">None</span></span>
<span data-ttu-id="ef044-141">Du kan ange indata för denna cmdlet efter egenskaps namn, men inte efter värde.</span><span class="sxs-lookup"><span data-stu-id="ef044-141">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="ef044-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ef044-142">OUTPUTS</span></span>

### <span data-ttu-id="ef044-143">Ingen</span><span class="sxs-lookup"><span data-stu-id="ef044-143">None</span></span>

## <span data-ttu-id="ef044-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ef044-144">NOTES</span></span>
* <span data-ttu-id="ef044-145">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, Redis, cache, Web, webapp, webbplats</span><span class="sxs-lookup"><span data-stu-id="ef044-145">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="ef044-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ef044-146">RELATED LINKS</span></span>

[<span data-ttu-id="ef044-147">Exportera-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="ef044-147">Export-AzureRmRedisCache</span></span>](./Export-AzureRmRedisCache.md)

[<span data-ttu-id="ef044-148">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="ef044-148">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="ef044-149">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="ef044-149">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="ef044-150">Reset-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="ef044-150">Reset-AzureRmRedisCache</span></span>](./Reset-AzureRmRedisCache.md)

[<span data-ttu-id="ef044-151">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="ef044-151">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)



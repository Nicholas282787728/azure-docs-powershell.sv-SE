---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: BC00DEF9-6A93-4DF5-8E5B-C488551BA1D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/import-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Import-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Import-AzRedisCache.md
ms.openlocfilehash: 1f51f156a0f45b014e9ff521adb959bdbd86bef7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98521724"
---
# <span data-ttu-id="f4cf5-101">Import-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="f4cf5-101">Import-AzRedisCache</span></span>

## <span data-ttu-id="f4cf5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f4cf5-102">SYNOPSIS</span></span>
<span data-ttu-id="f4cf5-103">Importerar data från blobbar till Azure Redis cache.</span><span class="sxs-lookup"><span data-stu-id="f4cf5-103">Imports data from blobs to Azure Redis Cache.</span></span>

## <span data-ttu-id="f4cf5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f4cf5-104">SYNTAX</span></span>

```
Import-AzRedisCache [-ResourceGroupName <String>] -Name <String> -Files <String[]> [-Format <String>] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4cf5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f4cf5-105">DESCRIPTION</span></span>
<span data-ttu-id="f4cf5-106">Cmdleten **import-AzRedisCache** importerar data från blobbar till Azure Redis-cachen.</span><span class="sxs-lookup"><span data-stu-id="f4cf5-106">The **Import-AzRedisCache** cmdlet imports data from blobs into Azure Redis Cache.</span></span>

## <span data-ttu-id="f4cf5-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f4cf5-107">EXAMPLES</span></span>

### <span data-ttu-id="f4cf5-108">Exempel 1: importera data</span><span class="sxs-lookup"><span data-stu-id="f4cf5-108">Example 1: Import data</span></span>
```
PS C:\>Import-AzRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Files @("https://mystorageaccount.blob.core.windows.net/container22/blobname?sv=2015-04-05&sr=b&sig=caIwutG2uDa0NZ8mjdNJdgOY8%2F8mhwRuGNdICU%2B0pI4%3D&st=2016-05-27T00%3A00%3A00Z&se=2016-05-28T00%3A00%3A00Z&sp=rwd") -Force
```

<span data-ttu-id="f4cf5-109">Det här kommandot importerar data från blobben som anges av SAS URL: en till Azure Redis cache.</span><span class="sxs-lookup"><span data-stu-id="f4cf5-109">This command imports data from the blob that is specified by the SAS URL into Azure Redis Cache.</span></span>

## <span data-ttu-id="f4cf5-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f4cf5-110">PARAMETERS</span></span>

### <span data-ttu-id="f4cf5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4cf5-111">-DefaultProfile</span></span>
<span data-ttu-id="f4cf5-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f4cf5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4cf5-113">-Filer</span><span class="sxs-lookup"><span data-stu-id="f4cf5-113">-Files</span></span>
<span data-ttu-id="f4cf5-114">Anger SAS-URL: er för blobbar vars innehåll denna cmdlet importerar till cacheminnet.</span><span class="sxs-lookup"><span data-stu-id="f4cf5-114">Specifies the SAS URLs of blobs whose content this cmdlet imports into the cache.</span></span> <span data-ttu-id="f4cf5-115">Du kan skapa SAS-webbadresserna med följande PowerShell-kommandon: $storageAccountContext = New-AzStorageContext-StorageAccountName "storageName"-StorageAccountKey "nyckeln" $sasKeyForBlob = New-AzStorageBlobSASToken-container "containerName"-BLOB "blobName"-permission "rwdl"-StartTime ([system. DateTime]:: nu). AddMinutes (-15)-ExpiryTime ([system. DateTime]:: nu). AddHours (5)-kontext $storageAccountContext-FullUri Import-AzRedisCache-ResourceGroupName "ResourceGroupName"-name "cacheName"-filer ($sasKeyForBlob)-Force</span><span class="sxs-lookup"><span data-stu-id="f4cf5-115">You can generate the SAS URLs using the following PowerShell commands: $storageAccountContext = New-AzStorageContext -StorageAccountName "storageName" -StorageAccountKey "key" $sasKeyForBlob = New-AzStorageBlobSASToken -Container "containerName" -blob "blobName" -Permission "rwdl" -StartTime ([System.DateTime]::Now).AddMinutes(-15) -ExpiryTime ([System.DateTime]::Now).AddHours(5) -Context $storageAccountContext -FullUri Import-AzRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Files ($sasKeyForBlob) -Force</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4cf5-116">-Force</span><span class="sxs-lookup"><span data-stu-id="f4cf5-116">-Force</span></span>
<span data-ttu-id="f4cf5-117">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="f4cf5-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f4cf5-118">-Format</span><span class="sxs-lookup"><span data-stu-id="f4cf5-118">-Format</span></span>
<span data-ttu-id="f4cf5-119">Anger formatet för blobben.</span><span class="sxs-lookup"><span data-stu-id="f4cf5-119">Specifies the format of the blob.</span></span>
<span data-ttu-id="f4cf5-120">För närvarande är RDB det enda format som stöds.</span><span class="sxs-lookup"><span data-stu-id="f4cf5-120">Currently rdb is the only supported format.</span></span>

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

### <span data-ttu-id="f4cf5-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="f4cf5-121">-Name</span></span>
<span data-ttu-id="f4cf5-122">Anger namnet på en cache.</span><span class="sxs-lookup"><span data-stu-id="f4cf5-122">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="f4cf5-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f4cf5-123">-PassThru</span></span>
<span data-ttu-id="f4cf5-124">Anger att denna cmdlet returnerar ett booleskt värde som anger om åtgärden lyckades.</span><span class="sxs-lookup"><span data-stu-id="f4cf5-124">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="f4cf5-125">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="f4cf5-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f4cf5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4cf5-126">-ResourceGroupName</span></span>
<span data-ttu-id="f4cf5-127">Anger namnet på den resurs grupp som innehåller cacheminnet.</span><span class="sxs-lookup"><span data-stu-id="f4cf5-127">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="f4cf5-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f4cf5-128">-Confirm</span></span>
<span data-ttu-id="f4cf5-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f4cf5-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4cf5-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4cf5-130">-WhatIf</span></span>
<span data-ttu-id="f4cf5-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f4cf5-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4cf5-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f4cf5-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4cf5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4cf5-133">CommonParameters</span></span>
<span data-ttu-id="f4cf5-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4cf5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4cf5-135">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4cf5-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4cf5-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f4cf5-136">INPUTS</span></span>

### <span data-ttu-id="f4cf5-137">System. String</span><span class="sxs-lookup"><span data-stu-id="f4cf5-137">System.String</span></span>

### <span data-ttu-id="f4cf5-138">System. string []</span><span class="sxs-lookup"><span data-stu-id="f4cf5-138">System.String[]</span></span>

## <span data-ttu-id="f4cf5-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f4cf5-139">OUTPUTS</span></span>

### <span data-ttu-id="f4cf5-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f4cf5-140">System.Boolean</span></span>

## <span data-ttu-id="f4cf5-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f4cf5-141">NOTES</span></span>
* <span data-ttu-id="f4cf5-142">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, Redis, cache, Web, webapp, webbplats</span><span class="sxs-lookup"><span data-stu-id="f4cf5-142">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="f4cf5-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f4cf5-143">RELATED LINKS</span></span>

[<span data-ttu-id="f4cf5-144">Exportera-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="f4cf5-144">Export-AzRedisCache</span></span>](./Export-AzRedisCache.md)

[<span data-ttu-id="f4cf5-145">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="f4cf5-145">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="f4cf5-146">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="f4cf5-146">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="f4cf5-147">Reset-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="f4cf5-147">Reset-AzRedisCache</span></span>](./Reset-AzRedisCache.md)

[<span data-ttu-id="f4cf5-148">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="f4cf5-148">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)



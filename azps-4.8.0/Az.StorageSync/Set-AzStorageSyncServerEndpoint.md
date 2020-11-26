---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/set-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: b8adfd7c069c4215ec8f26d259ed9d1bc39be2d9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94103384"
---
# <span data-ttu-id="7bc1b-101">Set-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7bc1b-101">Set-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="7bc1b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7bc1b-102">SYNOPSIS</span></span>
<span data-ttu-id="7bc1b-103">Det här kommandot möjliggör ändringar i de justerbara parametrarna för en server slut punkt.</span><span class="sxs-lookup"><span data-stu-id="7bc1b-103">This command allows for changes on the adjustable parameters of a server endpoint.</span></span>

## <span data-ttu-id="7bc1b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7bc1b-104">SYNTAX</span></span>

### <span data-ttu-id="7bc1b-105">StringParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="7bc1b-105">StringParameterSet (Default)</span></span>
```
Set-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>]
 [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [LocalCacheMode] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7bc1b-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7bc1b-106">ResourceIdParameterSet</span></span>
```
Set-AzStorageSyncServerEndpoint [-ResourceId] <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>]
 [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [LocalCacheMode] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7bc1b-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7bc1b-107">ObjectParameterSet</span></span>
```
Set-AzStorageSyncServerEndpoint [-InputObject] <PSServerEndpoint> [-CloudTiering]
 [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [LocalCacheMode] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7bc1b-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7bc1b-108">DESCRIPTION</span></span>
<span data-ttu-id="7bc1b-109">Det här kommandot möjliggör ändringar i de justerbara parametrarna för en server slut punkt.</span><span class="sxs-lookup"><span data-stu-id="7bc1b-109">This command allows for changes on the adjustable parameters of a server endpoint.</span></span> <span data-ttu-id="7bc1b-110">Principer för moln skiktning och moln nivå kan ändras när som helst.</span><span class="sxs-lookup"><span data-stu-id="7bc1b-110">For instance cloud tiering and cloud tiering policies can be changed at any time.</span></span> <span data-ttu-id="7bc1b-111">Flera delar av en server slut punkt, till exempel den lokala sökvägen, kan inte ändras efter att Server slut punkten skapades.</span><span class="sxs-lookup"><span data-stu-id="7bc1b-111">Several aspects of a server endpoint, such as the local path, cannot be changed after the server endpoint had been created.</span></span>

## <span data-ttu-id="7bc1b-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7bc1b-112">EXAMPLES</span></span>

### <span data-ttu-id="7bc1b-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7bc1b-113">Example 1</span></span>
```powershell
PS C:\> Set-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName"  -TierFilesOlderThanDays 30 -OfflineDataTransfer -OfflineDataTransfer $false
```

<span data-ttu-id="7bc1b-114">I det här exemplet utförs en ny moln nivå princip på den angivna Server slut punkten, som dirigerar servern till en nivå med alla filer som inte har använts under de senaste 30 dagarna och det inaktiverar också data överförings läget offline under skapandet.</span><span class="sxs-lookup"><span data-stu-id="7bc1b-114">This example performs two actions, it sets a new cloud tiering policy on the specified server endpoint, which directs the server to tier all files that have not been accessed in the past 30 days and it also disables the offline data transfer mode, which was initially enabled on this server endpoint during it's creation.</span></span> <span data-ttu-id="7bc1b-115">Offline-dataöverföring används som en del av interoperabilitet med bulk migration-tjänster, till exempel Azure Data box.</span><span class="sxs-lookup"><span data-stu-id="7bc1b-115">Offline data transfer is used as part of interoperability with bulk migration services, such as Azure Data Box.</span></span>

## <span data-ttu-id="7bc1b-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7bc1b-116">PARAMETERS</span></span>

### <span data-ttu-id="7bc1b-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7bc1b-117">-AsJob</span></span>
<span data-ttu-id="7bc1b-118">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="7bc1b-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7bc1b-119">-CloudTiering</span><span class="sxs-lookup"><span data-stu-id="7bc1b-119">-CloudTiering</span></span>
<span data-ttu-id="7bc1b-120">Parameter för moln skikt</span><span class="sxs-lookup"><span data-stu-id="7bc1b-120">Cloud Tiering Parameter</span></span>

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

### <span data-ttu-id="7bc1b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bc1b-121">-DefaultProfile</span></span>
<span data-ttu-id="7bc1b-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7bc1b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7bc1b-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7bc1b-123">-InputObject</span></span>
<span data-ttu-id="7bc1b-124">SyncGroup-objekt som normalt passerar genom parametern.</span><span class="sxs-lookup"><span data-stu-id="7bc1b-124">SyncGroup Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint
Parameter Sets: ObjectParameterSet
Aliases: RegisteredServer

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7bc1b-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="7bc1b-125">-Name</span></span>
<span data-ttu-id="7bc1b-126">Namn på ServerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="7bc1b-126">Name of the ServerEndpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ServerEndpointName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bc1b-127">-OfflineDataTransfer</span><span class="sxs-lookup"><span data-stu-id="7bc1b-127">-OfflineDataTransfer</span></span>
<span data-ttu-id="7bc1b-128">Parametern Seeded data parameter</span><span class="sxs-lookup"><span data-stu-id="7bc1b-128">Cloud Seeded Data Parameter</span></span>

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

### <span data-ttu-id="7bc1b-129">-localCacheMode</span><span class="sxs-lookup"><span data-stu-id="7bc1b-129">-localCacheMode</span></span>
<span data-ttu-id="7bc1b-130">Parametern Local cache</span><span class="sxs-lookup"><span data-stu-id="7bc1b-130">Local cache mode Parameter</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bc1b-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bc1b-131">-ResourceGroupName</span></span>
<span data-ttu-id="7bc1b-132">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="7bc1b-132">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bc1b-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7bc1b-133">-ResourceId</span></span>
<span data-ttu-id="7bc1b-134">Resurs-ID för ServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7bc1b-134">ServerEndpoint Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bc1b-135">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="7bc1b-135">-StorageSyncServiceName</span></span>
<span data-ttu-id="7bc1b-136">Namn på StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="7bc1b-136">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bc1b-137">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="7bc1b-137">-SyncGroupName</span></span>
<span data-ttu-id="7bc1b-138">Namn på SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="7bc1b-138">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bc1b-139">-TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="7bc1b-139">-TierFilesOlderThanDays</span></span>
<span data-ttu-id="7bc1b-140">Tier-filer äldre än dagar-parameter</span><span class="sxs-lookup"><span data-stu-id="7bc1b-140">Tier Files Older Than Days Parameter</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bc1b-141">-VolumeFreeSpacePercent</span><span class="sxs-lookup"><span data-stu-id="7bc1b-141">-VolumeFreeSpacePercent</span></span>
<span data-ttu-id="7bc1b-142">Parametern för ledigt utrymme på volymen</span><span class="sxs-lookup"><span data-stu-id="7bc1b-142">Volume Free Space Percent Parameter</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bc1b-143">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7bc1b-143">-Confirm</span></span>
<span data-ttu-id="7bc1b-144">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7bc1b-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7bc1b-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bc1b-145">-WhatIf</span></span>
<span data-ttu-id="7bc1b-146">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7bc1b-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7bc1b-147">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7bc1b-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7bc1b-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bc1b-148">CommonParameters</span></span>
<span data-ttu-id="7bc1b-149">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bc1b-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bc1b-150">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7bc1b-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bc1b-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7bc1b-151">INPUTS</span></span>

### <span data-ttu-id="7bc1b-152">System. String</span><span class="sxs-lookup"><span data-stu-id="7bc1b-152">System.String</span></span>

### <span data-ttu-id="7bc1b-153">Microsoft. Azure. commands. StorageSync. Models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7bc1b-153">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="7bc1b-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7bc1b-154">OUTPUTS</span></span>

### <span data-ttu-id="7bc1b-155">Microsoft. Azure. commands. StorageSync. Models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7bc1b-155">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="7bc1b-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7bc1b-156">NOTES</span></span>

## <span data-ttu-id="7bc1b-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7bc1b-157">RELATED LINKS</span></span>
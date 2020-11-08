---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 53da56d932d3e2b57c2b2bbf17107918c9c1226d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94100730"
---
# <span data-ttu-id="818f7-101">New-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="818f7-101">New-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="818f7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="818f7-102">SYNOPSIS</span></span>
<span data-ttu-id="818f7-103">Det här kommandot skapar en ny server slut punkt på en registrerad Server.</span><span class="sxs-lookup"><span data-stu-id="818f7-103">This command creates a new server endpoint on a registered server.</span></span> <span data-ttu-id="818f7-104">Då aktive ras den angivna sökvägen på servern för att synkronisera filer med andra slut punkter i synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="818f7-104">This enables the specified path on the server to start syncing the files with other endpoints in the sync group.</span></span>

## <span data-ttu-id="818f7-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="818f7-105">SYNTAX</span></span>

### <span data-ttu-id="818f7-106">StringParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="818f7-106">StringParameterSet (Default)</span></span>
```
New-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -ServerResourceId <String> -ServerLocalPath <String> [-CloudTiering]
 [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>]
 [-OfflineDataTransferShareName <String>] [InitialDownloadPolicy] [LocalCacheMode] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="818f7-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="818f7-107">ObjectParameterSet</span></span>
```
New-AzStorageSyncServerEndpoint [-ParentObject] <PSSyncGroup> -Name <String> -ServerResourceId <String>
 -ServerLocalPath <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer]
 [-TierFilesOlderThanDays <Int32>] [-OfflineDataTransferShareName <String>] [InitialDownloadPolicy] [LocalCacheMode] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="818f7-108">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="818f7-108">ParentStringParameterSet</span></span>
```
New-AzStorageSyncServerEndpoint [-ParentResourceId] <String> -Name <String> -ServerResourceId <String>
 -ServerLocalPath <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer]
 [-TierFilesOlderThanDays <Int32>] [-OfflineDataTransferShareName <String>] [InitialDownloadPolicy] [LocalCacheMode] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="818f7-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="818f7-109">DESCRIPTION</span></span>
<span data-ttu-id="818f7-110">Det här kommandot skapar en ny server slut punkt på en registrerad Server.</span><span class="sxs-lookup"><span data-stu-id="818f7-110">This command creates a new server endpoint on a registered server.</span></span> <span data-ttu-id="818f7-111">Då aktive ras den angivna sökvägen på servern för att synkronisera filer med andra slut punkter i synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="818f7-111">This enables the specified path on the server to start syncing the files with other endpoints in the sync group.</span></span> <span data-ttu-id="818f7-112">Om det redan finns filer på andra slut punkter i synkroniseringsresursen och den nyligen tillagda platsen innehåller filer, försöker avstämnings processen avgöra om filerna faktiskt är samma som på andra slut punkter.</span><span class="sxs-lookup"><span data-stu-id="818f7-112">If there are already files on other endpoints in the sync group and this newly added location also contains files, a reconciliation process will attempt to determine if files are in fact the same ones in the same folders as on other endpoints.</span></span> <span data-ttu-id="818f7-113">Namn områdena och avstämningen bidrar till att förhindra konfliktskapande filer.</span><span class="sxs-lookup"><span data-stu-id="818f7-113">The namespaces will merge and reconciliation helps to prevent conflict files.</span></span> <span data-ttu-id="818f7-114">Om det finns filer på andra server slut punkter är det ofta bättre att starta med en tom plats på den här servern så att filerna från molnet kommer till servern i en automatisk process med namnet snabb katastrof återställning.</span><span class="sxs-lookup"><span data-stu-id="818f7-114">If there are files on other server endpoints it is often better to start with an empty location on this server, so that the files from the cloud come down to the server in an automatic process called fast disaster recovery.</span></span> <span data-ttu-id="818f7-115">Metadata för namn områden synkroniseras först och sedan hämtas data strömmen för varje fil.</span><span class="sxs-lookup"><span data-stu-id="818f7-115">Namespace metadata will be synced down first, then the data stream of each file is downloaded.</span></span> <span data-ttu-id="818f7-116">Om en fil begärs av en användare eller ett program från nedladdnings ordning kommer denna fil att besvaras med prioritetsordning för att uppfylla åtkomstbegäran.</span><span class="sxs-lookup"><span data-stu-id="818f7-116">If a file is requested by a user or application out of download order, that file will be recalled with priority to satisfy the access request.</span></span> <span data-ttu-id="818f7-117">Du kan också använda moln skiktning på den här server slut punkten för att avgöra om slut punkten ska bli en cache med den fullständiga uppsättningen filer från molnet.</span><span class="sxs-lookup"><span data-stu-id="818f7-117">You can optionally use cloud tiering on this server endpoint to determine if this endpoint is supposed to become a cache of the complete set of files from the cloud.</span></span> <span data-ttu-id="818f7-118">Om moln skiktning används stannar fil innehålls nedladdningen vid den punkt som definieras av de principer för moln skikt som du kan ange.</span><span class="sxs-lookup"><span data-stu-id="818f7-118">If cloud tiering is used, then the file content download will stop at the point defined by the cloud tiering policies you can set.</span></span>

## <span data-ttu-id="818f7-119">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="818f7-119">EXAMPLES</span></span>

### <span data-ttu-id="818f7-120">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="818f7-120">Example 1</span></span>
```powershell
PS C:\> $RegisteredServer = Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
PS C:\> New-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName" -ServerResourceId $RegisteredServer.ResourceId -ServerLocalPath "myServerLocalPath" -CloudTiering -OfflineDataTransfer -OfflineDataTransferShareName "myOfflineDataTransferShareName" -TierFilesOlderThanDays "myTierFilesOlderThanDays"
```

<span data-ttu-id="818f7-121">Det här kommandot skapar en ny server slut punkt på en registrerad Server och infogar den i en synkroniseringsresurs.</span><span class="sxs-lookup"><span data-stu-id="818f7-121">This command creates a new server endpoint on a registered server and inserts it into a sync group.</span></span> <span data-ttu-id="818f7-122">Det här sättet är en del av en topologi av andra slut punkter och filmetadata och innehåll startas omedelbart för synkronisering mellan alla platser som refereras till som slut punkter i synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="818f7-122">THis way it is part of a topology of other endpoints and file metadata and content will immediately start to sync between all locations referenced as endpoints in the sync group.</span></span>

## <span data-ttu-id="818f7-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="818f7-123">PARAMETERS</span></span>

### <span data-ttu-id="818f7-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="818f7-124">-AsJob</span></span>
<span data-ttu-id="818f7-125">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="818f7-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="818f7-126">-CloudTiering</span><span class="sxs-lookup"><span data-stu-id="818f7-126">-CloudTiering</span></span>
<span data-ttu-id="818f7-127">Parameter för moln skikt</span><span class="sxs-lookup"><span data-stu-id="818f7-127">Cloud Tiering Parameter</span></span>

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

### <span data-ttu-id="818f7-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="818f7-128">-DefaultProfile</span></span>
<span data-ttu-id="818f7-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="818f7-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="818f7-130">-Namn</span><span class="sxs-lookup"><span data-stu-id="818f7-130">-Name</span></span>
<span data-ttu-id="818f7-131">Namn på ServerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="818f7-131">Name of the ServerEndpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServerEndpointName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="818f7-132">-OfflineDataTransfer</span><span class="sxs-lookup"><span data-stu-id="818f7-132">-OfflineDataTransfer</span></span>
<span data-ttu-id="818f7-133">Parametern Seeded data parameter</span><span class="sxs-lookup"><span data-stu-id="818f7-133">Cloud Seeded Data Parameter</span></span>

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

### <span data-ttu-id="818f7-134">-OfflineDataTransferShareName</span><span class="sxs-lookup"><span data-stu-id="818f7-134">-OfflineDataTransferShareName</span></span>
<span data-ttu-id="818f7-135">Cloud Seeded Data File Share URI parameter</span><span class="sxs-lookup"><span data-stu-id="818f7-135">Cloud Seeded Data File Share Uri Parameter</span></span>

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

### <span data-ttu-id="818f7-136">-initialDownloadPolicy</span><span class="sxs-lookup"><span data-stu-id="818f7-136">-initialDownloadPolicy</span></span>
<span data-ttu-id="818f7-137">Parametern Local cache</span><span class="sxs-lookup"><span data-stu-id="818f7-137">Local cache mode Parameter</span></span>

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

### <span data-ttu-id="818f7-138">-localCacheMode</span><span class="sxs-lookup"><span data-stu-id="818f7-138">-localCacheMode</span></span>
<span data-ttu-id="818f7-139">Parametern Local cache</span><span class="sxs-lookup"><span data-stu-id="818f7-139">Local cache mode Parameter</span></span>

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

### <span data-ttu-id="818f7-140">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="818f7-140">-ParentObject</span></span>
<span data-ttu-id="818f7-141">SyncGroup-objekt som normalt passerar genom parametern.</span><span class="sxs-lookup"><span data-stu-id="818f7-141">SyncGroup Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup
Parameter Sets: ObjectParameterSet
Aliases: SyncGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="818f7-142">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="818f7-142">-ParentResourceId</span></span>
<span data-ttu-id="818f7-143">Överordnat resurs-ID för SyncGroup</span><span class="sxs-lookup"><span data-stu-id="818f7-143">SyncGroup Parent Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ParentStringParameterSet
Aliases: SyncGroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="818f7-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="818f7-144">-ResourceGroupName</span></span>
<span data-ttu-id="818f7-145">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="818f7-145">Resource Group Name.</span></span>

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

### <span data-ttu-id="818f7-146">-ServerLocalPath</span><span class="sxs-lookup"><span data-stu-id="818f7-146">-ServerLocalPath</span></span>
<span data-ttu-id="818f7-147">Parametern lokal sökväg för servern</span><span class="sxs-lookup"><span data-stu-id="818f7-147">Server Local Path Parameter</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="818f7-148">-ServerResourceId</span><span class="sxs-lookup"><span data-stu-id="818f7-148">-ServerResourceId</span></span>
<span data-ttu-id="818f7-149">RegisteredServer-resurs-ID</span><span class="sxs-lookup"><span data-stu-id="818f7-149">RegisteredServer Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="818f7-150">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="818f7-150">-StorageSyncServiceName</span></span>
<span data-ttu-id="818f7-151">Namn på StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="818f7-151">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="818f7-152">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="818f7-152">-SyncGroupName</span></span>
<span data-ttu-id="818f7-153">Namn på SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="818f7-153">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="818f7-154">-TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="818f7-154">-TierFilesOlderThanDays</span></span>
<span data-ttu-id="818f7-155">Tier-filer äldre än dagar-parameter</span><span class="sxs-lookup"><span data-stu-id="818f7-155">Tier Files Older Than Days Parameter</span></span>

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

### <span data-ttu-id="818f7-156">-VolumeFreeSpacePercent</span><span class="sxs-lookup"><span data-stu-id="818f7-156">-VolumeFreeSpacePercent</span></span>
<span data-ttu-id="818f7-157">Parametern för ledigt utrymme på volymen</span><span class="sxs-lookup"><span data-stu-id="818f7-157">Volume Free Space Percent Parameter</span></span>

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

### <span data-ttu-id="818f7-158">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="818f7-158">-Confirm</span></span>
<span data-ttu-id="818f7-159">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="818f7-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="818f7-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="818f7-160">-WhatIf</span></span>
<span data-ttu-id="818f7-161">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="818f7-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="818f7-162">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="818f7-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="818f7-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="818f7-163">CommonParameters</span></span>
<span data-ttu-id="818f7-164">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="818f7-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="818f7-165">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="818f7-165">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="818f7-166">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="818f7-166">INPUTS</span></span>

### <span data-ttu-id="818f7-167">Microsoft. Azure. commands. StorageSync. Models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="818f7-167">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="818f7-168">System. String</span><span class="sxs-lookup"><span data-stu-id="818f7-168">System.String</span></span>

## <span data-ttu-id="818f7-169">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="818f7-169">OUTPUTS</span></span>

### <span data-ttu-id="818f7-170">Microsoft. Azure. commands. StorageSync. Models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="818f7-170">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="818f7-171">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="818f7-171">NOTES</span></span>

## <span data-ttu-id="818f7-172">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="818f7-172">RELATED LINKS</span></span>
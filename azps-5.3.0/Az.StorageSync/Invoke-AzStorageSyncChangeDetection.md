---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/invoke-azstoragesyncchangedetection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncChangeDetection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncChangeDetection.md
ms.openlocfilehash: 9b7c539074f38b730a8ab5cd767a62fb44216ef6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98521961"
---
# <span data-ttu-id="62a93-101">Invoke-AzStorageSyncChangeDetection</span><span class="sxs-lookup"><span data-stu-id="62a93-101">Invoke-AzStorageSyncChangeDetection</span></span>

## <span data-ttu-id="62a93-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="62a93-102">SYNOPSIS</span></span>
<span data-ttu-id="62a93-103">Det här kommandot kan användas för att manuellt identifiera ändringar av namn områden.</span><span class="sxs-lookup"><span data-stu-id="62a93-103">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="62a93-104">Den kan riktas till hela resursen, undermappen eller uppsättningen filer.</span><span class="sxs-lookup"><span data-stu-id="62a93-104">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="62a93-105">Högst 10 000 objekt kan identifieras.</span><span class="sxs-lookup"><span data-stu-id="62a93-105">A maximum of 10,000 items can be detected.</span></span> <span data-ttu-id="62a93-106">Om omfattningen av ändringar är känd för dig kan du begränsa körningen av det här kommandot till delar av namn området så att ändrings kontrollen kan slutföra snabbt och inom objekt gränsen för 10 000.</span><span class="sxs-lookup"><span data-stu-id="62a93-106">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within the 10,000 item limit.</span></span>

> [!Note]  
> <span data-ttu-id="62a93-107">Invoke-AzStorageSyncChangeDetection cmdlet känner inte igen följande ändringar i Azure-fildelningen:</span><span class="sxs-lookup"><span data-stu-id="62a93-107">The Invoke-AzStorageSyncChangeDetection cmdlet will not detect the following changes in the Azure file share:</span></span>
> - <span data-ttu-id="62a93-108">Filer som tas bort.</span><span class="sxs-lookup"><span data-stu-id="62a93-108">Files that are deleted.</span></span> 
> - <span data-ttu-id="62a93-109">Filer som flyttas från resursen.</span><span class="sxs-lookup"><span data-stu-id="62a93-109">Files that are moved out of the share.</span></span>
> - <span data-ttu-id="62a93-110">Filer som tas bort och skapas med samma namn.</span><span class="sxs-lookup"><span data-stu-id="62a93-110">Files that are deleted and created with the same name.</span></span>  
> 
>  <span data-ttu-id="62a93-111">Dessa ändringar identifieras när [jobbet för ändrings identifiering](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#afs-change-detection) körs.</span><span class="sxs-lookup"><span data-stu-id="62a93-111">These changes will be detected when the [change detection job](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#afs-change-detection) runs.</span></span>

## <span data-ttu-id="62a93-112">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="62a93-112">SYNTAX</span></span>

### <span data-ttu-id="62a93-113">StringAndDirectoryParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="62a93-113">StringAndDirectoryParameterSet (Default)</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -DirectoryPath <String> [-Recursive] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62a93-114">StringAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="62a93-114">StringAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62a93-115">ResourceIdAndDirectoryParameterSet</span><span class="sxs-lookup"><span data-stu-id="62a93-115">ResourceIdAndDirectoryParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceId] <String> -DirectoryPath <String> [-Recursive] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62a93-116">ResourceIdAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="62a93-116">ResourceIdAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceId] <String> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62a93-117">ObjectAndDirectoryParameterSet</span><span class="sxs-lookup"><span data-stu-id="62a93-117">ObjectAndDirectoryParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-InputObject] <PSCloudEndpoint> -DirectoryPath <String> [-Recursive]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62a93-118">ObjectAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="62a93-118">ObjectAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-InputObject] <PSCloudEndpoint> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62a93-119">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="62a93-119">DESCRIPTION</span></span>
<span data-ttu-id="62a93-120">Med jämna mellanrum kontrollerar Azure File Sync namn området i en synkroniserad Azure File-resurs för ändringar som kommer till fil resursen på annat sätt än synkronisering. Målet är att identifiera dessa ändringar och sedan synkronisera dem till anslutna servrar.</span><span class="sxs-lookup"><span data-stu-id="62a93-120">Periodically, Azure File Sync checks the namespace inside a syncing Azure file share for changes that came into the file share by other means than sync. The goal is to identify these changes and ultimately sync them to connected servers.</span></span> <span data-ttu-id="62a93-121">Det här kommandot kan användas för att manuellt identifiera ändringar av namn områden.</span><span class="sxs-lookup"><span data-stu-id="62a93-121">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="62a93-122">Den kan riktas till hela resursen, undermappen eller uppsättningen filer.</span><span class="sxs-lookup"><span data-stu-id="62a93-122">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="62a93-123">Om omfattningen av ändringar är känd för dig kan du begränsa körningen av det här kommandot till delar av namn området så att ändrings kontrollen kan slutföra snabbt och inom gränsen för 10 000 objekt.</span><span class="sxs-lookup"><span data-stu-id="62a93-123">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within the 10,000 items limit.</span></span>

## <span data-ttu-id="62a93-124">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="62a93-124">EXAMPLES</span></span>

### <span data-ttu-id="62a93-125">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="62a93-125">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "b38fc242-8100-4807-89d0-399cef5863bf" -Path "Data","Reporting\Templates"
```

<span data-ttu-id="62a93-126">I det här exemplet körs ändrings kontroll i katalogerna "data" och "Reporting\Templates" för en synkroniserad Azure-fildelning.</span><span class="sxs-lookup"><span data-stu-id="62a93-126">In this example, change detection is run in the "Data" and "Reporting\Templates" directories of a syncing Azure file share.</span></span> <span data-ttu-id="62a93-127">Alla sökvägar är relativa till roten för Azure File Share-namnområdet.</span><span class="sxs-lookup"><span data-stu-id="62a93-127">All paths are relative to the root of the Azure file share namespace.</span></span>

### <span data-ttu-id="62a93-128">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="62a93-128">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "b38fc242-8100-4807-89d0-399cef5863bf" -Path "Data\results.xslx","Reporting\Templates\generated.pptx"
```

<span data-ttu-id="62a93-129">I det här exemplet körs ändrings kontroll för en uppsättning filer som är kända för att den som anropas har ändrats.</span><span class="sxs-lookup"><span data-stu-id="62a93-129">In this example, change detection is run for a set of files that are known to the command caller to have changed.</span></span> <span data-ttu-id="62a93-130">Målet är att Azure-filsynkroniseringen ska upptäcka och synkronisera dessa ändringar.</span><span class="sxs-lookup"><span data-stu-id="62a93-130">The goal is to have Azure file sync detect and sync these changes as well.</span></span>

### <span data-ttu-id="62a93-131">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="62a93-131">Example 3</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "b38fc242-8100-4807-89d0-399cef5863bf" -DirectoryPath "Examples" -Recursive
```

<span data-ttu-id="62a93-132">I det här exemplet körs ändrings spårning för "exempel"-katalogen och identifierar ändringar i under katalogerna rekursivt.</span><span class="sxs-lookup"><span data-stu-id="62a93-132">In this example, change detection is run for the "Examples" directory and will recursively detect changes in subdirectories.</span></span> <span data-ttu-id="62a93-133">Kom ihåg att cmdleten Miss lyckas om sökvägen innehåller fler än 10 000 objekt.</span><span class="sxs-lookup"><span data-stu-id="62a93-133">Keep in mind the cmdlet will fail if the path contains more than 10,000 items.</span></span> <span data-ttu-id="62a93-134">Om sökvägen innehåller fler än 10 000 objekt kör du kommandot på under delarna i namn området.</span><span class="sxs-lookup"><span data-stu-id="62a93-134">If the path contains more than 10,000 items, run the command on sub-parts of the namespace.</span></span>

## <span data-ttu-id="62a93-135">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="62a93-135">PARAMETERS</span></span>

### <span data-ttu-id="62a93-136">-AsJob</span><span class="sxs-lookup"><span data-stu-id="62a93-136">-AsJob</span></span>
<span data-ttu-id="62a93-137">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="62a93-137">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="62a93-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62a93-138">-DefaultProfile</span></span>
<span data-ttu-id="62a93-139">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="62a93-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62a93-140">-DirectoryPath</span><span class="sxs-lookup"><span data-stu-id="62a93-140">-DirectoryPath</span></span>
<span data-ttu-id="62a93-141">Katalog där ändrings kontroll utförs.</span><span class="sxs-lookup"><span data-stu-id="62a93-141">Directory where change detection will be performed.</span></span>

```yaml
Type: System.String
Parameter Sets: StringAndDirectoryParameterSet, ResourceIdAndDirectoryParameterSet, ObjectAndDirectoryParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62a93-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="62a93-142">-InputObject</span></span>
<span data-ttu-id="62a93-143">CloudEndpoint-objekt som normalt passerar genom parametern.</span><span class="sxs-lookup"><span data-stu-id="62a93-143">CloudEndpoint Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint
Parameter Sets: ObjectAndDirectoryParameterSet, ObjectAndPathParameterSet
Aliases: CloudEndpoint

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62a93-144">-Namn</span><span class="sxs-lookup"><span data-stu-id="62a93-144">-Name</span></span>
<span data-ttu-id="62a93-145">Namn på CloudEndpoint.</span><span class="sxs-lookup"><span data-stu-id="62a93-145">Name of the CloudEndpoint.</span></span> <span data-ttu-id="62a93-146">Namnet är ett GUID, inte det namn som visas i portalen.</span><span class="sxs-lookup"><span data-stu-id="62a93-146">The name is a GUID, not the friendly name that's displayed in the portal.</span></span> <span data-ttu-id="62a93-147">Använd Get-AzStorageSyncCloudEndpoint cmdlet för att hämta CloudEndpointName.</span><span class="sxs-lookup"><span data-stu-id="62a93-147">To get the CloudEndpointName, use the Get-AzStorageSyncCloudEndpoint cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: StringAndDirectoryParameterSet, StringAndPathParameterSet
Aliases: CloudEndpointName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62a93-148">-PassThru</span><span class="sxs-lookup"><span data-stu-id="62a93-148">-PassThru</span></span>
<span data-ttu-id="62a93-149">I normal körning returnerar denna cmdlet inget värde vid framgång.</span><span class="sxs-lookup"><span data-stu-id="62a93-149">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="62a93-150">Om du anger parametern PassThru, skriver cmdleten ett värde till pipeline efter att körningen lyckats.</span><span class="sxs-lookup"><span data-stu-id="62a93-150">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="62a93-151">-Path</span><span class="sxs-lookup"><span data-stu-id="62a93-151">-Path</span></span>
<span data-ttu-id="62a93-152">Sökväg där ändrings kontroll ska utföras.</span><span class="sxs-lookup"><span data-stu-id="62a93-152">Path where change detection will be performed.</span></span>

```yaml
Type: System.String[]
Parameter Sets: StringAndPathParameterSet, ResourceIdAndPathParameterSet, ObjectAndPathParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62a93-153">-Rekursivt</span><span class="sxs-lookup"><span data-stu-id="62a93-153">-Recursive</span></span>
<span data-ttu-id="62a93-154">Indikation om att identifiering av katalog ändringar är rekursivt.</span><span class="sxs-lookup"><span data-stu-id="62a93-154">Indication whether directory change detection is recursive.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: StringAndDirectoryParameterSet, ResourceIdAndDirectoryParameterSet, ObjectAndDirectoryParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62a93-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62a93-155">-ResourceGroupName</span></span>
<span data-ttu-id="62a93-156">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="62a93-156">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringAndDirectoryParameterSet, StringAndPathParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62a93-157">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="62a93-157">-ResourceId</span></span>
<span data-ttu-id="62a93-158">Resurs-ID för CloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="62a93-158">CloudEndpoint Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdAndDirectoryParameterSet, ResourceIdAndPathParameterSet
Aliases: CloudEndpointId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62a93-159">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="62a93-159">-StorageSyncServiceName</span></span>
<span data-ttu-id="62a93-160">Namn på StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="62a93-160">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringAndDirectoryParameterSet, StringAndPathParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62a93-161">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="62a93-161">-SyncGroupName</span></span>
<span data-ttu-id="62a93-162">Namn på SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="62a93-162">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringAndDirectoryParameterSet, StringAndPathParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62a93-163">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="62a93-163">-Confirm</span></span>
<span data-ttu-id="62a93-164">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="62a93-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62a93-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62a93-165">-WhatIf</span></span>
<span data-ttu-id="62a93-166">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="62a93-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62a93-167">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="62a93-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62a93-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62a93-168">CommonParameters</span></span>
<span data-ttu-id="62a93-169">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62a93-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62a93-170">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62a93-170">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62a93-171">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="62a93-171">INPUTS</span></span>

### <span data-ttu-id="62a93-172">System. String</span><span class="sxs-lookup"><span data-stu-id="62a93-172">System.String</span></span>

### <span data-ttu-id="62a93-173">Microsoft. Azure. commands. StorageSync. Models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="62a93-173">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="62a93-174">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="62a93-174">OUTPUTS</span></span>

### <span data-ttu-id="62a93-175">System. Void</span><span class="sxs-lookup"><span data-stu-id="62a93-175">System.Void</span></span>

## <span data-ttu-id="62a93-176">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="62a93-176">NOTES</span></span>

## <span data-ttu-id="62a93-177">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="62a93-177">RELATED LINKS</span></span>

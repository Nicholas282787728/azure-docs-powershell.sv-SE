---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/invoke-azstoragesyncchangedetection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncChangeDetection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncChangeDetection.md
ms.openlocfilehash: 41710c328787f542188c828975402696c36f0854
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259767"
---
# <span data-ttu-id="ee459-101">Invoke-AzStorageSyncChangeDetection</span><span class="sxs-lookup"><span data-stu-id="ee459-101">Invoke-AzStorageSyncChangeDetection</span></span>

## <span data-ttu-id="ee459-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ee459-102">SYNOPSIS</span></span>
<span data-ttu-id="ee459-103">Det här kommandot kan användas för att manuellt identifiera ändringar av namn områden.</span><span class="sxs-lookup"><span data-stu-id="ee459-103">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="ee459-104">Den kan riktas till hela resursen, undermappen eller uppsättningen filer.</span><span class="sxs-lookup"><span data-stu-id="ee459-104">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="ee459-105">Högst 10 000 objekt kan identifieras.</span><span class="sxs-lookup"><span data-stu-id="ee459-105">A maximum of 10,000 items can be detected.</span></span> <span data-ttu-id="ee459-106">Om omfattningen av ändringar är känd för dig kan du begränsa körningen av det här kommandot till delar av namn området så att ändrings kontrollen kan slutföra snabbt och inom objekt gränsen för 10 000.</span><span class="sxs-lookup"><span data-stu-id="ee459-106">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within the 10,000 item limit.</span></span>

> [!Note]  
> <span data-ttu-id="ee459-107">Invoke-AzStorageSyncChangeDetection cmdlet identifierar inte filer som tas bort i Azure-fildelningen.</span><span class="sxs-lookup"><span data-stu-id="ee459-107">The Invoke-AzStorageSyncChangeDetection cmdlet will not detect files that are deleted in the Azure file share.</span></span> <span data-ttu-id="ee459-108">Om filer tas bort i Azure File Share identifieras de när [ändrings kontroll jobbet](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#afs-change-detection) körs.</span><span class="sxs-lookup"><span data-stu-id="ee459-108">If files are deleted in the Azure file share, they will be detected when the [change detection job](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#afs-change-detection) runs.</span></span>

## <span data-ttu-id="ee459-109">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ee459-109">SYNTAX</span></span>

### <span data-ttu-id="ee459-110">StringAndDirectoryParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="ee459-110">StringAndDirectoryParameterSet (Default)</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -DirectoryPath <String> [-Recursive] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee459-111">StringAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee459-111">StringAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee459-112">ResourceIdAndDirectoryParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee459-112">ResourceIdAndDirectoryParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceId] <String> -DirectoryPath <String> [-Recursive] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee459-113">ResourceIdAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee459-113">ResourceIdAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceId] <String> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee459-114">ObjectAndDirectoryParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee459-114">ObjectAndDirectoryParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-InputObject] <PSCloudEndpoint> -DirectoryPath <String> [-Recursive]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee459-115">ObjectAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee459-115">ObjectAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-InputObject] <PSCloudEndpoint> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee459-116">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ee459-116">DESCRIPTION</span></span>
<span data-ttu-id="ee459-117">Med jämna mellanrum kontrollerar Azure File Sync namn området i en synkroniserad Azure File-resurs för ändringar som kommer till fil resursen på annat sätt än synkronisering. Målet är att identifiera dessa ändringar och sedan synkronisera dem till anslutna servrar.</span><span class="sxs-lookup"><span data-stu-id="ee459-117">Periodically, Azure File Sync checks the namespace inside a syncing Azure file share for changes that came into the file share by other means than sync. The goal is to identify these changes and ultimately sync them to connected servers.</span></span> <span data-ttu-id="ee459-118">Det här kommandot kan användas för att manuellt identifiera ändringar av namn områden.</span><span class="sxs-lookup"><span data-stu-id="ee459-118">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="ee459-119">Den kan riktas till hela resursen, undermappen eller uppsättningen filer.</span><span class="sxs-lookup"><span data-stu-id="ee459-119">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="ee459-120">Om omfattningen av ändringar är känd för dig kan du begränsa körningen av det här kommandot till delar av namn området så att ändrings kontrollen kan slutföras snabbt och i en 10 000-ändrings gräns.</span><span class="sxs-lookup"><span data-stu-id="ee459-120">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within a 10,000 changes limit.</span></span>

## <span data-ttu-id="ee459-121">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ee459-121">EXAMPLES</span></span>

### <span data-ttu-id="ee459-122">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ee459-122">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "myCloudEndpointName" -Path "Data","Reporting\Templates"
```

<span data-ttu-id="ee459-123">I det här exemplet körs ändrings kontroll i katalogerna "data" och "Reporting\Templates" för en synkroniserad Azure-fildelning.</span><span class="sxs-lookup"><span data-stu-id="ee459-123">In this example, change detection is run in the "Data" and "Reporting\Templates" directories of a syncing Azure file share.</span></span> <span data-ttu-id="ee459-124">Alla sökvägar är relativa till roten för Azure File Share-namnområdet.</span><span class="sxs-lookup"><span data-stu-id="ee459-124">All paths are relative to the root of the Azure file share namespace.</span></span>

### <span data-ttu-id="ee459-125">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="ee459-125">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "myCloudEndpointName" -Path "Data\results.xslx","Reporting\Templates\generated.pptx"
```

<span data-ttu-id="ee459-126">I det här exemplet körs ändrings kontroll för en uppsättning filer som är kända för att den som anropas har ändrats.</span><span class="sxs-lookup"><span data-stu-id="ee459-126">In this example, change detection is run for a set of files that are known to the command caller to have changed.</span></span> <span data-ttu-id="ee459-127">Målet är att Azure-filsynkroniseringen ska upptäcka och synkronisera dessa ändringar.</span><span class="sxs-lookup"><span data-stu-id="ee459-127">The goal is to have Azure file sync detect and sync these changes as well.</span></span>

### <span data-ttu-id="ee459-128">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="ee459-128">Example 3</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "myCloudEndpointName" -DirectoryPath "Examples" -Recursive
```

<span data-ttu-id="ee459-129">I det här exemplet körs ändrings spårning för "exempel"-katalogen och identifierar ändringar i under katalogerna rekursivt.</span><span class="sxs-lookup"><span data-stu-id="ee459-129">In this example, change detection is run for the "Examples" directory and will recursively detect changes in subdirectories.</span></span> <span data-ttu-id="ee459-130">Kom ihåg att det här kommandot kan upptäcka upp till 10 000-ändringar innan det avbryts automatiskt.</span><span class="sxs-lookup"><span data-stu-id="ee459-130">Keep in mind that this command can detect up to 10,000 changes before it is automatically aborted.</span></span> <span data-ttu-id="ee459-131">Om du misstänker att fler än 10 000 ändringar har inträffat kör du kommandot på under delarna i namn området.</span><span class="sxs-lookup"><span data-stu-id="ee459-131">If you suspect more than 10,000 changes to have occurred, run the command on sub-parts of the namespace.</span></span>

## <span data-ttu-id="ee459-132">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ee459-132">PARAMETERS</span></span>

### <span data-ttu-id="ee459-133">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ee459-133">-AsJob</span></span>
<span data-ttu-id="ee459-134">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="ee459-134">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ee459-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee459-135">-DefaultProfile</span></span>
<span data-ttu-id="ee459-136">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ee459-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee459-137">-DirectoryPath</span><span class="sxs-lookup"><span data-stu-id="ee459-137">-DirectoryPath</span></span>
<span data-ttu-id="ee459-138">Katalog där ändrings kontroll utförs.</span><span class="sxs-lookup"><span data-stu-id="ee459-138">Directory where change detection will be performed.</span></span>

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

### <span data-ttu-id="ee459-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ee459-139">-InputObject</span></span>
<span data-ttu-id="ee459-140">CloudEndpoint-objekt som normalt passerar genom parametern.</span><span class="sxs-lookup"><span data-stu-id="ee459-140">CloudEndpoint Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="ee459-141">-Namn</span><span class="sxs-lookup"><span data-stu-id="ee459-141">-Name</span></span>
<span data-ttu-id="ee459-142">Namn på CloudEndpoint.</span><span class="sxs-lookup"><span data-stu-id="ee459-142">Name of the CloudEndpoint.</span></span>

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

### <span data-ttu-id="ee459-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ee459-143">-PassThru</span></span>
<span data-ttu-id="ee459-144">I normal körning returnerar denna cmdlet inget värde vid framgång.</span><span class="sxs-lookup"><span data-stu-id="ee459-144">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="ee459-145">Om du anger parametern PassThru, skriver cmdleten ett värde till pipeline efter att körningen lyckats.</span><span class="sxs-lookup"><span data-stu-id="ee459-145">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="ee459-146">-Path</span><span class="sxs-lookup"><span data-stu-id="ee459-146">-Path</span></span>
<span data-ttu-id="ee459-147">Sökväg där ändrings kontroll ska utföras.</span><span class="sxs-lookup"><span data-stu-id="ee459-147">Path where change detection will be performed.</span></span>

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

### <span data-ttu-id="ee459-148">-Rekursivt</span><span class="sxs-lookup"><span data-stu-id="ee459-148">-Recursive</span></span>
<span data-ttu-id="ee459-149">Indikation om att identifiering av katalog ändringar är rekursivt.</span><span class="sxs-lookup"><span data-stu-id="ee459-149">Indication whether directory change detection is recursive.</span></span>

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

### <span data-ttu-id="ee459-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee459-150">-ResourceGroupName</span></span>
<span data-ttu-id="ee459-151">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="ee459-151">Resource Group Name.</span></span>

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

### <span data-ttu-id="ee459-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ee459-152">-ResourceId</span></span>
<span data-ttu-id="ee459-153">Resurs-ID för CloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="ee459-153">CloudEndpoint Resource Id</span></span>

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

### <span data-ttu-id="ee459-154">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="ee459-154">-StorageSyncServiceName</span></span>
<span data-ttu-id="ee459-155">Namn på StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="ee459-155">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="ee459-156">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="ee459-156">-SyncGroupName</span></span>
<span data-ttu-id="ee459-157">Namn på SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="ee459-157">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="ee459-158">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ee459-158">-Confirm</span></span>
<span data-ttu-id="ee459-159">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ee459-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee459-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee459-160">-WhatIf</span></span>
<span data-ttu-id="ee459-161">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ee459-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee459-162">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ee459-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee459-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee459-163">CommonParameters</span></span>
<span data-ttu-id="ee459-164">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee459-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee459-165">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee459-165">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee459-166">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ee459-166">INPUTS</span></span>

### <span data-ttu-id="ee459-167">System. String</span><span class="sxs-lookup"><span data-stu-id="ee459-167">System.String</span></span>

### <span data-ttu-id="ee459-168">Microsoft. Azure. commands. StorageSync. Models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ee459-168">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="ee459-169">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ee459-169">OUTPUTS</span></span>

### <span data-ttu-id="ee459-170">System. Void</span><span class="sxs-lookup"><span data-stu-id="ee459-170">System.Void</span></span>

## <span data-ttu-id="ee459-171">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ee459-171">NOTES</span></span>

## <span data-ttu-id="ee459-172">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ee459-172">RELATED LINKS</span></span>

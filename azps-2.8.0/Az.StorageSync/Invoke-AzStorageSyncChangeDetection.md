---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/invoke-azstoragesyncchangedetection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncChangeDetection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncChangeDetection.md
ms.openlocfilehash: c266b6623463165f14e01e55f0fec4d2d59a581f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93921035"
---
# <span data-ttu-id="845ce-101">Invoke-AzStorageSyncChangeDetection</span><span class="sxs-lookup"><span data-stu-id="845ce-101">Invoke-AzStorageSyncChangeDetection</span></span>

## <span data-ttu-id="845ce-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="845ce-102">SYNOPSIS</span></span>
<span data-ttu-id="845ce-103">Det här kommandot kan användas för att manuellt identifiera ändringar av namn områden.</span><span class="sxs-lookup"><span data-stu-id="845ce-103">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="845ce-104">Den kan riktas till hela resursen, undermappen eller uppsättningen filer.</span><span class="sxs-lookup"><span data-stu-id="845ce-104">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="845ce-105">Högst 10 000-ändringar kan identifieras.</span><span class="sxs-lookup"><span data-stu-id="845ce-105">A maximum of 10,000 changes can be detected.</span></span> <span data-ttu-id="845ce-106">Om omfattningen av ändringar är känd för dig kan du begränsa körningen av det här kommandot till delar av namn området så att ändrings kontrollen kan slutföras snabbt och i en 10 000-ändrings gräns.</span><span class="sxs-lookup"><span data-stu-id="845ce-106">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within a 10,000 changes limit.</span></span>

## <span data-ttu-id="845ce-107">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="845ce-107">SYNTAX</span></span>

### <span data-ttu-id="845ce-108">StringAndDirectoryParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="845ce-108">StringAndDirectoryParameterSet (Default)</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -DirectoryPath <String> [-Recursive] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="845ce-109">StringAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="845ce-109">StringAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="845ce-110">ResourceIdAndDirectoryParameterSet</span><span class="sxs-lookup"><span data-stu-id="845ce-110">ResourceIdAndDirectoryParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceId] <String> -DirectoryPath <String> [-Recursive] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="845ce-111">ResourceIdAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="845ce-111">ResourceIdAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceId] <String> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="845ce-112">ObjectAndDirectoryParameterSet</span><span class="sxs-lookup"><span data-stu-id="845ce-112">ObjectAndDirectoryParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-InputObject] <PSCloudEndpoint> -DirectoryPath <String> [-Recursive]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="845ce-113">ObjectAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="845ce-113">ObjectAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-InputObject] <PSCloudEndpoint> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="845ce-114">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="845ce-114">DESCRIPTION</span></span>
<span data-ttu-id="845ce-115">Med jämna mellanrum kontrollerar Azure File Sync namn området i en synkroniserad Azure File-resurs för ändringar som kommer till fil resursen på annat sätt än synkronisering. Målet är att identifiera dessa ändringar och sedan synkronisera dem till anslutna servrar.</span><span class="sxs-lookup"><span data-stu-id="845ce-115">Periodically, Azure File Sync checks the namespace inside a syncing Azure file share for changes that came into the file share by other means than sync. The goal is to identify these changes and ultimately sync them to connected servers.</span></span> <span data-ttu-id="845ce-116">Det här kommandot kan användas för att manuellt identifiera ändringar av namn områden.</span><span class="sxs-lookup"><span data-stu-id="845ce-116">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="845ce-117">Den kan riktas till hela resursen, undermappen eller uppsättningen filer.</span><span class="sxs-lookup"><span data-stu-id="845ce-117">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="845ce-118">Om omfattningen av ändringar är känd för dig kan du begränsa körningen av det här kommandot till delar av namn området så att ändrings kontrollen kan slutföras snabbt och i en 10 000-ändrings gräns.</span><span class="sxs-lookup"><span data-stu-id="845ce-118">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within a 10,000 changes limit.</span></span>

## <span data-ttu-id="845ce-119">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="845ce-119">EXAMPLES</span></span>

### <span data-ttu-id="845ce-120">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="845ce-120">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "myCloudEndpointName" -Path "Data","Reporting\Templates"
```

<span data-ttu-id="845ce-121">I det här exemplet körs ändrings kontroll i katalogerna "data" och "Reporting\Templates" för en synkroniserad Azure-fildelning.</span><span class="sxs-lookup"><span data-stu-id="845ce-121">In this example, change detection is run in the "Data" and "Reporting\Templates" directories of a syncing Azure file share.</span></span> <span data-ttu-id="845ce-122">Alla sökvägar är relativa till roten för Azure File Share-namnområdet.</span><span class="sxs-lookup"><span data-stu-id="845ce-122">All paths are relative to the root of the Azure file share namespace.</span></span>

### <span data-ttu-id="845ce-123">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="845ce-123">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "myCloudEndpointName" -Path "Data\results.xslx","Reporting\Templates\generated.pptx"
```

<span data-ttu-id="845ce-124">I det här exemplet körs ändrings kontroll för en uppsättning filer som är kända för att den som anropas har ändrats.</span><span class="sxs-lookup"><span data-stu-id="845ce-124">In this example, change detection is run for a set of files that are known to the command caller to have changed.</span></span> <span data-ttu-id="845ce-125">Målet är att Azure-filsynkroniseringen ska upptäcka och synkronisera dessa ändringar.</span><span class="sxs-lookup"><span data-stu-id="845ce-125">The goal is to have Azure file sync detect and sync these changes as well.</span></span>

### <span data-ttu-id="845ce-126">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="845ce-126">Example 3</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "myCloudEndpointName" -DirectoryPath "Examples" -Recursive
```

<span data-ttu-id="845ce-127">I det här exemplet körs ändrings spårning för "exempel"-katalogen och identifierar ändringar i under katalogerna rekursivt.</span><span class="sxs-lookup"><span data-stu-id="845ce-127">In this example, change detection is run for the "Examples" directory and will recursively detect changes in subdirectories.</span></span> <span data-ttu-id="845ce-128">Kom ihåg att det här kommandot kan upptäcka upp till 10 000-ändringar innan det avbryts automatiskt.</span><span class="sxs-lookup"><span data-stu-id="845ce-128">Keep in mind that this command can detect up to 10,000 changes before it is automatically aborted.</span></span> <span data-ttu-id="845ce-129">Om du misstänker att fler än 10 000 ändringar har inträffat kör du kommandot på under delarna i namn området.</span><span class="sxs-lookup"><span data-stu-id="845ce-129">If you suspect more than 10,000 changes to have occurred, run the command on sub-parts of the namespace.</span></span>

## <span data-ttu-id="845ce-130">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="845ce-130">PARAMETERS</span></span>

### <span data-ttu-id="845ce-131">-AsJob</span><span class="sxs-lookup"><span data-stu-id="845ce-131">-AsJob</span></span>
<span data-ttu-id="845ce-132">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="845ce-132">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="845ce-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="845ce-133">-DefaultProfile</span></span>
<span data-ttu-id="845ce-134">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="845ce-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="845ce-135">-DirectoryPath</span><span class="sxs-lookup"><span data-stu-id="845ce-135">-DirectoryPath</span></span>
<span data-ttu-id="845ce-136">Katalog där ändrings kontroll utförs.</span><span class="sxs-lookup"><span data-stu-id="845ce-136">Directory where change detection will be performed.</span></span>

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

### <span data-ttu-id="845ce-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="845ce-137">-InputObject</span></span>
<span data-ttu-id="845ce-138">CloudEndpoint-objekt som normalt passerar genom parametern.</span><span class="sxs-lookup"><span data-stu-id="845ce-138">CloudEndpoint Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="845ce-139">-Namn</span><span class="sxs-lookup"><span data-stu-id="845ce-139">-Name</span></span>
<span data-ttu-id="845ce-140">Namn på CloudEndpoint.</span><span class="sxs-lookup"><span data-stu-id="845ce-140">Name of the CloudEndpoint.</span></span>

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

### <span data-ttu-id="845ce-141">-PassThru</span><span class="sxs-lookup"><span data-stu-id="845ce-141">-PassThru</span></span>
<span data-ttu-id="845ce-142">I normal körning returnerar denna cmdlet inget värde vid framgång.</span><span class="sxs-lookup"><span data-stu-id="845ce-142">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="845ce-143">Om du anger parametern PassThru, skriver cmdleten ett värde till pipeline efter att körningen lyckats.</span><span class="sxs-lookup"><span data-stu-id="845ce-143">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="845ce-144">-Path</span><span class="sxs-lookup"><span data-stu-id="845ce-144">-Path</span></span>
<span data-ttu-id="845ce-145">Sökväg där ändrings kontroll ska utföras.</span><span class="sxs-lookup"><span data-stu-id="845ce-145">Path where change detection will be performed.</span></span>

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

### <span data-ttu-id="845ce-146">-Rekursivt</span><span class="sxs-lookup"><span data-stu-id="845ce-146">-Recursive</span></span>
<span data-ttu-id="845ce-147">Indikation om att identifiering av katalog ändringar är rekursivt.</span><span class="sxs-lookup"><span data-stu-id="845ce-147">Indication whether directory change detection is recursive.</span></span>

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

### <span data-ttu-id="845ce-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="845ce-148">-ResourceGroupName</span></span>
<span data-ttu-id="845ce-149">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="845ce-149">Resource Group Name.</span></span>

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

### <span data-ttu-id="845ce-150">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="845ce-150">-ResourceId</span></span>
<span data-ttu-id="845ce-151">Resurs-ID för CloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="845ce-151">CloudEndpoint Resource Id</span></span>

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

### <span data-ttu-id="845ce-152">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="845ce-152">-StorageSyncServiceName</span></span>
<span data-ttu-id="845ce-153">Namn på StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="845ce-153">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="845ce-154">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="845ce-154">-SyncGroupName</span></span>
<span data-ttu-id="845ce-155">Namn på SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="845ce-155">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="845ce-156">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="845ce-156">-Confirm</span></span>
<span data-ttu-id="845ce-157">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="845ce-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="845ce-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="845ce-158">-WhatIf</span></span>
<span data-ttu-id="845ce-159">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="845ce-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="845ce-160">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="845ce-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="845ce-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="845ce-161">CommonParameters</span></span>
<span data-ttu-id="845ce-162">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="845ce-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="845ce-163">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="845ce-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="845ce-164">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="845ce-164">INPUTS</span></span>

### <span data-ttu-id="845ce-165">System. String</span><span class="sxs-lookup"><span data-stu-id="845ce-165">System.String</span></span>

### <span data-ttu-id="845ce-166">Microsoft. Azure. commands. StorageSync. Models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="845ce-166">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="845ce-167">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="845ce-167">OUTPUTS</span></span>

### <span data-ttu-id="845ce-168">System. Void</span><span class="sxs-lookup"><span data-stu-id="845ce-168">System.Void</span></span>

## <span data-ttu-id="845ce-169">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="845ce-169">NOTES</span></span>

## <span data-ttu-id="845ce-170">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="845ce-170">RELATED LINKS</span></span>

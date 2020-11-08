---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
ms.openlocfilehash: dce91ee25cac4a716dc604e38f1ac38e5a3f3f1d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102192"
---
# <span data-ttu-id="60586-101">New-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="60586-101">New-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="60586-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="60586-102">SYNOPSIS</span></span>
<span data-ttu-id="60586-103">Skapar en ny Azure NetApp (ANF) volym.</span><span class="sxs-lookup"><span data-stu-id="60586-103">Creates a new Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="60586-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="60586-104">SYNTAX</span></span>

### <span data-ttu-id="60586-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="60586-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesVolume -ResourceGroupName <String> -Location <String> -AccountName <String> -PoolName <String>
 -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String> [-VolumeType <String>]
 -ServiceLevel <String> [-SnapshotId <String>] [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>]
 [-ReplicationObject <PSNetAppFilesReplicationObject>] [-ProtocolType <String[]>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60586-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="60586-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesVolume -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String>
 -ServiceLevel <String> [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>]
 [-ReplicationObject <PSNetAppFilesReplicationObject>] [-ProtocolType <String[]>] [-Tag <Hashtable>]
 -PoolObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="60586-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="60586-107">DESCRIPTION</span></span>
<span data-ttu-id="60586-108">Cmdleten **New-AzNetAppFilesVolume** skapar en ANF-volym.</span><span class="sxs-lookup"><span data-stu-id="60586-108">The **New-AzNetAppFilesVolume** cmdlet creates an ANF volume.</span></span>

## <span data-ttu-id="60586-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="60586-109">EXAMPLES</span></span>

### <span data-ttu-id="60586-110">Exempel 1: skapa en ANF volym</span><span class="sxs-lookup"><span data-stu-id="60586-110">Example 1: Create an ANF volume</span></span>
```
PS C:\>New-AzNetAppFilesVolume -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume" -l "westus2" -CreationToken "MyAnfVolume" -UsageThreshold 1099511627776 -ServiceLevel "Premium" -SubnetId "/subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.Network/virtualNetworks/MyVnetName/subnets/MySubNetName"

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool/volumes/MyAnfVolume
Name              : MyAnfAccount/MyAnfPool/MyAnfVolume
Type              : Microsoft.NetApp/netAppAccounts/capacityPools/volumes
Tags              :
FileSystemId      : 3e2773a7-2a72-d003-0637-1a8b1fa3eaaf
CreationToken     : MyAnfVolume
ServiceLevel      : Premium
UsageThreshold    : 1099511627776
ProvisioningState : Succeeded
SubnetId          : /subscriptions/f557b96d-2308-4a18-aae1-b8f7e7e70cc7/resourceGroups/MyRG/providers/Microsoft.Network/virtualNetworks/MyVnetName/subnets/default
```

<span data-ttu-id="60586-111">Det här kommandot skapar den nya ANF-volymen "MyAnfVolume" i poolen "MyAnfPool".</span><span class="sxs-lookup"><span data-stu-id="60586-111">This command creates the new ANF volume "MyAnfVolume" within the pool "MyAnfPool".</span></span>

## <span data-ttu-id="60586-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="60586-112">PARAMETERS</span></span>

### <span data-ttu-id="60586-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="60586-113">-AccountName</span></span>
<span data-ttu-id="60586-114">Namnet på ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="60586-114">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60586-115">-CreationToken</span><span class="sxs-lookup"><span data-stu-id="60586-115">-CreationToken</span></span>
<span data-ttu-id="60586-116">En unik fil Sök väg för volymen</span><span class="sxs-lookup"><span data-stu-id="60586-116">A unique file path for the volume</span></span>

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

### <span data-ttu-id="60586-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60586-117">-DefaultProfile</span></span>
<span data-ttu-id="60586-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="60586-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60586-119">-ExportPolicy</span><span class="sxs-lookup"><span data-stu-id="60586-119">-ExportPolicy</span></span>
<span data-ttu-id="60586-120">En hash-matris som representerar export policyn</span><span class="sxs-lookup"><span data-stu-id="60586-120">A hashtable array which represents the export policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolumeExportPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60586-121">-Plats</span><span class="sxs-lookup"><span data-stu-id="60586-121">-Location</span></span>
<span data-ttu-id="60586-122">Resursens plats</span><span class="sxs-lookup"><span data-stu-id="60586-122">The location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60586-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="60586-123">-Name</span></span>
<span data-ttu-id="60586-124">Namnet på ANF-volymen</span><span class="sxs-lookup"><span data-stu-id="60586-124">The name of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60586-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="60586-125">-PoolName</span></span>
<span data-ttu-id="60586-126">Namnet på ANF-poolen</span><span class="sxs-lookup"><span data-stu-id="60586-126">The name of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60586-127">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="60586-127">-PoolObject</span></span>
<span data-ttu-id="60586-128">Poolen för det nya volym objektet</span><span class="sxs-lookup"><span data-stu-id="60586-128">The pool for the new volume object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="60586-129">-ProtocolType</span><span class="sxs-lookup"><span data-stu-id="60586-129">-ProtocolType</span></span>
<span data-ttu-id="60586-130">En hash-matris som representerar export policyn</span><span class="sxs-lookup"><span data-stu-id="60586-130">A hashtable array which represents the export policy</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60586-131">-ReplicationObject</span><span class="sxs-lookup"><span data-stu-id="60586-131">-ReplicationObject</span></span>
<span data-ttu-id="60586-132">En hash-tabell som representerar målobjektet</span><span class="sxs-lookup"><span data-stu-id="60586-132">A hashtable array which represents the replication object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesReplicationObject
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60586-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60586-133">-ResourceGroupName</span></span>
<span data-ttu-id="60586-134">Resurs gruppen för ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="60586-134">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60586-135">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="60586-135">-ServiceLevel</span></span>
<span data-ttu-id="60586-136">Service nivån för ANF-volymen</span><span class="sxs-lookup"><span data-stu-id="60586-136">The service level of the ANF volume</span></span>

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

### <span data-ttu-id="60586-137">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="60586-137">-SnapshotId</span></span>
<span data-ttu-id="60586-138">Skapa volym från en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="60586-138">Create volume from a snapshot.</span></span> <span data-ttu-id="60586-139">UUID v4 eller resurs-ID som används för att identifiera ögonblicks bilden</span><span class="sxs-lookup"><span data-stu-id="60586-139">UUID v4 or resource identifier used to identify the Snapshot</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60586-140">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="60586-140">-SubnetId</span></span>
<span data-ttu-id="60586-141">Azure Resource URI för ett delegerat undernät</span><span class="sxs-lookup"><span data-stu-id="60586-141">The Azure Resource URI for a delegated subnet</span></span>

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

### <span data-ttu-id="60586-142">-Tagg</span><span class="sxs-lookup"><span data-stu-id="60586-142">-Tag</span></span>
<span data-ttu-id="60586-143">En hash som representerar resurs koder</span><span class="sxs-lookup"><span data-stu-id="60586-143">A hashtable which represents resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60586-144">-UsageThreshold</span><span class="sxs-lookup"><span data-stu-id="60586-144">-UsageThreshold</span></span>
<span data-ttu-id="60586-145">Den maximala lagrings kvoten som tillåts för ett fil system i byte</span><span class="sxs-lookup"><span data-stu-id="60586-145">The maximum storage quota allowed for a file system in bytes</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60586-146">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="60586-146">-VolumeType</span></span>
<span data-ttu-id="60586-147">Typ av ANF-volym</span><span class="sxs-lookup"><span data-stu-id="60586-147">The type of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60586-148">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="60586-148">-Confirm</span></span>
<span data-ttu-id="60586-149">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="60586-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60586-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60586-150">-WhatIf</span></span>
<span data-ttu-id="60586-151">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="60586-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60586-152">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="60586-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60586-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60586-153">CommonParameters</span></span>
<span data-ttu-id="60586-154">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60586-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60586-155">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="60586-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60586-156">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="60586-156">INPUTS</span></span>

### <span data-ttu-id="60586-157">System. String</span><span class="sxs-lookup"><span data-stu-id="60586-157">System.String</span></span>

### <span data-ttu-id="60586-158">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="60586-158">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="60586-159">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="60586-159">OUTPUTS</span></span>

### <span data-ttu-id="60586-160">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="60586-160">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="60586-161">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="60586-161">NOTES</span></span>

## <span data-ttu-id="60586-162">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="60586-162">RELATED LINKS</span></span>

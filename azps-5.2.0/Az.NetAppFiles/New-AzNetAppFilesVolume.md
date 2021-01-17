---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
ms.openlocfilehash: 2326551a2b6a03e1904e8d0d90663ee796ccaa46
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98410720"
---
# <span data-ttu-id="27af6-101">New-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="27af6-101">New-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="27af6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="27af6-102">SYNOPSIS</span></span>
<span data-ttu-id="27af6-103">Skapar en ny Azure NetApp (ANF) volym.</span><span class="sxs-lookup"><span data-stu-id="27af6-103">Creates a new Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="27af6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="27af6-104">SYNTAX</span></span>

### <span data-ttu-id="27af6-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="27af6-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesVolume -ResourceGroupName <String> -Location <String> -AccountName <String> -PoolName <String>
 -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String> [-VolumeType <String>]
 -ServiceLevel <String> [-SnapshotId <String>] [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>]
 [-ReplicationObject <PSNetAppFilesReplicationObject>] [-Snapshot <PSNetAppFilesVolumeSnapshot>]
 [-Backup <PSNetAppFilesVolumeBackupProperties>] [-ProtocolType <String[]>] [-SnapshotDirectoryVisible]
 [-BackupId <String>] [-SecurityStyle <String>] [-ThroughputMibps <Double>] [-KerberosEnabled]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27af6-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="27af6-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesVolume -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String>
 -ServiceLevel <String> [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>]
 [-ReplicationObject <PSNetAppFilesReplicationObject>] [-Snapshot <PSNetAppFilesVolumeSnapshot>]
 [-Backup <PSNetAppFilesVolumeBackupProperties>] [-ProtocolType <String[]>] [-SnapshotDirectoryVisible]
 [-SecurityStyle <String>] [-ThroughputMibps <Double>] [-KerberosEnabled] [-Tag <Hashtable>]
 -PoolObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="27af6-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="27af6-107">DESCRIPTION</span></span>
<span data-ttu-id="27af6-108">Cmdleten **New-AzNetAppFilesVolume** skapar en ANF-volym.</span><span class="sxs-lookup"><span data-stu-id="27af6-108">The **New-AzNetAppFilesVolume** cmdlet creates an ANF volume.</span></span>

## <span data-ttu-id="27af6-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="27af6-109">EXAMPLES</span></span>

### <span data-ttu-id="27af6-110">Exempel 1: skapa en ANF volym</span><span class="sxs-lookup"><span data-stu-id="27af6-110">Example 1: Create an ANF volume</span></span>
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

<span data-ttu-id="27af6-111">Det här kommandot skapar den nya ANF-volymen "MyAnfVolume" i poolen "MyAnfPool".</span><span class="sxs-lookup"><span data-stu-id="27af6-111">This command creates the new ANF volume "MyAnfVolume" within the pool "MyAnfPool".</span></span>

## <span data-ttu-id="27af6-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="27af6-112">PARAMETERS</span></span>

### <span data-ttu-id="27af6-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="27af6-113">-AccountName</span></span>
<span data-ttu-id="27af6-114">Namnet på ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="27af6-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="27af6-115">-Säkerhets kopiering</span><span class="sxs-lookup"><span data-stu-id="27af6-115">-Backup</span></span>
<span data-ttu-id="27af6-116">En hash-tabell som representerar det säkerhetskopierade objektet</span><span class="sxs-lookup"><span data-stu-id="27af6-116">A hashtable array which represents the backup object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolumeBackupProperties
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27af6-117">-BackupId</span><span class="sxs-lookup"><span data-stu-id="27af6-117">-BackupId</span></span>
<span data-ttu-id="27af6-118">Säkerhetskopiera ID.</span><span class="sxs-lookup"><span data-stu-id="27af6-118">Backup ID.</span></span> <span data-ttu-id="27af6-119">UUID v4 eller resurs-ID som används för att identifiera säkerhets kopian</span><span class="sxs-lookup"><span data-stu-id="27af6-119">UUID v4 or resource identifier used to identify the Backup</span></span>

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

### <span data-ttu-id="27af6-120">-CreationToken</span><span class="sxs-lookup"><span data-stu-id="27af6-120">-CreationToken</span></span>
<span data-ttu-id="27af6-121">En unik fil Sök väg för volymen</span><span class="sxs-lookup"><span data-stu-id="27af6-121">A unique file path for the volume</span></span>

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

### <span data-ttu-id="27af6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27af6-122">-DefaultProfile</span></span>
<span data-ttu-id="27af6-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="27af6-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27af6-124">-ExportPolicy</span><span class="sxs-lookup"><span data-stu-id="27af6-124">-ExportPolicy</span></span>
<span data-ttu-id="27af6-125">En hash-matris som representerar export policyn</span><span class="sxs-lookup"><span data-stu-id="27af6-125">A hashtable array which represents the export policy</span></span>

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

### <span data-ttu-id="27af6-126">-KerberosEnabled</span><span class="sxs-lookup"><span data-stu-id="27af6-126">-KerberosEnabled</span></span>
<span data-ttu-id="27af6-127">Beskriv om en volym är Kerberos-aktiverad</span><span class="sxs-lookup"><span data-stu-id="27af6-127">Describe if a volume is Kerberos Enabled</span></span>

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

### <span data-ttu-id="27af6-128">-Plats</span><span class="sxs-lookup"><span data-stu-id="27af6-128">-Location</span></span>
<span data-ttu-id="27af6-129">Resursens plats</span><span class="sxs-lookup"><span data-stu-id="27af6-129">The location of the resource</span></span>

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

### <span data-ttu-id="27af6-130">-Namn</span><span class="sxs-lookup"><span data-stu-id="27af6-130">-Name</span></span>
<span data-ttu-id="27af6-131">Namnet på ANF-volymen</span><span class="sxs-lookup"><span data-stu-id="27af6-131">The name of the ANF volume</span></span>

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

### <span data-ttu-id="27af6-132">-PoolName</span><span class="sxs-lookup"><span data-stu-id="27af6-132">-PoolName</span></span>
<span data-ttu-id="27af6-133">Namnet på ANF-poolen</span><span class="sxs-lookup"><span data-stu-id="27af6-133">The name of the ANF pool</span></span>

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

### <span data-ttu-id="27af6-134">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="27af6-134">-PoolObject</span></span>
<span data-ttu-id="27af6-135">Poolen för det nya volym objektet</span><span class="sxs-lookup"><span data-stu-id="27af6-135">The pool for the new volume object</span></span>

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

### <span data-ttu-id="27af6-136">-ProtocolType</span><span class="sxs-lookup"><span data-stu-id="27af6-136">-ProtocolType</span></span>
<span data-ttu-id="27af6-137">En hash-matris som representerar export policyn</span><span class="sxs-lookup"><span data-stu-id="27af6-137">A hashtable array which represents the export policy</span></span>

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

### <span data-ttu-id="27af6-138">-ReplicationObject</span><span class="sxs-lookup"><span data-stu-id="27af6-138">-ReplicationObject</span></span>
<span data-ttu-id="27af6-139">En hash-tabell som representerar målobjektet</span><span class="sxs-lookup"><span data-stu-id="27af6-139">A hashtable array which represents the replication object</span></span>

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

### <span data-ttu-id="27af6-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27af6-140">-ResourceGroupName</span></span>
<span data-ttu-id="27af6-141">Resurs gruppen för ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="27af6-141">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="27af6-142">-SecurityStyle</span><span class="sxs-lookup"><span data-stu-id="27af6-142">-SecurityStyle</span></span>
<span data-ttu-id="27af6-143">Säkerhets formatet för volym.</span><span class="sxs-lookup"><span data-stu-id="27af6-143">The security style of volume.</span></span> <span data-ttu-id="27af6-144">Möjliga värden är: ' NTFS ', ' Unix '</span><span class="sxs-lookup"><span data-stu-id="27af6-144">Possible values include: 'ntfs', 'unix'</span></span>

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

### <span data-ttu-id="27af6-145">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="27af6-145">-ServiceLevel</span></span>
<span data-ttu-id="27af6-146">Service nivån för ANF-volymen</span><span class="sxs-lookup"><span data-stu-id="27af6-146">The service level of the ANF volume</span></span>

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

### <span data-ttu-id="27af6-147">-Stillbild</span><span class="sxs-lookup"><span data-stu-id="27af6-147">-Snapshot</span></span>
<span data-ttu-id="27af6-148">En hash-tabell som representerar ett SnapShot-objekt</span><span class="sxs-lookup"><span data-stu-id="27af6-148">A hashtable array which represents the snapshot object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolumeSnapshot
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27af6-149">-SnapshotDirectoryVisible</span><span class="sxs-lookup"><span data-stu-id="27af6-149">-SnapshotDirectoryVisible</span></span>
<span data-ttu-id="27af6-150">Om den är aktive rad (true) volymen kommer att innehålla skrivskyddad. snapshot-katalog som ger åtkomst till var och en av volymens stillbilder (standard är sant)</span><span class="sxs-lookup"><span data-stu-id="27af6-150">If enabled (true) the volume will contain a read-only .snapshot directory which provides access to each of the volume's snapshots (default to true)</span></span>

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

### <span data-ttu-id="27af6-151">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="27af6-151">-SnapshotId</span></span>
<span data-ttu-id="27af6-152">Skapa volym från en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="27af6-152">Create volume from a snapshot.</span></span> <span data-ttu-id="27af6-153">UUID v4 eller resurs-ID som används för att identifiera ögonblicks bilden</span><span class="sxs-lookup"><span data-stu-id="27af6-153">UUID v4 or resource identifier used to identify the Snapshot</span></span>

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

### <span data-ttu-id="27af6-154">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="27af6-154">-SubnetId</span></span>
<span data-ttu-id="27af6-155">Azure Resource URI för ett delegerat undernät</span><span class="sxs-lookup"><span data-stu-id="27af6-155">The Azure Resource URI for a delegated subnet</span></span>

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

### <span data-ttu-id="27af6-156">-Tagg</span><span class="sxs-lookup"><span data-stu-id="27af6-156">-Tag</span></span>
<span data-ttu-id="27af6-157">En hash som representerar resurs koder</span><span class="sxs-lookup"><span data-stu-id="27af6-157">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="27af6-158">-ThroughputMibps</span><span class="sxs-lookup"><span data-stu-id="27af6-158">-ThroughputMibps</span></span>
<span data-ttu-id="27af6-159">Maximalt genomflöde i Mibps som kan uppnås av den här volymen</span><span class="sxs-lookup"><span data-stu-id="27af6-159">Maximum throughput in Mibps that can be achieved by this volume</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27af6-160">-UsageThreshold</span><span class="sxs-lookup"><span data-stu-id="27af6-160">-UsageThreshold</span></span>
<span data-ttu-id="27af6-161">Den maximala lagrings kvoten som tillåts för ett fil system i byte</span><span class="sxs-lookup"><span data-stu-id="27af6-161">The maximum storage quota allowed for a file system in bytes</span></span>

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

### <span data-ttu-id="27af6-162">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="27af6-162">-VolumeType</span></span>
<span data-ttu-id="27af6-163">Typ av ANF-volym</span><span class="sxs-lookup"><span data-stu-id="27af6-163">The type of the ANF volume</span></span>

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

### <span data-ttu-id="27af6-164">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="27af6-164">-Confirm</span></span>
<span data-ttu-id="27af6-165">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="27af6-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27af6-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27af6-166">-WhatIf</span></span>
<span data-ttu-id="27af6-167">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="27af6-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27af6-168">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="27af6-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27af6-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27af6-169">CommonParameters</span></span>
<span data-ttu-id="27af6-170">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27af6-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27af6-171">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="27af6-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27af6-172">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="27af6-172">INPUTS</span></span>

### <span data-ttu-id="27af6-173">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="27af6-173">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="27af6-174">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="27af6-174">OUTPUTS</span></span>

### <span data-ttu-id="27af6-175">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="27af6-175">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="27af6-176">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="27af6-176">NOTES</span></span>

## <span data-ttu-id="27af6-177">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="27af6-177">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesVolume.md
ms.openlocfilehash: 2d3b212ea24c9dda665d2e2ec2516f25a59318b2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98394635"
---
# <span data-ttu-id="f64c2-101">Update-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="f64c2-101">Update-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="f64c2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f64c2-102">SYNOPSIS</span></span>
<span data-ttu-id="f64c2-103">Uppdaterar en Azure NetApp-fil (ANF) enligt de valfria modifieringarna.</span><span class="sxs-lookup"><span data-stu-id="f64c2-103">Updates an Azure NetApp Files (ANF) volume according to the optional modifiers provided.</span></span>

## <span data-ttu-id="f64c2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f64c2-104">SYNTAX</span></span>

### <span data-ttu-id="f64c2-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="f64c2-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesVolume -ResourceGroupName <String> -Location <String> -AccountName <String>
 -PoolName <String> -Name <String> [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Backup <PSNetAppFilesVolumeBackupProperties>]
 [-ThroughputMibps <Double>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f64c2-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f64c2-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesVolume -Name <String> [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Backup <PSNetAppFilesVolumeBackupProperties>]
 [-ThroughputMibps <Double>] [-Tag <Hashtable>] -PoolObject <PSNetAppFilesPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f64c2-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f64c2-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesVolume [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Backup <PSNetAppFilesVolumeBackupProperties>]
 [-ThroughputMibps <Double>] [-Tag <Hashtable>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f64c2-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f64c2-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesVolume [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Backup <PSNetAppFilesVolumeBackupProperties>]
 [-ThroughputMibps <Double>] [-Tag <Hashtable>] -InputObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f64c2-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f64c2-109">DESCRIPTION</span></span>
<span data-ttu-id="f64c2-110">Cmdleten **Update-AzNetAppFilesVolume** uppdaterar en ANF-volym.</span><span class="sxs-lookup"><span data-stu-id="f64c2-110">The **Update-AzNetAppFilesVolume** cmdlet updates an ANF volume.</span></span>

## <span data-ttu-id="f64c2-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f64c2-111">EXAMPLES</span></span>

### <span data-ttu-id="f64c2-112">Exempel 1: uppdatera en ANF-volym</span><span class="sxs-lookup"><span data-stu-id="f64c2-112">Example 1: Update an ANF volume</span></span>
```
PS C:\>Update-AzNetAppFilesVolume -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume" -UsageThreshold Size

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool/volumes/MyAnfVolume
Name              : MyAnfAccount/MyAnfPool/MyAnfVolume
Type              : Microsoft.NetApp/netAppAccounts/capacityPools/volumes
Tags              :
FileSystemId      : 3e2773a7-2a72-d003-0637-1a8b1fa3eaaf
CreationToken     : MyAnfVolume
ServiceLevel      : Premium
UsageThreshold    : 2199023255552
ProvisioningState : Succeeded
SubnetId          : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.Network/virtualNetworks/MyRG-vnet/subnets/default
```

<span data-ttu-id="f64c2-113">Det här kommandot uppdaterar ANF-volymen "MyAnfVolume" med den nya UsageThreshold-storleken.</span><span class="sxs-lookup"><span data-stu-id="f64c2-113">This command updates the ANF volume "MyAnfVolume" with the new UsageThreshold size.</span></span>

## <span data-ttu-id="f64c2-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f64c2-114">PARAMETERS</span></span>

### <span data-ttu-id="f64c2-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f64c2-115">-AccountName</span></span>
<span data-ttu-id="f64c2-116">Namnet på ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="f64c2-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="f64c2-117">-Säkerhets kopiering</span><span class="sxs-lookup"><span data-stu-id="f64c2-117">-Backup</span></span>
<span data-ttu-id="f64c2-118">En hash-tabell som representerar det säkerhetskopierade objektet</span><span class="sxs-lookup"><span data-stu-id="f64c2-118">A hashtable array which represents the backup object</span></span>

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

### <span data-ttu-id="f64c2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f64c2-119">-DefaultProfile</span></span>
<span data-ttu-id="f64c2-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f64c2-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f64c2-121">-ExportPolicy</span><span class="sxs-lookup"><span data-stu-id="f64c2-121">-ExportPolicy</span></span>
<span data-ttu-id="f64c2-122">En hash-matris som representerar export policyn</span><span class="sxs-lookup"><span data-stu-id="f64c2-122">A hashtable array which represents the export policy</span></span>

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

### <span data-ttu-id="f64c2-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f64c2-123">-InputObject</span></span>
<span data-ttu-id="f64c2-124">Volume-objekt som ska uppdateras</span><span class="sxs-lookup"><span data-stu-id="f64c2-124">The volume object to update</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f64c2-125">-Plats</span><span class="sxs-lookup"><span data-stu-id="f64c2-125">-Location</span></span>
<span data-ttu-id="f64c2-126">Resursens plats</span><span class="sxs-lookup"><span data-stu-id="f64c2-126">The location of the resource</span></span>

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

### <span data-ttu-id="f64c2-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="f64c2-127">-Name</span></span>
<span data-ttu-id="f64c2-128">Namnet på ANF-volymen</span><span class="sxs-lookup"><span data-stu-id="f64c2-128">The name of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f64c2-129">-PoolName</span><span class="sxs-lookup"><span data-stu-id="f64c2-129">-PoolName</span></span>
<span data-ttu-id="f64c2-130">Namnet på ANF-poolen</span><span class="sxs-lookup"><span data-stu-id="f64c2-130">The name of the ANF pool</span></span>

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

### <span data-ttu-id="f64c2-131">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="f64c2-131">-PoolObject</span></span>
<span data-ttu-id="f64c2-132">Det pool-objekt som innehåller volymen som ska uppdateras</span><span class="sxs-lookup"><span data-stu-id="f64c2-132">The pool object containing the volume to update</span></span>

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

### <span data-ttu-id="f64c2-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f64c2-133">-ResourceGroupName</span></span>
<span data-ttu-id="f64c2-134">Resurs gruppen för ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="f64c2-134">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="f64c2-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f64c2-135">-ResourceId</span></span>
<span data-ttu-id="f64c2-136">Resurs-ID för ANF volym</span><span class="sxs-lookup"><span data-stu-id="f64c2-136">The resource id of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f64c2-137">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="f64c2-137">-ServiceLevel</span></span>
<span data-ttu-id="f64c2-138">Service nivån för ANF-volymen</span><span class="sxs-lookup"><span data-stu-id="f64c2-138">The service level of the ANF volume</span></span>

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

### <span data-ttu-id="f64c2-139">-Tagg</span><span class="sxs-lookup"><span data-stu-id="f64c2-139">-Tag</span></span>
<span data-ttu-id="f64c2-140">En hash som representerar resurs koder</span><span class="sxs-lookup"><span data-stu-id="f64c2-140">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="f64c2-141">-ThroughputMibps</span><span class="sxs-lookup"><span data-stu-id="f64c2-141">-ThroughputMibps</span></span>
<span data-ttu-id="f64c2-142">Maximalt genomflöde i Mibps som kan uppnås av den här volymen</span><span class="sxs-lookup"><span data-stu-id="f64c2-142">Maximum throughput in Mibps that can be achieved by this volume</span></span>

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

### <span data-ttu-id="f64c2-143">-UsageThreshold</span><span class="sxs-lookup"><span data-stu-id="f64c2-143">-UsageThreshold</span></span>
<span data-ttu-id="f64c2-144">Den maximala lagrings kvoten som tillåts för ett fil system i byte</span><span class="sxs-lookup"><span data-stu-id="f64c2-144">The maximum storage quota allowed for a file system in bytes</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f64c2-145">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f64c2-145">-Confirm</span></span>
<span data-ttu-id="f64c2-146">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f64c2-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f64c2-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f64c2-147">-WhatIf</span></span>
<span data-ttu-id="f64c2-148">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f64c2-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f64c2-149">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f64c2-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f64c2-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f64c2-150">CommonParameters</span></span>
<span data-ttu-id="f64c2-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f64c2-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f64c2-152">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f64c2-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f64c2-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f64c2-153">INPUTS</span></span>

### <span data-ttu-id="f64c2-154">System. String</span><span class="sxs-lookup"><span data-stu-id="f64c2-154">System.String</span></span>

### <span data-ttu-id="f64c2-155">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="f64c2-155">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="f64c2-156">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="f64c2-156">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="f64c2-157">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f64c2-157">OUTPUTS</span></span>

### <span data-ttu-id="f64c2-158">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="f64c2-158">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="f64c2-159">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f64c2-159">NOTES</span></span>

## <span data-ttu-id="f64c2-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f64c2-160">RELATED LINKS</span></span>

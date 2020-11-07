---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesVolume.md
ms.openlocfilehash: d59bd7bea42e442aace3817f985098c4b2344ce4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93925610"
---
# <span data-ttu-id="84fc0-101">Update-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="84fc0-101">Update-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="84fc0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="84fc0-102">SYNOPSIS</span></span>
<span data-ttu-id="84fc0-103">Uppdaterar en Azure NetApp-fil (ANF) enligt de valfria modifieringarna.</span><span class="sxs-lookup"><span data-stu-id="84fc0-103">Updates an Azure NetApp Files (ANF) volume according to the optional modifiers provided.</span></span>

## <span data-ttu-id="84fc0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="84fc0-104">SYNTAX</span></span>

### <span data-ttu-id="84fc0-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="84fc0-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesVolume -ResourceGroupName <String> -Location <String> -AccountName <String>
 -PoolName <String> -Name <String> [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84fc0-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="84fc0-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesVolume -Name <String> [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Tag <Hashtable>] -PoolObject <PSNetAppFilesPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84fc0-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="84fc0-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesVolume [-UsageThreshold <Int64>] [-ServiceLevel <String>] [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>]
 [-Tag <Hashtable>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="84fc0-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="84fc0-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesVolume [-UsageThreshold <Int64>] [-ServiceLevel <String>] [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>]
 [-Tag <Hashtable>] -InputObject <PSNetAppFilesVolume> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84fc0-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="84fc0-109">DESCRIPTION</span></span>
<span data-ttu-id="84fc0-110">Cmdleten **Update-AzNetAppFilesVolume** uppdaterar en ANF-volym.</span><span class="sxs-lookup"><span data-stu-id="84fc0-110">The **Update-AzNetAppFilesVolume** cmdlet updates an ANF volume.</span></span>

## <span data-ttu-id="84fc0-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="84fc0-111">EXAMPLES</span></span>

### <span data-ttu-id="84fc0-112">Exempel 1: uppdatera en ANF-volym</span><span class="sxs-lookup"><span data-stu-id="84fc0-112">Example 1: Update an ANF volume</span></span>
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

<span data-ttu-id="84fc0-113">Det här kommandot uppdaterar ANF-volymen "MyAnfVolume" med den nya UsageThreshold-storleken.</span><span class="sxs-lookup"><span data-stu-id="84fc0-113">This command updates the ANF volume "MyAnfVolume" with the new UsageThreshold size.</span></span>

## <span data-ttu-id="84fc0-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="84fc0-114">PARAMETERS</span></span>

### <span data-ttu-id="84fc0-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="84fc0-115">-AccountName</span></span>
<span data-ttu-id="84fc0-116">Namnet på ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="84fc0-116">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84fc0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84fc0-117">-DefaultProfile</span></span>
<span data-ttu-id="84fc0-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="84fc0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84fc0-119">-ExportPolicy</span><span class="sxs-lookup"><span data-stu-id="84fc0-119">-ExportPolicy</span></span>
<span data-ttu-id="84fc0-120">En hash-matris som representerar export policyn</span><span class="sxs-lookup"><span data-stu-id="84fc0-120">A hashtable array which represents the export policy</span></span>

```yaml
Type: PSNetAppFilesVolumeExportPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84fc0-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="84fc0-121">-InputObject</span></span>
<span data-ttu-id="84fc0-122">Volume-objekt som ska uppdateras</span><span class="sxs-lookup"><span data-stu-id="84fc0-122">The volume object to update</span></span>

```yaml
Type: PSNetAppFilesVolume
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="84fc0-123">-Plats</span><span class="sxs-lookup"><span data-stu-id="84fc0-123">-Location</span></span>
<span data-ttu-id="84fc0-124">Resursens plats</span><span class="sxs-lookup"><span data-stu-id="84fc0-124">The location of the resource</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84fc0-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="84fc0-125">-Name</span></span>
<span data-ttu-id="84fc0-126">Namnet på ANF-volymen</span><span class="sxs-lookup"><span data-stu-id="84fc0-126">The name of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84fc0-127">-PoolName</span><span class="sxs-lookup"><span data-stu-id="84fc0-127">-PoolName</span></span>
<span data-ttu-id="84fc0-128">Namnet på ANF-poolen</span><span class="sxs-lookup"><span data-stu-id="84fc0-128">The name of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84fc0-129">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="84fc0-129">-PoolObject</span></span>
<span data-ttu-id="84fc0-130">Det pool-objekt som innehåller volymen som ska uppdateras</span><span class="sxs-lookup"><span data-stu-id="84fc0-130">The pool object containing the volume to update</span></span>

```yaml
Type: PSNetAppFilesPool
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="84fc0-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84fc0-131">-ResourceGroupName</span></span>
<span data-ttu-id="84fc0-132">Resurs gruppen för ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="84fc0-132">The resource group of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84fc0-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="84fc0-133">-ResourceId</span></span>
<span data-ttu-id="84fc0-134">Resurs-ID för ANF volym</span><span class="sxs-lookup"><span data-stu-id="84fc0-134">The resource id of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84fc0-135">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="84fc0-135">-ServiceLevel</span></span>
<span data-ttu-id="84fc0-136">Service nivån för ANF-volymen</span><span class="sxs-lookup"><span data-stu-id="84fc0-136">The service level of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84fc0-137">-Tagg</span><span class="sxs-lookup"><span data-stu-id="84fc0-137">-Tag</span></span>
<span data-ttu-id="84fc0-138">En hash som representerar resurs koder</span><span class="sxs-lookup"><span data-stu-id="84fc0-138">A hashtable which represents resource tags</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84fc0-139">-UsageThreshold</span><span class="sxs-lookup"><span data-stu-id="84fc0-139">-UsageThreshold</span></span>
<span data-ttu-id="84fc0-140">Den maximala lagrings kvoten som tillåts för ett fil system i byte</span><span class="sxs-lookup"><span data-stu-id="84fc0-140">The maximum storage quota allowed for a file system in bytes</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84fc0-141">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="84fc0-141">-Confirm</span></span>
<span data-ttu-id="84fc0-142">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="84fc0-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84fc0-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84fc0-143">-WhatIf</span></span>
<span data-ttu-id="84fc0-144">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="84fc0-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84fc0-145">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="84fc0-145">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84fc0-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84fc0-146">CommonParameters</span></span>
<span data-ttu-id="84fc0-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84fc0-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="84fc0-148">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84fc0-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84fc0-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="84fc0-149">INPUTS</span></span>

### <span data-ttu-id="84fc0-150">System. String</span><span class="sxs-lookup"><span data-stu-id="84fc0-150">System.String</span></span>

### <span data-ttu-id="84fc0-151">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="84fc0-151">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="84fc0-152">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="84fc0-152">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="84fc0-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="84fc0-153">OUTPUTS</span></span>

### <span data-ttu-id="84fc0-154">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="84fc0-154">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="84fc0-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="84fc0-155">NOTES</span></span>

## <span data-ttu-id="84fc0-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="84fc0-156">RELATED LINKS</span></span>

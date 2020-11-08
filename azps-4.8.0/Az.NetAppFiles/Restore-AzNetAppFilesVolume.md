---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/restore-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Restore-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Restore-AzNetAppFilesVolume.md
ms.openlocfilehash: 486bd44d3f48213fde6fb9b6c1d15a5683c1fd82
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258326"
---
# <span data-ttu-id="77e38-101">Restore-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="77e38-101">Restore-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="77e38-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="77e38-102">SYNOPSIS</span></span>
<span data-ttu-id="77e38-103">Återställa eller återställa en volym till en av dess stillbilder</span><span class="sxs-lookup"><span data-stu-id="77e38-103">Restore/Revert a volume to one of its snapshots</span></span>

## <span data-ttu-id="77e38-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="77e38-104">SYNTAX</span></span>

### <span data-ttu-id="77e38-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="77e38-105">ByFieldsParameterSet (Default)</span></span>
```
Revert-AzNetAppFilesVolume -ResourceGroupName <String> -AccountName <String> -PoolName <String> -Name <String>
 [-SnapshotId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="77e38-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="77e38-106">ByParentObjectParameterSet</span></span>
```
Restore-AzNetAppFilesVolume -Name <String> -PoolObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77e38-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="77e38-107">ByResourceIdParameterSet</span></span>
```
Restore-AzNetAppFilesVolume -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77e38-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="77e38-108">ByObjectParameterSet</span></span>
```
Restore-AzNetAppFilesVolume -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77e38-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="77e38-109">DESCRIPTION</span></span>
<span data-ttu-id="77e38-110">Återställa eller återställa en volym till den ögonblicks bild som anges i SnapshotId parameter</span><span class="sxs-lookup"><span data-stu-id="77e38-110">Restore/Revert a volume to the snapshot specified in the SnapshotId paramter</span></span>

## <span data-ttu-id="77e38-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="77e38-111">EXAMPLES</span></span>

### <span data-ttu-id="77e38-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="77e38-112">Example 1</span></span>
```powershell
PS C:\> Restore-AzNetAppFilesVolume -ResourceGroupName "MyRG" -Location "westus2" -AccountName "MyAccount" -PoolName "MyPool" -VolumeName "MyVolume" -SnapshotId 7d6e4069-6c78-6c61-7bf6-c60968e45fbf
```

<span data-ttu-id="77e38-113">Det här kommandot återställer/återställer volymen volym till en av sina stillbilder med snapshotId för 7d6e4069-6c78-6c61-7bf6-c60968e45fbf</span><span class="sxs-lookup"><span data-stu-id="77e38-113">This command Restores/Reverts the volume MyVolume to one of its snapshots with the snapshotId of 7d6e4069-6c78-6c61-7bf6-c60968e45fbf</span></span>

## <span data-ttu-id="77e38-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="77e38-114">PARAMETERS</span></span>

### <span data-ttu-id="77e38-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="77e38-115">-AccountName</span></span>
<span data-ttu-id="77e38-116">Namnet på ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="77e38-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="77e38-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77e38-117">-DefaultProfile</span></span>
<span data-ttu-id="77e38-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="77e38-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77e38-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="77e38-119">-InputObject</span></span>
<span data-ttu-id="77e38-120">Volume-objekt som ska tas bort</span><span class="sxs-lookup"><span data-stu-id="77e38-120">The volume object to remove</span></span>

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

### <span data-ttu-id="77e38-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="77e38-121">-Name</span></span>
<span data-ttu-id="77e38-122">Namnet på ANF-volymen</span><span class="sxs-lookup"><span data-stu-id="77e38-122">The name of the ANF volume</span></span>

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

### <span data-ttu-id="77e38-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="77e38-123">-PassThru</span></span>
<span data-ttu-id="77e38-124">Returnera om den angivna volymen har återställts eller återställts</span><span class="sxs-lookup"><span data-stu-id="77e38-124">Return whether the specified volume was successfully restored/reverted</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77e38-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="77e38-125">-PoolName</span></span>
<span data-ttu-id="77e38-126">Namnet på ANF-poolen</span><span class="sxs-lookup"><span data-stu-id="77e38-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="77e38-127">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="77e38-127">-PoolObject</span></span>
<span data-ttu-id="77e38-128">Det pool-objekt som innehåller volymen som ska tas bort</span><span class="sxs-lookup"><span data-stu-id="77e38-128">The pool object containing the volume to remove</span></span>

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

### <span data-ttu-id="77e38-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77e38-129">-ResourceGroupName</span></span>
<span data-ttu-id="77e38-130">ANF-volymens resurs grupp</span><span class="sxs-lookup"><span data-stu-id="77e38-130">The resource group of the ANF volume</span></span>

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

### <span data-ttu-id="77e38-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="77e38-131">-ResourceId</span></span>
<span data-ttu-id="77e38-132">Resurs-ID för ANF volym</span><span class="sxs-lookup"><span data-stu-id="77e38-132">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="77e38-133">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="77e38-133">-SnapshotId</span></span>
<span data-ttu-id="77e38-134">SnapshotId av ögonblicks bilden.</span><span class="sxs-lookup"><span data-stu-id="77e38-134">SnapshotId of the snapshot.</span></span>
<span data-ttu-id="77e38-135">UUID v4 som används för att identifiera ögonblicks bilden</span><span class="sxs-lookup"><span data-stu-id="77e38-135">UUID v4 used to identify the Snapshot</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77e38-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="77e38-136">-Confirm</span></span>
<span data-ttu-id="77e38-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="77e38-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77e38-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77e38-138">-WhatIf</span></span>
<span data-ttu-id="77e38-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="77e38-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77e38-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="77e38-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77e38-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77e38-141">CommonParameters</span></span>
<span data-ttu-id="77e38-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77e38-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77e38-143">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="77e38-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77e38-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="77e38-144">INPUTS</span></span>

### <span data-ttu-id="77e38-145">System. String</span><span class="sxs-lookup"><span data-stu-id="77e38-145">System.String</span></span>

### <span data-ttu-id="77e38-146">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="77e38-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="77e38-147">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="77e38-147">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="77e38-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="77e38-148">OUTPUTS</span></span>

### <span data-ttu-id="77e38-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="77e38-149">System.Boolean</span></span>

## <span data-ttu-id="77e38-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="77e38-150">NOTES</span></span>

## <span data-ttu-id="77e38-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="77e38-151">RELATED LINKS</span></span>

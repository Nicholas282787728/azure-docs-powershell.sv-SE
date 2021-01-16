---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/restore-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Restore-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Restore-AzNetAppFilesVolume.md
ms.openlocfilehash: 6606de1a5d4de6df6ecafa700ac1b93d31399b43
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98387648"
---
# <span data-ttu-id="2de18-101">Restore-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="2de18-101">Restore-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="2de18-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2de18-102">SYNOPSIS</span></span>
<span data-ttu-id="2de18-103">Återställa eller återställa en volym till en av dess stillbilder</span><span class="sxs-lookup"><span data-stu-id="2de18-103">Restore/Revert a volume to one of its snapshots</span></span>

## <span data-ttu-id="2de18-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2de18-104">SYNTAX</span></span>

### <span data-ttu-id="2de18-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="2de18-105">ByFieldsParameterSet (Default)</span></span>
```
Restore-AzNetAppFilesVolume -ResourceGroupName <String> -AccountName <String> -PoolName <String> -Name <String>
 [-SnapshotId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2de18-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2de18-106">ByParentObjectParameterSet</span></span>
```
Restore-AzNetAppFilesVolume -Name <String> -PoolObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2de18-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2de18-107">ByResourceIdParameterSet</span></span>
```
Restore-AzNetAppFilesVolume -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2de18-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2de18-108">ByObjectParameterSet</span></span>
```
Restore-AzNetAppFilesVolume -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2de18-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2de18-109">DESCRIPTION</span></span>
<span data-ttu-id="2de18-110">Återställa eller återställa en volym till den ögonblicks bild som anges i SnapshotId parameter</span><span class="sxs-lookup"><span data-stu-id="2de18-110">Restore/Revert a volume to the snapshot specified in the SnapshotId paramter</span></span>

## <span data-ttu-id="2de18-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2de18-111">EXAMPLES</span></span>

### <span data-ttu-id="2de18-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2de18-112">Example 1</span></span>
```powershell
PS C:\> Restore-AzNetAppFilesVolume -ResourceGroupName "MyRG" -Location "westus2" -AccountName "MyAccount" -PoolName "MyPool" -VolumeName "MyVolume" -SnapshotId 7d6e4069-6c78-6c61-7bf6-c60968e45fbf
```

<span data-ttu-id="2de18-113">Det här kommandot återställer/återställer volymen volym till en av sina stillbilder med snapshotId för 7d6e4069-6c78-6c61-7bf6-c60968e45fbf</span><span class="sxs-lookup"><span data-stu-id="2de18-113">This command Restores/Reverts the volume MyVolume to one of its snapshots with the snapshotId of 7d6e4069-6c78-6c61-7bf6-c60968e45fbf</span></span>

## <span data-ttu-id="2de18-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2de18-114">PARAMETERS</span></span>

### <span data-ttu-id="2de18-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2de18-115">-AccountName</span></span>
<span data-ttu-id="2de18-116">Namnet på ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="2de18-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="2de18-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2de18-117">-DefaultProfile</span></span>
<span data-ttu-id="2de18-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2de18-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2de18-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2de18-119">-InputObject</span></span>
<span data-ttu-id="2de18-120">Volume-objekt som ska tas bort</span><span class="sxs-lookup"><span data-stu-id="2de18-120">The volume object to remove</span></span>

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

### <span data-ttu-id="2de18-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="2de18-121">-Name</span></span>
<span data-ttu-id="2de18-122">Namnet på ANF-volymen</span><span class="sxs-lookup"><span data-stu-id="2de18-122">The name of the ANF volume</span></span>

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

### <span data-ttu-id="2de18-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2de18-123">-PassThru</span></span>
<span data-ttu-id="2de18-124">Returnera om den angivna volymen har återställts eller återställts</span><span class="sxs-lookup"><span data-stu-id="2de18-124">Return whether the specified volume was successfully restored/reverted</span></span>

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

### <span data-ttu-id="2de18-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="2de18-125">-PoolName</span></span>
<span data-ttu-id="2de18-126">Namnet på ANF-poolen</span><span class="sxs-lookup"><span data-stu-id="2de18-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="2de18-127">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="2de18-127">-PoolObject</span></span>
<span data-ttu-id="2de18-128">Det pool-objekt som innehåller volymen som ska tas bort</span><span class="sxs-lookup"><span data-stu-id="2de18-128">The pool object containing the volume to remove</span></span>

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

### <span data-ttu-id="2de18-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2de18-129">-ResourceGroupName</span></span>
<span data-ttu-id="2de18-130">ANF-volymens resurs grupp</span><span class="sxs-lookup"><span data-stu-id="2de18-130">The resource group of the ANF volume</span></span>

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

### <span data-ttu-id="2de18-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2de18-131">-ResourceId</span></span>
<span data-ttu-id="2de18-132">Resurs-ID för ANF volym</span><span class="sxs-lookup"><span data-stu-id="2de18-132">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="2de18-133">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="2de18-133">-SnapshotId</span></span>
<span data-ttu-id="2de18-134">SnapshotId av ögonblicks bilden.</span><span class="sxs-lookup"><span data-stu-id="2de18-134">SnapshotId of the snapshot.</span></span>
<span data-ttu-id="2de18-135">UUID v4 som används för att identifiera ögonblicks bilden</span><span class="sxs-lookup"><span data-stu-id="2de18-135">UUID v4 used to identify the Snapshot</span></span>

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

### <span data-ttu-id="2de18-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2de18-136">-Confirm</span></span>
<span data-ttu-id="2de18-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2de18-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2de18-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2de18-138">-WhatIf</span></span>
<span data-ttu-id="2de18-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2de18-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2de18-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2de18-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2de18-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2de18-141">CommonParameters</span></span>
<span data-ttu-id="2de18-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2de18-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2de18-143">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2de18-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2de18-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2de18-144">INPUTS</span></span>

### <span data-ttu-id="2de18-145">System. String</span><span class="sxs-lookup"><span data-stu-id="2de18-145">System.String</span></span>

### <span data-ttu-id="2de18-146">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="2de18-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="2de18-147">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="2de18-147">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="2de18-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2de18-148">OUTPUTS</span></span>

### <span data-ttu-id="2de18-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2de18-149">System.Boolean</span></span>

## <span data-ttu-id="2de18-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2de18-150">NOTES</span></span>

## <span data-ttu-id="2de18-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2de18-151">RELATED LINKS</span></span>

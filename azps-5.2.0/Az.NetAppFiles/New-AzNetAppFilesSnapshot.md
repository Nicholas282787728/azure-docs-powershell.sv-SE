---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilessnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesSnapshot.md
ms.openlocfilehash: 1fe8da5c9ee899b7aa1a77a9fbb0ac7a2bf3b35c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98410731"
---
# <span data-ttu-id="71e82-101">New-AzNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="71e82-101">New-AzNetAppFilesSnapshot</span></span>

## <span data-ttu-id="71e82-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="71e82-102">SYNOPSIS</span></span>
<span data-ttu-id="71e82-103">Skapar en ny Azure NetApp (ANF) ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="71e82-103">Creates a new Azure NetApp Files (ANF) snapshot.</span></span>

## <span data-ttu-id="71e82-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="71e82-104">SYNTAX</span></span>

### <span data-ttu-id="71e82-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="71e82-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesSnapshot -ResourceGroupName <String> -Location <String> -AccountName <String>
 -PoolName <String> -VolumeName <String> -Name <String> [-FileSystemId <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71e82-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="71e82-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesSnapshot -Name <String> [-Tag <Hashtable>] -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71e82-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="71e82-107">DESCRIPTION</span></span>
<span data-ttu-id="71e82-108">Cmdleten **New-AzNetAppFilesSnapshot** skapar en ANF-stillbild.</span><span class="sxs-lookup"><span data-stu-id="71e82-108">The **New-AzNetAppFilesSnapshot** cmdlet creates an ANF snapshot.</span></span>

## <span data-ttu-id="71e82-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="71e82-109">EXAMPLES</span></span>

### <span data-ttu-id="71e82-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="71e82-110">Example 1</span></span>
```
PS C:\>New-AzNetAppFilesSnapshot -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyAnfVolume" -SnapshotName "MyAnfSnapshot" -FileSystemId "3e2773a7-2a72-d003-0637-1a8b1fa3eaaf"

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool/volumes/MyAnfVolume/snapshots/MyAnfSnapshot
Name              : MyAnfAccount/MyAnfPool/MyAnfVolume/MyAnfSnapshot
Type              : Microsoft.NetApp/netAppAccounts/capacityPools/volumes/snapshots
Tags              :
SnapshotId        : ca7c4ebd-91cb-0e30-91f5-9154050033df
FileSystemId      : 3e2773a7-2a72-d003-0637-1a8b1fa3eaaf
Created           :
ProvisioningState : Succeeded
```

<span data-ttu-id="71e82-111">Det här kommandot skapar den nya ANF-stillbilden "MyAnfSnapshot" i volymen "MyAnfVolume".</span><span class="sxs-lookup"><span data-stu-id="71e82-111">This command creates the new ANF snapshot "MyAnfSnapshot" within the volume "MyAnfVolume".</span></span>

## <span data-ttu-id="71e82-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="71e82-112">PARAMETERS</span></span>

### <span data-ttu-id="71e82-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="71e82-113">-AccountName</span></span>
<span data-ttu-id="71e82-114">Namnet på ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="71e82-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="71e82-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71e82-115">-DefaultProfile</span></span>
<span data-ttu-id="71e82-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="71e82-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71e82-117">-FileSystemId</span><span class="sxs-lookup"><span data-stu-id="71e82-117">-FileSystemId</span></span>
<span data-ttu-id="71e82-118">Fil systemets ID</span><span class="sxs-lookup"><span data-stu-id="71e82-118">The file system id</span></span>

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

### <span data-ttu-id="71e82-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="71e82-119">-Location</span></span>
<span data-ttu-id="71e82-120">Resursens plats</span><span class="sxs-lookup"><span data-stu-id="71e82-120">The location of the resource</span></span>

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

### <span data-ttu-id="71e82-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="71e82-121">-Name</span></span>
<span data-ttu-id="71e82-122">Namn på ANF ögonblicks bild</span><span class="sxs-lookup"><span data-stu-id="71e82-122">The name of the ANF snapshot</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SnapshotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71e82-123">-PoolName</span><span class="sxs-lookup"><span data-stu-id="71e82-123">-PoolName</span></span>
<span data-ttu-id="71e82-124">Namnet på ANF-poolen</span><span class="sxs-lookup"><span data-stu-id="71e82-124">The name of the ANF pool</span></span>

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

### <span data-ttu-id="71e82-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71e82-125">-ResourceGroupName</span></span>
<span data-ttu-id="71e82-126">Resurs gruppen för ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="71e82-126">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="71e82-127">-Tagg</span><span class="sxs-lookup"><span data-stu-id="71e82-127">-Tag</span></span>
<span data-ttu-id="71e82-128">En hash som representerar resurs koder</span><span class="sxs-lookup"><span data-stu-id="71e82-128">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="71e82-129">-Volym namn</span><span class="sxs-lookup"><span data-stu-id="71e82-129">-VolumeName</span></span>
<span data-ttu-id="71e82-130">Namnet på ANF-volymen</span><span class="sxs-lookup"><span data-stu-id="71e82-130">The name of the ANF volume</span></span>

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

### <span data-ttu-id="71e82-131">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="71e82-131">-VolumeObject</span></span>
<span data-ttu-id="71e82-132">Volymen för det nya Snapshot-objektet</span><span class="sxs-lookup"><span data-stu-id="71e82-132">The volume for the new snapshot object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="71e82-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="71e82-133">-Confirm</span></span>
<span data-ttu-id="71e82-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="71e82-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71e82-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71e82-135">-WhatIf</span></span>
<span data-ttu-id="71e82-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="71e82-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71e82-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="71e82-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71e82-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71e82-138">CommonParameters</span></span>
<span data-ttu-id="71e82-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71e82-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71e82-140">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="71e82-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71e82-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="71e82-141">INPUTS</span></span>

### <span data-ttu-id="71e82-142">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="71e82-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="71e82-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="71e82-143">OUTPUTS</span></span>

### <span data-ttu-id="71e82-144">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="71e82-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span></span>

## <span data-ttu-id="71e82-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="71e82-145">NOTES</span></span>

## <span data-ttu-id="71e82-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="71e82-146">RELATED LINKS</span></span>

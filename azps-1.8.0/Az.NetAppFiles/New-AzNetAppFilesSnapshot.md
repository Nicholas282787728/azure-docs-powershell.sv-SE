---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilessnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesSnapshot.md
ms.openlocfilehash: bad4c1dfc2317bcc4d03414980cafa73c78949d2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754001"
---
# <span data-ttu-id="8cc33-101">New-AzNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="8cc33-101">New-AzNetAppFilesSnapshot</span></span>

## <span data-ttu-id="8cc33-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8cc33-102">SYNOPSIS</span></span>
<span data-ttu-id="8cc33-103">Skapar en ny Azure NetApp (ANF) ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="8cc33-103">Creates a new Azure NetApp Files (ANF) snapshot.</span></span>

## <span data-ttu-id="8cc33-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8cc33-104">SYNTAX</span></span>

### <span data-ttu-id="8cc33-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="8cc33-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesSnapshot -ResourceGroupName <String> -Location <String> -AccountName <String>
 -PoolName <String> -VolumeName <String> -Name <String> -FileSystemId <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cc33-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8cc33-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesSnapshot -Name <String> [-Tag <Hashtable>] -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8cc33-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8cc33-107">DESCRIPTION</span></span>
<span data-ttu-id="8cc33-108">Cmdleten **New-AzNetAppFilesSnapshot** skapar en ANF-stillbild.</span><span class="sxs-lookup"><span data-stu-id="8cc33-108">The **New-AzNetAppFilesSnapshot** cmdlet creates an ANF snapshot.</span></span>

## <span data-ttu-id="8cc33-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8cc33-109">EXAMPLES</span></span>

### <span data-ttu-id="8cc33-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8cc33-110">Example 1</span></span>
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
CreationDate      :
ProvisioningState : Succeeded
```

<span data-ttu-id="8cc33-111">Det här kommandot skapar den nya ANF-stillbilden "MyAnfSnapshot" i volymen "MyAnfVolume".</span><span class="sxs-lookup"><span data-stu-id="8cc33-111">This command creates the new ANF snapshot "MyAnfSnapshot" within the volume "MyAnfVolume".</span></span>

## <span data-ttu-id="8cc33-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8cc33-112">PARAMETERS</span></span>

### <span data-ttu-id="8cc33-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8cc33-113">-AccountName</span></span>
<span data-ttu-id="8cc33-114">Namnet på ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="8cc33-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="8cc33-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cc33-115">-DefaultProfile</span></span>
<span data-ttu-id="8cc33-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8cc33-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8cc33-117">-FileSystemId</span><span class="sxs-lookup"><span data-stu-id="8cc33-117">-FileSystemId</span></span>
<span data-ttu-id="8cc33-118">Fil systemets ID</span><span class="sxs-lookup"><span data-stu-id="8cc33-118">The file system id</span></span>

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

### <span data-ttu-id="8cc33-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="8cc33-119">-Location</span></span>
<span data-ttu-id="8cc33-120">Resursens plats</span><span class="sxs-lookup"><span data-stu-id="8cc33-120">The location of the resource</span></span>

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

### <span data-ttu-id="8cc33-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="8cc33-121">-Name</span></span>
<span data-ttu-id="8cc33-122">Namn på ANF ögonblicks bild</span><span class="sxs-lookup"><span data-stu-id="8cc33-122">The name of the ANF snapshot</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SnapshotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cc33-123">-PoolName</span><span class="sxs-lookup"><span data-stu-id="8cc33-123">-PoolName</span></span>
<span data-ttu-id="8cc33-124">Namnet på ANF-poolen</span><span class="sxs-lookup"><span data-stu-id="8cc33-124">The name of the ANF pool</span></span>

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

### <span data-ttu-id="8cc33-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cc33-125">-ResourceGroupName</span></span>
<span data-ttu-id="8cc33-126">Resurs gruppen för ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="8cc33-126">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="8cc33-127">-Tagg</span><span class="sxs-lookup"><span data-stu-id="8cc33-127">-Tag</span></span>
<span data-ttu-id="8cc33-128">En hash som representerar resurs koder</span><span class="sxs-lookup"><span data-stu-id="8cc33-128">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="8cc33-129">-Volym namn</span><span class="sxs-lookup"><span data-stu-id="8cc33-129">-VolumeName</span></span>
<span data-ttu-id="8cc33-130">Namnet på ANF-volymen</span><span class="sxs-lookup"><span data-stu-id="8cc33-130">The name of the ANF volume</span></span>

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

### <span data-ttu-id="8cc33-131">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="8cc33-131">-VolumeObject</span></span>
<span data-ttu-id="8cc33-132">Volymen för det nya Snapshot-objektet</span><span class="sxs-lookup"><span data-stu-id="8cc33-132">The volume for the new snapshot object</span></span>

```yaml
Type: PSNetAppFilesVolume
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8cc33-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8cc33-133">-Confirm</span></span>
<span data-ttu-id="8cc33-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8cc33-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8cc33-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8cc33-135">-WhatIf</span></span>
<span data-ttu-id="8cc33-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8cc33-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8cc33-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8cc33-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8cc33-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cc33-138">CommonParameters</span></span>
<span data-ttu-id="8cc33-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cc33-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="8cc33-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cc33-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cc33-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8cc33-141">INPUTS</span></span>

### <span data-ttu-id="8cc33-142">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="8cc33-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="8cc33-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8cc33-143">OUTPUTS</span></span>

### <span data-ttu-id="8cc33-144">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="8cc33-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span></span>

## <span data-ttu-id="8cc33-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8cc33-145">NOTES</span></span>

## <span data-ttu-id="8cc33-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8cc33-146">RELATED LINKS</span></span>

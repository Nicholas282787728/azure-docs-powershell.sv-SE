---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesVolume.md
ms.openlocfilehash: ea943c490a87dd4c62752b97753971f0941ed3b9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753988"
---
# <span data-ttu-id="3261c-101">Update-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="3261c-101">Update-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="3261c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3261c-102">SYNOPSIS</span></span>
<span data-ttu-id="3261c-103">Uppdaterar en Azure NetApp-fil (ANF) enligt de valfria modifieringarna.</span><span class="sxs-lookup"><span data-stu-id="3261c-103">Updates an Azure NetApp Files (ANF) volume according to the optional modifiers provided.</span></span>

## <span data-ttu-id="3261c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3261c-104">SYNTAX</span></span>

### <span data-ttu-id="3261c-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="3261c-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesVolume -ResourceGroupName <String> -Location <String> -AccountName <String>
 -PoolName <String> -Name <String> [-UsageThreshold <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3261c-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3261c-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesVolume -Name <String> [-UsageThreshold <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>]
 -PoolObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3261c-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3261c-107">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesVolume [-UsageThreshold <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>]
 -InputObject <PSNetAppFilesVolume> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3261c-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3261c-108">DESCRIPTION</span></span>
<span data-ttu-id="3261c-109">Cmdleten **Update-AzNetAppFilesVolume** uppdaterar en ANF-volym.</span><span class="sxs-lookup"><span data-stu-id="3261c-109">The **Update-AzNetAppFilesVolume** cmdlet updates an ANF volume.</span></span>

## <span data-ttu-id="3261c-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3261c-110">EXAMPLES</span></span>

### <span data-ttu-id="3261c-111">Exempel 1: uppdatera en ANF-volym</span><span class="sxs-lookup"><span data-stu-id="3261c-111">Example 1: Update an ANF volume</span></span>
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

<span data-ttu-id="3261c-112">Det här kommandot uppdaterar ANF-volymen "MyAnfVolume" med den nya UsageThreshold-storleken.</span><span class="sxs-lookup"><span data-stu-id="3261c-112">This command updates the ANF volume "MyAnfVolume" with the new UsageThreshold size.</span></span>

## <span data-ttu-id="3261c-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3261c-113">PARAMETERS</span></span>

### <span data-ttu-id="3261c-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3261c-114">-AccountName</span></span>
<span data-ttu-id="3261c-115">Namnet på ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="3261c-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="3261c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3261c-116">-DefaultProfile</span></span>
<span data-ttu-id="3261c-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3261c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3261c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3261c-118">-InputObject</span></span>
<span data-ttu-id="3261c-119">Volume-objekt som ska uppdateras</span><span class="sxs-lookup"><span data-stu-id="3261c-119">The volume object to update</span></span>

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

### <span data-ttu-id="3261c-120">-Plats</span><span class="sxs-lookup"><span data-stu-id="3261c-120">-Location</span></span>
<span data-ttu-id="3261c-121">Resursens plats</span><span class="sxs-lookup"><span data-stu-id="3261c-121">The location of the resource</span></span>

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

### <span data-ttu-id="3261c-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="3261c-122">-Name</span></span>
<span data-ttu-id="3261c-123">Namnet på ANF-volymen</span><span class="sxs-lookup"><span data-stu-id="3261c-123">The name of the ANF volume</span></span>

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

### <span data-ttu-id="3261c-124">-PoolName</span><span class="sxs-lookup"><span data-stu-id="3261c-124">-PoolName</span></span>
<span data-ttu-id="3261c-125">Namnet på ANF-poolen</span><span class="sxs-lookup"><span data-stu-id="3261c-125">The name of the ANF pool</span></span>

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

### <span data-ttu-id="3261c-126">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="3261c-126">-PoolObject</span></span>
<span data-ttu-id="3261c-127">Det pool-objekt som innehåller volymen som ska uppdateras</span><span class="sxs-lookup"><span data-stu-id="3261c-127">The pool object containing the volume to update</span></span>

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

### <span data-ttu-id="3261c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3261c-128">-ResourceGroupName</span></span>
<span data-ttu-id="3261c-129">Resurs gruppen för ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="3261c-129">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="3261c-130">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="3261c-130">-ServiceLevel</span></span>
<span data-ttu-id="3261c-131">Service nivån för ANF-volymen</span><span class="sxs-lookup"><span data-stu-id="3261c-131">The service level of the ANF volume</span></span>

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

### <span data-ttu-id="3261c-132">-Tagg</span><span class="sxs-lookup"><span data-stu-id="3261c-132">-Tag</span></span>
<span data-ttu-id="3261c-133">En hash som representerar resurs koder</span><span class="sxs-lookup"><span data-stu-id="3261c-133">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="3261c-134">-UsageThreshold</span><span class="sxs-lookup"><span data-stu-id="3261c-134">-UsageThreshold</span></span>
<span data-ttu-id="3261c-135">Den maximala lagrings kvoten som tillåts för ett fil system i byte</span><span class="sxs-lookup"><span data-stu-id="3261c-135">The maximum storage quota allowed for a file system in bytes</span></span>

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

### <span data-ttu-id="3261c-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3261c-136">-Confirm</span></span>
<span data-ttu-id="3261c-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3261c-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3261c-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3261c-138">-WhatIf</span></span>
<span data-ttu-id="3261c-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3261c-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3261c-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3261c-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3261c-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3261c-141">CommonParameters</span></span>
<span data-ttu-id="3261c-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3261c-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="3261c-143">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3261c-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3261c-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3261c-144">INPUTS</span></span>

### <span data-ttu-id="3261c-145">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="3261c-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="3261c-146">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="3261c-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="3261c-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3261c-147">OUTPUTS</span></span>

### <span data-ttu-id="3261c-148">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="3261c-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="3261c-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3261c-149">NOTES</span></span>

## <span data-ttu-id="3261c-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3261c-150">RELATED LINKS</span></span>
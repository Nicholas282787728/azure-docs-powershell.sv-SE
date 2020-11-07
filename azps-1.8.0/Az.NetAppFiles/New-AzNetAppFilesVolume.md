---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
ms.openlocfilehash: b742c8af0e8c36d07b2c608e74f0a02349502104
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754000"
---
# <span data-ttu-id="7ed84-101">New-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="7ed84-101">New-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="7ed84-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7ed84-102">SYNOPSIS</span></span>
<span data-ttu-id="7ed84-103">Skapar en ny Azure NetApp (ANF) volym.</span><span class="sxs-lookup"><span data-stu-id="7ed84-103">Creates a new Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="7ed84-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7ed84-104">SYNTAX</span></span>

### <span data-ttu-id="7ed84-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="7ed84-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesVolume -ResourceGroupName <String> -Location <String> -AccountName <String> -PoolName <String>
 -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String> -ServiceLevel <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ed84-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ed84-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesVolume -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String>
 -ServiceLevel <String> [-Tag <Hashtable>] -PoolObject <PSNetAppFilesPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ed84-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7ed84-107">DESCRIPTION</span></span>
<span data-ttu-id="7ed84-108">Cmdleten **New-AzNetAppFilesVolume** skapar en ANF-volym.</span><span class="sxs-lookup"><span data-stu-id="7ed84-108">The **New-AzNetAppFilesVolume** cmdlet creates an ANF volume.</span></span>

## <span data-ttu-id="7ed84-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7ed84-109">EXAMPLES</span></span>

### <span data-ttu-id="7ed84-110">Exempel 1: skapa en ANF volym</span><span class="sxs-lookup"><span data-stu-id="7ed84-110">Example 1: Create an ANF volume</span></span>
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

<span data-ttu-id="7ed84-111">Det här kommandot skapar den nya ANF-volymen "MyAnfVolume" i poolen "MyAnfPool".</span><span class="sxs-lookup"><span data-stu-id="7ed84-111">This command creates the new ANF volume "MyAnfVolume" within the pool "MyAnfPool".</span></span>

## <span data-ttu-id="7ed84-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7ed84-112">PARAMETERS</span></span>

### <span data-ttu-id="7ed84-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7ed84-113">-AccountName</span></span>
<span data-ttu-id="7ed84-114">Namnet på ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="7ed84-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="7ed84-115">-CreationToken</span><span class="sxs-lookup"><span data-stu-id="7ed84-115">-CreationToken</span></span>
<span data-ttu-id="7ed84-116">En unik fil Sök väg för volymen</span><span class="sxs-lookup"><span data-stu-id="7ed84-116">A unique file path for the volume</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ed84-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ed84-117">-DefaultProfile</span></span>
<span data-ttu-id="7ed84-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7ed84-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ed84-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="7ed84-119">-Location</span></span>
<span data-ttu-id="7ed84-120">Resursens plats</span><span class="sxs-lookup"><span data-stu-id="7ed84-120">The location of the resource</span></span>

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

### <span data-ttu-id="7ed84-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="7ed84-121">-Name</span></span>
<span data-ttu-id="7ed84-122">Namnet på ANF-volymen</span><span class="sxs-lookup"><span data-stu-id="7ed84-122">The name of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ed84-123">-PoolName</span><span class="sxs-lookup"><span data-stu-id="7ed84-123">-PoolName</span></span>
<span data-ttu-id="7ed84-124">Namnet på ANF-poolen</span><span class="sxs-lookup"><span data-stu-id="7ed84-124">The name of the ANF pool</span></span>

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

### <span data-ttu-id="7ed84-125">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="7ed84-125">-PoolObject</span></span>
<span data-ttu-id="7ed84-126">Poolen för det nya volym objektet</span><span class="sxs-lookup"><span data-stu-id="7ed84-126">The pool for the new volume object</span></span>

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

### <span data-ttu-id="7ed84-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ed84-127">-ResourceGroupName</span></span>
<span data-ttu-id="7ed84-128">Resurs gruppen för ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="7ed84-128">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="7ed84-129">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="7ed84-129">-ServiceLevel</span></span>
<span data-ttu-id="7ed84-130">Service nivån för ANF-volymen</span><span class="sxs-lookup"><span data-stu-id="7ed84-130">The service level of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ed84-131">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="7ed84-131">-SubnetId</span></span>
<span data-ttu-id="7ed84-132">Azure Resource URI för ett delegerat undernät</span><span class="sxs-lookup"><span data-stu-id="7ed84-132">The Azure Resource URI for a delegated subnet</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ed84-133">-Tagg</span><span class="sxs-lookup"><span data-stu-id="7ed84-133">-Tag</span></span>
<span data-ttu-id="7ed84-134">En hash som representerar resurs koder</span><span class="sxs-lookup"><span data-stu-id="7ed84-134">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="7ed84-135">-UsageThreshold</span><span class="sxs-lookup"><span data-stu-id="7ed84-135">-UsageThreshold</span></span>
<span data-ttu-id="7ed84-136">Den maximala lagrings kvoten som tillåts för ett fil system i byte</span><span class="sxs-lookup"><span data-stu-id="7ed84-136">The maximum storage quota allowed for a file system in bytes</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ed84-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7ed84-137">-Confirm</span></span>
<span data-ttu-id="7ed84-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7ed84-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ed84-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ed84-139">-WhatIf</span></span>
<span data-ttu-id="7ed84-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7ed84-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ed84-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7ed84-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ed84-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ed84-142">CommonParameters</span></span>
<span data-ttu-id="7ed84-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ed84-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="7ed84-144">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ed84-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ed84-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7ed84-145">INPUTS</span></span>

### <span data-ttu-id="7ed84-146">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="7ed84-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="7ed84-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7ed84-147">OUTPUTS</span></span>

### <span data-ttu-id="7ed84-148">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="7ed84-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="7ed84-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7ed84-149">NOTES</span></span>

## <span data-ttu-id="7ed84-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7ed84-150">RELATED LINKS</span></span>

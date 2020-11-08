---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
ms.openlocfilehash: cad30d489b53ccfd9f45cbc619ce4384cc904903
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918592"
---
# <span data-ttu-id="c152a-101">New-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="c152a-101">New-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="c152a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c152a-102">SYNOPSIS</span></span>
<span data-ttu-id="c152a-103">Skapar en ny Azure NetApp (ANF) volym.</span><span class="sxs-lookup"><span data-stu-id="c152a-103">Creates a new Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="c152a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c152a-104">SYNTAX</span></span>

### <span data-ttu-id="c152a-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="c152a-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesVolume -ResourceGroupName <String> -Location <String> -AccountName <String> -PoolName <String>
 -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String> -ServiceLevel <String>
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>]
 [-ProtocolType <System.String[]>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c152a-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c152a-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesVolume -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String>
 -ServiceLevel <String> [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>]
 [-ProtocolType <System.String[]>]
 [-Tag <Hashtable>] -PoolObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c152a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c152a-107">DESCRIPTION</span></span>
<span data-ttu-id="c152a-108">Cmdleten **New-AzNetAppFilesVolume** skapar en ANF-volym.</span><span class="sxs-lookup"><span data-stu-id="c152a-108">The **New-AzNetAppFilesVolume** cmdlet creates an ANF volume.</span></span>

## <span data-ttu-id="c152a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c152a-109">EXAMPLES</span></span>

### <span data-ttu-id="c152a-110">Exempel 1: skapa en ANF volym</span><span class="sxs-lookup"><span data-stu-id="c152a-110">Example 1: Create an ANF volume</span></span>
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

<span data-ttu-id="c152a-111">Det här kommandot skapar den nya ANF-volymen "MyAnfVolume" i poolen "MyAnfPool".</span><span class="sxs-lookup"><span data-stu-id="c152a-111">This command creates the new ANF volume "MyAnfVolume" within the pool "MyAnfPool".</span></span>

## <span data-ttu-id="c152a-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c152a-112">PARAMETERS</span></span>

### <span data-ttu-id="c152a-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c152a-113">-AccountName</span></span>
<span data-ttu-id="c152a-114">Namnet på ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="c152a-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="c152a-115">-CreationToken</span><span class="sxs-lookup"><span data-stu-id="c152a-115">-CreationToken</span></span>
<span data-ttu-id="c152a-116">En unik fil Sök väg för volymen</span><span class="sxs-lookup"><span data-stu-id="c152a-116">A unique file path for the volume</span></span>

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

### <span data-ttu-id="c152a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c152a-117">-DefaultProfile</span></span>
<span data-ttu-id="c152a-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c152a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c152a-119">-ExportPolicy</span><span class="sxs-lookup"><span data-stu-id="c152a-119">-ExportPolicy</span></span>
<span data-ttu-id="c152a-120">En hash-matris som representerar export policyn</span><span class="sxs-lookup"><span data-stu-id="c152a-120">A hashtable array which represents the export policy</span></span>

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

### <span data-ttu-id="c152a-121">-Plats</span><span class="sxs-lookup"><span data-stu-id="c152a-121">-Location</span></span>
<span data-ttu-id="c152a-122">Resursens plats</span><span class="sxs-lookup"><span data-stu-id="c152a-122">The location of the resource</span></span>

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

### <span data-ttu-id="c152a-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="c152a-123">-Name</span></span>
<span data-ttu-id="c152a-124">Namnet på ANF-volymen</span><span class="sxs-lookup"><span data-stu-id="c152a-124">The name of the ANF volume</span></span>

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

### <span data-ttu-id="c152a-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="c152a-125">-PoolName</span></span>
<span data-ttu-id="c152a-126">Namnet på ANF-poolen</span><span class="sxs-lookup"><span data-stu-id="c152a-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="c152a-127">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="c152a-127">-PoolObject</span></span>
<span data-ttu-id="c152a-128">Poolen för det nya volym objektet</span><span class="sxs-lookup"><span data-stu-id="c152a-128">The pool for the new volume object</span></span>

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

### <span data-ttu-id="c152a-129">-ProtocolType</span><span class="sxs-lookup"><span data-stu-id="c152a-129">-ProtocolType</span></span>
<span data-ttu-id="c152a-130">En hash-matris som representerar export policyn</span><span class="sxs-lookup"><span data-stu-id="c152a-130">A hashtable array which represents the export policy</span></span>

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

### <span data-ttu-id="c152a-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c152a-131">-ResourceGroupName</span></span>
<span data-ttu-id="c152a-132">Resurs gruppen för ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="c152a-132">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="c152a-133">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="c152a-133">-ServiceLevel</span></span>
<span data-ttu-id="c152a-134">Service nivån för ANF-volymen</span><span class="sxs-lookup"><span data-stu-id="c152a-134">The service level of the ANF volume</span></span>

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

```yaml
Type: String
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c152a-135">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="c152a-135">-SubnetId</span></span>
<span data-ttu-id="c152a-136">Azure Resource URI för ett delegerat undernät</span><span class="sxs-lookup"><span data-stu-id="c152a-136">The Azure Resource URI for a delegated subnet</span></span>

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

### <span data-ttu-id="c152a-137">-Tagg</span><span class="sxs-lookup"><span data-stu-id="c152a-137">-Tag</span></span>
<span data-ttu-id="c152a-138">En hash som representerar resurs koder</span><span class="sxs-lookup"><span data-stu-id="c152a-138">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="c152a-139">-UsageThreshold</span><span class="sxs-lookup"><span data-stu-id="c152a-139">-UsageThreshold</span></span>
<span data-ttu-id="c152a-140">Den maximala lagrings kvoten som tillåts för ett fil system i byte</span><span class="sxs-lookup"><span data-stu-id="c152a-140">The maximum storage quota allowed for a file system in bytes</span></span>

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

### <span data-ttu-id="c152a-141">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c152a-141">-Confirm</span></span>
<span data-ttu-id="c152a-142">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c152a-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c152a-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c152a-143">-WhatIf</span></span>
<span data-ttu-id="c152a-144">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c152a-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c152a-145">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c152a-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c152a-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c152a-146">CommonParameters</span></span>
<span data-ttu-id="c152a-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c152a-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="c152a-148">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c152a-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c152a-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c152a-149">INPUTS</span></span>

### <span data-ttu-id="c152a-150">System. String</span><span class="sxs-lookup"><span data-stu-id="c152a-150">System.String</span></span>

### <span data-ttu-id="c152a-151">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="c152a-151">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="c152a-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c152a-152">OUTPUTS</span></span>

### <span data-ttu-id="c152a-153">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="c152a-153">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="c152a-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c152a-154">NOTES</span></span>

## <span data-ttu-id="c152a-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c152a-155">RELATED LINKS</span></span>
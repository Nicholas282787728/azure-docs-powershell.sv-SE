---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/suspend-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Suspend-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Suspend-AzNetAppFilesReplication.md
ms.openlocfilehash: ab4d79b4770f438b233e5bfcc740e79364955ea6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98422491"
---
# <span data-ttu-id="25b2d-101">Suspend-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="25b2d-101">Suspend-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="25b2d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="25b2d-102">SYNOPSIS</span></span>
<span data-ttu-id="25b2d-103">Pausa/bryta förbindelsen på mål volymen</span><span class="sxs-lookup"><span data-stu-id="25b2d-103">Suspend/break the replication connection on the destination volume</span></span>

## <span data-ttu-id="25b2d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="25b2d-104">SYNTAX</span></span>

### <span data-ttu-id="25b2d-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="25b2d-105">ByFieldsParameterSet (Default)</span></span>
```
Suspend-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-ForceBreak] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="25b2d-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="25b2d-106">ByResourceIdParameterSet</span></span>
```
Suspend-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25b2d-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="25b2d-107">ByObjectParameterSet</span></span>
```
Suspend-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25b2d-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="25b2d-108">DESCRIPTION</span></span>
<span data-ttu-id="25b2d-109">Pausa/bryta förbindelsen på mål volymen</span><span class="sxs-lookup"><span data-stu-id="25b2d-109">Suspend/break the replication connection on the destination volume</span></span>

## <span data-ttu-id="25b2d-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="25b2d-110">EXAMPLES</span></span>

### <span data-ttu-id="25b2d-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="25b2d-111">Example 1</span></span>
```powershell
PS C:\> Suspend-AnfReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyDestinationAnfVolume"
```

<span data-ttu-id="25b2d-112">Det här kommandot avaktiverar ANF på volymen "MyDestinationAnfVolume".</span><span class="sxs-lookup"><span data-stu-id="25b2d-112">This command suspends the ANF Replication connection on volume "MyDestinationAnfVolume".</span></span>

## <span data-ttu-id="25b2d-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="25b2d-113">PARAMETERS</span></span>

### <span data-ttu-id="25b2d-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="25b2d-114">-AccountName</span></span>
<span data-ttu-id="25b2d-115">Namnet på ANF-kontot för replikeringstjänsten</span><span class="sxs-lookup"><span data-stu-id="25b2d-115">The name of the ANF account of the replication volume</span></span>

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

### <span data-ttu-id="25b2d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25b2d-116">-DefaultProfile</span></span>
<span data-ttu-id="25b2d-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="25b2d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25b2d-118">-ForceBreak</span><span class="sxs-lookup"><span data-stu-id="25b2d-118">-ForceBreak</span></span>
<span data-ttu-id="25b2d-119">Om replikeringen befinner sig i status överföring och du vill tvinga fram en paus</span><span class="sxs-lookup"><span data-stu-id="25b2d-119">If replication is in status transferring and you want to force break the replication, set to true</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25b2d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="25b2d-120">-InputObject</span></span>
<span data-ttu-id="25b2d-121">ANF mål volym objekt med replikering för att brytas</span><span class="sxs-lookup"><span data-stu-id="25b2d-121">The ANF destination volume object with the replication to break</span></span>

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

### <span data-ttu-id="25b2d-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="25b2d-122">-Name</span></span>
<span data-ttu-id="25b2d-123">Namnet på ANF</span><span class="sxs-lookup"><span data-stu-id="25b2d-123">The name of the ANF replication destination volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25b2d-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="25b2d-124">-PassThru</span></span>
<span data-ttu-id="25b2d-125">Returnera om rasten för den angivna volym replikeringen utfördes</span><span class="sxs-lookup"><span data-stu-id="25b2d-125">Return whether the break of the specified volume replication was performed</span></span>

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

### <span data-ttu-id="25b2d-126">-PoolName</span><span class="sxs-lookup"><span data-stu-id="25b2d-126">-PoolName</span></span>
<span data-ttu-id="25b2d-127">Namnet på ANF-poolen för replikeringstjänsten</span><span class="sxs-lookup"><span data-stu-id="25b2d-127">The name of the ANF pool of the replication volume</span></span>

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

### <span data-ttu-id="25b2d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25b2d-128">-ResourceGroupName</span></span>
<span data-ttu-id="25b2d-129">Resurs gruppen för ANF</span><span class="sxs-lookup"><span data-stu-id="25b2d-129">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="25b2d-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="25b2d-130">-ResourceId</span></span>
<span data-ttu-id="25b2d-131">Resurs-ID för ANF</span><span class="sxs-lookup"><span data-stu-id="25b2d-131">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="25b2d-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="25b2d-132">-Confirm</span></span>
<span data-ttu-id="25b2d-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="25b2d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25b2d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25b2d-134">-WhatIf</span></span>
<span data-ttu-id="25b2d-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="25b2d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25b2d-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="25b2d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25b2d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25b2d-137">CommonParameters</span></span>
<span data-ttu-id="25b2d-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25b2d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25b2d-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="25b2d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25b2d-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="25b2d-140">INPUTS</span></span>

### <span data-ttu-id="25b2d-141">System. String</span><span class="sxs-lookup"><span data-stu-id="25b2d-141">System.String</span></span>

### <span data-ttu-id="25b2d-142">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="25b2d-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="25b2d-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="25b2d-143">OUTPUTS</span></span>

### <span data-ttu-id="25b2d-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="25b2d-144">System.Boolean</span></span>

## <span data-ttu-id="25b2d-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="25b2d-145">NOTES</span></span>

## <span data-ttu-id="25b2d-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="25b2d-146">RELATED LINKS</span></span>

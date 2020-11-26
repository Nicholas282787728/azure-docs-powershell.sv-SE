---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/approve-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Approve-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Approve-AzNetAppFilesReplication.md
ms.openlocfilehash: 9afa4f22de142dba7608d33ed04c972758911aa9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271622"
---
# <span data-ttu-id="2eaeb-101">Approve-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="2eaeb-101">Approve-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="2eaeb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2eaeb-102">SYNOPSIS</span></span>
<span data-ttu-id="2eaeb-103">Godkänn/auktorisera replikeringsanslutning på käll volymen</span><span class="sxs-lookup"><span data-stu-id="2eaeb-103">Approve/Authorize replication connection on the source volume</span></span>

## <span data-ttu-id="2eaeb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2eaeb-104">SYNTAX</span></span>

### <span data-ttu-id="2eaeb-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="2eaeb-105">ByFieldsParameterSet (Default)</span></span>
```
Approve-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> -DataProtectionVolumeId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2eaeb-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2eaeb-106">ByResourceIdParameterSet</span></span>
```
Approve-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2eaeb-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2eaeb-107">ByObjectParameterSet</span></span>
```
Approve-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2eaeb-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2eaeb-108">DESCRIPTION</span></span>
<span data-ttu-id="2eaeb-109">Godkänna replikeringsanslutning på käll volymen</span><span class="sxs-lookup"><span data-stu-id="2eaeb-109">Approve the replication connection on the source volume</span></span>

## <span data-ttu-id="2eaeb-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2eaeb-110">EXAMPLES</span></span>

### <span data-ttu-id="2eaeb-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2eaeb-111">Example 1</span></span>
```powershell
PS C:\> Approve-AzNetAppFilesReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyAnfVolume" -DataProtectionVolumeId "MyDestinationVolumeId"

Output:
remoteVolumeResourceId          : resourceId
```

<span data-ttu-id="2eaeb-112">Det här kommandot godkänner replikeringen på MyAnfVolume.</span><span class="sxs-lookup"><span data-stu-id="2eaeb-112">This command Approves the Replication on MyAnfVolume.</span></span>

## <span data-ttu-id="2eaeb-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2eaeb-113">PARAMETERS</span></span>

### <span data-ttu-id="2eaeb-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2eaeb-114">-AccountName</span></span>
<span data-ttu-id="2eaeb-115">Namnet på ANF-kontot för volymens replikeringskälla</span><span class="sxs-lookup"><span data-stu-id="2eaeb-115">The name of the ANF account of the replication source volume</span></span>

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

### <span data-ttu-id="2eaeb-116">-DataProtectionVolumeId</span><span class="sxs-lookup"><span data-stu-id="2eaeb-116">-DataProtectionVolumeId</span></span>
<span data-ttu-id="2eaeb-117">Fil systemets ID för mål data skydds volymen</span><span class="sxs-lookup"><span data-stu-id="2eaeb-117">The file system id of the destination data protection volume</span></span>

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

### <span data-ttu-id="2eaeb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2eaeb-118">-DefaultProfile</span></span>
<span data-ttu-id="2eaeb-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2eaeb-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2eaeb-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2eaeb-120">-InputObject</span></span>
<span data-ttu-id="2eaeb-121">ANF käll volym objekt</span><span class="sxs-lookup"><span data-stu-id="2eaeb-121">The ANF source volume object to authorized the replication destination</span></span>

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

### <span data-ttu-id="2eaeb-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="2eaeb-122">-Name</span></span>
<span data-ttu-id="2eaeb-123">Namnet på ANF</span><span class="sxs-lookup"><span data-stu-id="2eaeb-123">The name of the ANF replication source volume</span></span>

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

### <span data-ttu-id="2eaeb-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2eaeb-124">-PassThru</span></span>
<span data-ttu-id="2eaeb-125">Ange om replikeringstillståndet för den angivna volymen utfördes</span><span class="sxs-lookup"><span data-stu-id="2eaeb-125">Return whether replication authorization of the specified volume was performed</span></span>

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

### <span data-ttu-id="2eaeb-126">-PoolName</span><span class="sxs-lookup"><span data-stu-id="2eaeb-126">-PoolName</span></span>
<span data-ttu-id="2eaeb-127">Namnet på ANF-poolen för volym för replikeringskälla</span><span class="sxs-lookup"><span data-stu-id="2eaeb-127">The name of the ANF pool of the replication source volume</span></span>

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

### <span data-ttu-id="2eaeb-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2eaeb-128">-ResourceGroupName</span></span>
<span data-ttu-id="2eaeb-129">Resurs gruppen för ANF</span><span class="sxs-lookup"><span data-stu-id="2eaeb-129">The resource group of the ANF replication source volume</span></span>

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

### <span data-ttu-id="2eaeb-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2eaeb-130">-ResourceId</span></span>
<span data-ttu-id="2eaeb-131">Resurs-ID för ANF volym</span><span class="sxs-lookup"><span data-stu-id="2eaeb-131">The resource id of the ANF replication source volume</span></span>

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

### <span data-ttu-id="2eaeb-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2eaeb-132">-Confirm</span></span>
<span data-ttu-id="2eaeb-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2eaeb-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2eaeb-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2eaeb-134">-WhatIf</span></span>
<span data-ttu-id="2eaeb-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2eaeb-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2eaeb-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2eaeb-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2eaeb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2eaeb-137">CommonParameters</span></span>
<span data-ttu-id="2eaeb-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2eaeb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2eaeb-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2eaeb-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2eaeb-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2eaeb-140">INPUTS</span></span>

### <span data-ttu-id="2eaeb-141">System. String</span><span class="sxs-lookup"><span data-stu-id="2eaeb-141">System.String</span></span>

### <span data-ttu-id="2eaeb-142">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="2eaeb-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="2eaeb-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2eaeb-143">OUTPUTS</span></span>

### <span data-ttu-id="2eaeb-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2eaeb-144">System.Boolean</span></span>

## <span data-ttu-id="2eaeb-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2eaeb-145">NOTES</span></span>

## <span data-ttu-id="2eaeb-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2eaeb-146">RELATED LINKS</span></span>
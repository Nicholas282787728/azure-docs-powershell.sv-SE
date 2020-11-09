---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/suspend-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Suspend-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Suspend-AzNetAppFilesReplication.md
ms.openlocfilehash: eb695da1dc1fea238a57ea1c98bec42899e8f28f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94325301"
---
# <span data-ttu-id="6f9b5-101">Suspend-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="6f9b5-101">Suspend-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="6f9b5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6f9b5-102">SYNOPSIS</span></span>
<span data-ttu-id="6f9b5-103">Pausa/bryta förbindelsen på mål volymen</span><span class="sxs-lookup"><span data-stu-id="6f9b5-103">Suspend/break the replication connection on the destination volume</span></span>

## <span data-ttu-id="6f9b5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6f9b5-104">SYNTAX</span></span>

### <span data-ttu-id="6f9b5-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="6f9b5-105">ByFieldsParameterSet (Default)</span></span>
```
Suspend-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6f9b5-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f9b5-106">ByResourceIdParameterSet</span></span>
```
Suspend-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f9b5-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f9b5-107">ByObjectParameterSet</span></span>
```
Suspend-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f9b5-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6f9b5-108">DESCRIPTION</span></span>
<span data-ttu-id="6f9b5-109">Pausa/bryta förbindelsen på mål volymen</span><span class="sxs-lookup"><span data-stu-id="6f9b5-109">Suspend/break the replication connection on the destination volume</span></span>

## <span data-ttu-id="6f9b5-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6f9b5-110">EXAMPLES</span></span>

### <span data-ttu-id="6f9b5-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6f9b5-111">Example 1</span></span>
```powershell
PS C:\> Suspend-AnfReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyDestinationAnfVolume"
```

<span data-ttu-id="6f9b5-112">Det här kommandot avaktiverar ANF på volymen "MyDestinationAnfVolume".</span><span class="sxs-lookup"><span data-stu-id="6f9b5-112">This command suspends the ANF Replication connection on volume "MyDestinationAnfVolume".</span></span>

## <span data-ttu-id="6f9b5-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6f9b5-113">PARAMETERS</span></span>

### <span data-ttu-id="6f9b5-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6f9b5-114">-AccountName</span></span>
<span data-ttu-id="6f9b5-115">Namnet på ANF-kontot för replikeringstjänsten</span><span class="sxs-lookup"><span data-stu-id="6f9b5-115">The name of the ANF account of the replication volume</span></span>

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

### <span data-ttu-id="6f9b5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f9b5-116">-DefaultProfile</span></span>
<span data-ttu-id="6f9b5-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6f9b5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f9b5-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6f9b5-118">-InputObject</span></span>
<span data-ttu-id="6f9b5-119">ANF mål volym objekt med replikering för att brytas</span><span class="sxs-lookup"><span data-stu-id="6f9b5-119">The ANF destination volume object with the replication to break</span></span>

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

### <span data-ttu-id="6f9b5-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="6f9b5-120">-Name</span></span>
<span data-ttu-id="6f9b5-121">Namnet på ANF</span><span class="sxs-lookup"><span data-stu-id="6f9b5-121">The name of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="6f9b5-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6f9b5-122">-PassThru</span></span>
<span data-ttu-id="6f9b5-123">Returnera om rasten för den angivna volym replikeringen utfördes</span><span class="sxs-lookup"><span data-stu-id="6f9b5-123">Return whether the break of the specified volume replication was performed</span></span>

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

### <span data-ttu-id="6f9b5-124">-PoolName</span><span class="sxs-lookup"><span data-stu-id="6f9b5-124">-PoolName</span></span>
<span data-ttu-id="6f9b5-125">Namnet på ANF-poolen för replikeringstjänsten</span><span class="sxs-lookup"><span data-stu-id="6f9b5-125">The name of the ANF pool of the replication volume</span></span>

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

### <span data-ttu-id="6f9b5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f9b5-126">-ResourceGroupName</span></span>
<span data-ttu-id="6f9b5-127">Resurs gruppen för ANF</span><span class="sxs-lookup"><span data-stu-id="6f9b5-127">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="6f9b5-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6f9b5-128">-ResourceId</span></span>
<span data-ttu-id="6f9b5-129">Resurs-ID för ANF</span><span class="sxs-lookup"><span data-stu-id="6f9b5-129">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="6f9b5-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6f9b5-130">-Confirm</span></span>
<span data-ttu-id="6f9b5-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6f9b5-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f9b5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f9b5-132">-WhatIf</span></span>
<span data-ttu-id="6f9b5-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6f9b5-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f9b5-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6f9b5-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f9b5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f9b5-135">CommonParameters</span></span>
<span data-ttu-id="6f9b5-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f9b5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f9b5-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6f9b5-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f9b5-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6f9b5-138">INPUTS</span></span>

### <span data-ttu-id="6f9b5-139">System. String</span><span class="sxs-lookup"><span data-stu-id="6f9b5-139">System.String</span></span>

### <span data-ttu-id="6f9b5-140">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="6f9b5-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="6f9b5-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6f9b5-141">OUTPUTS</span></span>

### <span data-ttu-id="6f9b5-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6f9b5-142">System.Boolean</span></span>

## <span data-ttu-id="6f9b5-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6f9b5-143">NOTES</span></span>

## <span data-ttu-id="6f9b5-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6f9b5-144">RELATED LINKS</span></span>

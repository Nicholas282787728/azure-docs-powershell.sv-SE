---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/resume-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Resume-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Resume-AzNetAppFilesReplication.md
ms.openlocfilehash: 95ed2dc354f32229727a3d1b13dbfdfb95fe001a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94325308"
---
# <span data-ttu-id="787e0-101">Resume-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="787e0-101">Resume-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="787e0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="787e0-102">SYNOPSIS</span></span>
<span data-ttu-id="787e0-103">Återuppta/synkronisera anslutningen på mål volymen.</span><span class="sxs-lookup"><span data-stu-id="787e0-103">Resume/Resync the connection on the destination volume.</span></span> <span data-ttu-id="787e0-104">Om åtgärden körs på käll volymen omkopplas anslutningen och synkroniseras från källan till destinationen.</span><span class="sxs-lookup"><span data-stu-id="787e0-104">If the operation is ran on the source volume it will reverse-resync the connection and sync from source to destination.</span></span>

## <span data-ttu-id="787e0-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="787e0-105">SYNTAX</span></span>

### <span data-ttu-id="787e0-106">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="787e0-106">ByFieldsParameterSet (Default)</span></span>
```
Resume-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="787e0-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="787e0-107">ByResourceIdParameterSet</span></span>
```
Resume-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="787e0-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="787e0-108">ByObjectParameterSet</span></span>
```
Resume-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="787e0-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="787e0-109">DESCRIPTION</span></span>
<span data-ttu-id="787e0-110">Återuppta/synkronisera anslutningen på mål volymen</span><span class="sxs-lookup"><span data-stu-id="787e0-110">Resume/Resync the connection on the destination volume</span></span>

## <span data-ttu-id="787e0-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="787e0-111">EXAMPLES</span></span>

### <span data-ttu-id="787e0-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="787e0-112">Example 1</span></span>
```powershell
PS C:\> Resume-AnfReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyDestinationAnfVolume"
```

<span data-ttu-id="787e0-113">Det här kommandot återupptar ANF på volymen "MyDestinationAnfVolume".</span><span class="sxs-lookup"><span data-stu-id="787e0-113">This command resumes the ANF Replication connection on volume "MyDestinationAnfVolume".</span></span>

## <span data-ttu-id="787e0-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="787e0-114">PARAMETERS</span></span>

### <span data-ttu-id="787e0-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="787e0-115">-AccountName</span></span>
<span data-ttu-id="787e0-116">Namnet på ANF-kontot för replikeringstjänsten</span><span class="sxs-lookup"><span data-stu-id="787e0-116">The name of the ANF account of the replication volume</span></span>

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

### <span data-ttu-id="787e0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="787e0-117">-DefaultProfile</span></span>
<span data-ttu-id="787e0-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="787e0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="787e0-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="787e0-119">-InputObject</span></span>
<span data-ttu-id="787e0-120">ANF till omsynkronisering</span><span class="sxs-lookup"><span data-stu-id="787e0-120">The ANF replication destination volume object to resync</span></span>

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

### <span data-ttu-id="787e0-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="787e0-121">-Name</span></span>
<span data-ttu-id="787e0-122">Namnet på ANF</span><span class="sxs-lookup"><span data-stu-id="787e0-122">The name of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="787e0-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="787e0-123">-PassThru</span></span>
<span data-ttu-id="787e0-124">Återvänd till omsynkronisering av den angivna replikeringstjänsten</span><span class="sxs-lookup"><span data-stu-id="787e0-124">Return whether resync of the specified replication volume was performed</span></span>

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

### <span data-ttu-id="787e0-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="787e0-125">-PoolName</span></span>
<span data-ttu-id="787e0-126">Namnet på ANF-poolen för replikeringstjänsten</span><span class="sxs-lookup"><span data-stu-id="787e0-126">The name of the ANF pool of the replication volume</span></span>

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

### <span data-ttu-id="787e0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="787e0-127">-ResourceGroupName</span></span>
<span data-ttu-id="787e0-128">Resurs gruppen för ANF</span><span class="sxs-lookup"><span data-stu-id="787e0-128">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="787e0-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="787e0-129">-ResourceId</span></span>
<span data-ttu-id="787e0-130">Resurs-ID för ANF</span><span class="sxs-lookup"><span data-stu-id="787e0-130">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="787e0-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="787e0-131">-Confirm</span></span>
<span data-ttu-id="787e0-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="787e0-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="787e0-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="787e0-133">-WhatIf</span></span>
<span data-ttu-id="787e0-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="787e0-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="787e0-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="787e0-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="787e0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="787e0-136">CommonParameters</span></span>
<span data-ttu-id="787e0-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="787e0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="787e0-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="787e0-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="787e0-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="787e0-139">INPUTS</span></span>

### <span data-ttu-id="787e0-140">System. String</span><span class="sxs-lookup"><span data-stu-id="787e0-140">System.String</span></span>

### <span data-ttu-id="787e0-141">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="787e0-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="787e0-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="787e0-142">OUTPUTS</span></span>

### <span data-ttu-id="787e0-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="787e0-143">System.Boolean</span></span>

## <span data-ttu-id="787e0-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="787e0-144">NOTES</span></span>

## <span data-ttu-id="787e0-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="787e0-145">RELATED LINKS</span></span>

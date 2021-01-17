---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesReplication.md
ms.openlocfilehash: 04ad7f188a2280dcdf84e8b5c1f45e20edf4d07b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98410672"
---
# <span data-ttu-id="9ed9f-101">Remove-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="9ed9f-101">Remove-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="9ed9f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9ed9f-102">SYNOPSIS</span></span>
<span data-ttu-id="9ed9f-103">Ta bort/ta bort replikeringsanslutning på mål volymen och skicka en version till källdomänkontrollanten</span><span class="sxs-lookup"><span data-stu-id="9ed9f-103">Remove/Delete the replication connection on the destination volume, and send release to the source replication</span></span>

## <span data-ttu-id="9ed9f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9ed9f-104">SYNTAX</span></span>

### <span data-ttu-id="9ed9f-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="9ed9f-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9ed9f-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ed9f-106">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ed9f-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ed9f-107">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ed9f-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9ed9f-108">DESCRIPTION</span></span>
<span data-ttu-id="9ed9f-109">Ta bort/ta bort replikeringsanslutning på mål volymen och skicka en version till källdomänkontrollanten</span><span class="sxs-lookup"><span data-stu-id="9ed9f-109">Remove/Delete the replication connection on the destination volume, and send release to the source replication</span></span>

## <span data-ttu-id="9ed9f-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9ed9f-110">EXAMPLES</span></span>

### <span data-ttu-id="9ed9f-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9ed9f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AnfReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyDestinationAnfVolume"
```

<span data-ttu-id="9ed9f-112">Det här kommandot tar bort ANF på volymen "MyDestinationAnfVolume".</span><span class="sxs-lookup"><span data-stu-id="9ed9f-112">This command removes the ANF Replication connection on volume "MyDestinationAnfVolume".</span></span>

## <span data-ttu-id="9ed9f-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9ed9f-113">PARAMETERS</span></span>

### <span data-ttu-id="9ed9f-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9ed9f-114">-AccountName</span></span>
<span data-ttu-id="9ed9f-115">Namnet på ANF-kontot för replikeringstjänsten</span><span class="sxs-lookup"><span data-stu-id="9ed9f-115">The name of the ANF account of the replication volume</span></span>

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

### <span data-ttu-id="9ed9f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ed9f-116">-DefaultProfile</span></span>
<span data-ttu-id="9ed9f-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9ed9f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ed9f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9ed9f-118">-InputObject</span></span>
<span data-ttu-id="9ed9f-119">ANF-målvolym med replikering att ta bort</span><span class="sxs-lookup"><span data-stu-id="9ed9f-119">The ANF destination volume with the replication to remove</span></span>

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

### <span data-ttu-id="9ed9f-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="9ed9f-120">-Name</span></span>
<span data-ttu-id="9ed9f-121">Namnet på ANF</span><span class="sxs-lookup"><span data-stu-id="9ed9f-121">The name of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="9ed9f-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9ed9f-122">-PassThru</span></span>
<span data-ttu-id="9ed9f-123">Returnera om den angivna ANF-replikeringen togs bort</span><span class="sxs-lookup"><span data-stu-id="9ed9f-123">Return whether the specified ANF replication was successfully removed</span></span>

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

### <span data-ttu-id="9ed9f-124">-PoolName</span><span class="sxs-lookup"><span data-stu-id="9ed9f-124">-PoolName</span></span>
<span data-ttu-id="9ed9f-125">Namnet på ANF-poolen för replikeringstjänsten</span><span class="sxs-lookup"><span data-stu-id="9ed9f-125">The name of the ANF pool of the replication volume</span></span>

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

### <span data-ttu-id="9ed9f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ed9f-126">-ResourceGroupName</span></span>
<span data-ttu-id="9ed9f-127">Resurs gruppen för ANF</span><span class="sxs-lookup"><span data-stu-id="9ed9f-127">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="9ed9f-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9ed9f-128">-ResourceId</span></span>
<span data-ttu-id="9ed9f-129">Resurs-ID för ANF</span><span class="sxs-lookup"><span data-stu-id="9ed9f-129">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="9ed9f-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9ed9f-130">-Confirm</span></span>
<span data-ttu-id="9ed9f-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9ed9f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ed9f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ed9f-132">-WhatIf</span></span>
<span data-ttu-id="9ed9f-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9ed9f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ed9f-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9ed9f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ed9f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ed9f-135">CommonParameters</span></span>
<span data-ttu-id="9ed9f-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ed9f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ed9f-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9ed9f-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ed9f-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9ed9f-138">INPUTS</span></span>

### <span data-ttu-id="9ed9f-139">System. String</span><span class="sxs-lookup"><span data-stu-id="9ed9f-139">System.String</span></span>

### <span data-ttu-id="9ed9f-140">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="9ed9f-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="9ed9f-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9ed9f-141">OUTPUTS</span></span>

### <span data-ttu-id="9ed9f-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9ed9f-142">System.Boolean</span></span>

## <span data-ttu-id="9ed9f-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9ed9f-143">NOTES</span></span>

## <span data-ttu-id="9ed9f-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9ed9f-144">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/remove-azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 9afb334e7c26b49bddcabdbcd1ac4036fc3a77c6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98414531"
---
# <span data-ttu-id="5b184-101">Remove-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="5b184-101">Remove-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="5b184-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5b184-102">SYNOPSIS</span></span>
<span data-ttu-id="5b184-103">Det här kommandot tar bort den angivna Server slut punkten.</span><span class="sxs-lookup"><span data-stu-id="5b184-103">This command will delete the specified server endpoint.</span></span> <span data-ttu-id="5b184-104">Synkronisering till den här platsen stoppas omedelbart.</span><span class="sxs-lookup"><span data-stu-id="5b184-104">Sync to this location will stop immediately.</span></span>

## <span data-ttu-id="5b184-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5b184-105">SYNTAX</span></span>

### <span data-ttu-id="5b184-106">StringParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="5b184-106">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b184-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b184-107">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncServerEndpoint [-InputObject] <PSServerEndpoint> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b184-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b184-108">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncServerEndpoint [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b184-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5b184-109">DESCRIPTION</span></span>
<span data-ttu-id="5b184-110">Att ta bort en server slut punkt är en destruktiv åtgärd.</span><span class="sxs-lookup"><span data-stu-id="5b184-110">Removing a server endpoint is a destructive operation.</span></span> <span data-ttu-id="5b184-111">Den här Server platsen slutar synkroniseras.</span><span class="sxs-lookup"><span data-stu-id="5b184-111">This server location will stop syncing.</span></span> <span data-ttu-id="5b184-112">Denna åtgärd ska inte utföras för att lösa synkroniseringsproblem.</span><span class="sxs-lookup"><span data-stu-id="5b184-112">This operation should not be performed to solve sync issues.</span></span> <span data-ttu-id="5b184-113">Om den här Server platsen (inkl. filer) läggs till i samma synkroniseringsresurs som en server slut punkt kan den leda till konfliktskapande filer och andra oavsiktliga konsekvenser.</span><span class="sxs-lookup"><span data-stu-id="5b184-113">If this server location (incl. it's files) is added again to the same sync group as a server endpoint, it can lead to conflict files and other unintended consequences.</span></span> <span data-ttu-id="5b184-114">Det här kommandot är endast avsett för att avställa.</span><span class="sxs-lookup"><span data-stu-id="5b184-114">This command is intended for decommissioning only.</span></span>

## <span data-ttu-id="5b184-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5b184-115">EXAMPLES</span></span>

### <span data-ttu-id="5b184-116">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5b184-116">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncServerEndpoint -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName"
```

<span data-ttu-id="5b184-117">Det här kommandot tar bort Server slut punkten.</span><span class="sxs-lookup"><span data-stu-id="5b184-117">This command will remove the server endpoint.</span></span>

## <span data-ttu-id="5b184-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5b184-118">PARAMETERS</span></span>

### <span data-ttu-id="5b184-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5b184-119">-AsJob</span></span>
<span data-ttu-id="5b184-120">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="5b184-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5b184-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b184-121">-DefaultProfile</span></span>
<span data-ttu-id="5b184-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5b184-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b184-123">-Force</span><span class="sxs-lookup"><span data-stu-id="5b184-123">-Force</span></span>
<span data-ttu-id="5b184-124">Försörjning-Force för att hoppa över bekräftelsen av det här kommandot.</span><span class="sxs-lookup"><span data-stu-id="5b184-124">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="5b184-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5b184-125">-InputObject</span></span>
<span data-ttu-id="5b184-126">ServerEndpoint, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="5b184-126">ServerEndpoint Input Object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b184-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="5b184-127">-Name</span></span>
<span data-ttu-id="5b184-128">Namn på ServerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="5b184-128">Name of the ServerEndpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b184-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5b184-129">-PassThru</span></span>
<span data-ttu-id="5b184-130">I normal körning returnerar denna cmdlet inget värde vid framgång.</span><span class="sxs-lookup"><span data-stu-id="5b184-130">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="5b184-131">Om du anger parametern PassThru, skriver cmdleten ett värde till pipeline efter att körningen lyckats.</span><span class="sxs-lookup"><span data-stu-id="5b184-131">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="5b184-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b184-132">-ResourceGroupName</span></span>
<span data-ttu-id="5b184-133">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="5b184-133">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b184-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5b184-134">-ResourceId</span></span>
<span data-ttu-id="5b184-135">Resurs-ID för ServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="5b184-135">ServerEndpoint Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b184-136">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="5b184-136">-StorageSyncServiceName</span></span>
<span data-ttu-id="5b184-137">Namn på StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="5b184-137">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b184-138">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="5b184-138">-SyncGroupName</span></span>
<span data-ttu-id="5b184-139">Namn på SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="5b184-139">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b184-140">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5b184-140">-Confirm</span></span>
<span data-ttu-id="5b184-141">Här visas en uppmaning om att bekräfta innan cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5b184-141">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b184-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b184-142">-WhatIf</span></span>
<span data-ttu-id="5b184-143">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5b184-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5b184-144">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5b184-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b184-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b184-145">CommonParameters</span></span>
<span data-ttu-id="5b184-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b184-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b184-147">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b184-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b184-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5b184-148">INPUTS</span></span>

### <span data-ttu-id="5b184-149">Microsoft. Azure. commands. StorageSync. Models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="5b184-149">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

### <span data-ttu-id="5b184-150">System. String</span><span class="sxs-lookup"><span data-stu-id="5b184-150">System.String</span></span>

## <span data-ttu-id="5b184-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5b184-151">OUTPUTS</span></span>

### <span data-ttu-id="5b184-152">System. Object</span><span class="sxs-lookup"><span data-stu-id="5b184-152">System.Object</span></span>
## <span data-ttu-id="5b184-153">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5b184-153">NOTES</span></span>

## <span data-ttu-id="5b184-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5b184-154">RELATED LINKS</span></span>

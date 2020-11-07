---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/remove-azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 328fd4c798380202b355974cc8d9150e1d138da5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746209"
---
# <span data-ttu-id="33fc9-101">Remove-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="33fc9-101">Remove-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="33fc9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="33fc9-102">SYNOPSIS</span></span>
<span data-ttu-id="33fc9-103">Det här kommandot tar bort den angivna Server slut punkten.</span><span class="sxs-lookup"><span data-stu-id="33fc9-103">This command will delete the specified server endpoint.</span></span> <span data-ttu-id="33fc9-104">Synkronisering till den här platsen stoppas omedelbart.</span><span class="sxs-lookup"><span data-stu-id="33fc9-104">Sync to this location will stop immediately.</span></span>

## <span data-ttu-id="33fc9-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="33fc9-105">SYNTAX</span></span>

### <span data-ttu-id="33fc9-106">StringParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="33fc9-106">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33fc9-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="33fc9-107">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncServerEndpoint [-InputObject] <PSServerEndpoint> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33fc9-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="33fc9-108">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncServerEndpoint [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33fc9-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="33fc9-109">DESCRIPTION</span></span>
<span data-ttu-id="33fc9-110">Att ta bort en server slut punkt är en destruktiv åtgärd.</span><span class="sxs-lookup"><span data-stu-id="33fc9-110">Removing a server endpoint is a destructive operation.</span></span> <span data-ttu-id="33fc9-111">Den här Server platsen slutar synkroniseras.</span><span class="sxs-lookup"><span data-stu-id="33fc9-111">This server location will stop syncing.</span></span> <span data-ttu-id="33fc9-112">Denna åtgärd ska inte utföras för att lösa synkroniseringsproblem.</span><span class="sxs-lookup"><span data-stu-id="33fc9-112">This operation should not be performed to solve sync issues.</span></span> <span data-ttu-id="33fc9-113">Om den här Server platsen (inkl. filer) läggs till i samma synkroniseringsresurs som en server slut punkt kan den leda till konfliktskapande filer och andra oavsiktliga konsekvenser.</span><span class="sxs-lookup"><span data-stu-id="33fc9-113">If this server location (incl. it's files) is added again to the same sync group as a server endpoint, it can lead to conflict files and other unintended consequences.</span></span> <span data-ttu-id="33fc9-114">Det här kommandot är endast avsett för att avställa.</span><span class="sxs-lookup"><span data-stu-id="33fc9-114">This command is intended for decommissioning only.</span></span>

## <span data-ttu-id="33fc9-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="33fc9-115">EXAMPLES</span></span>

### <span data-ttu-id="33fc9-116">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="33fc9-116">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncServerEndpoint -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName"
```

<span data-ttu-id="33fc9-117">Det här kommandot tar bort Server slut punkten.</span><span class="sxs-lookup"><span data-stu-id="33fc9-117">This command will remove the server endpoint.</span></span>

## <span data-ttu-id="33fc9-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="33fc9-118">PARAMETERS</span></span>

### <span data-ttu-id="33fc9-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="33fc9-119">-AsJob</span></span>
<span data-ttu-id="33fc9-120">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="33fc9-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="33fc9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33fc9-121">-DefaultProfile</span></span>
<span data-ttu-id="33fc9-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="33fc9-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33fc9-123">-Force</span><span class="sxs-lookup"><span data-stu-id="33fc9-123">-Force</span></span>
<span data-ttu-id="33fc9-124">Försörjning-Force för att hoppa över bekräftelsen av det här kommandot.</span><span class="sxs-lookup"><span data-stu-id="33fc9-124">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="33fc9-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="33fc9-125">-InputObject</span></span>
<span data-ttu-id="33fc9-126">ServerEndpoint, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="33fc9-126">ServerEndpoint Input Object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="33fc9-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="33fc9-127">-Name</span></span>
<span data-ttu-id="33fc9-128">Namn på ServerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="33fc9-128">Name of the ServerEndpoint.</span></span>

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

### <span data-ttu-id="33fc9-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="33fc9-129">-PassThru</span></span>
<span data-ttu-id="33fc9-130">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="33fc9-130">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="33fc9-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33fc9-131">-ResourceGroupName</span></span>
<span data-ttu-id="33fc9-132">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="33fc9-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="33fc9-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="33fc9-133">-ResourceId</span></span>
<span data-ttu-id="33fc9-134">Resurs-ID för ServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="33fc9-134">ServerEndpoint Resource Id</span></span>

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

### <span data-ttu-id="33fc9-135">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="33fc9-135">-StorageSyncServiceName</span></span>
<span data-ttu-id="33fc9-136">Namn på StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="33fc9-136">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="33fc9-137">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="33fc9-137">-SyncGroupName</span></span>
<span data-ttu-id="33fc9-138">Namn på SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="33fc9-138">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="33fc9-139">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="33fc9-139">-Confirm</span></span>
<span data-ttu-id="33fc9-140">Här visas en uppmaning om att bekräfta innan cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="33fc9-140">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33fc9-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33fc9-141">-WhatIf</span></span>
<span data-ttu-id="33fc9-142">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="33fc9-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="33fc9-143">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="33fc9-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33fc9-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33fc9-144">CommonParameters</span></span>
<span data-ttu-id="33fc9-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33fc9-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33fc9-146">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33fc9-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33fc9-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="33fc9-147">INPUTS</span></span>

### <span data-ttu-id="33fc9-148">Microsoft. Azure. commands. StorageSync. Models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="33fc9-148">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

### <span data-ttu-id="33fc9-149">System. String</span><span class="sxs-lookup"><span data-stu-id="33fc9-149">System.String</span></span>

## <span data-ttu-id="33fc9-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="33fc9-150">OUTPUTS</span></span>

### <span data-ttu-id="33fc9-151">System. Object</span><span class="sxs-lookup"><span data-stu-id="33fc9-151">System.Object</span></span>
## <span data-ttu-id="33fc9-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="33fc9-152">NOTES</span></span>

## <span data-ttu-id="33fc9-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="33fc9-153">RELATED LINKS</span></span>

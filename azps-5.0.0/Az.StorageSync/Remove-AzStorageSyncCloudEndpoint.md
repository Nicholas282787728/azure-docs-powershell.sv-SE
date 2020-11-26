---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/remove-Azstoragesynccloudendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncCloudEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncCloudEndpoint.md
ms.openlocfilehash: ae3d75b90e6e095072b8e6e6543e2f122fe4cb50
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269560"
---
# <span data-ttu-id="424c8-101">Remove-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="424c8-101">Remove-AzStorageSyncCloudEndpoint</span></span>

## <span data-ttu-id="424c8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="424c8-102">SYNOPSIS</span></span>
<span data-ttu-id="424c8-103">Det här kommandot tar bort den angivna moln slut punkten från en synkroniseringsresurs.</span><span class="sxs-lookup"><span data-stu-id="424c8-103">This command will delete the specified cloud endpoint from a sync group.</span></span> <span data-ttu-id="424c8-104">Utan åtminstone en moln slut punkt kan ingen annan server slut punkter i den här synkroniseringsresursen synkronisera.</span><span class="sxs-lookup"><span data-stu-id="424c8-104">Without at least one cloud endpoint, no other server endpoints in this sync group can sync.</span></span>

## <span data-ttu-id="424c8-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="424c8-105">SYNTAX</span></span>

### <span data-ttu-id="424c8-106">StringParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="424c8-106">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncCloudEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="424c8-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="424c8-107">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncCloudEndpoint [-InputObject] <PSCloudEndpoint> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="424c8-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="424c8-108">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncCloudEndpoint [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="424c8-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="424c8-109">DESCRIPTION</span></span>
<span data-ttu-id="424c8-110">Det här kommandot tar bort den angivna moln slut punkten från en synkroniseringsresurs.</span><span class="sxs-lookup"><span data-stu-id="424c8-110">This command will delete the specified cloud endpoint from a sync group.</span></span> <span data-ttu-id="424c8-111">Azure-filen dela moln slut punkts referenserna kvarstår inte under den här processen.</span><span class="sxs-lookup"><span data-stu-id="424c8-111">The Azure file share the cloud endpoint references remains untouched by this process.</span></span> <span data-ttu-id="424c8-112">Det här kommandot är endast avsett för avställning.</span><span class="sxs-lookup"><span data-stu-id="424c8-112">This command is only intended for decommissioning.</span></span> <span data-ttu-id="424c8-113">Borttagning av moln slut punkter är en destruktiv operation.</span><span class="sxs-lookup"><span data-stu-id="424c8-113">Removing a cloud endpoint is a destructive operation.</span></span> <span data-ttu-id="424c8-114">Server slut punkter kan inte synkroniseras utan minst en moln slut punkt.</span><span class="sxs-lookup"><span data-stu-id="424c8-114">Server endpoints cannot sync without at least one cloud endpoint present.</span></span> <span data-ttu-id="424c8-115">Denna åtgärd ska inte utföras för att lösa synkroniseringsproblem.</span><span class="sxs-lookup"><span data-stu-id="424c8-115">This operation should not be performed to solve sync issues.</span></span> <span data-ttu-id="424c8-116">Om den här Azure-fildelningen läggs till igen i samma synkroniseringsresurs som en moln slut punkt kan den leda till konfliktskapande filer och andra oavsiktliga konsekvenser.</span><span class="sxs-lookup"><span data-stu-id="424c8-116">If this Azure file share is added again to the same sync group, as a cloud endpoint, it can lead to conflict files and other unintended consequences.</span></span>

## <span data-ttu-id="424c8-117">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="424c8-117">EXAMPLES</span></span>

### <span data-ttu-id="424c8-118">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="424c8-118">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncCloudEndpoint -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myCloudEndpointName"
```

<span data-ttu-id="424c8-119">Det här kommandot tar bort moln slut punkten.</span><span class="sxs-lookup"><span data-stu-id="424c8-119">This command will remove the cloud endpoint.</span></span>

## <span data-ttu-id="424c8-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="424c8-120">PARAMETERS</span></span>

### <span data-ttu-id="424c8-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="424c8-121">-AsJob</span></span>
<span data-ttu-id="424c8-122">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="424c8-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="424c8-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="424c8-123">-DefaultProfile</span></span>
<span data-ttu-id="424c8-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="424c8-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="424c8-125">-Force</span><span class="sxs-lookup"><span data-stu-id="424c8-125">-Force</span></span>
<span data-ttu-id="424c8-126">Försörjning-Force för att hoppa över bekräftelsen av det här kommandot.</span><span class="sxs-lookup"><span data-stu-id="424c8-126">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="424c8-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="424c8-127">-InputObject</span></span>
<span data-ttu-id="424c8-128">CloudEndpoint, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="424c8-128">CloudEndpoint Input Object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="424c8-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="424c8-129">-Name</span></span>
<span data-ttu-id="424c8-130">Namn på CloudEndpoint.</span><span class="sxs-lookup"><span data-stu-id="424c8-130">Name of the CloudEndpoint.</span></span>

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

### <span data-ttu-id="424c8-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="424c8-131">-PassThru</span></span>
<span data-ttu-id="424c8-132">I normal körning returnerar denna cmdlet inget värde vid framgång.</span><span class="sxs-lookup"><span data-stu-id="424c8-132">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="424c8-133">Om du anger parametern PassThru, skriver cmdleten ett värde till pipeline efter att körningen lyckats.</span><span class="sxs-lookup"><span data-stu-id="424c8-133">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="424c8-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="424c8-134">-ResourceGroupName</span></span>
<span data-ttu-id="424c8-135">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="424c8-135">Resource Group Name.</span></span>

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

### <span data-ttu-id="424c8-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="424c8-136">-ResourceId</span></span>
<span data-ttu-id="424c8-137">Resurs-ID för CloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="424c8-137">CloudEndpoint Resource Id</span></span>

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

### <span data-ttu-id="424c8-138">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="424c8-138">-StorageSyncServiceName</span></span>
<span data-ttu-id="424c8-139">Namn på StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="424c8-139">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="424c8-140">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="424c8-140">-SyncGroupName</span></span>
<span data-ttu-id="424c8-141">Namn på SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="424c8-141">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="424c8-142">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="424c8-142">-Confirm</span></span>
<span data-ttu-id="424c8-143">Här visas en uppmaning om att bekräfta innan cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="424c8-143">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="424c8-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="424c8-144">-WhatIf</span></span>
<span data-ttu-id="424c8-145">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="424c8-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="424c8-146">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="424c8-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="424c8-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="424c8-147">CommonParameters</span></span>
<span data-ttu-id="424c8-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="424c8-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="424c8-149">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="424c8-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="424c8-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="424c8-150">INPUTS</span></span>

### <span data-ttu-id="424c8-151">Microsoft. Azure. commands. StorageSync. Models. PSCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="424c8-151">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span></span>

### <span data-ttu-id="424c8-152">System. String</span><span class="sxs-lookup"><span data-stu-id="424c8-152">System.String</span></span>

## <span data-ttu-id="424c8-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="424c8-153">OUTPUTS</span></span>

### <span data-ttu-id="424c8-154">System. Object</span><span class="sxs-lookup"><span data-stu-id="424c8-154">System.Object</span></span>
## <span data-ttu-id="424c8-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="424c8-155">NOTES</span></span>

## <span data-ttu-id="424c8-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="424c8-156">RELATED LINKS</span></span>
---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/remove-azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncGroup.md
ms.openlocfilehash: dad4af4f954fae03a68728de928614a81eed5e5a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269232"
---
# <span data-ttu-id="4e59c-101">Remove-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="4e59c-101">Remove-AzStorageSyncGroup</span></span>

## <span data-ttu-id="4e59c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4e59c-102">SYNOPSIS</span></span>
<span data-ttu-id="4e59c-103">Det här kommandot tar bort den angivna synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="4e59c-103">This command will delete the specified sync group.</span></span>

## <span data-ttu-id="4e59c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4e59c-104">SYNTAX</span></span>

### <span data-ttu-id="4e59c-105">StringParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="4e59c-105">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-Name] <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4e59c-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4e59c-106">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncGroup [-InputObject] <PSSyncGroup> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e59c-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4e59c-107">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncGroup [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e59c-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4e59c-108">DESCRIPTION</span></span>
<span data-ttu-id="4e59c-109">Det här kommandot tar bort den angivna synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="4e59c-109">This command will delete the specified sync group.</span></span> <span data-ttu-id="4e59c-110">En synkroniseringsresurs kan bara tas bort när alla slut punkter tas bort först.</span><span class="sxs-lookup"><span data-stu-id="4e59c-110">A sync group can only be removed when all of the contained endpoints are deleted first.</span></span>

## <span data-ttu-id="4e59c-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4e59c-111">EXAMPLES</span></span>

### <span data-ttu-id="4e59c-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4e59c-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncGroup -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -Name "mySyncGroupName"
```

<span data-ttu-id="4e59c-113">Det här kommandot tar bort synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="4e59c-113">This command will remove the sync group.</span></span>

## <span data-ttu-id="4e59c-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4e59c-114">PARAMETERS</span></span>

### <span data-ttu-id="4e59c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4e59c-115">-AsJob</span></span>
<span data-ttu-id="4e59c-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="4e59c-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4e59c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e59c-117">-DefaultProfile</span></span>
<span data-ttu-id="4e59c-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4e59c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e59c-119">-Force</span><span class="sxs-lookup"><span data-stu-id="4e59c-119">-Force</span></span>
<span data-ttu-id="4e59c-120">Försörjning-Force för att hoppa över bekräftelsen av det här kommandot.</span><span class="sxs-lookup"><span data-stu-id="4e59c-120">Supply -Force to skip confirmation of this command.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e59c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4e59c-121">-InputObject</span></span>
<span data-ttu-id="4e59c-122">SyncGroup</span><span class="sxs-lookup"><span data-stu-id="4e59c-122">SyncGroup Input Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4e59c-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="4e59c-123">-Name</span></span>
<span data-ttu-id="4e59c-124">Namn på SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="4e59c-124">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: SyncGroupName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e59c-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4e59c-125">-PassThru</span></span>
<span data-ttu-id="4e59c-126">I normal körning returnerar denna cmdlet inget värde vid framgång.</span><span class="sxs-lookup"><span data-stu-id="4e59c-126">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="4e59c-127">Om du anger parametern PassThru, skriver cmdleten ett värde till pipeline efter att körningen lyckats.</span><span class="sxs-lookup"><span data-stu-id="4e59c-127">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="4e59c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e59c-128">-ResourceGroupName</span></span>
<span data-ttu-id="4e59c-129">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="4e59c-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="4e59c-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4e59c-130">-ResourceId</span></span>
<span data-ttu-id="4e59c-131">Resurs-ID för SyncGroup</span><span class="sxs-lookup"><span data-stu-id="4e59c-131">SyncGroup Resource Id</span></span>

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

### <span data-ttu-id="4e59c-132">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="4e59c-132">-StorageSyncServiceName</span></span>
<span data-ttu-id="4e59c-133">Namn på StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="4e59c-133">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e59c-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4e59c-134">-Confirm</span></span>
<span data-ttu-id="4e59c-135">Här visas en uppmaning om att bekräfta innan cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4e59c-135">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e59c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e59c-136">-WhatIf</span></span>
<span data-ttu-id="4e59c-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4e59c-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4e59c-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4e59c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e59c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e59c-139">CommonParameters</span></span>
<span data-ttu-id="4e59c-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e59c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e59c-141">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e59c-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e59c-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4e59c-142">INPUTS</span></span>

### <span data-ttu-id="4e59c-143">Microsoft. Azure. commands. StorageSync. Models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="4e59c-143">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="4e59c-144">System. String</span><span class="sxs-lookup"><span data-stu-id="4e59c-144">System.String</span></span>

### <span data-ttu-id="4e59c-145">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4e59c-145">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4e59c-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4e59c-146">OUTPUTS</span></span>

### <span data-ttu-id="4e59c-147">System. Object</span><span class="sxs-lookup"><span data-stu-id="4e59c-147">System.Object</span></span>
## <span data-ttu-id="4e59c-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4e59c-148">NOTES</span></span>

## <span data-ttu-id="4e59c-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4e59c-149">RELATED LINKS</span></span>
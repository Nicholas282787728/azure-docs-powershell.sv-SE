---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/remove-azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncGroup.md
ms.openlocfilehash: f7c1f129d9a5f6f6bdd117597a2943567fb4001d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746207"
---
# <span data-ttu-id="fead5-101">Remove-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="fead5-101">Remove-AzStorageSyncGroup</span></span>

## <span data-ttu-id="fead5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fead5-102">SYNOPSIS</span></span>
<span data-ttu-id="fead5-103">Det här kommandot tar bort den angivna synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="fead5-103">This command will delete the specified sync group.</span></span>

## <span data-ttu-id="fead5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fead5-104">SYNTAX</span></span>

### <span data-ttu-id="fead5-105">StringParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="fead5-105">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-Name] <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fead5-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fead5-106">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncGroup [-InputObject] <PSSyncGroup> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fead5-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fead5-107">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncGroup [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fead5-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fead5-108">DESCRIPTION</span></span>
<span data-ttu-id="fead5-109">Det här kommandot tar bort den angivna synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="fead5-109">This command will delete the specified sync group.</span></span> <span data-ttu-id="fead5-110">En synkroniseringsresurs kan bara tas bort när alla slut punkter tas bort först.</span><span class="sxs-lookup"><span data-stu-id="fead5-110">A sync group can only be removed when all of the contained endpoints are deleted first.</span></span>

## <span data-ttu-id="fead5-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fead5-111">EXAMPLES</span></span>

### <span data-ttu-id="fead5-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="fead5-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncGroup -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -Name "mySyncGroupName"
```

<span data-ttu-id="fead5-113">Det här kommandot tar bort synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="fead5-113">This command will remove the sync group.</span></span>

## <span data-ttu-id="fead5-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fead5-114">PARAMETERS</span></span>

### <span data-ttu-id="fead5-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fead5-115">-AsJob</span></span>
<span data-ttu-id="fead5-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="fead5-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fead5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fead5-117">-DefaultProfile</span></span>
<span data-ttu-id="fead5-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fead5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fead5-119">-Force</span><span class="sxs-lookup"><span data-stu-id="fead5-119">-Force</span></span>
<span data-ttu-id="fead5-120">Försörjning-Force för att hoppa över bekräftelsen av det här kommandot.</span><span class="sxs-lookup"><span data-stu-id="fead5-120">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="fead5-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fead5-121">-InputObject</span></span>
<span data-ttu-id="fead5-122">SyncGroup</span><span class="sxs-lookup"><span data-stu-id="fead5-122">SyncGroup Input Object</span></span>

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

### <span data-ttu-id="fead5-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="fead5-123">-Name</span></span>
<span data-ttu-id="fead5-124">Namn på SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="fead5-124">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="fead5-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fead5-125">-PassThru</span></span>
<span data-ttu-id="fead5-126">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="fead5-126">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="fead5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fead5-127">-ResourceGroupName</span></span>
<span data-ttu-id="fead5-128">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="fead5-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="fead5-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fead5-129">-ResourceId</span></span>
<span data-ttu-id="fead5-130">Resurs-ID för SyncGroup</span><span class="sxs-lookup"><span data-stu-id="fead5-130">SyncGroup Resource Id</span></span>

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

### <span data-ttu-id="fead5-131">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="fead5-131">-StorageSyncServiceName</span></span>
<span data-ttu-id="fead5-132">Namn på StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="fead5-132">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="fead5-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fead5-133">-Confirm</span></span>
<span data-ttu-id="fead5-134">Här visas en uppmaning om att bekräfta innan cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fead5-134">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fead5-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fead5-135">-WhatIf</span></span>
<span data-ttu-id="fead5-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fead5-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fead5-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fead5-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fead5-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fead5-138">CommonParameters</span></span>
<span data-ttu-id="fead5-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fead5-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fead5-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fead5-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fead5-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fead5-141">INPUTS</span></span>

### <span data-ttu-id="fead5-142">Microsoft. Azure. commands. StorageSync. Models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="fead5-142">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="fead5-143">System. String</span><span class="sxs-lookup"><span data-stu-id="fead5-143">System.String</span></span>

### <span data-ttu-id="fead5-144">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="fead5-144">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="fead5-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fead5-145">OUTPUTS</span></span>

### <span data-ttu-id="fead5-146">System. Object</span><span class="sxs-lookup"><span data-stu-id="fead5-146">System.Object</span></span>
## <span data-ttu-id="fead5-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fead5-147">NOTES</span></span>

## <span data-ttu-id="fead5-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fead5-148">RELATED LINKS</span></span>

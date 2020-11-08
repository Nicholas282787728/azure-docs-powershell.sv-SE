---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/remove-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncService.md
ms.openlocfilehash: f64c085f742eeabea235660d4af7ba6bd5970fdf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269231"
---
# <span data-ttu-id="4f509-101">Remove-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="4f509-101">Remove-AzStorageSyncService</span></span>

## <span data-ttu-id="4f509-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4f509-102">SYNOPSIS</span></span>
<span data-ttu-id="4f509-103">Det här kommandot tar bort den angivna tjänsten för lagrings synkronisering.</span><span class="sxs-lookup"><span data-stu-id="4f509-103">This command will delete the specified storage sync service.</span></span>

## <span data-ttu-id="4f509-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4f509-104">SYNTAX</span></span>

### <span data-ttu-id="4f509-105">StringParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="4f509-105">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f509-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f509-106">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncService [-InputObject] <PSStorageSyncService> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f509-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f509-107">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncService [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f509-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4f509-108">DESCRIPTION</span></span>
<span data-ttu-id="4f509-109">Det här kommandot tar bort den angivna tjänsten för lagrings synkronisering.</span><span class="sxs-lookup"><span data-stu-id="4f509-109">This command will delete the specified storage sync service.</span></span> <span data-ttu-id="4f509-110">En lagrings tjänst kan bara tas bort när alla synkroniserade grupper och registrerade servrar tas bort först.</span><span class="sxs-lookup"><span data-stu-id="4f509-110">A storage sync service can only be removed when all of the contained sync groups and registered servers are deleted first.</span></span>

## <span data-ttu-id="4f509-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4f509-111">EXAMPLES</span></span>

### <span data-ttu-id="4f509-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4f509-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncService -Force -ResourceGroupName "myResourceGroup" -Name "myStorageSyncServiceName"
```

<span data-ttu-id="4f509-113">Det här kommandot tar bort tjänsten Storage Sync.</span><span class="sxs-lookup"><span data-stu-id="4f509-113">This command will remove the storage sync service.</span></span>

## <span data-ttu-id="4f509-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4f509-114">PARAMETERS</span></span>

### <span data-ttu-id="4f509-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4f509-115">-AsJob</span></span>
<span data-ttu-id="4f509-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="4f509-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4f509-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f509-117">-DefaultProfile</span></span>
<span data-ttu-id="4f509-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4f509-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f509-119">-Force</span><span class="sxs-lookup"><span data-stu-id="4f509-119">-Force</span></span>
<span data-ttu-id="4f509-120">Försörjning-Force för att hoppa över bekräftelsen av det här kommandot.</span><span class="sxs-lookup"><span data-stu-id="4f509-120">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="4f509-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4f509-121">-InputObject</span></span>
<span data-ttu-id="4f509-122">StorageSyncService, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="4f509-122">StorageSyncService Input Object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4f509-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="4f509-123">-Name</span></span>
<span data-ttu-id="4f509-124">Namn på StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="4f509-124">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: StorageSyncServiceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f509-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4f509-125">-PassThru</span></span>
<span data-ttu-id="4f509-126">I normal körning returnerar denna cmdlet inget värde vid framgång.</span><span class="sxs-lookup"><span data-stu-id="4f509-126">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="4f509-127">Om du anger parametern PassThru, skriver cmdleten ett värde till pipeline efter att körningen lyckats.</span><span class="sxs-lookup"><span data-stu-id="4f509-127">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="4f509-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f509-128">-ResourceGroupName</span></span>
<span data-ttu-id="4f509-129">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="4f509-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="4f509-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4f509-130">-ResourceId</span></span>
<span data-ttu-id="4f509-131">Resurs-ID för StorageSyncService</span><span class="sxs-lookup"><span data-stu-id="4f509-131">StorageSyncService Resource Id</span></span>

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

### <span data-ttu-id="4f509-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4f509-132">-Confirm</span></span>
<span data-ttu-id="4f509-133">Här visas en uppmaning om att bekräfta innan cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4f509-133">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f509-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f509-134">-WhatIf</span></span>
<span data-ttu-id="4f509-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4f509-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4f509-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4f509-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f509-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f509-137">CommonParameters</span></span>
<span data-ttu-id="4f509-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f509-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f509-139">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f509-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f509-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4f509-140">INPUTS</span></span>

### <span data-ttu-id="4f509-141">Microsoft. Azure. commands. StorageSync. Models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="4f509-141">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

### <span data-ttu-id="4f509-142">System. String</span><span class="sxs-lookup"><span data-stu-id="4f509-142">System.String</span></span>

### <span data-ttu-id="4f509-143">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4f509-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4f509-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4f509-144">OUTPUTS</span></span>

### <span data-ttu-id="4f509-145">System. Object</span><span class="sxs-lookup"><span data-stu-id="4f509-145">System.Object</span></span>
## <span data-ttu-id="4f509-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4f509-146">NOTES</span></span>

## <span data-ttu-id="4f509-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4f509-147">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/remove-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncService.md
ms.openlocfilehash: 5116ead7111902b1009517ff42ff6594ac87d8c5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746201"
---
# <span data-ttu-id="6ce9d-101">Remove-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="6ce9d-101">Remove-AzStorageSyncService</span></span>

## <span data-ttu-id="6ce9d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6ce9d-102">SYNOPSIS</span></span>
<span data-ttu-id="6ce9d-103">Det här kommandot tar bort den angivna tjänsten för lagrings synkronisering.</span><span class="sxs-lookup"><span data-stu-id="6ce9d-103">This command will delete the specified storage sync service.</span></span>

## <span data-ttu-id="6ce9d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6ce9d-104">SYNTAX</span></span>

### <span data-ttu-id="6ce9d-105">InputObjectParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="6ce9d-105">InputObjectParameterSet (Default)</span></span>
```
Remove-AzStorageSyncService [-InputObject] <PSStorageSyncService> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ce9d-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ce9d-106">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncService [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ce9d-107">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ce9d-107">StringParameterSet</span></span>
```
Remove-AzStorageSyncService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ce9d-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6ce9d-108">DESCRIPTION</span></span>
<span data-ttu-id="6ce9d-109">Det här kommandot tar bort den angivna tjänsten för lagrings synkronisering.</span><span class="sxs-lookup"><span data-stu-id="6ce9d-109">This command will delete the specified storage sync service.</span></span> <span data-ttu-id="6ce9d-110">En lagrings tjänst kan bara tas bort när alla synkroniserade grupper och registrerade servrar tas bort först.</span><span class="sxs-lookup"><span data-stu-id="6ce9d-110">A storage sync service can only be removed when all of the contained sync groups and registered servers are deleted first.</span></span>

## <span data-ttu-id="6ce9d-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6ce9d-111">EXAMPLES</span></span>

### <span data-ttu-id="6ce9d-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6ce9d-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncService -Force -ResourceGroupName "myResourceGroup" -Name "myStorageSyncServiceName"
```

<span data-ttu-id="6ce9d-113">Det här kommandot tar bort tjänsten Storage Sync.</span><span class="sxs-lookup"><span data-stu-id="6ce9d-113">This command will remove the storage sync service.</span></span>

## <span data-ttu-id="6ce9d-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6ce9d-114">PARAMETERS</span></span>

### <span data-ttu-id="6ce9d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6ce9d-115">-AsJob</span></span>
<span data-ttu-id="6ce9d-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="6ce9d-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6ce9d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ce9d-117">-DefaultProfile</span></span>
<span data-ttu-id="6ce9d-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6ce9d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ce9d-119">-Force</span><span class="sxs-lookup"><span data-stu-id="6ce9d-119">-Force</span></span>
<span data-ttu-id="6ce9d-120">Försörjning-Force för att hoppa över bekräftelsen av det här kommandot.</span><span class="sxs-lookup"><span data-stu-id="6ce9d-120">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="6ce9d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6ce9d-121">-InputObject</span></span>
<span data-ttu-id="6ce9d-122">StorageSyncService, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="6ce9d-122">StorageSyncService Input Object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="6ce9d-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="6ce9d-123">-Name</span></span>
<span data-ttu-id="6ce9d-124">Namn på StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="6ce9d-124">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="6ce9d-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6ce9d-125">-PassThru</span></span>
<span data-ttu-id="6ce9d-126">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="6ce9d-126">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="6ce9d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ce9d-127">-ResourceGroupName</span></span>
<span data-ttu-id="6ce9d-128">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="6ce9d-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="6ce9d-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6ce9d-129">-ResourceId</span></span>
<span data-ttu-id="6ce9d-130">Resurs-ID för StorageSyncService</span><span class="sxs-lookup"><span data-stu-id="6ce9d-130">StorageSyncService Resource Id</span></span>

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

### <span data-ttu-id="6ce9d-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6ce9d-131">-Confirm</span></span>
<span data-ttu-id="6ce9d-132">Här visas en uppmaning om att bekräfta innan cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6ce9d-132">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ce9d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ce9d-133">-WhatIf</span></span>
<span data-ttu-id="6ce9d-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6ce9d-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6ce9d-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6ce9d-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ce9d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ce9d-136">CommonParameters</span></span>
<span data-ttu-id="6ce9d-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ce9d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ce9d-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ce9d-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ce9d-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6ce9d-139">INPUTS</span></span>

### <span data-ttu-id="6ce9d-140">Microsoft. Azure. commands. StorageSync. Models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="6ce9d-140">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

### <span data-ttu-id="6ce9d-141">System. String</span><span class="sxs-lookup"><span data-stu-id="6ce9d-141">System.String</span></span>

### <span data-ttu-id="6ce9d-142">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6ce9d-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6ce9d-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6ce9d-143">OUTPUTS</span></span>

### <span data-ttu-id="6ce9d-144">System. Object</span><span class="sxs-lookup"><span data-stu-id="6ce9d-144">System.Object</span></span>
## <span data-ttu-id="6ce9d-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6ce9d-145">NOTES</span></span>

## <span data-ttu-id="6ce9d-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6ce9d-146">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGallery.md
ms.openlocfilehash: ac098616d2ee92b4d6910034735824289b971f5e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745055"
---
# <span data-ttu-id="e99ce-101">Remove-AzGallery</span><span class="sxs-lookup"><span data-stu-id="e99ce-101">Remove-AzGallery</span></span>

## <span data-ttu-id="e99ce-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e99ce-102">SYNOPSIS</span></span>
<span data-ttu-id="e99ce-103">Ta bort ett galleri.</span><span class="sxs-lookup"><span data-stu-id="e99ce-103">Delete a gallery.</span></span>

## <span data-ttu-id="e99ce-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e99ce-104">SYNTAX</span></span>

### <span data-ttu-id="e99ce-105">DefaultParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="e99ce-105">DefaultParameter (Default)</span></span>
```
Remove-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e99ce-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="e99ce-106">ResourceIdParameter</span></span>
```
Remove-AzGallery [-Force] [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e99ce-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="e99ce-107">ObjectParameter</span></span>
```
Remove-AzGallery [-Force] [-InputObject] <PSGallery> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e99ce-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e99ce-108">DESCRIPTION</span></span>
<span data-ttu-id="e99ce-109">Ta bort ett galleri.</span><span class="sxs-lookup"><span data-stu-id="e99ce-109">Delete a gallery.</span></span>

## <span data-ttu-id="e99ce-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e99ce-110">EXAMPLES</span></span>

### <span data-ttu-id="e99ce-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e99ce-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGallery -ResourceGroupName $rgname -GalleryName $galleryName
```

<span data-ttu-id="e99ce-112">Ta bort det angivna galleriet.</span><span class="sxs-lookup"><span data-stu-id="e99ce-112">Delete the given gallery.</span></span>

## <span data-ttu-id="e99ce-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e99ce-113">PARAMETERS</span></span>

### <span data-ttu-id="e99ce-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e99ce-114">-AsJob</span></span>
<span data-ttu-id="e99ce-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="e99ce-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e99ce-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e99ce-116">-DefaultProfile</span></span>
<span data-ttu-id="e99ce-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e99ce-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e99ce-118">-Force</span><span class="sxs-lookup"><span data-stu-id="e99ce-118">-Force</span></span>
<span data-ttu-id="e99ce-119">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="e99ce-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e99ce-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e99ce-120">-InputObject</span></span>
<span data-ttu-id="e99ce-121">PS-GALLERYITEM</span><span class="sxs-lookup"><span data-stu-id="e99ce-121">The PS Gallery Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery
Parameter Sets: ObjectParameter
Aliases: Gallery

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e99ce-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="e99ce-122">-Name</span></span>
<span data-ttu-id="e99ce-123">Namnet på galleriet.</span><span class="sxs-lookup"><span data-stu-id="e99ce-123">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e99ce-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e99ce-124">-ResourceGroupName</span></span>
<span data-ttu-id="e99ce-125">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="e99ce-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e99ce-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e99ce-126">-ResourceId</span></span>
<span data-ttu-id="e99ce-127">Resurs-ID för galleriet</span><span class="sxs-lookup"><span data-stu-id="e99ce-127">The resource Id for the gallery</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e99ce-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e99ce-128">-Confirm</span></span>
<span data-ttu-id="e99ce-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e99ce-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e99ce-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e99ce-130">-WhatIf</span></span>
<span data-ttu-id="e99ce-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e99ce-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e99ce-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e99ce-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e99ce-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e99ce-133">CommonParameters</span></span>
<span data-ttu-id="e99ce-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e99ce-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e99ce-135">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e99ce-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e99ce-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e99ce-136">INPUTS</span></span>

### <span data-ttu-id="e99ce-137">System. String</span><span class="sxs-lookup"><span data-stu-id="e99ce-137">System.String</span></span>

### <span data-ttu-id="e99ce-138">Microsoft. Azure. commands. Compute. Automation. Models. PSGallery</span><span class="sxs-lookup"><span data-stu-id="e99ce-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="e99ce-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e99ce-139">OUTPUTS</span></span>

### <span data-ttu-id="e99ce-140">Microsoft. Azure. commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="e99ce-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="e99ce-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e99ce-141">NOTES</span></span>

## <span data-ttu-id="e99ce-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e99ce-142">RELATED LINKS</span></span>

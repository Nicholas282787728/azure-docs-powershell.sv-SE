---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGallery.md
ms.openlocfilehash: 13964bf668533aa5c1bc09b9c4eaaab83c6c421e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98526820"
---
# <span data-ttu-id="80648-101">Remove-AzGallery</span><span class="sxs-lookup"><span data-stu-id="80648-101">Remove-AzGallery</span></span>

## <span data-ttu-id="80648-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="80648-102">SYNOPSIS</span></span>
<span data-ttu-id="80648-103">Ta bort ett galleri.</span><span class="sxs-lookup"><span data-stu-id="80648-103">Delete a gallery.</span></span>

## <span data-ttu-id="80648-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="80648-104">SYNTAX</span></span>

### <span data-ttu-id="80648-105">DefaultParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="80648-105">DefaultParameter (Default)</span></span>
```
Remove-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80648-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="80648-106">ResourceIdParameter</span></span>
```
Remove-AzGallery [-Force] [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80648-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="80648-107">ObjectParameter</span></span>
```
Remove-AzGallery [-Force] [-InputObject] <PSGallery> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80648-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="80648-108">DESCRIPTION</span></span>
<span data-ttu-id="80648-109">Ta bort ett galleri.</span><span class="sxs-lookup"><span data-stu-id="80648-109">Delete a gallery.</span></span>

## <span data-ttu-id="80648-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="80648-110">EXAMPLES</span></span>

### <span data-ttu-id="80648-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="80648-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGallery -ResourceGroupName $rgname -GalleryName $galleryName
```

<span data-ttu-id="80648-112">Ta bort det angivna galleriet.</span><span class="sxs-lookup"><span data-stu-id="80648-112">Delete the given gallery.</span></span>

## <span data-ttu-id="80648-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="80648-113">PARAMETERS</span></span>

### <span data-ttu-id="80648-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="80648-114">-AsJob</span></span>
<span data-ttu-id="80648-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="80648-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="80648-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80648-116">-DefaultProfile</span></span>
<span data-ttu-id="80648-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="80648-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80648-118">-Force</span><span class="sxs-lookup"><span data-stu-id="80648-118">-Force</span></span>
<span data-ttu-id="80648-119">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="80648-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="80648-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="80648-120">-InputObject</span></span>
<span data-ttu-id="80648-121">PS-GALLERYITEM</span><span class="sxs-lookup"><span data-stu-id="80648-121">The PS Gallery Object</span></span>

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

### <span data-ttu-id="80648-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="80648-122">-Name</span></span>
<span data-ttu-id="80648-123">Namnet på galleriet.</span><span class="sxs-lookup"><span data-stu-id="80648-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="80648-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80648-124">-ResourceGroupName</span></span>
<span data-ttu-id="80648-125">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="80648-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="80648-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="80648-126">-ResourceId</span></span>
<span data-ttu-id="80648-127">Resurs-ID för galleriet</span><span class="sxs-lookup"><span data-stu-id="80648-127">The resource Id for the gallery</span></span>

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

### <span data-ttu-id="80648-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="80648-128">-Confirm</span></span>
<span data-ttu-id="80648-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="80648-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80648-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80648-130">-WhatIf</span></span>
<span data-ttu-id="80648-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="80648-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80648-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="80648-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80648-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80648-133">CommonParameters</span></span>
<span data-ttu-id="80648-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80648-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80648-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="80648-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80648-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="80648-136">INPUTS</span></span>

### <span data-ttu-id="80648-137">System. String</span><span class="sxs-lookup"><span data-stu-id="80648-137">System.String</span></span>

### <span data-ttu-id="80648-138">Microsoft. Azure. commands. Compute. Automation. Models. PSGallery</span><span class="sxs-lookup"><span data-stu-id="80648-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="80648-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="80648-139">OUTPUTS</span></span>

### <span data-ttu-id="80648-140">Microsoft. Azure. commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="80648-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="80648-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="80648-141">NOTES</span></span>

## <span data-ttu-id="80648-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="80648-142">RELATED LINKS</span></span>

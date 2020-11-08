---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImage.md
ms.openlocfilehash: 614250a7fea7091f6098b44750f4c1b471d82d8b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088077"
---
# <span data-ttu-id="131a0-101">Remove-AzImage</span><span class="sxs-lookup"><span data-stu-id="131a0-101">Remove-AzImage</span></span>

## <span data-ttu-id="131a0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="131a0-102">SYNOPSIS</span></span>
<span data-ttu-id="131a0-103">Tar bort en bild.</span><span class="sxs-lookup"><span data-stu-id="131a0-103">Removes an image.</span></span>

## <span data-ttu-id="131a0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="131a0-104">SYNTAX</span></span>

```
Remove-AzImage [-ResourceGroupName] <String> [-ImageName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="131a0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="131a0-105">DESCRIPTION</span></span>
<span data-ttu-id="131a0-106">Cmdleten **Remove-AzImage** tar bort en bild..</span><span class="sxs-lookup"><span data-stu-id="131a0-106">The **Remove-AzImage** cmdlet removes an image..</span></span>

## <span data-ttu-id="131a0-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="131a0-107">EXAMPLES</span></span>

### <span data-ttu-id="131a0-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="131a0-108">Example 1</span></span>
```
PS C:\> Remove-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' -Force;
```

<span data-ttu-id="131a0-109">Det här kommandot tar bort bilden "Image01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="131a0-109">This command removes the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="131a0-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="131a0-110">PARAMETERS</span></span>

### <span data-ttu-id="131a0-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="131a0-111">-AsJob</span></span>
<span data-ttu-id="131a0-112">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="131a0-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="131a0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="131a0-113">-DefaultProfile</span></span>
<span data-ttu-id="131a0-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="131a0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="131a0-115">-Force</span><span class="sxs-lookup"><span data-stu-id="131a0-115">-Force</span></span>
<span data-ttu-id="131a0-116">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="131a0-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="131a0-117">-ImageName</span><span class="sxs-lookup"><span data-stu-id="131a0-117">-ImageName</span></span>
<span data-ttu-id="131a0-118">Anger namnet på en bild.</span><span class="sxs-lookup"><span data-stu-id="131a0-118">Specifies the name of an image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="131a0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="131a0-119">-ResourceGroupName</span></span>
<span data-ttu-id="131a0-120">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="131a0-120">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="131a0-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="131a0-121">-Confirm</span></span>
<span data-ttu-id="131a0-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="131a0-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="131a0-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="131a0-123">-WhatIf</span></span>
<span data-ttu-id="131a0-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="131a0-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="131a0-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="131a0-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="131a0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="131a0-126">CommonParameters</span></span>
<span data-ttu-id="131a0-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="131a0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="131a0-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="131a0-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="131a0-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="131a0-129">INPUTS</span></span>

### <span data-ttu-id="131a0-130">System. String</span><span class="sxs-lookup"><span data-stu-id="131a0-130">System.String</span></span>

## <span data-ttu-id="131a0-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="131a0-131">OUTPUTS</span></span>

### <span data-ttu-id="131a0-132">Microsoft. Azure. commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="131a0-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="131a0-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="131a0-133">NOTES</span></span>

## <span data-ttu-id="131a0-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="131a0-134">RELATED LINKS</span></span>
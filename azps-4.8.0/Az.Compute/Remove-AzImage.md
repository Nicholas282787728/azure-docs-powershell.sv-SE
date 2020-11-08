---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImage.md
ms.openlocfilehash: 614250a7fea7091f6098b44750f4c1b471d82d8b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94101638"
---
# <span data-ttu-id="f7f26-101">Remove-AzImage</span><span class="sxs-lookup"><span data-stu-id="f7f26-101">Remove-AzImage</span></span>

## <span data-ttu-id="f7f26-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f7f26-102">SYNOPSIS</span></span>
<span data-ttu-id="f7f26-103">Tar bort en bild.</span><span class="sxs-lookup"><span data-stu-id="f7f26-103">Removes an image.</span></span>

## <span data-ttu-id="f7f26-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f7f26-104">SYNTAX</span></span>

```
Remove-AzImage [-ResourceGroupName] <String> [-ImageName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7f26-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f7f26-105">DESCRIPTION</span></span>
<span data-ttu-id="f7f26-106">Cmdleten **Remove-AzImage** tar bort en bild..</span><span class="sxs-lookup"><span data-stu-id="f7f26-106">The **Remove-AzImage** cmdlet removes an image..</span></span>

## <span data-ttu-id="f7f26-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f7f26-107">EXAMPLES</span></span>

### <span data-ttu-id="f7f26-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f7f26-108">Example 1</span></span>
```
PS C:\> Remove-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' -Force;
```

<span data-ttu-id="f7f26-109">Det här kommandot tar bort bilden "Image01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="f7f26-109">This command removes the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="f7f26-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f7f26-110">PARAMETERS</span></span>

### <span data-ttu-id="f7f26-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f7f26-111">-AsJob</span></span>
<span data-ttu-id="f7f26-112">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="f7f26-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="f7f26-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7f26-113">-DefaultProfile</span></span>
<span data-ttu-id="f7f26-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f7f26-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7f26-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f7f26-115">-Force</span></span>
<span data-ttu-id="f7f26-116">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="f7f26-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f7f26-117">-ImageName</span><span class="sxs-lookup"><span data-stu-id="f7f26-117">-ImageName</span></span>
<span data-ttu-id="f7f26-118">Anger namnet på en bild.</span><span class="sxs-lookup"><span data-stu-id="f7f26-118">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="f7f26-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7f26-119">-ResourceGroupName</span></span>
<span data-ttu-id="f7f26-120">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="f7f26-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="f7f26-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f7f26-121">-Confirm</span></span>
<span data-ttu-id="f7f26-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f7f26-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7f26-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7f26-123">-WhatIf</span></span>
<span data-ttu-id="f7f26-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f7f26-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7f26-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f7f26-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7f26-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7f26-126">CommonParameters</span></span>
<span data-ttu-id="f7f26-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7f26-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7f26-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f7f26-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7f26-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f7f26-129">INPUTS</span></span>

### <span data-ttu-id="f7f26-130">System. String</span><span class="sxs-lookup"><span data-stu-id="f7f26-130">System.String</span></span>

## <span data-ttu-id="f7f26-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f7f26-131">OUTPUTS</span></span>

### <span data-ttu-id="f7f26-132">Microsoft. Azure. commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="f7f26-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="f7f26-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f7f26-133">NOTES</span></span>

## <span data-ttu-id="f7f26-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f7f26-134">RELATED LINKS</span></span>

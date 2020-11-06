---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmImage.md
ms.openlocfilehash: 7d6d130f639265cd2b7e2885f117d2e29899b8c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584772"
---
# <span data-ttu-id="bee74-101">Remove-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="bee74-101">Remove-AzureRmImage</span></span>

## <span data-ttu-id="bee74-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bee74-102">SYNOPSIS</span></span>
<span data-ttu-id="bee74-103">Tar bort en bild.</span><span class="sxs-lookup"><span data-stu-id="bee74-103">Removes an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bee74-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bee74-104">SYNTAX</span></span>

```
Remove-AzureRmImage [-ResourceGroupName] <String> [-ImageName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bee74-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bee74-105">DESCRIPTION</span></span>
<span data-ttu-id="bee74-106">Cmdleten **Remove-AzureRmImage** tar bort en bild..</span><span class="sxs-lookup"><span data-stu-id="bee74-106">The **Remove-AzureRmImage** cmdlet removes an image..</span></span>

## <span data-ttu-id="bee74-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bee74-107">EXAMPLES</span></span>

### <span data-ttu-id="bee74-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="bee74-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' -Force;
```

<span data-ttu-id="bee74-109">Det här kommandot tar bort bilden "Image01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="bee74-109">This command removes the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="bee74-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bee74-110">PARAMETERS</span></span>

### <span data-ttu-id="bee74-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bee74-111">-DefaultProfile</span></span>
<span data-ttu-id="bee74-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bee74-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bee74-113">-Force</span><span class="sxs-lookup"><span data-stu-id="bee74-113">-Force</span></span>
<span data-ttu-id="bee74-114">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="bee74-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bee74-115">-ImageName</span><span class="sxs-lookup"><span data-stu-id="bee74-115">-ImageName</span></span>
<span data-ttu-id="bee74-116">Anger namnet på en bild.</span><span class="sxs-lookup"><span data-stu-id="bee74-116">Specifies the name of an image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bee74-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bee74-117">-ResourceGroupName</span></span>
<span data-ttu-id="bee74-118">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="bee74-118">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bee74-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bee74-119">-Confirm</span></span>
<span data-ttu-id="bee74-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bee74-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bee74-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bee74-121">-WhatIf</span></span>
<span data-ttu-id="bee74-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bee74-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bee74-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bee74-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bee74-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bee74-124">CommonParameters</span></span>
<span data-ttu-id="bee74-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bee74-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bee74-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bee74-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bee74-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bee74-127">INPUTS</span></span>

### <span data-ttu-id="bee74-128">System. String</span><span class="sxs-lookup"><span data-stu-id="bee74-128">System.String</span></span>

## <span data-ttu-id="bee74-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bee74-129">OUTPUTS</span></span>

### <span data-ttu-id="bee74-130">System. Object</span><span class="sxs-lookup"><span data-stu-id="bee74-130">System.Object</span></span>

## <span data-ttu-id="bee74-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bee74-131">NOTES</span></span>

## <span data-ttu-id="bee74-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bee74-132">RELATED LINKS</span></span>


---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzImage.md
ms.openlocfilehash: 7dd0978bc408841c0474445dd3bb29d032d9a52c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93925001"
---
# <span data-ttu-id="6972e-101">Remove-AzImage</span><span class="sxs-lookup"><span data-stu-id="6972e-101">Remove-AzImage</span></span>

## <span data-ttu-id="6972e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6972e-102">SYNOPSIS</span></span>
<span data-ttu-id="6972e-103">Tar bort en bild.</span><span class="sxs-lookup"><span data-stu-id="6972e-103">Removes an image.</span></span>

## <span data-ttu-id="6972e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6972e-104">SYNTAX</span></span>

```
Remove-AzImage [-ResourceGroupName] <String> [-ImageName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6972e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6972e-105">DESCRIPTION</span></span>
<span data-ttu-id="6972e-106">Cmdleten **Remove-AzImage** tar bort en bild..</span><span class="sxs-lookup"><span data-stu-id="6972e-106">The **Remove-AzImage** cmdlet removes an image..</span></span>

## <span data-ttu-id="6972e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6972e-107">EXAMPLES</span></span>

### <span data-ttu-id="6972e-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6972e-108">Example 1</span></span>
```
PS C:\> Remove-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' -Force;
```

<span data-ttu-id="6972e-109">Det här kommandot tar bort bilden "Image01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="6972e-109">This command removes the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="6972e-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6972e-110">PARAMETERS</span></span>

### <span data-ttu-id="6972e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6972e-111">-AsJob</span></span>
<span data-ttu-id="6972e-112">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="6972e-112">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6972e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6972e-113">-DefaultProfile</span></span>
<span data-ttu-id="6972e-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6972e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6972e-115">-Force</span><span class="sxs-lookup"><span data-stu-id="6972e-115">-Force</span></span>
<span data-ttu-id="6972e-116">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="6972e-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6972e-117">-ImageName</span><span class="sxs-lookup"><span data-stu-id="6972e-117">-ImageName</span></span>
<span data-ttu-id="6972e-118">Anger namnet på en bild.</span><span class="sxs-lookup"><span data-stu-id="6972e-118">Specifies the name of an image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6972e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6972e-119">-ResourceGroupName</span></span>
<span data-ttu-id="6972e-120">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="6972e-120">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6972e-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6972e-121">-Confirm</span></span>
<span data-ttu-id="6972e-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6972e-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6972e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6972e-123">-WhatIf</span></span>
<span data-ttu-id="6972e-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6972e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6972e-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6972e-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6972e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6972e-126">CommonParameters</span></span>
<span data-ttu-id="6972e-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6972e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6972e-128">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6972e-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6972e-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6972e-129">INPUTS</span></span>

### <span data-ttu-id="6972e-130">System. String</span><span class="sxs-lookup"><span data-stu-id="6972e-130">System.String</span></span>

## <span data-ttu-id="6972e-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6972e-131">OUTPUTS</span></span>

### <span data-ttu-id="6972e-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="6972e-132">System.Object</span></span>

## <span data-ttu-id="6972e-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6972e-133">NOTES</span></span>

## <span data-ttu-id="6972e-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6972e-134">RELATED LINKS</span></span>


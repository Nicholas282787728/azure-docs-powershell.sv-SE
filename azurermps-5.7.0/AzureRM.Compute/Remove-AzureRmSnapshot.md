---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmSnapshot.md
ms.openlocfilehash: 36dec1f8d4374f2e5bbed1f742aa7733bb760f67
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576599"
---
# <span data-ttu-id="73e09-101">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="73e09-101">Remove-AzureRmSnapshot</span></span>

## <span data-ttu-id="73e09-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="73e09-102">SYNOPSIS</span></span>
<span data-ttu-id="73e09-103">Tar bort en stillbild.</span><span class="sxs-lookup"><span data-stu-id="73e09-103">Removes a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73e09-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="73e09-104">SYNTAX</span></span>

```
Remove-AzureRmSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="73e09-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="73e09-105">DESCRIPTION</span></span>
<span data-ttu-id="73e09-106">Cmdleten **Remove-AzureRmSnapshot** tar bort en stillbild.</span><span class="sxs-lookup"><span data-stu-id="73e09-106">The **Remove-AzureRmSnapshot** cmdlet removes a snapshot.</span></span>

## <span data-ttu-id="73e09-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="73e09-107">EXAMPLES</span></span>

### <span data-ttu-id="73e09-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="73e09-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Force;
```

<span data-ttu-id="73e09-109">Det här kommandot tar bort stillbilden "Snapshot01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="73e09-109">This command removes the snapshot named 'Snapshot01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="73e09-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="73e09-110">PARAMETERS</span></span>

### <span data-ttu-id="73e09-111">-Force</span><span class="sxs-lookup"><span data-stu-id="73e09-111">-Force</span></span>
<span data-ttu-id="73e09-112">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="73e09-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73e09-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73e09-113">-ResourceGroupName</span></span>
<span data-ttu-id="73e09-114">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="73e09-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="73e09-115">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="73e09-115">-SnapshotName</span></span>
<span data-ttu-id="73e09-116">Anger namnet på en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="73e09-116">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="73e09-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="73e09-117">-Confirm</span></span>
<span data-ttu-id="73e09-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="73e09-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73e09-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73e09-119">-WhatIf</span></span>
<span data-ttu-id="73e09-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="73e09-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73e09-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="73e09-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73e09-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73e09-122">CommonParameters</span></span>
<span data-ttu-id="73e09-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73e09-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73e09-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73e09-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73e09-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="73e09-125">INPUTS</span></span>

### <span data-ttu-id="73e09-126">System. String</span><span class="sxs-lookup"><span data-stu-id="73e09-126">System.String</span></span>

## <span data-ttu-id="73e09-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="73e09-127">OUTPUTS</span></span>

### <span data-ttu-id="73e09-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="73e09-128">System.Object</span></span>

## <span data-ttu-id="73e09-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="73e09-129">NOTES</span></span>

## <span data-ttu-id="73e09-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="73e09-130">RELATED LINKS</span></span>


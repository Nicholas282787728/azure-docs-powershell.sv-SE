---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Revoke-AzureRmDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Revoke-AzureRmDiskAccess.md
ms.openlocfilehash: 2b9573e3add842478977cf620873d3cf0cfdaa8f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584416"
---
# <span data-ttu-id="e63ea-101">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="e63ea-101">Revoke-AzureRmDiskAccess</span></span>

## <span data-ttu-id="e63ea-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e63ea-102">SYNOPSIS</span></span>
<span data-ttu-id="e63ea-103">Återkallar en åtkomst till en disk.</span><span class="sxs-lookup"><span data-stu-id="e63ea-103">Revokes an access to a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e63ea-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e63ea-104">SYNTAX</span></span>

```
Revoke-AzureRmDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e63ea-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e63ea-105">DESCRIPTION</span></span>
<span data-ttu-id="e63ea-106">Cmdleten **REVOKE-AzureRmDiskAccess** avvisar en åtkomst till en disk.</span><span class="sxs-lookup"><span data-stu-id="e63ea-106">The **Revoke-AzureRmDiskAccess** cmdlet revokes an access to a disk.</span></span>

## <span data-ttu-id="e63ea-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e63ea-107">EXAMPLES</span></span>

### <span data-ttu-id="e63ea-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e63ea-108">Example 1</span></span>
```
PS C:\> Revoke-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="e63ea-109">Återkalla åtkomsten till disken "Disk01" i resurs gruppen med namnet "ResourceGroup01"</span><span class="sxs-lookup"><span data-stu-id="e63ea-109">Revoke the access to the disk named 'Disk01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="e63ea-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e63ea-110">PARAMETERS</span></span>

### <span data-ttu-id="e63ea-111">-DiskName</span><span class="sxs-lookup"><span data-stu-id="e63ea-111">-DiskName</span></span>
<span data-ttu-id="e63ea-112">Anger namnet på en disk.</span><span class="sxs-lookup"><span data-stu-id="e63ea-112">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="e63ea-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e63ea-113">-ResourceGroupName</span></span>
<span data-ttu-id="e63ea-114">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="e63ea-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="e63ea-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e63ea-115">-Confirm</span></span>
<span data-ttu-id="e63ea-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e63ea-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e63ea-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e63ea-117">-WhatIf</span></span>
<span data-ttu-id="e63ea-118">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e63ea-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e63ea-119">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e63ea-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e63ea-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e63ea-120">CommonParameters</span></span>
<span data-ttu-id="e63ea-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e63ea-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e63ea-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e63ea-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e63ea-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e63ea-123">INPUTS</span></span>

### <span data-ttu-id="e63ea-124">System. String</span><span class="sxs-lookup"><span data-stu-id="e63ea-124">System.String</span></span>

## <span data-ttu-id="e63ea-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e63ea-125">OUTPUTS</span></span>

### <span data-ttu-id="e63ea-126">System. Object</span><span class="sxs-lookup"><span data-stu-id="e63ea-126">System.Object</span></span>

## <span data-ttu-id="e63ea-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e63ea-127">NOTES</span></span>

## <span data-ttu-id="e63ea-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e63ea-128">RELATED LINKS</span></span>


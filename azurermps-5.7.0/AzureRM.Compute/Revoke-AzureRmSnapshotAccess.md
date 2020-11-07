---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Revoke-AzureRmSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Revoke-AzureRmSnapshotAccess.md
ms.openlocfilehash: d081218a17bd5cac99256918d40ece722b73a85b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757698"
---
# <span data-ttu-id="807bb-101">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="807bb-101">Revoke-AzureRmSnapshotAccess</span></span>

## <span data-ttu-id="807bb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="807bb-102">SYNOPSIS</span></span>
<span data-ttu-id="807bb-103">Återkallar en åtkomst till en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="807bb-103">Revokes an access to a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="807bb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="807bb-104">SYNTAX</span></span>

```
Revoke-AzureRmSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="807bb-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="807bb-105">DESCRIPTION</span></span>
<span data-ttu-id="807bb-106">Cmdleten **REVOKE-AzureRmSnapshotAccess** avvisar en åtkomst till en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="807bb-106">The **Revoke-AzureRmSnapshotAccess** cmdlet revokes an access to a snapshot.</span></span>

## <span data-ttu-id="807bb-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="807bb-107">EXAMPLES</span></span>

### <span data-ttu-id="807bb-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="807bb-108">Example 1</span></span>
```
PS C:\> Revoke-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01'
```

<span data-ttu-id="807bb-109">Återkalla åtkomsten till ögonblicks bilden med namnet "Snapshot01" i resurs gruppen med namnet "ResourceGroup01"</span><span class="sxs-lookup"><span data-stu-id="807bb-109">Revoke the access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="807bb-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="807bb-110">PARAMETERS</span></span>

### <span data-ttu-id="807bb-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="807bb-111">-ResourceGroupName</span></span>
<span data-ttu-id="807bb-112">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="807bb-112">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="807bb-113">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="807bb-113">-SnapshotName</span></span>
<span data-ttu-id="807bb-114">Anger namnet på en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="807bb-114">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="807bb-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="807bb-115">-Confirm</span></span>
<span data-ttu-id="807bb-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="807bb-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="807bb-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="807bb-117">-WhatIf</span></span>
<span data-ttu-id="807bb-118">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="807bb-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="807bb-119">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="807bb-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="807bb-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="807bb-120">CommonParameters</span></span>
<span data-ttu-id="807bb-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="807bb-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="807bb-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="807bb-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="807bb-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="807bb-123">INPUTS</span></span>

### <span data-ttu-id="807bb-124">System. String</span><span class="sxs-lookup"><span data-stu-id="807bb-124">System.String</span></span>

## <span data-ttu-id="807bb-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="807bb-125">OUTPUTS</span></span>

### <span data-ttu-id="807bb-126">System. Object</span><span class="sxs-lookup"><span data-stu-id="807bb-126">System.Object</span></span>

## <span data-ttu-id="807bb-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="807bb-127">NOTES</span></span>

## <span data-ttu-id="807bb-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="807bb-128">RELATED LINKS</span></span>


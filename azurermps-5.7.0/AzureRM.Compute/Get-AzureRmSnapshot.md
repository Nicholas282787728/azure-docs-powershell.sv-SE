---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmSnapshot.md
ms.openlocfilehash: 9f4d2c4e6321d36079cf4c5e87747863c8dc51c3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578308"
---
# <span data-ttu-id="ec120-101">Get-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="ec120-101">Get-AzureRmSnapshot</span></span>

## <span data-ttu-id="ec120-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ec120-102">SYNOPSIS</span></span>
<span data-ttu-id="ec120-103">Hämtar egenskaperna för en ögonblicks bild</span><span class="sxs-lookup"><span data-stu-id="ec120-103">Gets the properties of a snapshot</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec120-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ec120-104">SYNTAX</span></span>

```
Get-AzureRmSnapshot [[-ResourceGroupName] <String>] [[-SnapshotName] <String>] [<CommonParameters>]
```

## <span data-ttu-id="ec120-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ec120-105">DESCRIPTION</span></span>
<span data-ttu-id="ec120-106">Cmdleten **Get-AzureRmSnapshot** hämtar egenskaperna för en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="ec120-106">The **Get-AzureRmSnapshot** cmdlet gets the properties of a snapshot.</span></span>

## <span data-ttu-id="ec120-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ec120-107">EXAMPLES</span></span>

### <span data-ttu-id="ec120-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ec120-108">Example 1</span></span>
```
PS C:\> Get-AzureRmSnapshot
```

<span data-ttu-id="ec120-109">Det här kommandot får egenskaperna för alla stillbilder av abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="ec120-109">This command gets the properties of all snapshots of the subscription.</span></span>

### <span data-ttu-id="ec120-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="ec120-110">Example 2</span></span>
```
PS C:\> Get-AzureRmSnapshot -ResourceGroupName "ResourceGroupName1"
```

<span data-ttu-id="ec120-111">Det här kommandot får egenskaperna för alla stillbilder i resurs gruppen "ResourceGroupName1"</span><span class="sxs-lookup"><span data-stu-id="ec120-111">This command gets the properties of all snapshots in the resource group named "ResourceGroupName1"</span></span>

### <span data-ttu-id="ec120-112">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="ec120-112">Example 3</span></span>
```
PS C:\> Get-AzureRmSnapshot -ResourceGroupName "ResourceGroupName1" -SnapshotName "SnapshotName1"
```

<span data-ttu-id="ec120-113">Det här kommandot får egenskaperna för fixeringen med namnet "SnapshotName1" i resurs gruppen med namnet "ResourceGroupName1"</span><span class="sxs-lookup"><span data-stu-id="ec120-113">This command gets the properties of the snapshot named "SnapshotName1" in the resource group named "ResourceGroupName1"</span></span>

## <span data-ttu-id="ec120-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ec120-114">PARAMETERS</span></span>

### <span data-ttu-id="ec120-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec120-115">-ResourceGroupName</span></span>
<span data-ttu-id="ec120-116">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="ec120-116">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec120-117">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="ec120-117">-SnapshotName</span></span>
<span data-ttu-id="ec120-118">Anger namnet på en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="ec120-118">Specifies the name of a snapshot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec120-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec120-119">CommonParameters</span></span>
<span data-ttu-id="ec120-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec120-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec120-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec120-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec120-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ec120-122">INPUTS</span></span>

### <span data-ttu-id="ec120-123">System. String</span><span class="sxs-lookup"><span data-stu-id="ec120-123">System.String</span></span>

## <span data-ttu-id="ec120-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ec120-124">OUTPUTS</span></span>

### <span data-ttu-id="ec120-125">System. Object</span><span class="sxs-lookup"><span data-stu-id="ec120-125">System.Object</span></span>

## <span data-ttu-id="ec120-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ec120-126">NOTES</span></span>

## <span data-ttu-id="ec120-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ec120-127">RELATED LINKS</span></span>


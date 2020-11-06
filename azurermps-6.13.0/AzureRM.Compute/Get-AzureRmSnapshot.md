---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmSnapshot.md
ms.openlocfilehash: 14b1c1179e9fee15f398c4518e446cf47396e660
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575292"
---
# <span data-ttu-id="fe76b-101">Get-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="fe76b-101">Get-AzureRmSnapshot</span></span>

## <span data-ttu-id="fe76b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fe76b-102">SYNOPSIS</span></span>
<span data-ttu-id="fe76b-103">Hämtar egenskaperna för en ögonblicks bild</span><span class="sxs-lookup"><span data-stu-id="fe76b-103">Gets the properties of a snapshot</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe76b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fe76b-104">SYNTAX</span></span>

```
Get-AzureRmSnapshot [[-ResourceGroupName] <String>] [[-SnapshotName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe76b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fe76b-105">DESCRIPTION</span></span>
<span data-ttu-id="fe76b-106">Cmdleten **Get-AzureRmSnapshot** hämtar egenskaperna för en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="fe76b-106">The **Get-AzureRmSnapshot** cmdlet gets the properties of a snapshot.</span></span>

## <span data-ttu-id="fe76b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fe76b-107">EXAMPLES</span></span>

### <span data-ttu-id="fe76b-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="fe76b-108">Example 1</span></span>
```
PS C:\> Get-AzureRmSnapshot
```

<span data-ttu-id="fe76b-109">Det här kommandot får egenskaperna för alla stillbilder av abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="fe76b-109">This command gets the properties of all snapshots of the subscription.</span></span>

### <span data-ttu-id="fe76b-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="fe76b-110">Example 2</span></span>
```
PS C:\> Get-AzureRmSnapshot -ResourceGroupName "ResourceGroupName1"
```

<span data-ttu-id="fe76b-111">Det här kommandot får egenskaperna för alla stillbilder i resurs gruppen "ResourceGroupName1"</span><span class="sxs-lookup"><span data-stu-id="fe76b-111">This command gets the properties of all snapshots in the resource group named "ResourceGroupName1"</span></span>

### <span data-ttu-id="fe76b-112">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="fe76b-112">Example 3</span></span>
```
PS C:\> Get-AzureRmSnapshot -ResourceGroupName "ResourceGroupName1" -SnapshotName "SnapshotName1"
```

<span data-ttu-id="fe76b-113">Det här kommandot får egenskaperna för fixeringen med namnet "SnapshotName1" i resurs gruppen med namnet "ResourceGroupName1"</span><span class="sxs-lookup"><span data-stu-id="fe76b-113">This command gets the properties of the snapshot named "SnapshotName1" in the resource group named "ResourceGroupName1"</span></span>

## <span data-ttu-id="fe76b-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fe76b-114">PARAMETERS</span></span>

### <span data-ttu-id="fe76b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe76b-115">-DefaultProfile</span></span>
<span data-ttu-id="fe76b-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fe76b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe76b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe76b-117">-ResourceGroupName</span></span>
<span data-ttu-id="fe76b-118">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="fe76b-118">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe76b-119">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="fe76b-119">-SnapshotName</span></span>
<span data-ttu-id="fe76b-120">Anger namnet på en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="fe76b-120">Specifies the name of a snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe76b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe76b-121">CommonParameters</span></span>
<span data-ttu-id="fe76b-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe76b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe76b-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe76b-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe76b-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fe76b-124">INPUTS</span></span>

### <span data-ttu-id="fe76b-125">System. String</span><span class="sxs-lookup"><span data-stu-id="fe76b-125">System.String</span></span>

## <span data-ttu-id="fe76b-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fe76b-126">OUTPUTS</span></span>

### <span data-ttu-id="fe76b-127">Microsoft. Azure. commands. Compute. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="fe76b-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="fe76b-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fe76b-128">NOTES</span></span>

## <span data-ttu-id="fe76b-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fe76b-129">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermsnapshot
schema: 2.0.0
ms.openlocfilehash: 8133bfc8381f08e69afbd6bfbd3a25084e9eb2b9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929490"
---
# <span data-ttu-id="23fec-101">Get-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="23fec-101">Get-AzureRmSnapshot</span></span>

## <span data-ttu-id="23fec-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="23fec-102">SYNOPSIS</span></span>
<span data-ttu-id="23fec-103">Hämtar egenskaperna för en ögonblicks bild</span><span class="sxs-lookup"><span data-stu-id="23fec-103">Gets the properties of a snapshot</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23fec-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="23fec-104">SYNTAX</span></span>

```
Get-AzureRmSnapshot [[-ResourceGroupName] <String>] [[-SnapshotName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23fec-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="23fec-105">DESCRIPTION</span></span>
<span data-ttu-id="23fec-106">Cmdleten **Get-AzureRmSnapshot** hämtar egenskaperna för en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="23fec-106">The **Get-AzureRmSnapshot** cmdlet gets the properties of a snapshot.</span></span>

## <span data-ttu-id="23fec-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="23fec-107">EXAMPLES</span></span>

### <span data-ttu-id="23fec-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="23fec-108">Example 1</span></span>
```
PS C:\> Get-AzureRmSnapshot
```

<span data-ttu-id="23fec-109">Det här kommandot får egenskaperna för alla stillbilder av abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="23fec-109">This command gets the properties of all snapshots of the subscription.</span></span>

### <span data-ttu-id="23fec-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="23fec-110">Example 2</span></span>
```
PS C:\> Get-AzureRmSnapshot -ResourceGroupName "ResourceGroupName1"
```

<span data-ttu-id="23fec-111">Det här kommandot får egenskaperna för alla stillbilder i resurs gruppen "ResourceGroupName1"</span><span class="sxs-lookup"><span data-stu-id="23fec-111">This command gets the properties of all snapshots in the resource group named "ResourceGroupName1"</span></span>

### <span data-ttu-id="23fec-112">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="23fec-112">Example 3</span></span>
```
PS C:\> Get-AzureRmSnapshot -ResourceGroupName "ResourceGroupName1" -SnapshotName "SnapshotName1"
```

<span data-ttu-id="23fec-113">Det här kommandot får egenskaperna för fixeringen med namnet "SnapshotName1" i resurs gruppen med namnet "ResourceGroupName1"</span><span class="sxs-lookup"><span data-stu-id="23fec-113">This command gets the properties of the snapshot named "SnapshotName1" in the resource group named "ResourceGroupName1"</span></span>

## <span data-ttu-id="23fec-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="23fec-114">PARAMETERS</span></span>

### <span data-ttu-id="23fec-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23fec-115">-DefaultProfile</span></span>
<span data-ttu-id="23fec-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="23fec-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23fec-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23fec-117">-ResourceGroupName</span></span>
<span data-ttu-id="23fec-118">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="23fec-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="23fec-119">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="23fec-119">-SnapshotName</span></span>
<span data-ttu-id="23fec-120">Anger namnet på en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="23fec-120">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="23fec-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23fec-121">CommonParameters</span></span>
<span data-ttu-id="23fec-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23fec-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23fec-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23fec-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23fec-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="23fec-124">INPUTS</span></span>

### <span data-ttu-id="23fec-125">System. String</span><span class="sxs-lookup"><span data-stu-id="23fec-125">System.String</span></span>

## <span data-ttu-id="23fec-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="23fec-126">OUTPUTS</span></span>

### <span data-ttu-id="23fec-127">Microsoft. Azure. commands. Compute. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="23fec-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="23fec-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="23fec-128">NOTES</span></span>

## <span data-ttu-id="23fec-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="23fec-129">RELATED LINKS</span></span>


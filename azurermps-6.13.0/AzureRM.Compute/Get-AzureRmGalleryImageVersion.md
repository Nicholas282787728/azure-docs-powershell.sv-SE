---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmGalleryImageVersion.md
ms.openlocfilehash: bff748b8c867b272208469d34229cc2724bc8610
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575296"
---
# <span data-ttu-id="0410c-101">Get-AzureRmGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="0410c-101">Get-AzureRmGalleryImageVersion</span></span>

## <span data-ttu-id="0410c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0410c-102">SYNOPSIS</span></span>
<span data-ttu-id="0410c-103">Bild versioner för hämta eller lista</span><span class="sxs-lookup"><span data-stu-id="0410c-103">Get or list gallery image versions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0410c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0410c-104">SYNTAX</span></span>

### <span data-ttu-id="0410c-105">DefaultParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="0410c-105">DefaultParameter (Default)</span></span>
```
Get-AzureRmGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [[-Name] <String>] [-ExpandReplicationStatus]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0410c-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="0410c-106">ResourceIdParameter</span></span>
```
Get-AzureRmGalleryImageVersion [-ResourceId] <String> [-ExpandReplicationStatus]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0410c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0410c-107">DESCRIPTION</span></span>
<span data-ttu-id="0410c-108">Bild versioner för hämta eller lista</span><span class="sxs-lookup"><span data-stu-id="0410c-108">Get or list gallery image versions.</span></span>

## <span data-ttu-id="0410c-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0410c-109">EXAMPLES</span></span>

### <span data-ttu-id="0410c-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0410c-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmGalleryImageVersion -ResourceGroupName $rgname -GalleryName $gallery -ImageDefinitionName $image -GalleryImageVersionName $version
```

<span data-ttu-id="0410c-111">Hämta bild versionen för galleriet.</span><span class="sxs-lookup"><span data-stu-id="0410c-111">Get the gallery image version.</span></span>

## <span data-ttu-id="0410c-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0410c-112">PARAMETERS</span></span>

### <span data-ttu-id="0410c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0410c-113">-DefaultProfile</span></span>
<span data-ttu-id="0410c-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0410c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0410c-115">-ExpandReplicationStatus</span><span class="sxs-lookup"><span data-stu-id="0410c-115">-ExpandReplicationStatus</span></span>
<span data-ttu-id="0410c-116">Visa replikeringsstatus.</span><span class="sxs-lookup"><span data-stu-id="0410c-116">Show replication status.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0410c-117">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="0410c-117">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="0410c-118">Namnet på bild definitionen för galleriet.</span><span class="sxs-lookup"><span data-stu-id="0410c-118">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0410c-119">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="0410c-119">-GalleryName</span></span>
<span data-ttu-id="0410c-120">Namnet på galleriet.</span><span class="sxs-lookup"><span data-stu-id="0410c-120">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0410c-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="0410c-121">-Name</span></span>
<span data-ttu-id="0410c-122">Namnet på Galleri bild versionen.</span><span class="sxs-lookup"><span data-stu-id="0410c-122">The name of the gallery image version.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryImageVersionName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0410c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0410c-123">-ResourceGroupName</span></span>
<span data-ttu-id="0410c-124">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="0410c-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0410c-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0410c-125">-ResourceId</span></span>
<span data-ttu-id="0410c-126">Resurs-ID för galleri bild versionen</span><span class="sxs-lookup"><span data-stu-id="0410c-126">The resource ID for the gallery image version</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0410c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0410c-127">CommonParameters</span></span>
<span data-ttu-id="0410c-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0410c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0410c-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0410c-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0410c-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0410c-130">INPUTS</span></span>

### <span data-ttu-id="0410c-131">System. String</span><span class="sxs-lookup"><span data-stu-id="0410c-131">System.String</span></span>

### <span data-ttu-id="0410c-132">Microsoft. Azure. commands. Compute. Automation. Models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="0410c-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="0410c-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0410c-133">OUTPUTS</span></span>

### <span data-ttu-id="0410c-134">Microsoft. Azure. commands. Compute. Automation. Models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="0410c-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="0410c-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0410c-135">NOTES</span></span>

## <span data-ttu-id="0410c-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0410c-136">RELATED LINKS</span></span>

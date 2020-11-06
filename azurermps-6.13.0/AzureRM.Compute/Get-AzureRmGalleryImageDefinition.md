---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmGalleryImageDefinition.md
ms.openlocfilehash: 75d30165c5dc5d69eabd08e89ad2577df82f7ebd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575297"
---
# <span data-ttu-id="e35ef-101">Get-AzureRmGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="e35ef-101">Get-AzureRmGalleryImageDefinition</span></span>

## <span data-ttu-id="e35ef-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e35ef-102">SYNOPSIS</span></span>
<span data-ttu-id="e35ef-103">Bild definitionerna hämta eller lista Galleri.</span><span class="sxs-lookup"><span data-stu-id="e35ef-103">Get or list gallery image definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e35ef-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e35ef-104">SYNTAX</span></span>

### <span data-ttu-id="e35ef-105">DefaultParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="e35ef-105">DefaultParameter (Default)</span></span>
```
Get-AzureRmGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e35ef-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="e35ef-106">ResourceIdParameter</span></span>
```
Get-AzureRmGalleryImageDefinition [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e35ef-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e35ef-107">DESCRIPTION</span></span>
<span data-ttu-id="e35ef-108">Bild definitionerna hämta eller lista Galleri.</span><span class="sxs-lookup"><span data-stu-id="e35ef-108">Get or list gallery image definitions.</span></span>

## <span data-ttu-id="e35ef-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e35ef-109">EXAMPLES</span></span>

### <span data-ttu-id="e35ef-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e35ef-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmGalleryImageDefinition -ResourceGroupName $rgname -GalleryName $gallery -GalleryImageDefinitionName $image
```

<span data-ttu-id="e35ef-111">Hämta bild definitionen för galleriet.</span><span class="sxs-lookup"><span data-stu-id="e35ef-111">Get the gallery image definition.</span></span>

## <span data-ttu-id="e35ef-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e35ef-112">PARAMETERS</span></span>

### <span data-ttu-id="e35ef-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e35ef-113">-DefaultProfile</span></span>
<span data-ttu-id="e35ef-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e35ef-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e35ef-115">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="e35ef-115">-GalleryName</span></span>
<span data-ttu-id="e35ef-116">Namnet på galleriet.</span><span class="sxs-lookup"><span data-stu-id="e35ef-116">The name of the gallery.</span></span>

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

### <span data-ttu-id="e35ef-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="e35ef-117">-Name</span></span>
<span data-ttu-id="e35ef-118">Namnet på bild definitionen för galleriet.</span><span class="sxs-lookup"><span data-stu-id="e35ef-118">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryImageDefinitionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e35ef-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e35ef-119">-ResourceGroupName</span></span>
<span data-ttu-id="e35ef-120">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="e35ef-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="e35ef-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e35ef-121">-ResourceId</span></span>
<span data-ttu-id="e35ef-122">Resurs-ID för bild definitionen för galleriet</span><span class="sxs-lookup"><span data-stu-id="e35ef-122">The resource ID for the gallery image definition</span></span>

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

### <span data-ttu-id="e35ef-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e35ef-123">CommonParameters</span></span>
<span data-ttu-id="e35ef-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e35ef-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e35ef-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e35ef-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e35ef-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e35ef-126">INPUTS</span></span>

### <span data-ttu-id="e35ef-127">System. String</span><span class="sxs-lookup"><span data-stu-id="e35ef-127">System.String</span></span>

## <span data-ttu-id="e35ef-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e35ef-128">OUTPUTS</span></span>

### <span data-ttu-id="e35ef-129">Microsoft. Azure. commands. Compute. Automation. Models. PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="e35ef-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="e35ef-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e35ef-130">NOTES</span></span>

## <span data-ttu-id="e35ef-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e35ef-131">RELATED LINKS</span></span>

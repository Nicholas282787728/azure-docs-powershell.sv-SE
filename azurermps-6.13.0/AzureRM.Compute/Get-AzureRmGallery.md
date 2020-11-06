---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmGallery.md
ms.openlocfilehash: cdb703144daa6f9abd62aee41eaad94b2cfa50e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575304"
---
# <span data-ttu-id="53160-101">Get-AzureRmGallery</span><span class="sxs-lookup"><span data-stu-id="53160-101">Get-AzureRmGallery</span></span>

## <span data-ttu-id="53160-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="53160-102">SYNOPSIS</span></span>
<span data-ttu-id="53160-103">Hämta eller lista gallerier.</span><span class="sxs-lookup"><span data-stu-id="53160-103">Get or list galleries.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53160-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="53160-104">SYNTAX</span></span>

### <span data-ttu-id="53160-105">DefaultParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="53160-105">DefaultParameter (Default)</span></span>
```
Get-AzureRmGallery [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53160-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="53160-106">ResourceIdParameter</span></span>
```
Get-AzureRmGallery [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53160-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="53160-107">DESCRIPTION</span></span>
<span data-ttu-id="53160-108">Hämta eller lista gallerier.</span><span class="sxs-lookup"><span data-stu-id="53160-108">Get or list galleries.</span></span>

## <span data-ttu-id="53160-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="53160-109">EXAMPLES</span></span>

### <span data-ttu-id="53160-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="53160-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmGallery -ResourceGroupName $rgname -GalleryName $galleryName

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery1
Name              : gallery1
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}
```

<span data-ttu-id="53160-111">Skaffa galleriet.</span><span class="sxs-lookup"><span data-stu-id="53160-111">Get the gallery.</span></span>

## <span data-ttu-id="53160-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="53160-112">PARAMETERS</span></span>

### <span data-ttu-id="53160-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53160-113">-DefaultProfile</span></span>
<span data-ttu-id="53160-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="53160-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53160-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="53160-115">-Name</span></span>
<span data-ttu-id="53160-116">Namnet på galleriet.</span><span class="sxs-lookup"><span data-stu-id="53160-116">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53160-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53160-117">-ResourceGroupName</span></span>
<span data-ttu-id="53160-118">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="53160-118">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53160-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="53160-119">-ResourceId</span></span>
<span data-ttu-id="53160-120">Resurs-ID för galleriet</span><span class="sxs-lookup"><span data-stu-id="53160-120">The resource id for Gallery</span></span>

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

### <span data-ttu-id="53160-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53160-121">CommonParameters</span></span>
<span data-ttu-id="53160-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53160-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53160-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53160-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53160-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="53160-124">INPUTS</span></span>

### <span data-ttu-id="53160-125">System. String</span><span class="sxs-lookup"><span data-stu-id="53160-125">System.String</span></span>

### <span data-ttu-id="53160-126">Microsoft. Azure. commands. Compute. Automation. Models. PSGallery</span><span class="sxs-lookup"><span data-stu-id="53160-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="53160-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="53160-127">OUTPUTS</span></span>

### <span data-ttu-id="53160-128">Microsoft. Azure. commands. Compute. Automation. Models. PSGallery</span><span class="sxs-lookup"><span data-stu-id="53160-128">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="53160-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="53160-129">NOTES</span></span>

## <span data-ttu-id="53160-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="53160-130">RELATED LINKS</span></span>

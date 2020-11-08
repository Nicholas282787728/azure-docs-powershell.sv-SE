---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGallery.md
ms.openlocfilehash: baa3730ee03dd8f871e64e7964659c62f60e8032
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94101376"
---
# <span data-ttu-id="941f0-101">Get-AzGallery</span><span class="sxs-lookup"><span data-stu-id="941f0-101">Get-AzGallery</span></span>

## <span data-ttu-id="941f0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="941f0-102">SYNOPSIS</span></span>
<span data-ttu-id="941f0-103">Hämta eller lista gallerier.</span><span class="sxs-lookup"><span data-stu-id="941f0-103">Get or list galleries.</span></span>

## <span data-ttu-id="941f0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="941f0-104">SYNTAX</span></span>

### <span data-ttu-id="941f0-105">DefaultParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="941f0-105">DefaultParameter (Default)</span></span>
```
Get-AzGallery [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="941f0-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="941f0-106">ResourceIdParameter</span></span>
```
Get-AzGallery [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="941f0-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="941f0-107">DESCRIPTION</span></span>
<span data-ttu-id="941f0-108">Hämta eller lista gallerier.</span><span class="sxs-lookup"><span data-stu-id="941f0-108">Get or list galleries.</span></span>

## <span data-ttu-id="941f0-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="941f0-109">EXAMPLES</span></span>

### <span data-ttu-id="941f0-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="941f0-110">Example 1</span></span>
```powershell
PS C:\> Get-AzGallery -ResourceGroupName rg1 -GalleryName gallery1

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

<span data-ttu-id="941f0-111">Skaffa galleriet "gallery1"</span><span class="sxs-lookup"><span data-stu-id="941f0-111">Get the gallery "gallery1"</span></span>

### <span data-ttu-id="941f0-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="941f0-112">Example 2</span></span>
```powershell
PS C:\> Get-AzGallery -ResourceGroupName rg1

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

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery2
Name              : gallery2
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}
```

<span data-ttu-id="941f0-113">Hämta alla gallerier i RG1.</span><span class="sxs-lookup"><span data-stu-id="941f0-113">Get all galleries in rg1.</span></span>

### <span data-ttu-id="941f0-114">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="941f0-114">Example 3</span></span>
```powershell
PS C:\> Get-AzGallery

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

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery2
Name              : gallery2
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}

ResourceGroupName : rg2
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg2/providers/Microsoft.Compute/galleries/gallery3
Name              : gallery3
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}
```

<span data-ttu-id="941f0-115">Hämta alla gallerier i abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="941f0-115">Get all galleries in subscription.</span></span>

### <span data-ttu-id="941f0-116">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="941f0-116">Example 4</span></span>
```powershell
PS C:\> Get-AzGallery -Name gallery*

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

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery2
Name              : gallery2
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}

ResourceGroupName : rg2
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg2/providers/Microsoft.Compute/galleries/gallery3
Name              : gallery3
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}
```

<span data-ttu-id="941f0-117">Hämta alla gallerier i abonnemanget som börjar med "Galleri".</span><span class="sxs-lookup"><span data-stu-id="941f0-117">Get all galleries in subscription that start with "gallery".</span></span>

## <span data-ttu-id="941f0-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="941f0-118">PARAMETERS</span></span>

### <span data-ttu-id="941f0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="941f0-119">-DefaultProfile</span></span>
<span data-ttu-id="941f0-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="941f0-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="941f0-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="941f0-121">-Name</span></span>
<span data-ttu-id="941f0-122">Namnet på galleriet.</span><span class="sxs-lookup"><span data-stu-id="941f0-122">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="941f0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="941f0-123">-ResourceGroupName</span></span>
<span data-ttu-id="941f0-124">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="941f0-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="941f0-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="941f0-125">-ResourceId</span></span>
<span data-ttu-id="941f0-126">Resurs-ID för galleriet</span><span class="sxs-lookup"><span data-stu-id="941f0-126">The resource id for Gallery</span></span>

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

### <span data-ttu-id="941f0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="941f0-127">CommonParameters</span></span>
<span data-ttu-id="941f0-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="941f0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="941f0-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="941f0-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="941f0-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="941f0-130">INPUTS</span></span>

### <span data-ttu-id="941f0-131">System. String</span><span class="sxs-lookup"><span data-stu-id="941f0-131">System.String</span></span>

## <span data-ttu-id="941f0-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="941f0-132">OUTPUTS</span></span>

### <span data-ttu-id="941f0-133">Microsoft. Azure. commands. Compute. Automation. Models. PSGallery</span><span class="sxs-lookup"><span data-stu-id="941f0-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="941f0-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="941f0-134">NOTES</span></span>

## <span data-ttu-id="941f0-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="941f0-135">RELATED LINKS</span></span>

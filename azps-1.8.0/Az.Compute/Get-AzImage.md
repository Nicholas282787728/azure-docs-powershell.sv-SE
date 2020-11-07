---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzImage.md
ms.openlocfilehash: ffebc22d2ad5c28c40d79ffb9c6ba8b5ba5bf5a8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754589"
---
# <span data-ttu-id="54601-101">Get-AzImage</span><span class="sxs-lookup"><span data-stu-id="54601-101">Get-AzImage</span></span>

## <span data-ttu-id="54601-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="54601-102">SYNOPSIS</span></span>
<span data-ttu-id="54601-103">Hämtar egenskaperna för en bild.</span><span class="sxs-lookup"><span data-stu-id="54601-103">Gets the properties of an image.</span></span>

## <span data-ttu-id="54601-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="54601-104">SYNTAX</span></span>

```
Get-AzImage [[-ResourceGroupName] <String>] [[-ImageName] <String>] [[-Expand] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54601-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="54601-105">DESCRIPTION</span></span>
<span data-ttu-id="54601-106">Cmdleten **Get-AzImage** hämtar egenskaperna för en bild.</span><span class="sxs-lookup"><span data-stu-id="54601-106">The **Get-AzImage** cmdlet gets the properties of an image.</span></span>

## <span data-ttu-id="54601-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="54601-107">EXAMPLES</span></span>

### <span data-ttu-id="54601-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="54601-108">Example 1</span></span>
```
PS C:\> Get-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01'

ResourceGroupName    : ResourceGroup01
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/prov
                       iders/Microsoft.Compute/images/Image01
Name                 : Image01
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}
```

<span data-ttu-id="54601-109">Det här kommandot får egenskaperna för bilden med namnet "Image01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="54601-109">This command gets the properties of the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="54601-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="54601-110">Example 2</span></span>
```
PS C:\> Get-AzImage -ResourceGroupName 'ResourceGroup01'

ResourceGroupName    : ResourceGroup01
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/prov
                       iders/Microsoft.Compute/images/Image01
Name                 : Image01
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}

ResourceGroupName    : ResourceGroup01
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/prov
                       iders/Microsoft.Compute/images/Image02
Name                 : Image02
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}
```

<span data-ttu-id="54601-111">Det här kommandot får egenskaperna för alla bilder i resurs gruppen ' ResourceGroup01 '.</span><span class="sxs-lookup"><span data-stu-id="54601-111">This command gets the properties of all images in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="54601-112">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="54601-112">Example 3</span></span>
```
PS C:\> Get-AzImage

ResourceGroupName    : ResourceGroup01
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/prov
                       iders/Microsoft.Compute/images/Image01
Name                 : Image01
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}

ResourceGroupName    : ResourceGroup01
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/prov
                       iders/Microsoft.Compute/images/Image02
Name                 : Image02
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}

ResourceGroupName    : ResourceGroup02
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup02/prov
                       iders/Microsoft.Compute/images/Image03
Name                 : Image03
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}
```

<span data-ttu-id="54601-113">Det här kommandot får egenskaperna för alla bilder under prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="54601-113">This command gets the properties of all images under the subscription.</span></span>

### <span data-ttu-id="54601-114">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="54601-114">Example 4</span></span>
```
PS C:\> Get-AzImage -Name "Image*"

ResourceGroupName    : ResourceGroup01
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/prov
                       iders/Microsoft.Compute/images/Image01
Name                 : Image01
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}

ResourceGroupName    : ResourceGroup01
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/prov
                       iders/Microsoft.Compute/images/Image02
Name                 : Image02
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}

ResourceGroupName    : ResourceGroup02
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup02/prov
                       iders/Microsoft.Compute/images/Image03
Name                 : Image03
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}
```

<span data-ttu-id="54601-115">Det här kommandot får egenskaperna för alla bilder under prenumerationen som börjar med "bild".</span><span class="sxs-lookup"><span data-stu-id="54601-115">This command gets the properties of all images under the subscription that start with "Image".</span></span>

## <span data-ttu-id="54601-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="54601-116">PARAMETERS</span></span>

### <span data-ttu-id="54601-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54601-117">-DefaultProfile</span></span>
<span data-ttu-id="54601-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="54601-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54601-119">-Expandera</span><span class="sxs-lookup"><span data-stu-id="54601-119">-Expand</span></span>
<span data-ttu-id="54601-120">Anger frågan expandera uttryck.</span><span class="sxs-lookup"><span data-stu-id="54601-120">Specifies the expand expression query.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54601-121">-ImageName</span><span class="sxs-lookup"><span data-stu-id="54601-121">-ImageName</span></span>
<span data-ttu-id="54601-122">Anger namnet på en bild.</span><span class="sxs-lookup"><span data-stu-id="54601-122">Specifies the name of an image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="54601-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54601-123">-ResourceGroupName</span></span>
<span data-ttu-id="54601-124">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="54601-124">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="54601-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54601-125">CommonParameters</span></span>
<span data-ttu-id="54601-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54601-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54601-127">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="54601-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54601-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="54601-128">INPUTS</span></span>

### <span data-ttu-id="54601-129">System. String</span><span class="sxs-lookup"><span data-stu-id="54601-129">System.String</span></span>

## <span data-ttu-id="54601-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="54601-130">OUTPUTS</span></span>

### <span data-ttu-id="54601-131">Microsoft. Azure. commands. Compute. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="54601-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="54601-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="54601-132">NOTES</span></span>

## <span data-ttu-id="54601-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="54601-133">RELATED LINKS</span></span>

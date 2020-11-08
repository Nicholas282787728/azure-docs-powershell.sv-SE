---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: F46041A3-355F-4449-B582-4D2F7314CA05
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmextensionimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImage.md
ms.openlocfilehash: 83d54f9c0b47db5dc718d273b1a1760ab319a666
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090621"
---
# <span data-ttu-id="365b2-101">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="365b2-101">Get-AzVMExtensionImage</span></span>

## <span data-ttu-id="365b2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="365b2-102">SYNOPSIS</span></span>
<span data-ttu-id="365b2-103">Hämtar alla versioner för ett Azure-tillägg.</span><span class="sxs-lookup"><span data-stu-id="365b2-103">Gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="365b2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="365b2-104">SYNTAX</span></span>

```
Get-AzVMExtensionImage -Location <String> -PublisherName <String> -Type <String> [-FilterExpression <String>]
 [-Version <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="365b2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="365b2-105">DESCRIPTION</span></span>
<span data-ttu-id="365b2-106">Cmdleten **Get-AzVMExtensionImage** hämtar alla versioner av ett Azure-tillägg.</span><span class="sxs-lookup"><span data-stu-id="365b2-106">The **Get-AzVMExtensionImage** cmdlet gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="365b2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="365b2-107">EXAMPLES</span></span>

### <span data-ttu-id="365b2-108">Exempel 1: Hämta versionerna av en tilläggs bild</span><span class="sxs-lookup"><span data-stu-id="365b2-108">Example 1: Get the versions of an extension image</span></span>
```
PS C:\> Get-AzVMExtensionImage -Location "West US" -PublisherName "Chef.Bootstrap.WindowsAzure" -Type "ChefClient"

Id               : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/westus/Pub
                   lishers/Chef.Bootstrap.WindowsAzure/ArtifactTypes/VMExtension/Types/ChefClient/Versions/11.18.6.2
Location         : westus
PublisherName    : Chef.Bootstrap.WindowsAzure
Type             : ChefClient
Version          : 11.18.6.2
FilterExpression :

Id               : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/westus/Pub
                   lishers/Chef.Bootstrap.WindowsAzure/ArtifactTypes/VMExtension/Types/ChefClient/Versions/1207.12.3.0
Location         : westus
PublisherName    : Chef.Bootstrap.WindowsAzure
Type             : ChefClient
Version          : 1207.12.3.0
FilterExpression :

Id               : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/westus/Pub
                   lishers/Chef.Bootstrap.WindowsAzure/ArtifactTypes/VMExtension/Types/ChefClient/Versions/1210.12.109.
                   1004
Location         : westus
PublisherName    : Chef.Bootstrap.WindowsAzure
Type             : ChefClient
Version          : 1210.12.109.1004
FilterExpression :
```

<span data-ttu-id="365b2-109">Det här kommandot får alla versioner av tilläggs bilden för den angivna platsen, utgivaren och typen.</span><span class="sxs-lookup"><span data-stu-id="365b2-109">This command gets all the versions of the extension image for the specified location, publisher, and type.</span></span>

### <span data-ttu-id="365b2-110">Exempel 2: Hämta versionerna av en tilläggs bild med filter över version</span><span class="sxs-lookup"><span data-stu-id="365b2-110">Example 2: Get the versions of an extension image with filter over version</span></span>
```
PS C:\> Get-AzVMExtensionImage -Location "West US" -PublisherName "Chef.Bootstrap.WindowsAzure" -Type "ChefClient" -Version 12*

Id               : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/westus/Pub
                   lishers/Chef.Bootstrap.WindowsAzure/ArtifactTypes/VMExtension/Types/ChefClient/Versions/1207.12.3.0
Location         : westus
PublisherName    : Chef.Bootstrap.WindowsAzure
Type             : ChefClient
Version          : 1207.12.3.0
FilterExpression :

Id               : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/westus/Pub
                   lishers/Chef.Bootstrap.WindowsAzure/ArtifactTypes/VMExtension/Types/ChefClient/Versions/1210.12.109.
                   1004
Location         : westus
PublisherName    : Chef.Bootstrap.WindowsAzure
Type             : ChefClient
Version          : 1210.12.109.1004
FilterExpression :
```

<span data-ttu-id="365b2-111">Det här kommandot får alla versioner av tilläggs bilden för den angivna platsen, den andra typen och versionen som börjar med 12.</span><span class="sxs-lookup"><span data-stu-id="365b2-111">This command gets all the versions of the extension image for the specified location, publisher, type, and version starting with 12.</span></span>

### <span data-ttu-id="365b2-112">Exempel 3: Hämta versionerna av en tilläggs bild med filter över version</span><span class="sxs-lookup"><span data-stu-id="365b2-112">Example 3: Get the versions of an extension image with filter over version</span></span>
```
PS C:\> Get-AzVMExtensionImage -Location "West US" -PublisherName "Chef.Bootstrap.WindowsAzure" -Type "ChefClient" -Version 1207.12.3.0

Id                         : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/
                             westus/Publishers/Chef.Bootstrap.WindowsAzure/ArtifactTypes/VMExtension/Types/ChefClient/V
                             ersions/1207.12.3.0
Location                   : westus
PublisherName              : Chef.Bootstrap.WindowsAzure
Type                       : ChefClient
Version                    : 1207.12.3.0
FilterExpression           :
Name                       :
HandlerSchema              :
OperatingSystem            : Windows
ComputeRole                : IaaS
SupportsMultipleExtensions : False
VMScaleSetEnabled          : False
```

<span data-ttu-id="365b2-113">Med det här kommandot får du alla versioner av tilläggs bilden för den angivna platsen, Publisher, typ och version.</span><span class="sxs-lookup"><span data-stu-id="365b2-113">This command gets all the versions of the extension image for the specified location, publisher, type, and version.</span></span>

## <span data-ttu-id="365b2-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="365b2-114">PARAMETERS</span></span>

### <span data-ttu-id="365b2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="365b2-115">-DefaultProfile</span></span>
<span data-ttu-id="365b2-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="365b2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="365b2-117">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="365b2-117">-FilterExpression</span></span>
<span data-ttu-id="365b2-118">Anger ett filter uttryck.</span><span class="sxs-lookup"><span data-stu-id="365b2-118">Specifies a filter expression.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="365b2-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="365b2-119">-Location</span></span>
<span data-ttu-id="365b2-120">Anger platsen för ett tillägg.</span><span class="sxs-lookup"><span data-stu-id="365b2-120">Specifies the location of an extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="365b2-121">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="365b2-121">-PublisherName</span></span>
<span data-ttu-id="365b2-122">Anger namnet på en förlängnings utgivare.</span><span class="sxs-lookup"><span data-stu-id="365b2-122">Specifies the name of an extension publisher.</span></span>
<span data-ttu-id="365b2-123">Använd Get-AzVMImagePublisher cmdlet för att få en förlängnings utgivare.</span><span class="sxs-lookup"><span data-stu-id="365b2-123">To obtain an extension publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="365b2-124">– Skriv</span><span class="sxs-lookup"><span data-stu-id="365b2-124">-Type</span></span>
<span data-ttu-id="365b2-125">Anger typen av tillägget.</span><span class="sxs-lookup"><span data-stu-id="365b2-125">Specifies the type of the extension.</span></span>
<span data-ttu-id="365b2-126">För att få en tilläggs typ, Använd cmdleten Get-AzVMExtensionImageType.</span><span class="sxs-lookup"><span data-stu-id="365b2-126">To obtain an extension type, use the Get-AzVMExtensionImageType cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="365b2-127">-Version</span><span class="sxs-lookup"><span data-stu-id="365b2-127">-Version</span></span>
<span data-ttu-id="365b2-128">Anger vilken version av tillägget som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="365b2-128">Specifies the version of the extension that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="365b2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="365b2-129">CommonParameters</span></span>
<span data-ttu-id="365b2-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="365b2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="365b2-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="365b2-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="365b2-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="365b2-132">INPUTS</span></span>

### <span data-ttu-id="365b2-133">System. String</span><span class="sxs-lookup"><span data-stu-id="365b2-133">System.String</span></span>

## <span data-ttu-id="365b2-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="365b2-134">OUTPUTS</span></span>

### <span data-ttu-id="365b2-135">Microsoft. Azure. commands. Compute. Models. PSVirtualMachineExtensionImage</span><span class="sxs-lookup"><span data-stu-id="365b2-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImage</span></span>

### <span data-ttu-id="365b2-136">Microsoft. Azure. commands. Compute. Models. PSVirtualMachineExtensionImageDetails</span><span class="sxs-lookup"><span data-stu-id="365b2-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageDetails</span></span>

## <span data-ttu-id="365b2-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="365b2-137">NOTES</span></span>

## <span data-ttu-id="365b2-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="365b2-138">RELATED LINKS</span></span>

[<span data-ttu-id="365b2-139">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="365b2-139">Get-AzVMExtensionImageType</span></span>](./Get-AzVMExtensionImageType.md)

[<span data-ttu-id="365b2-140">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="365b2-140">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="365b2-141">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="365b2-141">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)



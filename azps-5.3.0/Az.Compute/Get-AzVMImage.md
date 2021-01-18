---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D5254218-8B3B-4DE2-9480-D65EE5483018
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImage.md
ms.openlocfilehash: 350e03d6e238eb0cf1aa6b27da6b9a321603a664
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98526951"
---
# <span data-ttu-id="9cff8-101">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="9cff8-101">Get-AzVMImage</span></span>

## <span data-ttu-id="9cff8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9cff8-102">SYNOPSIS</span></span>
<span data-ttu-id="9cff8-103">Får alla versioner av en VMImage.</span><span class="sxs-lookup"><span data-stu-id="9cff8-103">Gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="9cff8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9cff8-104">SYNTAX</span></span>

### <span data-ttu-id="9cff8-105">ListVMImage</span><span class="sxs-lookup"><span data-stu-id="9cff8-105">ListVMImage</span></span>
```
Get-AzVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> [-Top <Int32>]
 [-OrderBy <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9cff8-106">GetVMImageDetail</span><span class="sxs-lookup"><span data-stu-id="9cff8-106">GetVMImageDetail</span></span>
```
Get-AzVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> -Version <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9cff8-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9cff8-107">DESCRIPTION</span></span>
<span data-ttu-id="9cff8-108">Cmdleten **Get-AzVMImage** får alla versioner av en VMImage.</span><span class="sxs-lookup"><span data-stu-id="9cff8-108">The **Get-AzVMImage** cmdlet gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="9cff8-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9cff8-109">EXAMPLES</span></span>

### <span data-ttu-id="9cff8-110">Exempel 1: skaffa VMImage-objekt</span><span class="sxs-lookup"><span data-stu-id="9cff8-110">Example 1: Get VMImage objects</span></span>
```
PS C:\> Get-AzVMImage -Location "Central US" -PublisherName "MicrosoftWindowsServer" -Offer "windowsserver" -Skus "2012-R2-Datacenter"

Version        FilterExpression Skus               Offer         PublisherName          Location  Id
-------        ---------------- ----               -----         -------------          --------  --
4.127.20180315                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180510                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180815                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180912                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20181010                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20181125                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20190104                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20190115                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20190204                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20190218                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
```

<span data-ttu-id="9cff8-111">Det här kommandot får alla versioner av VMImage som matchar de angivna värdena.</span><span class="sxs-lookup"><span data-stu-id="9cff8-111">This command gets all the versions of VMImage that match the specified values.</span></span>

### <span data-ttu-id="9cff8-112">Exempel 2: skaffa VMImage-objekt</span><span class="sxs-lookup"><span data-stu-id="9cff8-112">Example 2: Get VMImage object</span></span>
```
PS C:\> Get-AzVMImage -Location "Central US" -PublisherName "MicrosoftWindowsServer" -Offer "windowsserver" -Skus "2012-R2-Datacenter" -Version 4.127.20180315

Id               : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/centralus/
                   Publishers/MicrosoftWindowsServer/ArtifactTypes/VMImage/Offers/windowsserver/Skus/2012-R2-Datacenter
                   /Versions/4.127.20180315
Location         : centralus
PublisherName    : MicrosoftWindowsServer
Offer            : windowsserver
Skus             : 2012-R2-Datacenter
Version          : 4.127.20180315
FilterExpression :
Name             : 4.127.20180315
OSDiskImage      : {
                     "operatingSystem": "Windows"
                   }
PurchasePlan     : null
DataDiskImages   : []
```

<span data-ttu-id="9cff8-113">Det här kommandot får en specifik version av VMImage som matchar de angivna värdena.</span><span class="sxs-lookup"><span data-stu-id="9cff8-113">This command gets a specific version of VMImage that matches the specified values.</span></span>

### <span data-ttu-id="9cff8-114">Exempel 3: skaffa VMImage-objekt</span><span class="sxs-lookup"><span data-stu-id="9cff8-114">Example 3: Get VMImage objects</span></span>
```
PS C:\> Get-AzVMImage -Location "Central US" -PublisherName "MicrosoftWindowsServer" -Offer "windowsserver" -Skus "2012-R2-Datacenter" -Version 4.127.2018*

Version        FilterExpression Skus               Offer         PublisherName          Location  Id
-------        ---------------- ----               -----         -------------          --------  --
4.127.20180315                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180510                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180815                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180912                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20181010                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20181125                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
```

<span data-ttu-id="9cff8-115">Det här kommandot får alla versioner av VMImage som matchar de angivna värdena med filtrering över version.</span><span class="sxs-lookup"><span data-stu-id="9cff8-115">This command gets all the versions of VMImage that match the specified values with filtering over version.</span></span>

## <span data-ttu-id="9cff8-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9cff8-116">PARAMETERS</span></span>

### <span data-ttu-id="9cff8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cff8-117">-DefaultProfile</span></span>
<span data-ttu-id="9cff8-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9cff8-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9cff8-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="9cff8-119">-Location</span></span>
<span data-ttu-id="9cff8-120">Anger platsen för en VMImage.</span><span class="sxs-lookup"><span data-stu-id="9cff8-120">Specifies the location of a VMImage.</span></span>

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

### <span data-ttu-id="9cff8-121">-Ge</span><span class="sxs-lookup"><span data-stu-id="9cff8-121">-Offer</span></span>
<span data-ttu-id="9cff8-122">Anger typen av VMImage-offer.</span><span class="sxs-lookup"><span data-stu-id="9cff8-122">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="9cff8-123">För att få ett bild utbud, Använd cmdleten Get-AzVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="9cff8-123">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="9cff8-124">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="9cff8-124">-OrderBy</span></span>
<span data-ttu-id="9cff8-125">Anger ordningen på resultatet som returneras.</span><span class="sxs-lookup"><span data-stu-id="9cff8-125">Specifies the order of the results returned.</span></span> <span data-ttu-id="9cff8-126">Formaterad som en OData-fråga.</span><span class="sxs-lookup"><span data-stu-id="9cff8-126">Formatted as an OData query.</span></span>

```yaml
Type: System.String
Parameter Sets: ListVMImage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cff8-127">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="9cff8-127">-PublisherName</span></span>
<span data-ttu-id="9cff8-128">Anger utgivaren av en VMImage.</span><span class="sxs-lookup"><span data-stu-id="9cff8-128">Specifies the publisher of a VMImage.</span></span>
<span data-ttu-id="9cff8-129">Använd Get-AzVMImagePublisher cmdlet för att få en bild utgivare.</span><span class="sxs-lookup"><span data-stu-id="9cff8-129">To obtain an image publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="9cff8-130">-SKU: er</span><span class="sxs-lookup"><span data-stu-id="9cff8-130">-Skus</span></span>
<span data-ttu-id="9cff8-131">Anger en VMImage-SKU.</span><span class="sxs-lookup"><span data-stu-id="9cff8-131">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="9cff8-132">För att skaffa en SKU, Använd cmdleten Get-AzVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="9cff8-132">To obtain an SKU, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="9cff8-133">-Överst</span><span class="sxs-lookup"><span data-stu-id="9cff8-133">-Top</span></span>
<span data-ttu-id="9cff8-134">Anger maximalt antal virtuella dator bilder som returneras.</span><span class="sxs-lookup"><span data-stu-id="9cff8-134">Specifies the maximum number of virtual machine images returned.</span></span> 

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ListVMImage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cff8-135">-Version</span><span class="sxs-lookup"><span data-stu-id="9cff8-135">-Version</span></span>
<span data-ttu-id="9cff8-136">Anger versionen för VMImage.</span><span class="sxs-lookup"><span data-stu-id="9cff8-136">Specifies the version of the VMImage.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVMImageDetail
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cff8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cff8-137">CommonParameters</span></span>
<span data-ttu-id="9cff8-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cff8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cff8-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9cff8-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cff8-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9cff8-140">INPUTS</span></span>

### <span data-ttu-id="9cff8-141">System. String</span><span class="sxs-lookup"><span data-stu-id="9cff8-141">System.String</span></span>

## <span data-ttu-id="9cff8-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9cff8-142">OUTPUTS</span></span>

### <span data-ttu-id="9cff8-143">Microsoft. Azure. commands. Compute. Models. PSVirtualMachineImage</span><span class="sxs-lookup"><span data-stu-id="9cff8-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImage</span></span>

### <span data-ttu-id="9cff8-144">Microsoft. Azure. commands. Compute. Models. PSVirtualMachineImageDetail</span><span class="sxs-lookup"><span data-stu-id="9cff8-144">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageDetail</span></span>

## <span data-ttu-id="9cff8-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9cff8-145">NOTES</span></span>

## <span data-ttu-id="9cff8-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9cff8-146">RELATED LINKS</span></span>

[<span data-ttu-id="9cff8-147">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="9cff8-147">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="9cff8-148">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="9cff8-148">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="9cff8-149">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="9cff8-149">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="9cff8-150">Spara – AzVMImage</span><span class="sxs-lookup"><span data-stu-id="9cff8-150">Save-AzVMImage</span></span>](./Save-AzVMImage.md)



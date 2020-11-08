---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D5254218-8B3B-4DE2-9480-D65EE5483018
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImage.md
ms.openlocfilehash: d5fd6e6dea5af9ed3d8bc02e69f155e74a4bb3f5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090611"
---
# <span data-ttu-id="c543d-101">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="c543d-101">Get-AzVMImage</span></span>

## <span data-ttu-id="c543d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c543d-102">SYNOPSIS</span></span>
<span data-ttu-id="c543d-103">Får alla versioner av en VMImage.</span><span class="sxs-lookup"><span data-stu-id="c543d-103">Gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="c543d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c543d-104">SYNTAX</span></span>

### <span data-ttu-id="c543d-105">ListVMImage</span><span class="sxs-lookup"><span data-stu-id="c543d-105">ListVMImage</span></span>
```
Get-AzVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String>
 [-FilterExpression <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c543d-106">GetVMImageDetail</span><span class="sxs-lookup"><span data-stu-id="c543d-106">GetVMImageDetail</span></span>
```
Get-AzVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> -Version <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c543d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c543d-107">DESCRIPTION</span></span>
<span data-ttu-id="c543d-108">Cmdleten **Get-AzVMImage** får alla versioner av en VMImage.</span><span class="sxs-lookup"><span data-stu-id="c543d-108">The **Get-AzVMImage** cmdlet gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="c543d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c543d-109">EXAMPLES</span></span>

### <span data-ttu-id="c543d-110">Exempel 1: skaffa VMImage-objekt</span><span class="sxs-lookup"><span data-stu-id="c543d-110">Example 1: Get VMImage objects</span></span>
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

<span data-ttu-id="c543d-111">Det här kommandot får alla versioner av VMImage som matchar de angivna värdena.</span><span class="sxs-lookup"><span data-stu-id="c543d-111">This command gets all the versions of VMImage that match the specified values.</span></span>

### <span data-ttu-id="c543d-112">Exempel 2: skaffa VMImage-objekt</span><span class="sxs-lookup"><span data-stu-id="c543d-112">Example 2: Get VMImage object</span></span>
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

<span data-ttu-id="c543d-113">Det här kommandot får en specifik version av VMImage som matchar de angivna värdena.</span><span class="sxs-lookup"><span data-stu-id="c543d-113">This command gets a specific version of VMImage that matches the specified values.</span></span>

### <span data-ttu-id="c543d-114">Exempel 3: skaffa VMImage-objekt</span><span class="sxs-lookup"><span data-stu-id="c543d-114">Example 3: Get VMImage objects</span></span>
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

<span data-ttu-id="c543d-115">Det här kommandot får alla versioner av VMImage som matchar de angivna värdena med filtrering över version.</span><span class="sxs-lookup"><span data-stu-id="c543d-115">This command gets all the versions of VMImage that match the specified values with filtering over version.</span></span>

## <span data-ttu-id="c543d-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c543d-116">PARAMETERS</span></span>

### <span data-ttu-id="c543d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c543d-117">-DefaultProfile</span></span>
<span data-ttu-id="c543d-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c543d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c543d-119">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="c543d-119">-FilterExpression</span></span>
<span data-ttu-id="c543d-120">Anger ett filter uttryck.</span><span class="sxs-lookup"><span data-stu-id="c543d-120">Specifies a filter expression.</span></span>

```yaml
Type: System.String
Parameter Sets: ListVMImage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c543d-121">-Plats</span><span class="sxs-lookup"><span data-stu-id="c543d-121">-Location</span></span>
<span data-ttu-id="c543d-122">Anger platsen för en VMImage.</span><span class="sxs-lookup"><span data-stu-id="c543d-122">Specifies the location of a VMImage.</span></span>

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

### <span data-ttu-id="c543d-123">-Ge</span><span class="sxs-lookup"><span data-stu-id="c543d-123">-Offer</span></span>
<span data-ttu-id="c543d-124">Anger typen av VMImage-offer.</span><span class="sxs-lookup"><span data-stu-id="c543d-124">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="c543d-125">För att få ett bild utbud, Använd cmdleten Get-AzVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="c543d-125">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="c543d-126">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="c543d-126">-PublisherName</span></span>
<span data-ttu-id="c543d-127">Anger utgivaren av en VMImage.</span><span class="sxs-lookup"><span data-stu-id="c543d-127">Specifies the publisher of a VMImage.</span></span>
<span data-ttu-id="c543d-128">Använd Get-AzVMImagePublisher cmdlet för att få en bild utgivare.</span><span class="sxs-lookup"><span data-stu-id="c543d-128">To obtain an image publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="c543d-129">-SKU: er</span><span class="sxs-lookup"><span data-stu-id="c543d-129">-Skus</span></span>
<span data-ttu-id="c543d-130">Anger en VMImage-SKU.</span><span class="sxs-lookup"><span data-stu-id="c543d-130">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="c543d-131">För att skaffa en SKU, Använd cmdleten Get-AzVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="c543d-131">To obtain an SKU, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="c543d-132">-Version</span><span class="sxs-lookup"><span data-stu-id="c543d-132">-Version</span></span>
<span data-ttu-id="c543d-133">Anger versionen för VMImage.</span><span class="sxs-lookup"><span data-stu-id="c543d-133">Specifies the version of the VMImage.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVMImageDetail
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="c543d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c543d-134">CommonParameters</span></span>
<span data-ttu-id="c543d-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c543d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c543d-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c543d-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c543d-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c543d-137">INPUTS</span></span>

### <span data-ttu-id="c543d-138">System. String</span><span class="sxs-lookup"><span data-stu-id="c543d-138">System.String</span></span>

## <span data-ttu-id="c543d-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c543d-139">OUTPUTS</span></span>

### <span data-ttu-id="c543d-140">Microsoft. Azure. commands. Compute. Models. PSVirtualMachineImage</span><span class="sxs-lookup"><span data-stu-id="c543d-140">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImage</span></span>

### <span data-ttu-id="c543d-141">Microsoft. Azure. commands. Compute. Models. PSVirtualMachineImageDetail</span><span class="sxs-lookup"><span data-stu-id="c543d-141">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageDetail</span></span>

## <span data-ttu-id="c543d-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c543d-142">NOTES</span></span>

## <span data-ttu-id="c543d-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c543d-143">RELATED LINKS</span></span>

[<span data-ttu-id="c543d-144">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="c543d-144">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="c543d-145">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="c543d-145">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="c543d-146">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="c543d-146">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="c543d-147">Spara – AzVMImage</span><span class="sxs-lookup"><span data-stu-id="c543d-147">Save-AzVMImage</span></span>](./Save-AzVMImage.md)



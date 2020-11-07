---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: F46041A3-355F-4449-B582-4D2F7314CA05
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmextensionimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMExtensionImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMExtensionImage.md
ms.openlocfilehash: 1864b4c2dcbd4b3d9934ffb15c54fae18082c920
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93925173"
---
# <span data-ttu-id="77e42-101">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="77e42-101">Get-AzVMExtensionImage</span></span>

## <span data-ttu-id="77e42-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="77e42-102">SYNOPSIS</span></span>
<span data-ttu-id="77e42-103">Hämtar alla versioner för ett Azure-tillägg.</span><span class="sxs-lookup"><span data-stu-id="77e42-103">Gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="77e42-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="77e42-104">SYNTAX</span></span>

```
Get-AzVMExtensionImage -Location <String> -PublisherName <String> -Type <String>
 [-FilterExpression <String>] [-Version <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="77e42-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="77e42-105">DESCRIPTION</span></span>
<span data-ttu-id="77e42-106">Cmdleten **Get-AzVMExtensionImage** hämtar alla versioner av ett Azure-tillägg.</span><span class="sxs-lookup"><span data-stu-id="77e42-106">The **Get-AzVMExtensionImage** cmdlet gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="77e42-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="77e42-107">EXAMPLES</span></span>

### <span data-ttu-id="77e42-108">Exempel 1: Hämta versionerna av en tilläggs bild</span><span class="sxs-lookup"><span data-stu-id="77e42-108">Example 1: Get the versions of an extension image</span></span>
```
PS C:\> Get-AzVMExtensionImage -Location "Central US" -PublisherName "Fabrikam" -Type "FabrikamEndpointProtection"
```

<span data-ttu-id="77e42-109">Det här kommandot får alla versioner av tilläggs bilden för den angivna platsen, utgivaren och typen.</span><span class="sxs-lookup"><span data-stu-id="77e42-109">This command gets all the versions of the extension image for the specified location, publisher, and type.</span></span>

## <span data-ttu-id="77e42-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="77e42-110">PARAMETERS</span></span>

### <span data-ttu-id="77e42-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77e42-111">-DefaultProfile</span></span>
<span data-ttu-id="77e42-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="77e42-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="77e42-113">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="77e42-113">-FilterExpression</span></span>
<span data-ttu-id="77e42-114">Anger ett filter uttryck.</span><span class="sxs-lookup"><span data-stu-id="77e42-114">Specifies a filter expression.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77e42-115">-Plats</span><span class="sxs-lookup"><span data-stu-id="77e42-115">-Location</span></span>
<span data-ttu-id="77e42-116">Anger platsen för ett tillägg.</span><span class="sxs-lookup"><span data-stu-id="77e42-116">Specifies the location of an extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77e42-117">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="77e42-117">-PublisherName</span></span>
<span data-ttu-id="77e42-118">Anger namnet på en förlängnings utgivare.</span><span class="sxs-lookup"><span data-stu-id="77e42-118">Specifies the name of an extension publisher.</span></span>
<span data-ttu-id="77e42-119">Använd Get-AzVMImagePublisher cmdlet för att få en förlängnings utgivare.</span><span class="sxs-lookup"><span data-stu-id="77e42-119">To obtain an extension publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77e42-120">– Skriv</span><span class="sxs-lookup"><span data-stu-id="77e42-120">-Type</span></span>
<span data-ttu-id="77e42-121">Anger typen av tillägget.</span><span class="sxs-lookup"><span data-stu-id="77e42-121">Specifies the type of the extension.</span></span>
<span data-ttu-id="77e42-122">För att få en tilläggs typ, Använd cmdleten Get-AzVMExtensionImageType.</span><span class="sxs-lookup"><span data-stu-id="77e42-122">To obtain an extension type, use the Get-AzVMExtensionImageType cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77e42-123">-Version</span><span class="sxs-lookup"><span data-stu-id="77e42-123">-Version</span></span>
<span data-ttu-id="77e42-124">Anger vilken version av tillägget som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="77e42-124">Specifies the version of the extension that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77e42-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77e42-125">CommonParameters</span></span>
<span data-ttu-id="77e42-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77e42-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77e42-127">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77e42-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77e42-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="77e42-128">INPUTS</span></span>

### <span data-ttu-id="77e42-129">Ingen</span><span class="sxs-lookup"><span data-stu-id="77e42-129">None</span></span>
<span data-ttu-id="77e42-130">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="77e42-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="77e42-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="77e42-131">OUTPUTS</span></span>

### <span data-ttu-id="77e42-132">Microsoft. Azure. commands. Compute. Models. PSVirtualMachineExtensionImage</span><span class="sxs-lookup"><span data-stu-id="77e42-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImage</span></span>

### <span data-ttu-id="77e42-133">Microsoft. Azure. commands. Compute. Models. PSVirtualMachineExtensionImageDetails</span><span class="sxs-lookup"><span data-stu-id="77e42-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageDetails</span></span>

## <span data-ttu-id="77e42-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="77e42-134">NOTES</span></span>

## <span data-ttu-id="77e42-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="77e42-135">RELATED LINKS</span></span>

[<span data-ttu-id="77e42-136">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="77e42-136">Get-AzVMExtensionImageType</span></span>](./Get-AzVMExtensionImageType.md)

[<span data-ttu-id="77e42-137">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="77e42-137">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="77e42-138">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="77e42-138">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)



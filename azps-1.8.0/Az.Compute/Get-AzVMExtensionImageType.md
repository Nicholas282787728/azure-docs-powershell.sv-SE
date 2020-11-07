---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 45F35BDD-969E-4521-9E8D-3499A15434A6
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmextensionimagetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImageType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImageType.md
ms.openlocfilehash: 0e3c1a9113bf3872ca86227272e36abd67781b7b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754573"
---
# <span data-ttu-id="1afb2-101">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="1afb2-101">Get-AzVMExtensionImageType</span></span>

## <span data-ttu-id="1afb2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1afb2-102">SYNOPSIS</span></span>
<span data-ttu-id="1afb2-103">Hämtar typen av ett Azure-tillägg.</span><span class="sxs-lookup"><span data-stu-id="1afb2-103">Gets the type of an Azure extension.</span></span>

## <span data-ttu-id="1afb2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1afb2-104">SYNTAX</span></span>

```
Get-AzVMExtensionImageType -Location <String> -PublisherName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1afb2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1afb2-105">DESCRIPTION</span></span>
<span data-ttu-id="1afb2-106">Cmdleten **Get-AzVMExtensionImageType** hämtar typen av ett Azure-tillägg.</span><span class="sxs-lookup"><span data-stu-id="1afb2-106">The **Get-AzVMExtensionImageType** cmdlet gets the type of an Azure extension.</span></span>

## <span data-ttu-id="1afb2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1afb2-107">EXAMPLES</span></span>

### <span data-ttu-id="1afb2-108">Exempel 1: Hämta en bild av typen tillägg</span><span class="sxs-lookup"><span data-stu-id="1afb2-108">Example 1: Get an extension image type</span></span>
```
PS C:\> Get-AzVMExtensionImageType -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="1afb2-109">Det här kommandot får bild typen tillägg för angiven utgivare och plats.</span><span class="sxs-lookup"><span data-stu-id="1afb2-109">This command gets the extension image type for the specified publisher and location.</span></span>

## <span data-ttu-id="1afb2-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1afb2-110">PARAMETERS</span></span>

### <span data-ttu-id="1afb2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1afb2-111">-DefaultProfile</span></span>
<span data-ttu-id="1afb2-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1afb2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1afb2-113">-Plats</span><span class="sxs-lookup"><span data-stu-id="1afb2-113">-Location</span></span>
<span data-ttu-id="1afb2-114">Anger platsen för ett tillägg.</span><span class="sxs-lookup"><span data-stu-id="1afb2-114">Specifies the location of an extension.</span></span>
<span data-ttu-id="1afb2-115">Denna cmdlet får typen för ett tillägg på den plats som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="1afb2-115">This cmdlet gets the type for an extension at the location that this parameter specifies.</span></span>

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

### <span data-ttu-id="1afb2-116">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="1afb2-116">-PublisherName</span></span>
<span data-ttu-id="1afb2-117">Anger namnet på en utgivare av ett tillägg.</span><span class="sxs-lookup"><span data-stu-id="1afb2-117">Specifies the name of a publisher of an extension.</span></span>
<span data-ttu-id="1afb2-118">Använd Get-AzVMImagePublisher cmdlet för att få en förlängnings utgivare.</span><span class="sxs-lookup"><span data-stu-id="1afb2-118">To obtain an extension publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>
<span data-ttu-id="1afb2-119">Denna cmdlet får typen för ett tillägg från den utgivare som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="1afb2-119">This cmdlet gets the type for an extension from the publisher that this parameter specifies.</span></span>

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

### <span data-ttu-id="1afb2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1afb2-120">CommonParameters</span></span>
<span data-ttu-id="1afb2-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1afb2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1afb2-122">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1afb2-122">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1afb2-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1afb2-123">INPUTS</span></span>

### <span data-ttu-id="1afb2-124">System. String</span><span class="sxs-lookup"><span data-stu-id="1afb2-124">System.String</span></span>

## <span data-ttu-id="1afb2-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1afb2-125">OUTPUTS</span></span>

### <span data-ttu-id="1afb2-126">Microsoft. Azure. commands. Compute. Models. PSVirtualMachineExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="1afb2-126">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageType</span></span>

## <span data-ttu-id="1afb2-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1afb2-127">NOTES</span></span>

## <span data-ttu-id="1afb2-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1afb2-128">RELATED LINKS</span></span>

[<span data-ttu-id="1afb2-129">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="1afb2-129">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

[<span data-ttu-id="1afb2-130">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="1afb2-130">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)


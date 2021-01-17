---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 45F35BDD-969E-4521-9E8D-3499A15434A6
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmextensionimagetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImageType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImageType.md
ms.openlocfilehash: eb2c92b0efcbcd5333c600fe481e21752a96be9e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98399843"
---
# <span data-ttu-id="84661-101">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="84661-101">Get-AzVMExtensionImageType</span></span>

## <span data-ttu-id="84661-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="84661-102">SYNOPSIS</span></span>
<span data-ttu-id="84661-103">Hämtar typen av ett Azure-tillägg.</span><span class="sxs-lookup"><span data-stu-id="84661-103">Gets the type of an Azure extension.</span></span>

## <span data-ttu-id="84661-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="84661-104">SYNTAX</span></span>

```
Get-AzVMExtensionImageType -Location <String> -PublisherName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="84661-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="84661-105">DESCRIPTION</span></span>
<span data-ttu-id="84661-106">Cmdleten **Get-AzVMExtensionImageType** hämtar typen av ett Azure-tillägg.</span><span class="sxs-lookup"><span data-stu-id="84661-106">The **Get-AzVMExtensionImageType** cmdlet gets the type of an Azure extension.</span></span>

## <span data-ttu-id="84661-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="84661-107">EXAMPLES</span></span>

### <span data-ttu-id="84661-108">Exempel 1: Hämta en bild av typen tillägg</span><span class="sxs-lookup"><span data-stu-id="84661-108">Example 1: Get an extension image type</span></span>
```
PS C:\> Get-AzVMExtensionImageType -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="84661-109">Det här kommandot får bild typen tillägg för angiven utgivare och plats.</span><span class="sxs-lookup"><span data-stu-id="84661-109">This command gets the extension image type for the specified publisher and location.</span></span>

## <span data-ttu-id="84661-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="84661-110">PARAMETERS</span></span>

### <span data-ttu-id="84661-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84661-111">-DefaultProfile</span></span>
<span data-ttu-id="84661-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="84661-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84661-113">-Plats</span><span class="sxs-lookup"><span data-stu-id="84661-113">-Location</span></span>
<span data-ttu-id="84661-114">Anger platsen för ett tillägg.</span><span class="sxs-lookup"><span data-stu-id="84661-114">Specifies the location of an extension.</span></span>
<span data-ttu-id="84661-115">Denna cmdlet får typen för ett tillägg på den plats som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="84661-115">This cmdlet gets the type for an extension at the location that this parameter specifies.</span></span>

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

### <span data-ttu-id="84661-116">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="84661-116">-PublisherName</span></span>
<span data-ttu-id="84661-117">Anger namnet på en utgivare av ett tillägg.</span><span class="sxs-lookup"><span data-stu-id="84661-117">Specifies the name of a publisher of an extension.</span></span>
<span data-ttu-id="84661-118">Använd Get-AzVMImagePublisher cmdlet för att få en förlängnings utgivare.</span><span class="sxs-lookup"><span data-stu-id="84661-118">To obtain an extension publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>
<span data-ttu-id="84661-119">Denna cmdlet får typen för ett tillägg från den utgivare som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="84661-119">This cmdlet gets the type for an extension from the publisher that this parameter specifies.</span></span>

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

### <span data-ttu-id="84661-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84661-120">CommonParameters</span></span>
<span data-ttu-id="84661-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84661-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84661-122">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="84661-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84661-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="84661-123">INPUTS</span></span>

### <span data-ttu-id="84661-124">System. String</span><span class="sxs-lookup"><span data-stu-id="84661-124">System.String</span></span>

## <span data-ttu-id="84661-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="84661-125">OUTPUTS</span></span>

### <span data-ttu-id="84661-126">Microsoft. Azure. commands. Compute. Models. PSVirtualMachineExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="84661-126">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageType</span></span>

## <span data-ttu-id="84661-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="84661-127">NOTES</span></span>

## <span data-ttu-id="84661-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="84661-128">RELATED LINKS</span></span>

[<span data-ttu-id="84661-129">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="84661-129">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

[<span data-ttu-id="84661-130">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="84661-130">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)



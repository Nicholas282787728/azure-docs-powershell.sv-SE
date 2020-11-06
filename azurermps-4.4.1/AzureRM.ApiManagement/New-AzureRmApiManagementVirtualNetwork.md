---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: FB5E4ED2-8EF3-462F-A053-7EC82C767E8D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementVirtualNetwork.md
ms.openlocfilehash: 42213ddd4a7780b4d69b357c4b801df34aa9aca4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573774"
---
# <span data-ttu-id="82ff1-101">New-AzureRmApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="82ff1-101">New-AzureRmApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="82ff1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="82ff1-102">SYNOPSIS</span></span>
<span data-ttu-id="82ff1-103">Skapar en instans av PsApiManagementVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="82ff1-103">Creates an instance of PsApiManagementVirtualNetwork.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82ff1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="82ff1-104">SYNTAX</span></span>

```
New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82ff1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="82ff1-105">DESCRIPTION</span></span>
<span data-ttu-id="82ff1-106">**New-AzureRmApiManagementVirtualNetwork** cmdlet är ett hjälp kommando för att skapa en instans av **PsApiManagementVirtualNetwork**.</span><span class="sxs-lookup"><span data-stu-id="82ff1-106">The **New-AzureRmApiManagementVirtualNetwork** cmdlet is a helper command to create an instance of **PsApiManagementVirtualNetwork**.</span></span>
<span data-ttu-id="82ff1-107">Det här kommandot används med cmdleten **set-AzureRMApiManagementVirtualNetworks** .</span><span class="sxs-lookup"><span data-stu-id="82ff1-107">This command is used with **Set-AzureRMApiManagementVirtualNetworks** cmdlet.</span></span>

## <span data-ttu-id="82ff1-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="82ff1-108">EXAMPLES</span></span>

### <span data-ttu-id="82ff1-109">Exempel 1: skapa ett virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="82ff1-109">Example 1: Create a virtual network</span></span>
```
PS C:\>$VirtualNetworks = @()
PS C:\> $VirtualNetworks += New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubtenName "ContosoNet" -VnetId "089D3F4D-B986-4DFD-9259-9112BA7A1F03"
PS C:\> Set-AzureRmApiManagementVirtualNetworks -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetworks $VirtualNetworks
```

<span data-ttu-id="82ff1-110">I det här exemplet skapas ett virtuellt nätverk och sedan anropas cmdleten **set-AzureRmApiManagementVirtualNetworks** .</span><span class="sxs-lookup"><span data-stu-id="82ff1-110">This example creates a virtual network and then calls the **Set-AzureRmApiManagementVirtualNetworks** cmdlet.</span></span>

## <span data-ttu-id="82ff1-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="82ff1-111">PARAMETERS</span></span>

### <span data-ttu-id="82ff1-112">-Plats</span><span class="sxs-lookup"><span data-stu-id="82ff1-112">-Location</span></span>
<span data-ttu-id="82ff1-113">Anger platsen för det virtuella nätverk där denna cmdlet skapar instansen.</span><span class="sxs-lookup"><span data-stu-id="82ff1-113">Specifies the location of the virtual network in which this cmdlet creates the instance.</span></span>

<span data-ttu-id="82ff1-114">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="82ff1-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="82ff1-115">Norra Central USA</span><span class="sxs-lookup"><span data-stu-id="82ff1-115">North Central US</span></span>
- <span data-ttu-id="82ff1-116">Södra centrala USA</span><span class="sxs-lookup"><span data-stu-id="82ff1-116">South Central US</span></span>
- <span data-ttu-id="82ff1-117">Central</span><span class="sxs-lookup"><span data-stu-id="82ff1-117">Central US</span></span>
- <span data-ttu-id="82ff1-118">Västeuropa</span><span class="sxs-lookup"><span data-stu-id="82ff1-118">West Europe</span></span>
- <span data-ttu-id="82ff1-119">Nord Europa</span><span class="sxs-lookup"><span data-stu-id="82ff1-119">North Europe</span></span>
- <span data-ttu-id="82ff1-120">Västra USA</span><span class="sxs-lookup"><span data-stu-id="82ff1-120">West US</span></span>
- <span data-ttu-id="82ff1-121">Östra USA</span><span class="sxs-lookup"><span data-stu-id="82ff1-121">East US</span></span>
- <span data-ttu-id="82ff1-122">Östra USA 2</span><span class="sxs-lookup"><span data-stu-id="82ff1-122">East US 2</span></span>
- <span data-ttu-id="82ff1-123">Östra Japan</span><span class="sxs-lookup"><span data-stu-id="82ff1-123">Japan East</span></span>
- <span data-ttu-id="82ff1-124">Västra Japan</span><span class="sxs-lookup"><span data-stu-id="82ff1-124">Japan West</span></span>
- <span data-ttu-id="82ff1-125">Brasilien, Syd</span><span class="sxs-lookup"><span data-stu-id="82ff1-125">Brazil South</span></span>
- <span data-ttu-id="82ff1-126">Sydostasien</span><span class="sxs-lookup"><span data-stu-id="82ff1-126">Southeast Asia</span></span>
- <span data-ttu-id="82ff1-127">Östasien</span><span class="sxs-lookup"><span data-stu-id="82ff1-127">East Asia</span></span>
- <span data-ttu-id="82ff1-128">Östra Australien</span><span class="sxs-lookup"><span data-stu-id="82ff1-128">Australia East</span></span>
- <span data-ttu-id="82ff1-129">Australien, sydöst</span><span class="sxs-lookup"><span data-stu-id="82ff1-129">Australia Southeast</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82ff1-130">-SubnetResourceId</span><span class="sxs-lookup"><span data-stu-id="82ff1-130">-SubnetResourceId</span></span>
<span data-ttu-id="82ff1-131">Anger det virtuella nätverkets ID för under nätet.</span><span class="sxs-lookup"><span data-stu-id="82ff1-131">Specifies the subnet resource ID of the virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82ff1-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82ff1-132">-DefaultProfile</span></span>
<span data-ttu-id="82ff1-133">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="82ff1-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="82ff1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82ff1-134">CommonParameters</span></span>
<span data-ttu-id="82ff1-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82ff1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82ff1-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82ff1-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82ff1-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="82ff1-137">INPUTS</span></span>

## <span data-ttu-id="82ff1-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="82ff1-138">OUTPUTS</span></span>

### <span data-ttu-id="82ff1-139">Microsoft. Azure. commands. ApiManagement. Models. PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="82ff1-139">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="82ff1-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="82ff1-140">NOTES</span></span>

## <span data-ttu-id="82ff1-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="82ff1-141">RELATED LINKS</span></span>


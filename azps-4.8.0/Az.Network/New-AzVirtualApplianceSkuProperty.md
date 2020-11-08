---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualapplianceskuproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSkuProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSkuProperty.md
ms.openlocfilehash: cfe9fb07854fcc5850e1c5f73f4da7fe43f172a8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259278"
---
# <span data-ttu-id="8937c-101">New-AzVirtualApplianceSkuProperty</span><span class="sxs-lookup"><span data-stu-id="8937c-101">New-AzVirtualApplianceSkuProperty</span></span>

## <span data-ttu-id="8937c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8937c-102">SYNOPSIS</span></span>
<span data-ttu-id="8937c-103">Definiera en virtuell enhet för nätverks enheter för resursen.</span><span class="sxs-lookup"><span data-stu-id="8937c-103">Define a Network Virtual Appliance sku for the resource.</span></span>

## <span data-ttu-id="8937c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8937c-104">SYNTAX</span></span>

```
New-AzVirtualApplianceSkuProperty -VendorName <String> -BundledScaleUnit <String> -MarketPlaceVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8937c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8937c-105">DESCRIPTION</span></span>
<span data-ttu-id="8937c-106">Med kommandot New-AzVirtualApplianceSkuProperties definierar du en SKU för nätverks resurser för virtuella enheter.</span><span class="sxs-lookup"><span data-stu-id="8937c-106">The New-AzVirtualApplianceSkuProperties command defines a Sku for Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="8937c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8937c-107">EXAMPLES</span></span>

### <span data-ttu-id="8937c-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8937c-108">Example 1</span></span>
```powershell
PS C:\> $var=New-AzVirtualApplianceSkuProperty -VendorName "barracudasdwanrelease" -BundledScaleUnit 1 -MarketPlaceVersion 'latest'
```

<span data-ttu-id="8937c-109">Skapa ett objekt för SKU-egenskaper för virtuella enheter som ska användas med New-AzNetworkVirtualAppliance-kommando.</span><span class="sxs-lookup"><span data-stu-id="8937c-109">Create a Virtual Appliance Sku Properties object to be used with New-AzNetworkVirtualAppliance command.</span></span> 

## <span data-ttu-id="8937c-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8937c-110">PARAMETERS</span></span>

### <span data-ttu-id="8937c-111">-BundledScaleUnit</span><span class="sxs-lookup"><span data-stu-id="8937c-111">-BundledScaleUnit</span></span>
<span data-ttu-id="8937c-112">Den buntade skalnings enheten.</span><span class="sxs-lookup"><span data-stu-id="8937c-112">The bundled scale unit.</span></span>

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

### <span data-ttu-id="8937c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8937c-113">-DefaultProfile</span></span>
<span data-ttu-id="8937c-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8937c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8937c-115">-MarketPlaceVersion</span><span class="sxs-lookup"><span data-stu-id="8937c-115">-MarketPlaceVersion</span></span>
<span data-ttu-id="8937c-116">Marknads plats versionen.</span><span class="sxs-lookup"><span data-stu-id="8937c-116">The market place version.</span></span>

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

### <span data-ttu-id="8937c-117">-Leverantörs namn</span><span class="sxs-lookup"><span data-stu-id="8937c-117">-VendorName</span></span>
<span data-ttu-id="8937c-118">Namnet på leverantören.</span><span class="sxs-lookup"><span data-stu-id="8937c-118">The name of the vendor.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8937c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8937c-119">CommonParameters</span></span>
<span data-ttu-id="8937c-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8937c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8937c-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8937c-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8937c-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8937c-122">INPUTS</span></span>

### <span data-ttu-id="8937c-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="8937c-123">None</span></span>

## <span data-ttu-id="8937c-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8937c-124">OUTPUTS</span></span>

### <span data-ttu-id="8937c-125">Microsoft. Azure. commands. Networks. Models. PSVirtualApplianceSkuProperties</span><span class="sxs-lookup"><span data-stu-id="8937c-125">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties</span></span>

## <span data-ttu-id="8937c-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8937c-126">NOTES</span></span>

## <span data-ttu-id="8937c-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8937c-127">RELATED LINKS</span></span>

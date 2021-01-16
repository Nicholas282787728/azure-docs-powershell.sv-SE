---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualapplianceskuproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSkuProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSkuProperty.md
ms.openlocfilehash: cfe9fb07854fcc5850e1c5f73f4da7fe43f172a8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98391515"
---
# <span data-ttu-id="4d9d1-101">New-AzVirtualApplianceSkuProperty</span><span class="sxs-lookup"><span data-stu-id="4d9d1-101">New-AzVirtualApplianceSkuProperty</span></span>

## <span data-ttu-id="4d9d1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4d9d1-102">SYNOPSIS</span></span>
<span data-ttu-id="4d9d1-103">Definiera en virtuell enhet för nätverks enheter för resursen.</span><span class="sxs-lookup"><span data-stu-id="4d9d1-103">Define a Network Virtual Appliance sku for the resource.</span></span>

## <span data-ttu-id="4d9d1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4d9d1-104">SYNTAX</span></span>

```
New-AzVirtualApplianceSkuProperty -VendorName <String> -BundledScaleUnit <String> -MarketPlaceVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d9d1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4d9d1-105">DESCRIPTION</span></span>
<span data-ttu-id="4d9d1-106">Med kommandot New-AzVirtualApplianceSkuProperties definierar du en SKU för nätverks resurser för virtuella enheter.</span><span class="sxs-lookup"><span data-stu-id="4d9d1-106">The New-AzVirtualApplianceSkuProperties command defines a Sku for Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="4d9d1-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4d9d1-107">EXAMPLES</span></span>

### <span data-ttu-id="4d9d1-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4d9d1-108">Example 1</span></span>
```powershell
PS C:\> $var=New-AzVirtualApplianceSkuProperty -VendorName "barracudasdwanrelease" -BundledScaleUnit 1 -MarketPlaceVersion 'latest'
```

<span data-ttu-id="4d9d1-109">Skapa ett objekt för SKU-egenskaper för virtuella enheter som ska användas med New-AzNetworkVirtualAppliance-kommando.</span><span class="sxs-lookup"><span data-stu-id="4d9d1-109">Create a Virtual Appliance Sku Properties object to be used with New-AzNetworkVirtualAppliance command.</span></span> 

## <span data-ttu-id="4d9d1-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4d9d1-110">PARAMETERS</span></span>

### <span data-ttu-id="4d9d1-111">-BundledScaleUnit</span><span class="sxs-lookup"><span data-stu-id="4d9d1-111">-BundledScaleUnit</span></span>
<span data-ttu-id="4d9d1-112">Den buntade skalnings enheten.</span><span class="sxs-lookup"><span data-stu-id="4d9d1-112">The bundled scale unit.</span></span>

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

### <span data-ttu-id="4d9d1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d9d1-113">-DefaultProfile</span></span>
<span data-ttu-id="4d9d1-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4d9d1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d9d1-115">-MarketPlaceVersion</span><span class="sxs-lookup"><span data-stu-id="4d9d1-115">-MarketPlaceVersion</span></span>
<span data-ttu-id="4d9d1-116">Marknads plats versionen.</span><span class="sxs-lookup"><span data-stu-id="4d9d1-116">The market place version.</span></span>

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

### <span data-ttu-id="4d9d1-117">-Leverantörs namn</span><span class="sxs-lookup"><span data-stu-id="4d9d1-117">-VendorName</span></span>
<span data-ttu-id="4d9d1-118">Namnet på leverantören.</span><span class="sxs-lookup"><span data-stu-id="4d9d1-118">The name of the vendor.</span></span>

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

### <span data-ttu-id="4d9d1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d9d1-119">CommonParameters</span></span>
<span data-ttu-id="4d9d1-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d9d1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d9d1-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4d9d1-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d9d1-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4d9d1-122">INPUTS</span></span>

### <span data-ttu-id="4d9d1-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="4d9d1-123">None</span></span>

## <span data-ttu-id="4d9d1-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4d9d1-124">OUTPUTS</span></span>

### <span data-ttu-id="4d9d1-125">Microsoft. Azure. commands. Networks. Models. PSVirtualApplianceSkuProperties</span><span class="sxs-lookup"><span data-stu-id="4d9d1-125">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties</span></span>

## <span data-ttu-id="4d9d1-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4d9d1-126">NOTES</span></span>

## <span data-ttu-id="4d9d1-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4d9d1-127">RELATED LINKS</span></span>

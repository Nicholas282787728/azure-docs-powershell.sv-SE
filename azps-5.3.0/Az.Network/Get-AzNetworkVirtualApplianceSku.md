---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkvirtualappliancesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualApplianceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualApplianceSku.md
ms.openlocfilehash: e38e489207267faf53bb790aaab65ad60c74c8b5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98422160"
---
# <span data-ttu-id="dea25-101">Get-AzNetworkVirtualApplianceSku</span><span class="sxs-lookup"><span data-stu-id="dea25-101">Get-AzNetworkVirtualApplianceSku</span></span>

## <span data-ttu-id="dea25-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dea25-102">SYNOPSIS</span></span>
<span data-ttu-id="dea25-103">Hämta eller lista tillgängliga virtuella nätverk enheter SKU: er i lagret.</span><span class="sxs-lookup"><span data-stu-id="dea25-103">Get or List available Network Virtual Appliance Skus in the inventory.</span></span>

## <span data-ttu-id="dea25-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dea25-104">SYNTAX</span></span>

```
Get-AzNetworkVirtualApplianceSku [-SkuName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dea25-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dea25-105">DESCRIPTION</span></span>
<span data-ttu-id="dea25-106">Get-AzNetworkVirtualApplianceSku hämtar eller visar tillgängliga virtuella nätverks enheter (SKU) i Microsoft Azure-inventeringen.</span><span class="sxs-lookup"><span data-stu-id="dea25-106">The Get-AzNetworkVirtualApplianceSku gets or lists available Network Virtual Appliance Skus in the Microsoft Azure inventory.</span></span>

## <span data-ttu-id="dea25-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dea25-107">EXAMPLES</span></span>

### <span data-ttu-id="dea25-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="dea25-108">Example 1</span></span>
```powershell
PS C:\> Get-AzNetworkVirtualApplianceSku -SkuName barracudasdwanrelease                                                                                                                        

Vendor              : barracudasdwanrelease
AvailableVersions   : {8.1.0038301, latest}
AvailableScaleUnits : {Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances, Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances}
Name                : barracudasdwanrelease
Etag                : 00000000-0000-0000-0000-000000000000
Id                  :
```

<span data-ttu-id="dea25-109">Skaffa en SKU efter namn.</span><span class="sxs-lookup"><span data-stu-id="dea25-109">Get a sku by name.</span></span>

### <span data-ttu-id="dea25-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="dea25-110">Example 2</span></span>
```powershell
PS C:\> Get-AzNetworkVirtualApplianceSku                                                                                                                                                       

Vendor              : barracuda sdwan nightly
AvailableVersions   : {latest}
AvailableScaleUnits : {Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances}
Name                : barracuda sdwan nightly
Etag                : 00000000-0000-0000-0000-000000000000
Id                  :

Vendor              : barracuda sdwan
AvailableVersions   : {latest}
AvailableScaleUnits : {Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances}
Name                : barracuda sdwan
Etag                : 00000000-0000-0000-0000-000000000000
Id                  :

Vendor              : barracudasdwanrelease
AvailableVersions   : {8.1.0038301, latest}
AvailableScaleUnits : {Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances, Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances}
Name                : barracudasdwanrelease
Etag                : 00000000-0000-0000-0000-000000000000
Id                  :
```

<span data-ttu-id="dea25-111">Lista alla tillgängliga SKU: er för virtuella nätverk.</span><span class="sxs-lookup"><span data-stu-id="dea25-111">List all available Skus of Network Virtual Appliance.</span></span>

## <span data-ttu-id="dea25-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dea25-112">PARAMETERS</span></span>

### <span data-ttu-id="dea25-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dea25-113">-DefaultProfile</span></span>
<span data-ttu-id="dea25-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dea25-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dea25-115">-SkuName</span><span class="sxs-lookup"><span data-stu-id="dea25-115">-SkuName</span></span>
<span data-ttu-id="dea25-116">SKU-namnet.</span><span class="sxs-lookup"><span data-stu-id="dea25-116">The Sku name.</span></span>

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

### <span data-ttu-id="dea25-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dea25-117">CommonParameters</span></span>
<span data-ttu-id="dea25-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dea25-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dea25-119">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dea25-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dea25-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dea25-120">INPUTS</span></span>

### <span data-ttu-id="dea25-121">Ingen</span><span class="sxs-lookup"><span data-stu-id="dea25-121">None</span></span>

## <span data-ttu-id="dea25-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dea25-122">OUTPUTS</span></span>

### <span data-ttu-id="dea25-123">Microsoft. Azure. commands. Networks. Models. PSNetworkVirtualApplianceSku</span><span class="sxs-lookup"><span data-stu-id="dea25-123">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSku</span></span>

## <span data-ttu-id="dea25-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dea25-124">NOTES</span></span>

## <span data-ttu-id="dea25-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dea25-125">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualApplianceSite.md
ms.openlocfilehash: b21fe2cc51668548d4fedc8eb6fc9404d5626a41
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323820"
---
# <span data-ttu-id="a873d-101">Get-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="a873d-101">Get-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="a873d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a873d-102">SYNOPSIS</span></span>
<span data-ttu-id="a873d-103">Hämta eller lista webbplatser som är anslutna till resurser för virtuella enheter.</span><span class="sxs-lookup"><span data-stu-id="a873d-103">Get or List sites connected to Network Virtual Appliance resource(s).</span></span>

## <span data-ttu-id="a873d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a873d-104">SYNTAX</span></span>

### <span data-ttu-id="a873d-105">ResourceNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="a873d-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzVirtualApplianceSite [-Name <String>] [-NetworkVirtualApplianceId <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a873d-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a873d-106">ResourceIdParameterSet</span></span>
```
Get-AzVirtualApplianceSite -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a873d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a873d-107">DESCRIPTION</span></span>
<span data-ttu-id="a873d-108">Get-AzVirtualApplianceSite får eller lista webbplatser som är anslutna till en eller flera virtuella nätverks utrustnings resurser.</span><span class="sxs-lookup"><span data-stu-id="a873d-108">The Get-AzVirtualApplianceSite gets or lists sites connected to one or more Network Virtual Appliance resources.</span></span>

## <span data-ttu-id="a873d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a873d-109">EXAMPLES</span></span>

### <span data-ttu-id="a873d-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a873d-110">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualApplianceSite -Name testsite -NetworkVirtualApplianceId $nva.Id -ResourceGroupName testrg


AddressPrefix     : 10.0.1.0/24
O365Policy        : Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties
ProvisioningState : Succeeded
Name              : testsite
Etag              : 00000000-0000-0000-0000-000000000000
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/providers/Microsoft.Network/networkVirtualAppliances/nva/virtualApplianceSites/testsite
```

<span data-ttu-id="a873d-111">Skaffa en webbplats resurs för virtuell enhet.</span><span class="sxs-lookup"><span data-stu-id="a873d-111">Get a Virtual Appliance site resource.</span></span>

### <span data-ttu-id="a873d-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="a873d-112">Example 2</span></span>
```powershell
PS C:\> Get-AzVirtualApplianceSite -NetworkVirtualApplianceId $nva.Id -ResourceGroupName testrg


AddressPrefix     : 10.0.1.0/24
O365Policy        : Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties
ProvisioningState : Succeeded
Name              : testsite
Etag              : 00000000-0000-0000-0000-000000000000
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/providers/Microsoft.Network/networkVirtualAppliances/nva/virtualApplianceSites/testsite

AddressPrefix     : 10.0.2.0/24
O365Policy        : Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties
ProvisioningState : Succeeded
Name              : testsite2
Etag              : 00000000-0000-0000-0000-000000000000
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/providers/Microsoft.Network/networkVirtualAppliances/nva/virtualApplianceSites/testsite2
```

<span data-ttu-id="a873d-113">Visa en lista över resurser för virtuella enheter i en virtuell nätverks apparat.</span><span class="sxs-lookup"><span data-stu-id="a873d-113">List Virtual Appliance site resources in a Network Virtual Appliance.</span></span>


## <span data-ttu-id="a873d-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a873d-114">PARAMETERS</span></span>

### <span data-ttu-id="a873d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a873d-115">-DefaultProfile</span></span>
<span data-ttu-id="a873d-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a873d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a873d-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="a873d-117">-Name</span></span>
<span data-ttu-id="a873d-118">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="a873d-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a873d-119">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="a873d-119">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="a873d-120">Den virtuella nätverks apparaten som webbplatsen är ansluten till.</span><span class="sxs-lookup"><span data-stu-id="a873d-120">The Network Virtual Appliance that the site is attached.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a873d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a873d-121">-ResourceGroupName</span></span>
<span data-ttu-id="a873d-122">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="a873d-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a873d-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a873d-123">-ResourceId</span></span>
<span data-ttu-id="a873d-124">Resurs-ID för den virtuella produktens webbplats.</span><span class="sxs-lookup"><span data-stu-id="a873d-124">The resource Id of the Virtual Appliance Site.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a873d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a873d-125">CommonParameters</span></span>
<span data-ttu-id="a873d-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a873d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a873d-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a873d-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a873d-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a873d-128">INPUTS</span></span>

### <span data-ttu-id="a873d-129">System. String</span><span class="sxs-lookup"><span data-stu-id="a873d-129">System.String</span></span>

## <span data-ttu-id="a873d-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a873d-130">OUTPUTS</span></span>

### <span data-ttu-id="a873d-131">Microsoft. Azure. commands. Networks. Models. PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="a873d-131">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="a873d-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a873d-132">NOTES</span></span>

## <span data-ttu-id="a873d-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a873d-133">RELATED LINKS</span></span>

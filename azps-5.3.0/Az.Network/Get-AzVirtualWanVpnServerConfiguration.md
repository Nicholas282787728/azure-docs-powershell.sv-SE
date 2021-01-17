---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualwanvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfiguration.md
ms.openlocfilehash: 6124b3ddb862254d11bd141560a682bb91bb7fb7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98422064"
---
# <span data-ttu-id="5fcb0-101">Get-AzVirtualWanVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="5fcb0-101">Get-AzVirtualWanVpnServerConfiguration</span></span>

## <span data-ttu-id="5fcb0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5fcb0-102">SYNOPSIS</span></span>
<span data-ttu-id="5fcb0-103">Hämtar listan över alla VpnServerConfigurations som är kopplade till den här VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="5fcb0-103">Gets the list of all VpnServerConfigurations that are associated with this VirtualWan.</span></span>

## <span data-ttu-id="5fcb0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5fcb0-104">SYNTAX</span></span>

### <span data-ttu-id="5fcb0-105">ByVirtualWanName (standard)</span><span class="sxs-lookup"><span data-stu-id="5fcb0-105">ByVirtualWanName (Default)</span></span>
```
Get-AzVirtualWanVpnServerConfiguration [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5fcb0-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="5fcb0-106">ByVirtualWanObject</span></span>
```
Get-AzVirtualWanVpnServerConfiguration [-Name <String>] -ResourceGroupName <String>
 -VirtualWanObject <PSVirtualWan> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5fcb0-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="5fcb0-107">ByVirtualWanResourceId</span></span>
```
Get-AzVirtualWanVpnServerConfiguration [-Name <String>] -ResourceGroupName <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5fcb0-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5fcb0-108">DESCRIPTION</span></span>
<span data-ttu-id="5fcb0-109">Cmdleten **Get-AzVirtualWanVpnServerConfiguration** returnerar listan med alla VpnServerConfigurations som är kopplade till den här VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="5fcb0-109">The **Get-AzVirtualWanVpnServerConfiguration** cmdlet will return the list of all VpnServerConfigurations that are associated with this VirtualWan.</span></span> <span data-ttu-id="5fcb0-110">d.v.s. alla VpnServerConfigurations som är kopplade till valfri P2SVpnGateways under VirutalHubs i denna VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="5fcb0-110">i.e. All the VpnServerConfigurations which are attached to any P2SVpnGateways under VirutalHubs of this VirtualWan.</span></span>

## <span data-ttu-id="5fcb0-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5fcb0-111">EXAMPLES</span></span>

### <span data-ttu-id="5fcb0-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5fcb0-112">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualWanVpnServerConfiguration -Name WestUsVirtualWan -ResourceGroupName P2SCortexGATesting

VpnServerConfigurationResourceIds : [
                                      "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/WestUsConfig"                           ]
```

## <span data-ttu-id="5fcb0-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5fcb0-113">PARAMETERS</span></span>

### <span data-ttu-id="5fcb0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fcb0-114">-DefaultProfile</span></span>
<span data-ttu-id="5fcb0-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5fcb0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5fcb0-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="5fcb0-116">-Name</span></span>
<span data-ttu-id="5fcb0-117">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="5fcb0-117">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fcb0-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fcb0-118">-ResourceGroupName</span></span>
<span data-ttu-id="5fcb0-119">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="5fcb0-119">The resource group name.</span></span>

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

### <span data-ttu-id="5fcb0-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5fcb0-120">-ResourceId</span></span>
<span data-ttu-id="5fcb0-121">Azure Resource ID för den virtuella WAN-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="5fcb0-121">The Azure resource ID for the virtual wan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanResourceId
Aliases: VirtualWanId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fcb0-122">-VirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="5fcb0-122">-VirtualWanObject</span></span>
<span data-ttu-id="5fcb0-123">Virtuellt WAN-objekt.</span><span class="sxs-lookup"><span data-stu-id="5fcb0-123">The virtual wan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases: VirtualWan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5fcb0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fcb0-124">CommonParameters</span></span>
<span data-ttu-id="5fcb0-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fcb0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fcb0-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fcb0-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fcb0-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5fcb0-127">INPUTS</span></span>

### <span data-ttu-id="5fcb0-128">System. String</span><span class="sxs-lookup"><span data-stu-id="5fcb0-128">System.String</span></span>
<span data-ttu-id="5fcb0-129">Microsoft. Azure. commands. Networks. Models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="5fcb0-129">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="5fcb0-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5fcb0-130">OUTPUTS</span></span>

### <span data-ttu-id="5fcb0-131">Microsoft. Azure. commands. Networks. Models. PSVpnServerConfigurationsResponse</span><span class="sxs-lookup"><span data-stu-id="5fcb0-131">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfigurationsResponse</span></span>

## <span data-ttu-id="5fcb0-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5fcb0-132">NOTES</span></span>

## <span data-ttu-id="5fcb0-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5fcb0-133">RELATED LINKS</span></span>

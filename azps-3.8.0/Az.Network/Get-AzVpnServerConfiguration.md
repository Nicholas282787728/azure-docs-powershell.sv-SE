---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnServerConfiguration.md
ms.openlocfilehash: 47450d65b883f23bda8141df6be0eb11bc0fa908
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092580"
---
# <span data-ttu-id="300a3-101">Get-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="300a3-101">Get-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="300a3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="300a3-102">SYNOPSIS</span></span>
<span data-ttu-id="300a3-103">Hämtar en befintlig VpnServerConfiguration för pekar på webbplats anslutningar.</span><span class="sxs-lookup"><span data-stu-id="300a3-103">Gets an existing VpnServerConfiguration for point to site connectivity.</span></span>

## <span data-ttu-id="300a3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="300a3-104">SYNTAX</span></span>

### <span data-ttu-id="300a3-105">ListBySubscriptionId (standard)</span><span class="sxs-lookup"><span data-stu-id="300a3-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzVpnServerConfiguration [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="300a3-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="300a3-106">ListByResourceGroupName</span></span>
```
Get-AzVpnServerConfiguration [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="300a3-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="300a3-107">DESCRIPTION</span></span>
<span data-ttu-id="300a3-108">Cmdleten **Get-AzVpnServerConfiguration** returnerar den befintliga VpnServerConfiguration för att peka på webbplats anslutningar.</span><span class="sxs-lookup"><span data-stu-id="300a3-108">The **Get-AzVpnServerConfiguration** cmdlet returns the existing VpnServerConfiguration for Point to site connectivity.</span></span>

## <span data-ttu-id="300a3-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="300a3-109">EXAMPLES</span></span>

### <span data-ttu-id="300a3-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="300a3-110">Example 1</span></span>
```powershell
PS C:\> Get-AzVpnServerConfiguration -ResourceGroupName P2SCortexGATesting -Name test1config

ResourceGroupName            : P2SCortexGATesting
Name                         : test1config
Id                           : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/test1config
Location                     : westus
VpnProtocols                 : {IkeV2, OpenVPN}
VpnAuthenticationTypes       : {Certificate}
VpnClientRootCertificates    :
VpnClientRevokedCertificates : [
                                 {
                                   "Name": "cert2",
                                   "Thumbprint": "83FFBFC8848B5A5836C94D0112367E16148A286F"
                                 }
                               ]
RadiusServerAddress          :
RadiusServerRootCertificates : []
RadiusClientRootCertificates : []
VpnClientIpsecPolicies       : []
AadAuthenticationParameters  : null
P2sVpnGateways               : []
Type                         : Microsoft.Network/vpnServerConfigurations
ProvisioningState            : Succeeded
```

<span data-ttu-id="300a3-111">Kommandot ovan kommer att hämta de befintliga VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="300a3-111">The above command will get the existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="300a3-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="300a3-112">PARAMETERS</span></span>

### <span data-ttu-id="300a3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="300a3-113">-DefaultProfile</span></span>
<span data-ttu-id="300a3-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="300a3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="300a3-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="300a3-115">-Name</span></span>
<span data-ttu-id="300a3-116">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="300a3-116">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, VpnServerConfigurationName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="300a3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="300a3-117">-ResourceGroupName</span></span>
<span data-ttu-id="300a3-118">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="300a3-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="300a3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="300a3-119">CommonParameters</span></span>
<span data-ttu-id="300a3-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="300a3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="300a3-121">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="300a3-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="300a3-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="300a3-122">INPUTS</span></span>

### <span data-ttu-id="300a3-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="300a3-123">None</span></span>

## <span data-ttu-id="300a3-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="300a3-124">OUTPUTS</span></span>

### <span data-ttu-id="300a3-125">Microsoft. Azure. commands. Networks. Models. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="300a3-125">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="300a3-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="300a3-126">NOTES</span></span>

## <span data-ttu-id="300a3-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="300a3-127">RELATED LINKS</span></span>

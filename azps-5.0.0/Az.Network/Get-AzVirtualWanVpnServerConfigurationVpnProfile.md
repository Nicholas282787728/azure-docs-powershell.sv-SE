---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualwanvpnserverconfigurationvpnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfigurationVpnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfigurationVpnProfile.md
ms.openlocfilehash: 5e19f63c0497535c44513c55a28d7117d0783574
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94273083"
---
# <span data-ttu-id="6d1e2-101">Get-AzVirtualWanVpnServerConfigurationVpnProfile</span><span class="sxs-lookup"><span data-stu-id="6d1e2-101">Get-AzVirtualWanVpnServerConfigurationVpnProfile</span></span>

## <span data-ttu-id="6d1e2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6d1e2-102">SYNOPSIS</span></span>
<span data-ttu-id="6d1e2-103">Skapar och laddar ned VPN-profil på VirtualWan-VpnServerConfiguration nivå för klient installation med peka-och-webbplats.</span><span class="sxs-lookup"><span data-stu-id="6d1e2-103">Generates and downloads Vpn profile at VirtualWan-VpnServerConfiguration level for Point to site client setup.</span></span>

## <span data-ttu-id="6d1e2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6d1e2-104">SYNTAX</span></span>

### <span data-ttu-id="6d1e2-105">ByVirtualWanNameByVpnServerConfigurationObject (standard)</span><span class="sxs-lookup"><span data-stu-id="6d1e2-105">ByVirtualWanNameByVpnServerConfigurationObject (Default)</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile [-Name <String>] -ResourceGroupName <String>
 -VpnServerConfiguration <PSVpnServerConfiguration> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d1e2-106">ByVirtualWanNameByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="6d1e2-106">ByVirtualWanNameByVpnServerConfigurationResourceId</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile [-Name <String>] -ResourceGroupName <String>
 -VpnServerConfigurationId <String> [-AuthenticationMethod <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6d1e2-107">ByVirtualWanObjectByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="6d1e2-107">ByVirtualWanObjectByVpnServerConfigurationObject</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile -VirtualWanObject <PSVirtualWan>
 -VpnServerConfiguration <PSVpnServerConfiguration> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d1e2-108">ByVirtualWanObjectByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="6d1e2-108">ByVirtualWanObjectByVpnServerConfigurationResourceId</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile -VirtualWanObject <PSVirtualWan>
 -VpnServerConfigurationId <String> [-AuthenticationMethod <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6d1e2-109">ByVirtualWanResourceIdByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="6d1e2-109">ByVirtualWanResourceIdByVpnServerConfigurationObject</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile -ResourceId <String>
 -VpnServerConfiguration <PSVpnServerConfiguration> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d1e2-110">ByVirtualWanResourceIdByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="6d1e2-110">ByVirtualWanResourceIdByVpnServerConfigurationResourceId</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile -ResourceId <String> -VpnServerConfigurationId <String>
 [-AuthenticationMethod <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d1e2-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6d1e2-111">DESCRIPTION</span></span>
<span data-ttu-id="6d1e2-112">Med cmdleten **Get-AzVirtualWanVpnServerConfigurationVpnProfile** kan du skapa och ladda ned VPN-profilen på VirtualWan-VpnServerConfiguration nivå för klient installation med punkt till webbplats.</span><span class="sxs-lookup"><span data-stu-id="6d1e2-112">The **Get-AzVirtualWanVpnServerConfigurationVpnProfile** cmdlet enables you to generate and download the Vpn profile at VirtualWan-VpnServerConfiguration level for Point to site client setup.</span></span> <span data-ttu-id="6d1e2-113">Det här krävs för att peka på webbplats anslutningen från peka på webbplats klient till Azure P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="6d1e2-113">This is required for Point to site connectivity from Point to site client to Azure P2SVpnGateway.</span></span>

## <span data-ttu-id="6d1e2-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6d1e2-114">EXAMPLES</span></span>

### <span data-ttu-id="6d1e2-115">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6d1e2-115">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualWanVpnServerConfigurationVpnProfile -Name WestUsVirtualWan -ResourceGroupName P2SCortexGATesting -VpnServerConfiguration $vpnServerConfig -AuthenticationMethod EAPTLS

ProfileUrl : https://nfvprodsuppby.blob.core.windows.net/vpnprofileimmutable/aa316f33-d0f6-4e61-994a-9aa24c0e5f70/vpnprofile/eb99aa3d-1106-49eb-9644-791c045c5cca/vpnclientconfiguration.zip?sv=2017-04-17&sr=b&sig=kZinevNqW
             qsEAbWAcYiKfUHFxZzh2hwvtb49dfVtUDA%3D&st=2019-10-25T19%3A52%3A36Z&se=2019-10-25T20%3A52%3A36Z&sp=r&fileExtension=.zip
```

<span data-ttu-id="6d1e2-116">Med kommandot ovan skapas och returneras SAS-URL: en för kund för att ladda ned VPN-profilen på VirtualWan-VpnServerConfiguration nivå för klient installationen för Point-to-Site.</span><span class="sxs-lookup"><span data-stu-id="6d1e2-116">The above command will generate and returns SAS Url for customer to download the Vpn profile at VirtualWan-VpnServerConfiguration level for Point to site client setup.</span></span>

## <span data-ttu-id="6d1e2-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6d1e2-117">PARAMETERS</span></span>

### <span data-ttu-id="6d1e2-118">-AuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="6d1e2-118">-AuthenticationMethod</span></span>
<span data-ttu-id="6d1e2-119">Autentiseringsmetod</span><span class="sxs-lookup"><span data-stu-id="6d1e2-119">Authentication Method</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: EAPTLS, EAPMSCHAPv2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d1e2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d1e2-120">-DefaultProfile</span></span>
<span data-ttu-id="6d1e2-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6d1e2-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d1e2-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="6d1e2-122">-Name</span></span>
<span data-ttu-id="6d1e2-123">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="6d1e2-123">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanNameByVpnServerConfigurationObject, ByVirtualWanNameByVpnServerConfigurationResourceId
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d1e2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d1e2-124">-ResourceGroupName</span></span>
<span data-ttu-id="6d1e2-125">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="6d1e2-125">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanNameByVpnServerConfigurationObject, ByVirtualWanNameByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d1e2-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6d1e2-126">-ResourceId</span></span>
<span data-ttu-id="6d1e2-127">Azure Resource ID för den virtuella WAN-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="6d1e2-127">The Azure resource ID for the virtual wan.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanResourceIdByVpnServerConfigurationObject, ByVirtualWanResourceIdByVpnServerConfigurationResourceId
Aliases: VirtualWanId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d1e2-128">-VirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="6d1e2-128">-VirtualWanObject</span></span>
<span data-ttu-id="6d1e2-129">Virtuellt WAN-objekt.</span><span class="sxs-lookup"><span data-stu-id="6d1e2-129">The virtual wan object.</span></span>

```yaml
Type: PSVirtualWan
Parameter Sets: ByVirtualWanObjectByVpnServerConfigurationObject, ByVirtualWanObjectByVpnServerConfigurationResourceId
Aliases: VirtualWan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d1e2-130">-VpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="6d1e2-130">-VpnServerConfiguration</span></span>
<span data-ttu-id="6d1e2-131">VpnServerConfiguration som den här VirtualWan är associerad med.</span><span class="sxs-lookup"><span data-stu-id="6d1e2-131">The VpnServerConfiguration with which this VirtualWan is associated.</span></span>

```yaml
Type: PSVpnServerConfiguration
Parameter Sets: ByVirtualWanNameByVpnServerConfigurationObject, ByVirtualWanObjectByVpnServerConfigurationObject, ByVirtualWanResourceIdByVpnServerConfigurationObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d1e2-132">-VpnServerConfigurationId</span><span class="sxs-lookup"><span data-stu-id="6d1e2-132">-VpnServerConfigurationId</span></span>
<span data-ttu-id="6d1e2-133">ID för VPN-servern configuraiton detta virtuella WAN-objekt associeras med.</span><span class="sxs-lookup"><span data-stu-id="6d1e2-133">The id of Vpn server configuraiton object this Virtual wan will be associated with.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanNameByVpnServerConfigurationResourceId, ByVirtualWanObjectByVpnServerConfigurationResourceId, ByVirtualWanResourceIdByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d1e2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d1e2-134">CommonParameters</span></span>
<span data-ttu-id="6d1e2-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d1e2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d1e2-136">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d1e2-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d1e2-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6d1e2-137">INPUTS</span></span>

### <span data-ttu-id="6d1e2-138">System. String</span><span class="sxs-lookup"><span data-stu-id="6d1e2-138">System.String</span></span>
<span data-ttu-id="6d1e2-139">Microsoft. Azure. commands. Networks. Models. PSVirtualWan Microsoft. Azure. commands. Network. Models. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="6d1e2-139">Microsoft.Azure.Commands.Network.Models.PSVirtualWan Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="6d1e2-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6d1e2-140">OUTPUTS</span></span>

### <span data-ttu-id="6d1e2-141">Microsoft. Azure. commands. Networks. Models. PSVpnProfileResponse</span><span class="sxs-lookup"><span data-stu-id="6d1e2-141">Microsoft.Azure.Commands.Network.Models.PSVpnProfileResponse</span></span>

## <span data-ttu-id="6d1e2-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6d1e2-142">NOTES</span></span>

## <span data-ttu-id="6d1e2-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6d1e2-143">RELATED LINKS</span></span>

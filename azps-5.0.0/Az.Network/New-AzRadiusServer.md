---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azradiusserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRadiusServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRadiusServer.md
ms.openlocfilehash: 0f92f09d3caf481f845c96942fd038a82c1078ee
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323748"
---
# <span data-ttu-id="61aad-101">New-AzRadiusServer</span><span class="sxs-lookup"><span data-stu-id="61aad-101">New-AzRadiusServer</span></span>

## <span data-ttu-id="61aad-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="61aad-102">SYNOPSIS</span></span>
<span data-ttu-id="61aad-103">Skapar en extern RADIUS-serverkonfiguration</span><span class="sxs-lookup"><span data-stu-id="61aad-103">Creates an external radius server configuration</span></span>

## <span data-ttu-id="61aad-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="61aad-104">SYNTAX</span></span>

```
New-AzRadiusServer -RadiusServerAddress <String> -RadiusServerSecret <SecureString>
 [-RadiusServerScore <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61aad-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="61aad-105">DESCRIPTION</span></span>
<span data-ttu-id="61aad-106">Med den här New-AzRadiusServer cmdleten skapar du en extern RADIUS-serverkonfiguration för att använda den virtuella Nätverksgatewayen och VPN-serverkonfigurationen.</span><span class="sxs-lookup"><span data-stu-id="61aad-106">The New-AzRadiusServer cmdlet creates an external radius server configuration to be used in virtual network gateway and VPN server configuration.</span></span>

## <span data-ttu-id="61aad-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="61aad-107">EXAMPLES</span></span>

### <span data-ttu-id="61aad-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="61aad-108">Example 1</span></span>
```powershell
PS C:\> $radiusServer1 = New-AzRadiusServer -RadiusServerAddress 10.1.0.1 -RadiusServerSecret $radiuspd -RadiusServerScore 30
PS C:\> $radiusServer2 = New-AzRadiusServer -RadiusServerAddress 10.1.0.2 -RadiusServerSecret $radiuspd -RadiusServerScore 1
PS C:\> New-AzVirtualNetworkGateway -ResourceGroupName $rgname -name $rname -location $location -IpConfigurations $vnetIpConfig -GatewayType Vpn -VpnType RouteBased -EnableBgp $false -GatewaySku VpnGw1 -VpnClientAddressPool 201.169.0.0/16 -VpnClientProtocol "IkeV2" -RadiusServerList $radiusServers
```

<span data-ttu-id="61aad-109">Skapa flera externa RADIUS-serverkonfigurationer som ska användas för att konfigurera P2S på en ny virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="61aad-109">Creating multiple external radius server configurations to be used for configuring P2S on a new virtual network gateway.</span></span>

## <span data-ttu-id="61aad-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="61aad-110">PARAMETERS</span></span>

### <span data-ttu-id="61aad-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61aad-111">-DefaultProfile</span></span>
<span data-ttu-id="61aad-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="61aad-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61aad-113">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="61aad-113">-RadiusServerAddress</span></span>
<span data-ttu-id="61aad-114">Extern RADIUS-serveradress</span><span class="sxs-lookup"><span data-stu-id="61aad-114">External radius server address</span></span>

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

### <span data-ttu-id="61aad-115">-RadiusServerScore</span><span class="sxs-lookup"><span data-stu-id="61aad-115">-RadiusServerScore</span></span>
<span data-ttu-id="61aad-116">Poäng för extern RADIUS-server</span><span class="sxs-lookup"><span data-stu-id="61aad-116">External radius server score</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61aad-117">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="61aad-117">-RadiusServerSecret</span></span>
<span data-ttu-id="61aad-118">Hemlig Server hemlighet</span><span class="sxs-lookup"><span data-stu-id="61aad-118">External radius server secret</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61aad-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61aad-119">CommonParameters</span></span>
<span data-ttu-id="61aad-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61aad-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61aad-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="61aad-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61aad-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="61aad-122">INPUTS</span></span>

### <span data-ttu-id="61aad-123">System. String</span><span class="sxs-lookup"><span data-stu-id="61aad-123">System.String</span></span>

### <span data-ttu-id="61aad-124">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="61aad-124">System.Security.SecureString</span></span>

### <span data-ttu-id="61aad-125">System. Int32</span><span class="sxs-lookup"><span data-stu-id="61aad-125">System.Int32</span></span>

## <span data-ttu-id="61aad-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="61aad-126">OUTPUTS</span></span>

### <span data-ttu-id="61aad-127">Microsoft. Azure. commands. Networks. Models. PSRadiusServer</span><span class="sxs-lookup"><span data-stu-id="61aad-127">Microsoft.Azure.Commands.Network.Models.PSRadiusServer</span></span>

## <span data-ttu-id="61aad-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="61aad-128">NOTES</span></span>

## <span data-ttu-id="61aad-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="61aad-129">RELATED LINKS</span></span>
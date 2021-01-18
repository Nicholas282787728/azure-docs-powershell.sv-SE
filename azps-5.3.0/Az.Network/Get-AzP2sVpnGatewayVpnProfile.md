---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azp2svpngatewayvpnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayVpnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayVpnProfile.md
ms.openlocfilehash: 60937898e7e8c0532a0f0815ee44f2e9f75041c7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98527695"
---
# <span data-ttu-id="e9c96-101">Get-AzP2sVpnGatewayVpnProfile</span><span class="sxs-lookup"><span data-stu-id="e9c96-101">Get-AzP2sVpnGatewayVpnProfile</span></span>

## <span data-ttu-id="e9c96-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e9c96-102">SYNOPSIS</span></span>
<span data-ttu-id="e9c96-103">Skapar och returnerar en SAS-URL för kund för att ladda ned VPN-profil för klient installations programmet för att peka på webbplats anslutningen till P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="e9c96-103">Generates and returns a SAS url for customer to download Vpn profile for point to site client setup to have point to site connectivity to P2SVpnGateway.</span></span>

## <span data-ttu-id="e9c96-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e9c96-104">SYNTAX</span></span>

### <span data-ttu-id="e9c96-105">ByP2SVpnGatewayName (standard)</span><span class="sxs-lookup"><span data-stu-id="e9c96-105">ByP2SVpnGatewayName (Default)</span></span>
```
Get-AzP2sVpnGatewayVpnProfile [-Name <String>] -ResourceGroupName <String> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e9c96-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="e9c96-106">ByP2SVpnGatewayObject</span></span>
```
Get-AzP2sVpnGatewayVpnProfile -InputObject <PSP2SVpnGateway> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e9c96-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="e9c96-107">ByP2SVpnGatewayResourceId</span></span>
```
Get-AzP2sVpnGatewayVpnProfile -ResourceId <String> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9c96-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e9c96-108">DESCRIPTION</span></span>
<span data-ttu-id="e9c96-109">Med cmdleten **Get-AzP2sVpnGatewayVpnProfile** kan du skapa och skaffa en SAS-URL för kunder för att ladda ned VPN-profil för klient installations programmet för att peka på webbplats anslutningar till P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="e9c96-109">The **Get-AzP2sVpnGatewayVpnProfile** cmdlet enables you to generate and get a SAS url for customer to download Vpn profile for point to site client setup to have point to site connectivity to P2SVpnGateway.</span></span> <span data-ttu-id="e9c96-110">Peka på webbplats klient installation med denna VPN-profil kan du bara ansluta till denna specifika P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="e9c96-110">Point to site client setup using this Vpn profile can connect to this specific P2SVpnGateway only.</span></span>

## <span data-ttu-id="e9c96-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e9c96-111">EXAMPLES</span></span>

### <span data-ttu-id="e9c96-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e9c96-112">Example 1</span></span>
```powershell
PS C:\> Get-AzP2sVpnGatewayVpnProfile -Name 683482ade8564515aed4b8448c9757ea-westus-gw -ResourceGroupName P2SCortexGATesting -AuthenticationMethod EAPTLS


ProfileUrl : https://nfvprodsuppby.blob.core.windows.net/vpnprofileimmutable/8cf00031-37ec-4949-b74a-48f9021bf4c0/vpnprofile/2f132439-1051-44c6-9128-b704c1c48cf7/vpnclientconfiguration.zip?sv=2017-04-17&sr=b&sig=HmBSprVrs
             6hDY3x1HX958nimOjavnEjL2rlSuKIIW8Q%3D&st=2019-10-25T19%3A20%3A04Z&se=2019-10-25T20%3A20%3A04Z&sp=r&fileExtension=.zip
```

<span data-ttu-id="e9c96-113">Med cmdleten **Get-AzP2sVpnGatewayVpnProfile** kan du skapa och skaffa en SAS-URL för kunder för att ladda ned VPN-profil för klient installations programmet för att peka på webbplats anslutningar till P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="e9c96-113">The **Get-AzP2sVpnGatewayVpnProfile** cmdlet enables you to generate and get a SAS url for customer to download Vpn profile for point to site client setup to have point to site connectivity to P2SVpnGateway.</span></span> <span data-ttu-id="e9c96-114">ProfileUrl visar SAS-URL: en från vilken en kund kan ladda ner VPN-profil för installation av peka på webbplats klient.</span><span class="sxs-lookup"><span data-stu-id="e9c96-114">ProfileUrl shows the SAS url from where customer can download Vpn profile for point to site client setup.</span></span>

## <span data-ttu-id="e9c96-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e9c96-115">PARAMETERS</span></span>

### <span data-ttu-id="e9c96-116">-AuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="e9c96-116">-AuthenticationMethod</span></span>
<span data-ttu-id="e9c96-117">Autentiseringsmetod</span><span class="sxs-lookup"><span data-stu-id="e9c96-117">Authentication Method</span></span>

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

### <span data-ttu-id="e9c96-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9c96-118">-DefaultProfile</span></span>
<span data-ttu-id="e9c96-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e9c96-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9c96-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e9c96-120">-InputObject</span></span>
<span data-ttu-id="e9c96-121">P2s VPN gateway-objekt som ska ändras</span><span class="sxs-lookup"><span data-stu-id="e9c96-121">The p2s vpn gateway object to be modified</span></span>

```yaml
Type: PSP2SVpnGateway
Parameter Sets: ByP2SVpnGatewayObject
Aliases: P2SVpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e9c96-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="e9c96-122">-Name</span></span>
<span data-ttu-id="e9c96-123">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="e9c96-123">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9c96-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9c96-124">-ResourceGroupName</span></span>
<span data-ttu-id="e9c96-125">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="e9c96-125">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9c96-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e9c96-126">-ResourceId</span></span>
<span data-ttu-id="e9c96-127">Azure-resurs-ID för P2SVpnGateway som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="e9c96-127">The Azure resource ID of the P2SVpnGateway to be modified.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9c96-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9c96-128">CommonParameters</span></span>
<span data-ttu-id="e9c96-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9c96-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9c96-130">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9c96-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9c96-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e9c96-131">INPUTS</span></span>

### <span data-ttu-id="e9c96-132">System. String</span><span class="sxs-lookup"><span data-stu-id="e9c96-132">System.String</span></span>
<span data-ttu-id="e9c96-133">Microsoft. Azure. commands. Networks. Models. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="e9c96-133">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="e9c96-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e9c96-134">OUTPUTS</span></span>

### <span data-ttu-id="e9c96-135">Microsoft. Azure. commands. Networks. Models. PSVpnProfileResponse</span><span class="sxs-lookup"><span data-stu-id="e9c96-135">Microsoft.Azure.Commands.Network.Models.PSVpnProfileResponse</span></span>

## <span data-ttu-id="e9c96-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e9c96-136">NOTES</span></span>

## <span data-ttu-id="e9c96-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e9c96-137">RELATED LINKS</span></span>

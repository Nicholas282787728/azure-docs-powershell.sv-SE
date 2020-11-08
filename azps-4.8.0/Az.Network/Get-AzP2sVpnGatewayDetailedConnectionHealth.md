---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azp2svpngatewaydetailedconnectionhealth
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayDetailedConnectionHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayDetailedConnectionHealth.md
ms.openlocfilehash: 13c74416591318bdebdc869475930111e695d3f2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258787"
---
# <span data-ttu-id="4b182-101">Get-AzP2sVpnGatewayDetailedConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="4b182-101">Get-AzP2sVpnGatewayDetailedConnectionHealth</span></span>

## <span data-ttu-id="4b182-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4b182-102">SYNOPSIS</span></span>
<span data-ttu-id="4b182-103">Hämtar detaljerad information om aktuella punkter till webbplats anslutningar från P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="4b182-103">Gets the detailed information of current point to site connections from P2SVpnGateway.</span></span>

## <span data-ttu-id="4b182-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4b182-104">SYNTAX</span></span>

### <span data-ttu-id="4b182-105">ByP2SVpnGatewayName (standard)</span><span class="sxs-lookup"><span data-stu-id="4b182-105">ByP2SVpnGatewayName (Default)</span></span>
```
Get-AzP2sVpnGatewayDetailedConnectionHealth [-Name <String>] -ResourceGroupName <String>
 -OutputBlobSasUrl <String> [-VpnUserNamesFilter <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4b182-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="4b182-106">ByP2SVpnGatewayObject</span></span>
```
Get-AzP2sVpnGatewayDetailedConnectionHealth -InputObject <PSP2SVpnGateway> -OutputBlobSasUrl <String>
 [-VpnUserNamesFilter <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4b182-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="4b182-107">ByP2SVpnGatewayResourceId</span></span>
```
Get-AzP2sVpnGatewayDetailedConnectionHealth -ResourceId <String> -OutputBlobSasUrl <String>
 [-VpnUserNamesFilter <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b182-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4b182-108">DESCRIPTION</span></span>
<span data-ttu-id="4b182-109">Med cmdleten **Get-AzP2sVpnGatewayDetailedConnectionHealth** kan du få detaljerad information om aktuella punkter för webbplats anslutningar från P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="4b182-109">The **Get-AzP2sVpnGatewayDetailedConnectionHealth** cmdlet enables you to get the detailed information of current point to site connections from P2SVpnGateway.</span></span> <span data-ttu-id="4b182-110">Kunden måste skicka SAS-URL: er där vi kan ange den detaljerade hälso informationen.</span><span class="sxs-lookup"><span data-stu-id="4b182-110">Customer needs to pass SAS url where we can put this detailed health information.</span></span>

## <span data-ttu-id="4b182-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4b182-111">EXAMPLES</span></span>

### <span data-ttu-id="4b182-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4b182-112">Example 1</span></span>
```powershell
PS C:\> $blobSasUrl = New-AzStorageBlobSASToken -Container contp2stesting -Blob emptyfile.txt -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
PS C:\> $blobSasUrl
SignedSasUrl
PS C:\> Get-AzP2sVpnGatewayDetailedConnectionHealth -Name 683482ade8564515aed4b8448c9757ea-westus-gw -ResourceGroupName P2SCortexGATesting -OutputBlobSasUrl $blobSasUrl
SasUrl : SignedSasUrl
```

<span data-ttu-id="4b182-113">Med cmdleten **Get-AzP2sVpnGatewayDetailedConnectionHealth** kan du få detaljerad information om aktuella punkter för webbplats anslutningar från P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="4b182-113">The **Get-AzP2sVpnGatewayDetailedConnectionHealth** cmdlet enables you to get the detailed information of current point to site connections from P2SVpnGateway.</span></span> <span data-ttu-id="4b182-114">Kunden kan ladda ned hälso information från godkänd URL-nedladdning.</span><span class="sxs-lookup"><span data-stu-id="4b182-114">Customer can download health details from passed SAS url download.</span></span> <span data-ttu-id="4b182-115">Då visas information om varje punkt för webbplats anslutning med användar namn, byte in, byte ut, tilldelad IP-adress etc.</span><span class="sxs-lookup"><span data-stu-id="4b182-115">This will show information of each point to site connection with usernames, bytes in, bytes out, allocated ip address etc.</span></span>

## <span data-ttu-id="4b182-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4b182-116">PARAMETERS</span></span>

### <span data-ttu-id="4b182-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b182-117">-DefaultProfile</span></span>
<span data-ttu-id="4b182-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4b182-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b182-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4b182-119">-InputObject</span></span>
<span data-ttu-id="4b182-120">P2s VPN gateway-objekt som ska ändras</span><span class="sxs-lookup"><span data-stu-id="4b182-120">The p2s vpn gateway object to be modified</span></span>

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

### <span data-ttu-id="4b182-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="4b182-121">-Name</span></span>
<span data-ttu-id="4b182-122">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="4b182-122">The resource name.</span></span>

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

### <span data-ttu-id="4b182-123">-OutputBlobSasUrl</span><span class="sxs-lookup"><span data-stu-id="4b182-123">-OutputBlobSasUrl</span></span>
<span data-ttu-id="4b182-124">OutputBlob SAS URL till vilken P2s för VPN-anslutningen skrivs.</span><span class="sxs-lookup"><span data-stu-id="4b182-124">OutputBlob Sas url to which the p2s vpn connection health will be written.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b182-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b182-125">-ResourceGroupName</span></span>
<span data-ttu-id="4b182-126">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="4b182-126">The resource group name.</span></span>

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

### <span data-ttu-id="4b182-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4b182-127">-ResourceId</span></span>
<span data-ttu-id="4b182-128">Azure-resurs-ID för P2SVpnGateway som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="4b182-128">The Azure resource ID of the P2SVpnGateway to be modified.</span></span>

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

### <span data-ttu-id="4b182-129">-VpnUserNamesFilter</span><span class="sxs-lookup"><span data-stu-id="4b182-129">-VpnUserNamesFilter</span></span>
<span data-ttu-id="4b182-130">Listan med P2S VPN-namn som ska filtreras.</span><span class="sxs-lookup"><span data-stu-id="4b182-130">The list of P2S vpn user names to filter.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b182-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b182-131">CommonParameters</span></span>
<span data-ttu-id="4b182-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b182-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b182-133">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b182-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b182-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4b182-134">INPUTS</span></span>

### <span data-ttu-id="4b182-135">System. String</span><span class="sxs-lookup"><span data-stu-id="4b182-135">System.String</span></span>
<span data-ttu-id="4b182-136">Microsoft. Azure. commands. Networks. Models. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="4b182-136">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="4b182-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4b182-137">OUTPUTS</span></span>

### <span data-ttu-id="4b182-138">Microsoft. Azure. commands. Networks. Models. PSP2SVpnConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="4b182-138">Microsoft.Azure.Commands.Network.Models.PSP2SVpnConnectionHealth</span></span>

## <span data-ttu-id="4b182-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4b182-139">NOTES</span></span>

## <span data-ttu-id="4b182-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4b182-140">RELATED LINKS</span></span>

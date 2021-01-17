---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azp2svpngatewaydetailedconnectionhealth
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayDetailedConnectionHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayDetailedConnectionHealth.md
ms.openlocfilehash: 13c74416591318bdebdc869475930111e695d3f2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98417064"
---
# <span data-ttu-id="d0a11-101">Get-AzP2sVpnGatewayDetailedConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="d0a11-101">Get-AzP2sVpnGatewayDetailedConnectionHealth</span></span>

## <span data-ttu-id="d0a11-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d0a11-102">SYNOPSIS</span></span>
<span data-ttu-id="d0a11-103">Hämtar detaljerad information om aktuella punkter till webbplats anslutningar från P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="d0a11-103">Gets the detailed information of current point to site connections from P2SVpnGateway.</span></span>

## <span data-ttu-id="d0a11-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d0a11-104">SYNTAX</span></span>

### <span data-ttu-id="d0a11-105">ByP2SVpnGatewayName (standard)</span><span class="sxs-lookup"><span data-stu-id="d0a11-105">ByP2SVpnGatewayName (Default)</span></span>
```
Get-AzP2sVpnGatewayDetailedConnectionHealth [-Name <String>] -ResourceGroupName <String>
 -OutputBlobSasUrl <String> [-VpnUserNamesFilter <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d0a11-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="d0a11-106">ByP2SVpnGatewayObject</span></span>
```
Get-AzP2sVpnGatewayDetailedConnectionHealth -InputObject <PSP2SVpnGateway> -OutputBlobSasUrl <String>
 [-VpnUserNamesFilter <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d0a11-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="d0a11-107">ByP2SVpnGatewayResourceId</span></span>
```
Get-AzP2sVpnGatewayDetailedConnectionHealth -ResourceId <String> -OutputBlobSasUrl <String>
 [-VpnUserNamesFilter <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0a11-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d0a11-108">DESCRIPTION</span></span>
<span data-ttu-id="d0a11-109">Med cmdleten **Get-AzP2sVpnGatewayDetailedConnectionHealth** kan du få detaljerad information om aktuella punkter för webbplats anslutningar från P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="d0a11-109">The **Get-AzP2sVpnGatewayDetailedConnectionHealth** cmdlet enables you to get the detailed information of current point to site connections from P2SVpnGateway.</span></span> <span data-ttu-id="d0a11-110">Kunden måste skicka SAS-URL: er där vi kan ange den detaljerade hälso informationen.</span><span class="sxs-lookup"><span data-stu-id="d0a11-110">Customer needs to pass SAS url where we can put this detailed health information.</span></span>

## <span data-ttu-id="d0a11-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d0a11-111">EXAMPLES</span></span>

### <span data-ttu-id="d0a11-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d0a11-112">Example 1</span></span>
```powershell
PS C:\> $blobSasUrl = New-AzStorageBlobSASToken -Container contp2stesting -Blob emptyfile.txt -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
PS C:\> $blobSasUrl
SignedSasUrl
PS C:\> Get-AzP2sVpnGatewayDetailedConnectionHealth -Name 683482ade8564515aed4b8448c9757ea-westus-gw -ResourceGroupName P2SCortexGATesting -OutputBlobSasUrl $blobSasUrl
SasUrl : SignedSasUrl
```

<span data-ttu-id="d0a11-113">Med cmdleten **Get-AzP2sVpnGatewayDetailedConnectionHealth** kan du få detaljerad information om aktuella punkter för webbplats anslutningar från P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="d0a11-113">The **Get-AzP2sVpnGatewayDetailedConnectionHealth** cmdlet enables you to get the detailed information of current point to site connections from P2SVpnGateway.</span></span> <span data-ttu-id="d0a11-114">Kunden kan ladda ned hälso information från godkänd URL-nedladdning.</span><span class="sxs-lookup"><span data-stu-id="d0a11-114">Customer can download health details from passed SAS url download.</span></span> <span data-ttu-id="d0a11-115">Då visas information om varje punkt för webbplats anslutning med användar namn, byte in, byte ut, tilldelad IP-adress etc.</span><span class="sxs-lookup"><span data-stu-id="d0a11-115">This will show information of each point to site connection with usernames, bytes in, bytes out, allocated ip address etc.</span></span>

## <span data-ttu-id="d0a11-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d0a11-116">PARAMETERS</span></span>

### <span data-ttu-id="d0a11-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0a11-117">-DefaultProfile</span></span>
<span data-ttu-id="d0a11-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d0a11-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0a11-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d0a11-119">-InputObject</span></span>
<span data-ttu-id="d0a11-120">P2s VPN gateway-objekt som ska ändras</span><span class="sxs-lookup"><span data-stu-id="d0a11-120">The p2s vpn gateway object to be modified</span></span>

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

### <span data-ttu-id="d0a11-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="d0a11-121">-Name</span></span>
<span data-ttu-id="d0a11-122">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="d0a11-122">The resource name.</span></span>

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

### <span data-ttu-id="d0a11-123">-OutputBlobSasUrl</span><span class="sxs-lookup"><span data-stu-id="d0a11-123">-OutputBlobSasUrl</span></span>
<span data-ttu-id="d0a11-124">OutputBlob SAS URL till vilken P2s för VPN-anslutningen skrivs.</span><span class="sxs-lookup"><span data-stu-id="d0a11-124">OutputBlob Sas url to which the p2s vpn connection health will be written.</span></span>

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

### <span data-ttu-id="d0a11-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0a11-125">-ResourceGroupName</span></span>
<span data-ttu-id="d0a11-126">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="d0a11-126">The resource group name.</span></span>

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

### <span data-ttu-id="d0a11-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d0a11-127">-ResourceId</span></span>
<span data-ttu-id="d0a11-128">Azure-resurs-ID för P2SVpnGateway som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="d0a11-128">The Azure resource ID of the P2SVpnGateway to be modified.</span></span>

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

### <span data-ttu-id="d0a11-129">-VpnUserNamesFilter</span><span class="sxs-lookup"><span data-stu-id="d0a11-129">-VpnUserNamesFilter</span></span>
<span data-ttu-id="d0a11-130">Listan med P2S VPN-namn som ska filtreras.</span><span class="sxs-lookup"><span data-stu-id="d0a11-130">The list of P2S vpn user names to filter.</span></span>

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

### <span data-ttu-id="d0a11-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0a11-131">CommonParameters</span></span>
<span data-ttu-id="d0a11-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0a11-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0a11-133">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0a11-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0a11-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d0a11-134">INPUTS</span></span>

### <span data-ttu-id="d0a11-135">System. String</span><span class="sxs-lookup"><span data-stu-id="d0a11-135">System.String</span></span>
<span data-ttu-id="d0a11-136">Microsoft. Azure. commands. Networks. Models. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="d0a11-136">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="d0a11-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d0a11-137">OUTPUTS</span></span>

### <span data-ttu-id="d0a11-138">Microsoft. Azure. commands. Networks. Models. PSP2SVpnConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="d0a11-138">Microsoft.Azure.Commands.Network.Models.PSP2SVpnConnectionHealth</span></span>

## <span data-ttu-id="d0a11-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d0a11-139">NOTES</span></span>

## <span data-ttu-id="d0a11-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d0a11-140">RELATED LINKS</span></span>

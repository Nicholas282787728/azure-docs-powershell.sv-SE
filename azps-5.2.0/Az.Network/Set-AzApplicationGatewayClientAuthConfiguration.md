---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayclientauthconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayClientAuthConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayClientAuthConfiguration.md
ms.openlocfilehash: 9512d2d2a51e70b2a0b5e7aa2e8240a8aeb1be1a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98391283"
---
# <span data-ttu-id="1fd76-101">Set-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="1fd76-101">Set-AzApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="1fd76-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1fd76-102">SYNOPSIS</span></span>
<span data-ttu-id="1fd76-103">Ändrar konfigurationen för klientautentisering för ett SSL-profil objekt.</span><span class="sxs-lookup"><span data-stu-id="1fd76-103">Modifies the client auth configuration of a ssl profile object.</span></span>

## <span data-ttu-id="1fd76-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1fd76-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayClientAuthConfiguration -SslProfile <PSApplicationGatewaySslProfile>
 [-VerifyClientCertIssuerDN] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1fd76-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1fd76-105">DESCRIPTION</span></span>
<span data-ttu-id="1fd76-106">Cmdleten **set-AzApplicationGatewayClientAuthConfiguration** ändrar konfigurationen för klientautentisering för ett SSL-profil objekt.</span><span class="sxs-lookup"><span data-stu-id="1fd76-106">The **Set-AzApplicationGatewayClientAuthConfiguration** cmdlet modifies the client auth configuration of a ssl profile object.</span></span>

## <span data-ttu-id="1fd76-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1fd76-107">EXAMPLES</span></span>

### <span data-ttu-id="1fd76-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1fd76-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $profile  = Get-AzApplicationGatewaySslProfile -Name "SslProfile01" -ApplicationGateway $AppGw
PS C:\> Set-AzApplicationGatewayClientAuthConfiguration -SslProfile $profile -VerifyClientCertIssuerDN
```

<span data-ttu-id="1fd76-109">Det första kommandot får den Programgateway som heter ApplicationGateway01 i resurs gruppen som heter ResourceGroup01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="1fd76-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="1fd76-110">Det andra kommandot får den SSL-profil som heter SslProfile01 för $AppGw och lagrar inställningarna i $profile-variabeln.</span><span class="sxs-lookup"><span data-stu-id="1fd76-110">The second command gets the ssl profile named SslProfile01 for $AppGw and stores the settings in the $profile variable.</span></span> <span data-ttu-id="1fd76-111">Det senaste kommandot ändrar konfigurationen för klientautentisering för det SSL-profil objekt som lagras i $profile.</span><span class="sxs-lookup"><span data-stu-id="1fd76-111">The last command modifies the client auth configuration of the ssl profile object stored in $profile.</span></span>

## <span data-ttu-id="1fd76-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1fd76-112">PARAMETERS</span></span>

### <span data-ttu-id="1fd76-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fd76-113">-DefaultProfile</span></span>
<span data-ttu-id="1fd76-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1fd76-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1fd76-115">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="1fd76-115">-SslProfile</span></span>
<span data-ttu-id="1fd76-116">SSL-profil</span><span class="sxs-lookup"><span data-stu-id="1fd76-116">The ssl profile</span></span>

```yaml
Type: PSApplicationGatewaySslProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1fd76-117">-VerifyClientCertIssuerDN</span><span class="sxs-lookup"><span data-stu-id="1fd76-117">-VerifyClientCertIssuerDN</span></span>
<span data-ttu-id="1fd76-118">Verifiera namnet på klient certifikat utfärdaren.</span><span class="sxs-lookup"><span data-stu-id="1fd76-118">Verify client certificate issuer name.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fd76-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fd76-119">CommonParameters</span></span>
<span data-ttu-id="1fd76-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fd76-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fd76-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1fd76-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fd76-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1fd76-122">INPUTS</span></span>

### <span data-ttu-id="1fd76-123">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="1fd76-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="1fd76-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1fd76-124">OUTPUTS</span></span>

### <span data-ttu-id="1fd76-125">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="1fd76-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="1fd76-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1fd76-126">NOTES</span></span>

## <span data-ttu-id="1fd76-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1fd76-127">RELATED LINKS</span></span>

[<span data-ttu-id="1fd76-128">Add-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="1fd76-128">Add-AzApplicationGatewayClientAuthConfiguration</span></span>](./Add-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="1fd76-129">New-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="1fd76-129">New-AzApplicationGatewayClientAuthConfiguration</span></span>](./New-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="1fd76-130">Get-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="1fd76-130">Get-AzApplicationGatewayClientAuthConfiguration</span></span>](./Get-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="1fd76-131">Remove-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="1fd76-131">Remove-AzApplicationGatewayClientAuthConfiguration</span></span>](./Remove-AzApplicationGatewayClientAuthConfiguration.md)
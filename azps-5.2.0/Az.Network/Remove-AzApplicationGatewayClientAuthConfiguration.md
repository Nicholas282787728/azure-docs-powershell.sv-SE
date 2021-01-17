---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayclientauthconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayClientAuthConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayClientAuthConfiguration.md
ms.openlocfilehash: 92d3945e92dc4996fbbe3fc0abbcc296ab141621
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98394579"
---
# <span data-ttu-id="b911c-101">Remove-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="b911c-101">Remove-AzApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="b911c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b911c-102">SYNOPSIS</span></span>
<span data-ttu-id="b911c-103">Tar bort konfigurationen för klientautentisering för ett SSL-profil objekt.</span><span class="sxs-lookup"><span data-stu-id="b911c-103">Removes the client authentication configuration of a SSL profile object.</span></span>

## <span data-ttu-id="b911c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b911c-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayClientAuthConfiguration -SslProfile <PSApplicationGatewaySslProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b911c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b911c-105">DESCRIPTION</span></span>
<span data-ttu-id="b911c-106">Cmdleten **Remove-AzApplicationGatewayClientAuthConfiguration** tar bort konfigurationen för klientautentisering för ett SSL-profil objekt.</span><span class="sxs-lookup"><span data-stu-id="b911c-106">The **Remove-AzApplicationGatewayClientAuthConfiguration** cmdlet removes the client authentication configuration of a SSL profile object.</span></span>

## <span data-ttu-id="b911c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b911c-107">EXAMPLES</span></span>

### <span data-ttu-id="b911c-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b911c-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $profile  = Get-AzApplicationGatewaySslProfile -Name "Profile01" -ApplicationGateway $AppGw
PS C:\> Remove-AzApplicationGatewayClientAuthConfiguration -SslProfile $profile
```

<span data-ttu-id="b911c-109">Det första kommandot får den Programgateway som heter ApplicationGateway01 i resurs gruppen som heter ResourceGroup01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="b911c-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="b911c-110">Det andra kommandot får den SSL-profil som heter Profile01 för $AppGw och lagrar den i $profile-variabeln.</span><span class="sxs-lookup"><span data-stu-id="b911c-110">The second command gets the SSL profile named Profile01 for $AppGw and stores it in the $profile variable.</span></span> <span data-ttu-id="b911c-111">Med det senaste kommandot tar du bort klientautentisering för den SSL-profil som lagras i $profile.</span><span class="sxs-lookup"><span data-stu-id="b911c-111">The last command removes the client authentication configuration of the ssl profile stored in $profile.</span></span>

## <span data-ttu-id="b911c-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b911c-112">PARAMETERS</span></span>

### <span data-ttu-id="b911c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b911c-113">-DefaultProfile</span></span>
<span data-ttu-id="b911c-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b911c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b911c-115">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="b911c-115">-SslProfile</span></span>
<span data-ttu-id="b911c-116">SSL-profil</span><span class="sxs-lookup"><span data-stu-id="b911c-116">The ssl profile</span></span>

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

### <span data-ttu-id="b911c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b911c-117">CommonParameters</span></span>
<span data-ttu-id="b911c-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b911c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b911c-119">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b911c-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b911c-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b911c-120">INPUTS</span></span>

### <span data-ttu-id="b911c-121">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="b911c-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="b911c-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b911c-122">OUTPUTS</span></span>

### <span data-ttu-id="b911c-123">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="b911c-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="b911c-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b911c-124">NOTES</span></span>

## <span data-ttu-id="b911c-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b911c-125">RELATED LINKS</span></span>

[<span data-ttu-id="b911c-126">New-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="b911c-126">New-AzApplicationGatewayClientAuthConfiguration</span></span>](./New-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="b911c-127">Add-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="b911c-127">Add-AzApplicationGatewayClientAuthConfiguration</span></span>](./Add-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="b911c-128">Get-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="b911c-128">Get-AzApplicationGatewayClientAuthConfiguration</span></span>](./Get-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="b911c-129">Set-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="b911c-129">Set-AzApplicationGatewayClientAuthConfiguration</span></span>](./Set-AzApplicationGatewayClientAuthConfiguration.md)
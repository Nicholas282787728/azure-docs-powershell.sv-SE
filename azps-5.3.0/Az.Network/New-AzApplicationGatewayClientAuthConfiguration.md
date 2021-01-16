---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayclientauthconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayClientAuthConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayClientAuthConfiguration.md
ms.openlocfilehash: 6e8c3cdbfa1242cba19d3aa3250c4bf4e381ae92
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98421936"
---
# <span data-ttu-id="7a40b-101">New-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="7a40b-101">New-AzApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="7a40b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7a40b-102">SYNOPSIS</span></span>
<span data-ttu-id="7a40b-103">Skapar en ny konfiguration för klientautentisering för SSL-profil.</span><span class="sxs-lookup"><span data-stu-id="7a40b-103">Creates a new client authentication configuration for SSL profile.</span></span>

## <span data-ttu-id="7a40b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7a40b-104">SYNTAX</span></span>

```
New-AzApplicationGatewayClientAuthConfiguration [-VerifyClientCertIssuerDN]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a40b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7a40b-105">DESCRIPTION</span></span>
<span data-ttu-id="7a40b-106">Cmdleten **New-AzApplicationGatewayClientAuthConfiguration** skapar en ny konfiguration för KLIENTAUTENTISERING för SSL-profil.</span><span class="sxs-lookup"><span data-stu-id="7a40b-106">The **New-AzApplicationGatewayClientAuthConfiguration** cmdlet creates a new client authentication configuration for SSL profile.</span></span>

## <span data-ttu-id="7a40b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7a40b-107">EXAMPLES</span></span>

### <span data-ttu-id="7a40b-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7a40b-108">Example 1</span></span>
```powershell
PS C:\> $clientAuthConfig = New-AzApplicationGatewayClientAuthConfiguration -VerifyClientCertIssuerDN
```

<span data-ttu-id="7a40b-109">Kommandot skapar en ny konfiguration för klientautentisering och lagrar den i $clientAuthConfig variabel som ska användas i en SSL-profil.</span><span class="sxs-lookup"><span data-stu-id="7a40b-109">The command create a new client auth configuration and stores it in $clientAuthConfig variable to be used in a SSL profile.</span></span> 

## <span data-ttu-id="7a40b-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7a40b-110">PARAMETERS</span></span>

### <span data-ttu-id="7a40b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a40b-111">-DefaultProfile</span></span>
<span data-ttu-id="7a40b-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7a40b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a40b-113">-VerifyClientCertIssuerDN</span><span class="sxs-lookup"><span data-stu-id="7a40b-113">-VerifyClientCertIssuerDN</span></span>
<span data-ttu-id="7a40b-114">Verifiera namnet på klient certifikat utfärdaren.</span><span class="sxs-lookup"><span data-stu-id="7a40b-114">Verify client certificate issuer name.</span></span>

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

### <span data-ttu-id="7a40b-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a40b-115">CommonParameters</span></span>
<span data-ttu-id="7a40b-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a40b-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a40b-117">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7a40b-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a40b-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7a40b-118">INPUTS</span></span>

### <span data-ttu-id="7a40b-119">Ingen</span><span class="sxs-lookup"><span data-stu-id="7a40b-119">None</span></span>

## <span data-ttu-id="7a40b-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7a40b-120">OUTPUTS</span></span>

### <span data-ttu-id="7a40b-121">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="7a40b-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="7a40b-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7a40b-122">NOTES</span></span>

## <span data-ttu-id="7a40b-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7a40b-123">RELATED LINKS</span></span>

[<span data-ttu-id="7a40b-124">Add-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="7a40b-124">Add-AzApplicationGatewayClientAuthConfiguration</span></span>](./Add-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="7a40b-125">Get-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="7a40b-125">Get-AzApplicationGatewayClientAuthConfiguration</span></span>](./Get-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="7a40b-126">Remove-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="7a40b-126">Remove-AzApplicationGatewayClientAuthConfiguration</span></span>](./Remove-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="7a40b-127">Set-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="7a40b-127">Set-AzApplicationGatewayClientAuthConfiguration</span></span>](./Set-AzApplicationGatewayClientAuthConfiguration.md)
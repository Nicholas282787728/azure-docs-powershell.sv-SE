---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: 99d56b837b67fe8b816c4f27c8658932a74452e7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522457"
---
# <span data-ttu-id="cfcb6-101">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="cfcb6-101">Get-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="cfcb6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cfcb6-102">SYNOPSIS</span></span>
<span data-ttu-id="cfcb6-103">Hämtar den betrodda klient certifikat utfärdarens certifikats kedja med ett visst namn från Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="cfcb6-103">Gets the trusted client CA certificate chain with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="cfcb6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cfcb6-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayTrustedClientCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cfcb6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cfcb6-105">DESCRIPTION</span></span>
<span data-ttu-id="cfcb6-106">Get-AzApplicationGatewayTrustedClientCertificate-cmdleten hämtar kedjan med betrodda klient certifikat utfärdare med ett visst namn från Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="cfcb6-106">The Get-AzApplicationGatewayTrustedClientCertificate cmdlet gets the trusted client CA certificate chain with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="cfcb6-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cfcb6-107">EXAMPLES</span></span>

### <span data-ttu-id="cfcb6-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="cfcb6-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $trustedClientCert = Get-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway $gw -Name $certName
```

<span data-ttu-id="cfcb6-109">Med det första kommandot hämtas programgatewayen och lagras i $gw variabel.</span><span class="sxs-lookup"><span data-stu-id="cfcb6-109">The first command gets the Application Gateway and stores it in $gw variable.</span></span> <span data-ttu-id="cfcb6-110">Det andra kommandot får den betrodda klient certifikat utfärdarens certifikat kedja med ett angivet namn från Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="cfcb6-110">The second command gets the trusted client CA certificate chain with a specified name from the Application Gateway.</span></span>

## <span data-ttu-id="cfcb6-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cfcb6-111">PARAMETERS</span></span>

### <span data-ttu-id="cfcb6-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cfcb6-112">-ApplicationGateway</span></span>
<span data-ttu-id="cfcb6-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cfcb6-113">The applicationGateway</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cfcb6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfcb6-114">-DefaultProfile</span></span>
<span data-ttu-id="cfcb6-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cfcb6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cfcb6-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="cfcb6-116">-Name</span></span>
<span data-ttu-id="cfcb6-117">Namnet på den betrodda klient certifikat utfärdarens certifikat kedja</span><span class="sxs-lookup"><span data-stu-id="cfcb6-117">The name of the trusted client CA certificate chain</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfcb6-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfcb6-118">CommonParameters</span></span>
<span data-ttu-id="cfcb6-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfcb6-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfcb6-120">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cfcb6-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfcb6-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cfcb6-121">INPUTS</span></span>

### <span data-ttu-id="cfcb6-122">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cfcb6-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="cfcb6-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cfcb6-123">OUTPUTS</span></span>

### <span data-ttu-id="cfcb6-124">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="cfcb6-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="cfcb6-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cfcb6-125">NOTES</span></span>

## <span data-ttu-id="cfcb6-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cfcb6-126">RELATED LINKS</span></span>

[<span data-ttu-id="cfcb6-127">New-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="cfcb6-127">New-AzApplicationGatewayTrustedClientCertificate</span></span>](./New-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="cfcb6-128">Add-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="cfcb6-128">Add-AzApplicationGatewayTrustedClientCertificate</span></span>](./Add-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="cfcb6-129">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="cfcb6-129">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>](./Remove-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="cfcb6-130">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="cfcb6-130">Set-AzApplicationGatewayTrustedClientCertificate</span></span>](./Set-AzApplicationGatewayTrustedClientCertificate.md)
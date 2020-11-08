---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 5c3976ddeeaa856f956ecb785a9d35e62ba322fb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93927289"
---
# <span data-ttu-id="a3dfd-101">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="a3dfd-101">Get-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="a3dfd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a3dfd-102">SYNOPSIS</span></span>
<span data-ttu-id="a3dfd-103">Hämtar det betrodda rot certifikatet med ett angivet namn från Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="a3dfd-103">Gets the Trusted Root Certificate with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="a3dfd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a3dfd-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayTrustedRootCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3dfd-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a3dfd-105">DESCRIPTION</span></span>
<span data-ttu-id="a3dfd-106">Cmdleten **Get-AzApplicationGatewayTrustedRootCertificate** hämtar ett betrott rot certifikat med ett specifikt namn från Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="a3dfd-106">The **Get-AzApplicationGatewayTrustedRootCertificate** cmdlet gets Trusted Root Certificate with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="a3dfd-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a3dfd-107">EXAMPLES</span></span>

### <span data-ttu-id="a3dfd-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a3dfd-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $trustedRootCert = Get-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\rootCA.cer"
```

<span data-ttu-id="a3dfd-109">Med det första kommandot hämtas programgatewayen och lagras i $gw variabel.</span><span class="sxs-lookup"><span data-stu-id="a3dfd-109">The first command gets the Application Gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="a3dfd-110">Det andra kommandot får det betrodda rot certifikatet med ett angivet namn från Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="a3dfd-110">The second command gets the Trusted Root Certificate with a specified name from the Application Gateway.</span></span>

## <span data-ttu-id="a3dfd-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a3dfd-111">PARAMETERS</span></span>

### <span data-ttu-id="a3dfd-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a3dfd-112">-ApplicationGateway</span></span>
<span data-ttu-id="a3dfd-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a3dfd-113">The applicationGateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3dfd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3dfd-114">-DefaultProfile</span></span>
<span data-ttu-id="a3dfd-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a3dfd-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3dfd-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="a3dfd-116">-Name</span></span>
<span data-ttu-id="a3dfd-117">Namnet på TrustedRoot-certifikatet</span><span class="sxs-lookup"><span data-stu-id="a3dfd-117">The name of the TrustedRoot certificate</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3dfd-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3dfd-118">CommonParameters</span></span>
<span data-ttu-id="a3dfd-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3dfd-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3dfd-120">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a3dfd-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3dfd-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a3dfd-121">INPUTS</span></span>

### <span data-ttu-id="a3dfd-122">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a3dfd-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a3dfd-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a3dfd-123">OUTPUTS</span></span>

### <span data-ttu-id="a3dfd-124">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="a3dfd-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="a3dfd-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a3dfd-125">NOTES</span></span>

## <span data-ttu-id="a3dfd-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a3dfd-126">RELATED LINKS</span></span>

[<span data-ttu-id="a3dfd-127">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="a3dfd-127">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="a3dfd-128">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="a3dfd-128">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="a3dfd-129">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="a3dfd-129">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="a3dfd-130">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="a3dfd-130">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)
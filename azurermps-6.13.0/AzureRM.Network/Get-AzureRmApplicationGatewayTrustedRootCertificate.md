---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: c37c55539f983b490c917e1fe062f14b252ee477
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756681"
---
# <span data-ttu-id="e7bd4-101">Get-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="e7bd4-101">Get-AzureRmApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="e7bd4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e7bd4-102">SYNOPSIS</span></span>
<span data-ttu-id="e7bd4-103">Hämtar det betrodda rot certifikatet med ett angivet namn från Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="e7bd4-103">Gets the Trusted Root Certificate with a specific name from the Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7bd4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e7bd4-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayTrustedRootCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7bd4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e7bd4-105">DESCRIPTION</span></span>
<span data-ttu-id="e7bd4-106">Cmdleten **Get-AzureRmApplicationGatewayTrustedRootCertificate** hämtar ett betrott rot certifikat med ett specifikt namn från Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="e7bd4-106">The **Get-AzureRmApplicationGatewayTrustedRootCertificate** cmdlet gets Trusted Root Certificate with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="e7bd4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e7bd4-107">EXAMPLES</span></span>

### <span data-ttu-id="e7bd4-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e7bd4-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzureRmApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $trustedRootCert = Get-AzureRmApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\rootCA.cer"
```

<span data-ttu-id="e7bd4-109">Med det första kommandot hämtas programgatewayen och lagras i $gw variabel.</span><span class="sxs-lookup"><span data-stu-id="e7bd4-109">The first command gets the Application Gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="e7bd4-110">Det andra kommandot får det betrodda rot certifikatet med ett angivet namn från Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="e7bd4-110">The second command gets the Trusted Root Certificate with a specified name from the Application Gateway.</span></span>

## <span data-ttu-id="e7bd4-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e7bd4-111">PARAMETERS</span></span>

### <span data-ttu-id="e7bd4-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e7bd4-112">-ApplicationGateway</span></span>
<span data-ttu-id="e7bd4-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e7bd4-113">The applicationGateway</span></span>

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

### <span data-ttu-id="e7bd4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7bd4-114">-DefaultProfile</span></span>
<span data-ttu-id="e7bd4-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e7bd4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7bd4-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="e7bd4-116">-Name</span></span>
<span data-ttu-id="e7bd4-117">Namnet på TrustedRoot-certifikatet</span><span class="sxs-lookup"><span data-stu-id="e7bd4-117">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="e7bd4-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7bd4-118">CommonParameters</span></span>
<span data-ttu-id="e7bd4-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7bd4-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7bd4-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7bd4-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7bd4-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e7bd4-121">INPUTS</span></span>

### <span data-ttu-id="e7bd4-122">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e7bd4-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e7bd4-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e7bd4-123">OUTPUTS</span></span>

### <span data-ttu-id="e7bd4-124">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="e7bd4-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="e7bd4-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e7bd4-125">NOTES</span></span>

## <span data-ttu-id="e7bd4-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e7bd4-126">RELATED LINKS</span></span>

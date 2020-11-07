---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: 320588b81791c033b94a07261f769fa0886d2f2c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922057"
---
# <span data-ttu-id="5f6ad-101">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="5f6ad-101">Remove-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="5f6ad-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5f6ad-102">SYNOPSIS</span></span>
<span data-ttu-id="5f6ad-103">Tar bort en hälso sökning från en befintlig Programgateway.</span><span class="sxs-lookup"><span data-stu-id="5f6ad-103">Removes a health probe from an existing application gateway.</span></span>

## <span data-ttu-id="5f6ad-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5f6ad-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayProbeConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f6ad-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5f6ad-105">DESCRIPTION</span></span>
<span data-ttu-id="5f6ad-106">Remove-AzApplicationGatewayProbeConfig cmdlet tar bort en Heath PROBE från en befintlig Programgateway.</span><span class="sxs-lookup"><span data-stu-id="5f6ad-106">The Remove-AzApplicationGatewayProbeConfig cmdlet removes a heath probe from an existing application gateway.</span></span>

## <span data-ttu-id="5f6ad-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5f6ad-107">EXAMPLES</span></span>

### <span data-ttu-id="5f6ad-108">Exempel 1: ta bort en hälso sökning från en befintlig Application Gateway</span><span class="sxs-lookup"><span data-stu-id="5f6ad-108">Example 1: Remove a health probe from an existing application gateway</span></span>
```
PS C:\>$Gateway = Remove-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe04"
```

<span data-ttu-id="5f6ad-109">Det här kommandot tar bort hälso avsökningen med namnet Probe04 från gatewayen för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="5f6ad-109">This command removes the health probe named Probe04 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="5f6ad-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5f6ad-110">PARAMETERS</span></span>

### <span data-ttu-id="5f6ad-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5f6ad-111">-ApplicationGateway</span></span>
<span data-ttu-id="5f6ad-112">Anger den Programgateway som denna cmdlet tar bort en sond för.</span><span class="sxs-lookup"><span data-stu-id="5f6ad-112">Specifies the application gateway to which this cmdlet removes a probe.</span></span>

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

### <span data-ttu-id="5f6ad-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f6ad-113">-DefaultProfile</span></span>
<span data-ttu-id="5f6ad-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5f6ad-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f6ad-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="5f6ad-115">-Name</span></span>
<span data-ttu-id="5f6ad-116">Anger namnet på den sond som cmdleten tas bort för.</span><span class="sxs-lookup"><span data-stu-id="5f6ad-116">Specifies the name of the probe for which this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f6ad-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f6ad-117">CommonParameters</span></span>
<span data-ttu-id="5f6ad-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f6ad-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f6ad-119">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f6ad-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f6ad-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5f6ad-120">INPUTS</span></span>

### <span data-ttu-id="5f6ad-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5f6ad-121">PSApplicationGateway</span></span>
<span data-ttu-id="5f6ad-122">Parametern ' ApplicationGateway ' godkänner värdet av typen ' PSApplicationGateway ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="5f6ad-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="5f6ad-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5f6ad-123">OUTPUTS</span></span>

### <span data-ttu-id="5f6ad-124">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5f6ad-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5f6ad-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5f6ad-125">NOTES</span></span>

## <span data-ttu-id="5f6ad-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5f6ad-126">RELATED LINKS</span></span>

[<span data-ttu-id="5f6ad-127">Ta bort en sond från en befintlig Application Gateway</span><span class="sxs-lookup"><span data-stu-id="5f6ad-127">Remove a probe from an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#remove-a-probe-from-an-existing-application-gateway)

[<span data-ttu-id="5f6ad-128">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="5f6ad-128">Add-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="5f6ad-129">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="5f6ad-129">Get-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="5f6ad-130">New-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="5f6ad-130">New-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="5f6ad-131">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="5f6ad-131">Set-AzApplicationGatewayProbeConfig</span></span>]()


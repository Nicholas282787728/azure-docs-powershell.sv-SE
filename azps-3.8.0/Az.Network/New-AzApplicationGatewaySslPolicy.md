---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 98FA4E95-CAC5-4FBD-AA84-113BE9ED7FEA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: 758dddc18e029aadd1e3d548d613a07abd7fd565
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092502"
---
# <span data-ttu-id="ccec6-101">New-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="ccec6-101">New-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="ccec6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ccec6-102">SYNOPSIS</span></span>
<span data-ttu-id="ccec6-103">Skapar en SSL-princip för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="ccec6-103">Creates an SSL policy for an application gateway.</span></span>

## <span data-ttu-id="ccec6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ccec6-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySslPolicy [-DisabledSslProtocols <String[]>] [-PolicyType <String>]
 [-PolicyName <String>] [-CipherSuite <String[]>] [-MinProtocolVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ccec6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ccec6-105">DESCRIPTION</span></span>
<span data-ttu-id="ccec6-106">Cmdleten **New-AzApplicationGatewaySslPolicy** skapar en SSL-princip för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="ccec6-106">The **New-AzApplicationGatewaySslPolicy** cmdlet creates an SSL policy for an application gateway.</span></span>

## <span data-ttu-id="ccec6-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ccec6-107">EXAMPLES</span></span>

### <span data-ttu-id="ccec6-108">9.1</span><span class="sxs-lookup"><span data-stu-id="ccec6-108">1:</span></span>
```
PS C:\>$sslPolicy = New-AzApplicationGatewaySslPolicy -PolicyType Custom -MinProtocolVersion TLSv1_1 -CipherSuite "TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256", "TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384", "TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA", "TLS_RSA_WITH_AES_128_GCM_SHA256"
```

<span data-ttu-id="ccec6-109">Det här kommandot skapar en anpassad princip.</span><span class="sxs-lookup"><span data-stu-id="ccec6-109">This command creates a custom policy.</span></span>

## <span data-ttu-id="ccec6-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ccec6-110">PARAMETERS</span></span>

### <span data-ttu-id="ccec6-111">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="ccec6-111">-CipherSuite</span></span>
<span data-ttu-id="ccec6-112">SSL-chiffersviter kan aktive ras i angiven ordning för Programgateway</span><span class="sxs-lookup"><span data-stu-id="ccec6-112">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccec6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccec6-113">-DefaultProfile</span></span>
<span data-ttu-id="ccec6-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ccec6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ccec6-115">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="ccec6-115">-DisabledSslProtocols</span></span>
<span data-ttu-id="ccec6-116">Anger vilka protokoll som är inaktiverade.</span><span class="sxs-lookup"><span data-stu-id="ccec6-116">Specifies which protocols are disabled.</span></span>
<span data-ttu-id="ccec6-117">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="ccec6-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ccec6-118">TLSv1_0</span><span class="sxs-lookup"><span data-stu-id="ccec6-118">TLSv1_0</span></span> 
- <span data-ttu-id="ccec6-119">TLSv1_1</span><span class="sxs-lookup"><span data-stu-id="ccec6-119">TLSv1_1</span></span> 
- <span data-ttu-id="ccec6-120">TLSv1_2</span><span class="sxs-lookup"><span data-stu-id="ccec6-120">TLSv1_2</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: TLSv1_0, TLSv1_1, TLSv1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccec6-121">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="ccec6-121">-MinProtocolVersion</span></span>
<span data-ttu-id="ccec6-122">Minsta version av SSL-protokoll som stöds på Application Gateway</span><span class="sxs-lookup"><span data-stu-id="ccec6-122">Minimum version of Ssl protocol to be supported on application gateway</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: TLSv1_0, TLSv1_1, TLSv1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccec6-123">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="ccec6-123">-PolicyName</span></span>
<span data-ttu-id="ccec6-124">Namn på den fördefinierade SSL-principen</span><span class="sxs-lookup"><span data-stu-id="ccec6-124">Name of Ssl predefined policy</span></span>

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

### <span data-ttu-id="ccec6-125">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="ccec6-125">-PolicyType</span></span>
<span data-ttu-id="ccec6-126">Typ av SSL-princip</span><span class="sxs-lookup"><span data-stu-id="ccec6-126">Type of Ssl Policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Predefined, Custom

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccec6-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ccec6-127">-Confirm</span></span>
<span data-ttu-id="ccec6-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ccec6-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccec6-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ccec6-129">-WhatIf</span></span>
<span data-ttu-id="ccec6-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ccec6-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ccec6-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ccec6-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccec6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccec6-132">CommonParameters</span></span>
<span data-ttu-id="ccec6-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ccec6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccec6-134">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccec6-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccec6-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ccec6-135">INPUTS</span></span>

### <span data-ttu-id="ccec6-136">Ingen</span><span class="sxs-lookup"><span data-stu-id="ccec6-136">None</span></span>

## <span data-ttu-id="ccec6-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ccec6-137">OUTPUTS</span></span>

### <span data-ttu-id="ccec6-138">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="ccec6-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="ccec6-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ccec6-139">NOTES</span></span>
* <span data-ttu-id="ccec6-140">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk</span><span class="sxs-lookup"><span data-stu-id="ccec6-140">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="ccec6-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ccec6-141">RELATED LINKS</span></span>

[<span data-ttu-id="ccec6-142">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="ccec6-142">Get-AzApplicationGatewaySslPolicy</span></span>](./Get-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="ccec6-143">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="ccec6-143">Set-AzApplicationGatewaySslPolicy</span></span>](./Set-AzApplicationGatewaySslPolicy.md)



---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 98FA4E95-CAC5-4FBD-AA84-113BE9ED7FEA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewaySslPolicy.md
ms.openlocfilehash: 140bfd84d2758badc45a902e4ed14e027c5bca3e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585932"
---
# <span data-ttu-id="bd838-101">New-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="bd838-101">New-AzureRmApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="bd838-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bd838-102">SYNOPSIS</span></span>
<span data-ttu-id="bd838-103">Skapar en SSL-princip för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="bd838-103">Creates an SSL policy for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd838-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bd838-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewaySslPolicy
 [-DisabledSslProtocols <System.Collections.Generic.List`1[System.String]>] [-PolicyType <String>]
 [-PolicyName <String>] [-CipherSuite <System.Collections.Generic.List`1[System.String]>]
 [-MinProtocolVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bd838-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bd838-105">DESCRIPTION</span></span>
<span data-ttu-id="bd838-106">Cmdleten **New-AzureRmApplicationGatewaySslPolicy** skapar en SSL-princip för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="bd838-106">The **New-AzureRmApplicationGatewaySslPolicy** cmdlet creates an SSL policy for an application gateway.</span></span>

## <span data-ttu-id="bd838-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bd838-107">EXAMPLES</span></span>

### <span data-ttu-id="bd838-108">9.1</span><span class="sxs-lookup"><span data-stu-id="bd838-108">1:</span></span>
```
PS C:\>$sslPolicy = New-AzureRmApplicationGatewaySslPolicy -PolicyType Custom -MinProtocolVersion TLSv1_1 -CipherSuite "TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256", "TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384", "TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA", "TLS_RSA_WITH_AES_128_GCM_SHA256"
```

<span data-ttu-id="bd838-109">Det här kommandot skapar en anpassad princip.</span><span class="sxs-lookup"><span data-stu-id="bd838-109">This command creates a custom policy.</span></span>

## <span data-ttu-id="bd838-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bd838-110">PARAMETERS</span></span>

### <span data-ttu-id="bd838-111">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="bd838-111">-CipherSuite</span></span>
<span data-ttu-id="bd838-112">SSL-chiffersviter kan aktive ras i angiven ordning för Programgateway</span><span class="sxs-lookup"><span data-stu-id="bd838-112">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd838-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd838-113">-DefaultProfile</span></span>
<span data-ttu-id="bd838-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bd838-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd838-115">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="bd838-115">-DisabledSslProtocols</span></span>
<span data-ttu-id="bd838-116">Anger vilka protokoll som är inaktiverade.</span><span class="sxs-lookup"><span data-stu-id="bd838-116">Specifies which protocols are disabled.</span></span>
<span data-ttu-id="bd838-117">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="bd838-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bd838-118">TLSv1_0</span><span class="sxs-lookup"><span data-stu-id="bd838-118">TLSv1_0</span></span> 
- <span data-ttu-id="bd838-119">TLSv1_1</span><span class="sxs-lookup"><span data-stu-id="bd838-119">TLSv1_1</span></span> 
- <span data-ttu-id="bd838-120">TLSv1_2</span><span class="sxs-lookup"><span data-stu-id="bd838-120">TLSv1_2</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:
Accepted values: TLSv1_0, TLSv1_1, TLSv1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd838-121">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="bd838-121">-MinProtocolVersion</span></span>
<span data-ttu-id="bd838-122">Minsta version av SSL-protokoll som stöds på Application Gateway</span><span class="sxs-lookup"><span data-stu-id="bd838-122">Minimum version of Ssl protocol to be supported on application gateway</span></span>

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

### <span data-ttu-id="bd838-123">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="bd838-123">-PolicyName</span></span>
<span data-ttu-id="bd838-124">Namn på den fördefinierade SSL-principen</span><span class="sxs-lookup"><span data-stu-id="bd838-124">Name of Ssl predefined policy</span></span>

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

### <span data-ttu-id="bd838-125">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="bd838-125">-PolicyType</span></span>
<span data-ttu-id="bd838-126">Typ av SSL-princip</span><span class="sxs-lookup"><span data-stu-id="bd838-126">Type of Ssl Policy</span></span>

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

### <span data-ttu-id="bd838-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bd838-127">-Confirm</span></span>
<span data-ttu-id="bd838-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bd838-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd838-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd838-129">-WhatIf</span></span>
<span data-ttu-id="bd838-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bd838-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd838-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bd838-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd838-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd838-132">CommonParameters</span></span>
<span data-ttu-id="bd838-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd838-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd838-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd838-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd838-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bd838-135">INPUTS</span></span>

### <span data-ttu-id="bd838-136">Ingen</span><span class="sxs-lookup"><span data-stu-id="bd838-136">None</span></span>

## <span data-ttu-id="bd838-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bd838-137">OUTPUTS</span></span>

### <span data-ttu-id="bd838-138">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="bd838-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="bd838-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bd838-139">NOTES</span></span>
* <span data-ttu-id="bd838-140">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk</span><span class="sxs-lookup"><span data-stu-id="bd838-140">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="bd838-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bd838-141">RELATED LINKS</span></span>

[<span data-ttu-id="bd838-142">Get-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="bd838-142">Get-AzureRmApplicationGatewaySslPolicy</span></span>](./Get-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="bd838-143">Set-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="bd838-143">Set-AzureRmApplicationGatewaySslPolicy</span></span>](./Set-AzureRmApplicationGatewaySslPolicy.md)



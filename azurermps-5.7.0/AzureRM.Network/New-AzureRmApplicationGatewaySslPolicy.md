---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 98FA4E95-CAC5-4FBD-AA84-113BE9ED7FEA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewaySslPolicy.md
ms.openlocfilehash: 3887f8cdbc4256d39e76fc6b86ff9e9113385519
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/21/2020
ms.locfileid: "93586600"
---
# <span data-ttu-id="71fea-101">New-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="71fea-101">New-AzureRmApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="71fea-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="71fea-102">SYNOPSIS</span></span>
<span data-ttu-id="71fea-103">Skapar en SSL-princip för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="71fea-103">Creates an SSL policy for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71fea-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="71fea-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewaySslPolicy
 [-DisabledSslProtocols <System.Collections.Generic.List`1[System.String]>] [-PolicyType <String>]
 [-PolicyName <String>] [-CipherSuite <System.Collections.Generic.List`1[System.String]>]
 [-MinProtocolVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="71fea-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="71fea-105">DESCRIPTION</span></span>
<span data-ttu-id="71fea-106">Cmdleten **New-AzureRmApplicationGatewaySslPolicy** skapar en SSL-princip för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="71fea-106">The **New-AzureRmApplicationGatewaySslPolicy** cmdlet creates an SSL policy for an application gateway.</span></span>

## <span data-ttu-id="71fea-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="71fea-107">EXAMPLES</span></span>

### <span data-ttu-id="71fea-108">9.1</span><span class="sxs-lookup"><span data-stu-id="71fea-108">1:</span></span>
```
PS C:\>$sslPolicy = New-AzureRmApplicationGatewaySslPolicy -PolicyType Custom -MinProtocolVersion TLSv1_1 -CipherSuite "TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256", "TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384", "TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA", "TLS_RSA_WITH_AES_128_GCM_SHA256"
```

<span data-ttu-id="71fea-109">Det här kommandot skapar en anpassad princip.</span><span class="sxs-lookup"><span data-stu-id="71fea-109">This command creates a custom policy.</span></span>

## <span data-ttu-id="71fea-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="71fea-110">PARAMETERS</span></span>

### <span data-ttu-id="71fea-111">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="71fea-111">-CipherSuite</span></span>
<span data-ttu-id="71fea-112">SSL-chiffersviter kan aktive ras i angiven ordning för Programgateway</span><span class="sxs-lookup"><span data-stu-id="71fea-112">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

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

### <span data-ttu-id="71fea-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71fea-113">-DefaultProfile</span></span>
<span data-ttu-id="71fea-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="71fea-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71fea-115">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="71fea-115">-DisabledSslProtocols</span></span>
<span data-ttu-id="71fea-116">Anger vilka protokoll som är inaktiverade.</span><span class="sxs-lookup"><span data-stu-id="71fea-116">Specifies which protocols are disabled.</span></span>
<span data-ttu-id="71fea-117">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="71fea-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="71fea-118">TLSv1_0</span><span class="sxs-lookup"><span data-stu-id="71fea-118">TLSv1_0</span></span> 
- <span data-ttu-id="71fea-119">TLSv1_1</span><span class="sxs-lookup"><span data-stu-id="71fea-119">TLSv1_1</span></span> 
- <span data-ttu-id="71fea-120">TLSv1_2</span><span class="sxs-lookup"><span data-stu-id="71fea-120">TLSv1_2</span></span>

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

### <span data-ttu-id="71fea-121">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="71fea-121">-MinProtocolVersion</span></span>
<span data-ttu-id="71fea-122">Minsta version av SSL-protokoll som stöds på Application Gateway</span><span class="sxs-lookup"><span data-stu-id="71fea-122">Minimum version of Ssl protocol to be supported on application gateway</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: TLSv1_0, TLSv1_1, TLSv1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71fea-123">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="71fea-123">-PolicyName</span></span>
<span data-ttu-id="71fea-124">Namn på den fördefinierade SSL-principen</span><span class="sxs-lookup"><span data-stu-id="71fea-124">Name of Ssl predefined policy</span></span>

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

### <span data-ttu-id="71fea-125">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="71fea-125">-PolicyType</span></span>
<span data-ttu-id="71fea-126">Typ av SSL-princip</span><span class="sxs-lookup"><span data-stu-id="71fea-126">Type of Ssl Policy</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Predefined, Custom

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71fea-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="71fea-127">-Confirm</span></span>
<span data-ttu-id="71fea-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="71fea-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71fea-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71fea-129">-WhatIf</span></span>
<span data-ttu-id="71fea-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="71fea-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71fea-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="71fea-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71fea-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71fea-132">CommonParameters</span></span>
<span data-ttu-id="71fea-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71fea-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71fea-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71fea-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71fea-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="71fea-135">INPUTS</span></span>

### <span data-ttu-id="71fea-136">System. String</span><span class="sxs-lookup"><span data-stu-id="71fea-136">System.String</span></span>

## <span data-ttu-id="71fea-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="71fea-137">OUTPUTS</span></span>

### <span data-ttu-id="71fea-138">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="71fea-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="71fea-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="71fea-139">NOTES</span></span>
* <span data-ttu-id="71fea-140">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk</span><span class="sxs-lookup"><span data-stu-id="71fea-140">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="71fea-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="71fea-141">RELATED LINKS</span></span>

[<span data-ttu-id="71fea-142">Get-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="71fea-142">Get-AzureRmApplicationGatewaySslPolicy</span></span>](./Get-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="71fea-143">Set-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="71fea-143">Set-AzureRmApplicationGatewaySslPolicy</span></span>](./Set-AzureRmApplicationGatewaySslPolicy.md)



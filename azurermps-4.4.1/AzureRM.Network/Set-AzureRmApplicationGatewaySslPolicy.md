---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 30A34CA8-AC07-4327-B7B9-19F001DA996A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySslPolicy.md
ms.openlocfilehash: 984556937e57d710b9f62d80f20f7f30955865ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575982"
---
# <span data-ttu-id="a534c-101">Set-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="a534c-101">Set-AzureRmApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="a534c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a534c-102">SYNOPSIS</span></span>
<span data-ttu-id="a534c-103">Ändrar SSL-principen för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="a534c-103">Modifies the SSL policy of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a534c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a534c-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway>
 [-DisabledSslProtocols <System.Collections.Generic.List`1[System.String]>] [-PolicyType <String>]
 [-PolicyName <String>] [-CipherSuite <System.Collections.Generic.List`1[System.String]>]
 [-MinProtocolVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a534c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a534c-105">DESCRIPTION</span></span>
<span data-ttu-id="a534c-106">Cmdleten **set-AzureRmApplicationGatewaySslPolicy** ändrar SSL-principen för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="a534c-106">The **Set-AzureRmApplicationGatewaySslPolicy** cmdlet modifies the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="a534c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a534c-107">EXAMPLES</span></span>

### <span data-ttu-id="a534c-108">9.1</span><span class="sxs-lookup"><span data-stu-id="a534c-108">1:</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewaySslPolicy -ApplicationGateway $getgw -PolicyType Predefined -PolicyName AppGwSslPolicy20170401
```

<span data-ttu-id="a534c-109">Det första kommandot får programgatewayen som heter ApplicationGateway01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="a534c-109">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="a534c-110">Med det här andra kommandot ändras SSL-principen till en princip typ som fördefinierat och princip namn AppGwSslPolicy20170401.</span><span class="sxs-lookup"><span data-stu-id="a534c-110">This second command modifies the ssl policy to a policy type Predefined and policy name AppGwSslPolicy20170401.</span></span>

## <span data-ttu-id="a534c-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a534c-111">PARAMETERS</span></span>

### <span data-ttu-id="a534c-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a534c-112">-ApplicationGateway</span></span>
<span data-ttu-id="a534c-113">Anger Application Gateway för SSL-policyn som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="a534c-113">Specifies the application gateway of the SSL policy that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="a534c-114">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="a534c-114">-CipherSuite</span></span>
<span data-ttu-id="a534c-115">SSL-chiffersviter kan aktive ras i angiven ordning för Programgateway</span><span class="sxs-lookup"><span data-stu-id="a534c-115">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

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

### <span data-ttu-id="a534c-116">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="a534c-116">-DisabledSslProtocols</span></span>
<span data-ttu-id="a534c-117">Anger vilka protokoll som är inaktiverade.</span><span class="sxs-lookup"><span data-stu-id="a534c-117">Specifies which protocols are disabled.</span></span>
<span data-ttu-id="a534c-118">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="a534c-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a534c-119">TLSv1_0</span><span class="sxs-lookup"><span data-stu-id="a534c-119">TLSv1_0</span></span> 
- <span data-ttu-id="a534c-120">TLSv1_1</span><span class="sxs-lookup"><span data-stu-id="a534c-120">TLSv1_1</span></span> 
- <span data-ttu-id="a534c-121">TLSv1_2</span><span class="sxs-lookup"><span data-stu-id="a534c-121">TLSv1_2</span></span>

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

### <span data-ttu-id="a534c-122">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="a534c-122">-MinProtocolVersion</span></span>
<span data-ttu-id="a534c-123">Minsta version av SSL-protokoll som stöds på Application Gateway</span><span class="sxs-lookup"><span data-stu-id="a534c-123">Minimum version of Ssl protocol to be supported on application gateway</span></span>

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

### <span data-ttu-id="a534c-124">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="a534c-124">-PolicyName</span></span>
<span data-ttu-id="a534c-125">Namn på den fördefinierade SSL-principen</span><span class="sxs-lookup"><span data-stu-id="a534c-125">Name of Ssl predefined policy</span></span>

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

### <span data-ttu-id="a534c-126">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="a534c-126">-PolicyType</span></span>
<span data-ttu-id="a534c-127">Typ av SSL-princip</span><span class="sxs-lookup"><span data-stu-id="a534c-127">Type of Ssl Policy</span></span>

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

### <span data-ttu-id="a534c-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a534c-128">-Confirm</span></span>
<span data-ttu-id="a534c-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a534c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a534c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a534c-130">-WhatIf</span></span>
<span data-ttu-id="a534c-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a534c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a534c-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a534c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a534c-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a534c-133">-DefaultProfile</span></span>
<span data-ttu-id="a534c-134">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a534c-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a534c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a534c-135">CommonParameters</span></span>
<span data-ttu-id="a534c-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a534c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a534c-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a534c-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a534c-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a534c-138">INPUTS</span></span>

### <span data-ttu-id="a534c-139">System. String</span><span class="sxs-lookup"><span data-stu-id="a534c-139">System.String</span></span>

## <span data-ttu-id="a534c-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a534c-140">OUTPUTS</span></span>

### <span data-ttu-id="a534c-141">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a534c-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a534c-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a534c-142">NOTES</span></span>
* <span data-ttu-id="a534c-143">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk</span><span class="sxs-lookup"><span data-stu-id="a534c-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="a534c-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a534c-144">RELATED LINKS</span></span>

[<span data-ttu-id="a534c-145">Get-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="a534c-145">Get-AzureRmApplicationGatewaySslPolicy</span></span>](./Get-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="a534c-146">New-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="a534c-146">New-AzureRmApplicationGatewaySslPolicy</span></span>](./New-AzureRmApplicationGatewaySslPolicy.md)



---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 30A34CA8-AC07-4327-B7B9-19F001DA996A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySslPolicy.md
ms.openlocfilehash: 7ab968539cb57568540a0e1c60f59b36d6de79ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574885"
---
# <span data-ttu-id="f283a-101">Set-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="f283a-101">Set-AzureRmApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="f283a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f283a-102">SYNOPSIS</span></span>
<span data-ttu-id="f283a-103">Ändrar SSL-principen för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="f283a-103">Modifies the SSL policy of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f283a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f283a-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway>
 [-DisabledSslProtocols <System.Collections.Generic.List`1[System.String]>] [-PolicyType <String>]
 [-PolicyName <String>] [-CipherSuite <System.Collections.Generic.List`1[System.String]>]
 [-MinProtocolVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f283a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f283a-105">DESCRIPTION</span></span>
<span data-ttu-id="f283a-106">Cmdleten **set-AzureRmApplicationGatewaySslPolicy** ändrar SSL-principen för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="f283a-106">The **Set-AzureRmApplicationGatewaySslPolicy** cmdlet modifies the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="f283a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f283a-107">EXAMPLES</span></span>

### <span data-ttu-id="f283a-108">9.1</span><span class="sxs-lookup"><span data-stu-id="f283a-108">1:</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewaySslPolicy -ApplicationGateway $getgw -PolicyType Predefined -PolicyName AppGwSslPolicy20170401
```

<span data-ttu-id="f283a-109">Det första kommandot får programgatewayen som heter ApplicationGateway01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="f283a-109">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="f283a-110">Med det här andra kommandot ändras SSL-principen till en princip typ som fördefinierat och princip namn AppGwSslPolicy20170401.</span><span class="sxs-lookup"><span data-stu-id="f283a-110">This second command modifies the ssl policy to a policy type Predefined and policy name AppGwSslPolicy20170401.</span></span>

## <span data-ttu-id="f283a-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f283a-111">PARAMETERS</span></span>

### <span data-ttu-id="f283a-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f283a-112">-ApplicationGateway</span></span>
<span data-ttu-id="f283a-113">Anger Application Gateway för SSL-policyn som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="f283a-113">Specifies the application gateway of the SSL policy that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="f283a-114">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="f283a-114">-CipherSuite</span></span>
<span data-ttu-id="f283a-115">SSL-chiffersviter kan aktive ras i angiven ordning för Programgateway</span><span class="sxs-lookup"><span data-stu-id="f283a-115">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

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

### <span data-ttu-id="f283a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f283a-116">-DefaultProfile</span></span>
<span data-ttu-id="f283a-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f283a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f283a-118">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="f283a-118">-DisabledSslProtocols</span></span>
<span data-ttu-id="f283a-119">Anger vilka protokoll som är inaktiverade.</span><span class="sxs-lookup"><span data-stu-id="f283a-119">Specifies which protocols are disabled.</span></span>
<span data-ttu-id="f283a-120">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="f283a-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f283a-121">TLSv1_0</span><span class="sxs-lookup"><span data-stu-id="f283a-121">TLSv1_0</span></span> 
- <span data-ttu-id="f283a-122">TLSv1_1</span><span class="sxs-lookup"><span data-stu-id="f283a-122">TLSv1_1</span></span> 
- <span data-ttu-id="f283a-123">TLSv1_2</span><span class="sxs-lookup"><span data-stu-id="f283a-123">TLSv1_2</span></span>

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

### <span data-ttu-id="f283a-124">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="f283a-124">-MinProtocolVersion</span></span>
<span data-ttu-id="f283a-125">Minsta version av SSL-protokoll som stöds på Application Gateway</span><span class="sxs-lookup"><span data-stu-id="f283a-125">Minimum version of Ssl protocol to be supported on application gateway</span></span>

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

### <span data-ttu-id="f283a-126">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="f283a-126">-PolicyName</span></span>
<span data-ttu-id="f283a-127">Namn på den fördefinierade SSL-principen</span><span class="sxs-lookup"><span data-stu-id="f283a-127">Name of Ssl predefined policy</span></span>

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

### <span data-ttu-id="f283a-128">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="f283a-128">-PolicyType</span></span>
<span data-ttu-id="f283a-129">Typ av SSL-princip</span><span class="sxs-lookup"><span data-stu-id="f283a-129">Type of Ssl Policy</span></span>

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

### <span data-ttu-id="f283a-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f283a-130">-Confirm</span></span>
<span data-ttu-id="f283a-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f283a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f283a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f283a-132">-WhatIf</span></span>
<span data-ttu-id="f283a-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f283a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f283a-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f283a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f283a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f283a-135">CommonParameters</span></span>
<span data-ttu-id="f283a-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f283a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f283a-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f283a-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f283a-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f283a-138">INPUTS</span></span>

### <span data-ttu-id="f283a-139">System. String</span><span class="sxs-lookup"><span data-stu-id="f283a-139">System.String</span></span>

## <span data-ttu-id="f283a-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f283a-140">OUTPUTS</span></span>

### <span data-ttu-id="f283a-141">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f283a-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f283a-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f283a-142">NOTES</span></span>
* <span data-ttu-id="f283a-143">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk</span><span class="sxs-lookup"><span data-stu-id="f283a-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="f283a-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f283a-144">RELATED LINKS</span></span>

[<span data-ttu-id="f283a-145">Get-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="f283a-145">Get-AzureRmApplicationGatewaySslPolicy</span></span>](./Get-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="f283a-146">New-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="f283a-146">New-AzureRmApplicationGatewaySslPolicy</span></span>](./New-AzureRmApplicationGatewaySslPolicy.md)



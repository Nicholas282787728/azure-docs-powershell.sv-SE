---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaysslprofilepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslProfilePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslProfilePolicy.md
ms.openlocfilehash: 344be8b71bc74f3620ca90dd60b61f9a59026ea0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525805"
---
# <span data-ttu-id="13c2a-101">Set-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="13c2a-101">Set-AzApplicationGatewaySslProfilePolicy</span></span>

## <span data-ttu-id="13c2a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="13c2a-102">SYNOPSIS</span></span>
<span data-ttu-id="13c2a-103">Ändrar SSL-principen för en Application Gateway SSL-profil.</span><span class="sxs-lookup"><span data-stu-id="13c2a-103">Modifies the SSL policy of an application gateway SSL profile.</span></span>

## <span data-ttu-id="13c2a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="13c2a-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySslProfilePolicy -SslProfile <PSApplicationGatewaySslProfile>
 [-DisabledSslProtocols <String[]>] [-PolicyType <String>] [-PolicyName <String>] [-CipherSuite <String[]>]
 [-MinProtocolVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="13c2a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="13c2a-105">DESCRIPTION</span></span>
<span data-ttu-id="13c2a-106">Cmdleten **set-AzApplicationGatewaySslProfilePolicy** ändrar SSL-principen för en SSL-profil för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="13c2a-106">The **Set-AzApplicationGatewaySslProfilePolicy** cmdlet modifies the SSL policy of an application gateway SSL profile.</span></span>

## <span data-ttu-id="13c2a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="13c2a-107">EXAMPLES</span></span>

### <span data-ttu-id="13c2a-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="13c2a-108">Example 1</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $profile  = Get-AzApplicationGatewaySslProfile -Name "SslProfile01" -ApplicationGateway $AppGw
PS C:\> $profile = Set-AzApplicationGatewaySslProfilePolicy -SslProfile $profile -PolicyType Predefined -PolicyName AppGwSslPolicy20170401
```

<span data-ttu-id="13c2a-109">Det första kommandot får den Programgateway som heter ApplicationGateway01 i resurs gruppen som heter ResourceGroup01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="13c2a-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="13c2a-110">Det andra kommandot får den SSL-profil som heter SslProfile01 för $AppGw och lagrar inställningarna i $profile-variabeln.</span><span class="sxs-lookup"><span data-stu-id="13c2a-110">The second command gets the ssl profile named SslProfile01 for $AppGw and stores the settings in the $profile variable.</span></span> <span data-ttu-id="13c2a-111">Det senaste kommandot ändrar SSL-principen för det SSL-profil objekt som lagras i $profile.</span><span class="sxs-lookup"><span data-stu-id="13c2a-111">The last command modifies the ssl policy of the ssl profile object stored in $profile.</span></span>

## <span data-ttu-id="13c2a-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="13c2a-112">PARAMETERS</span></span>

### <span data-ttu-id="13c2a-113">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="13c2a-113">-CipherSuite</span></span>
<span data-ttu-id="13c2a-114">SSL-chiffersviter kan aktive ras i angiven ordning för Programgateway</span><span class="sxs-lookup"><span data-stu-id="13c2a-114">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13c2a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13c2a-115">-DefaultProfile</span></span>
<span data-ttu-id="13c2a-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="13c2a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13c2a-117">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="13c2a-117">-DisabledSslProtocols</span></span>
<span data-ttu-id="13c2a-118">Lista över SSL-protokoll som ska inaktive ras</span><span class="sxs-lookup"><span data-stu-id="13c2a-118">List of SSL protocols to be disabled</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:
Accepted values: TLSv1_0, TLSv1_1, TLSv1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13c2a-119">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="13c2a-119">-MinProtocolVersion</span></span>
<span data-ttu-id="13c2a-120">Minsta version av SSL-protokoll som stöds på Application Gateway</span><span class="sxs-lookup"><span data-stu-id="13c2a-120">Minimum version of Ssl protocol to be supported on application gateway</span></span>

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

### <span data-ttu-id="13c2a-121">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="13c2a-121">-PolicyName</span></span>
<span data-ttu-id="13c2a-122">Namn på den fördefinierade SSL-principen</span><span class="sxs-lookup"><span data-stu-id="13c2a-122">Name of Ssl predefined policy</span></span>

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

### <span data-ttu-id="13c2a-123">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="13c2a-123">-PolicyType</span></span>
<span data-ttu-id="13c2a-124">Typ av SSL-princip</span><span class="sxs-lookup"><span data-stu-id="13c2a-124">Type of Ssl Policy</span></span>

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

### <span data-ttu-id="13c2a-125">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="13c2a-125">-SslProfile</span></span>
<span data-ttu-id="13c2a-126">SSL-profilen för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="13c2a-126">The application gateway SSL profile</span></span>

```yaml
Type: PSApplicationGatewaySslProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13c2a-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="13c2a-127">-Confirm</span></span>
<span data-ttu-id="13c2a-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="13c2a-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13c2a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13c2a-129">-WhatIf</span></span>
<span data-ttu-id="13c2a-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="13c2a-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13c2a-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="13c2a-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13c2a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13c2a-132">CommonParameters</span></span>
<span data-ttu-id="13c2a-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13c2a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13c2a-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="13c2a-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13c2a-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="13c2a-135">INPUTS</span></span>

### <span data-ttu-id="13c2a-136">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="13c2a-136">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="13c2a-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="13c2a-137">OUTPUTS</span></span>

### <span data-ttu-id="13c2a-138">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="13c2a-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="13c2a-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="13c2a-139">NOTES</span></span>

## <span data-ttu-id="13c2a-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="13c2a-140">RELATED LINKS</span></span>

[<span data-ttu-id="13c2a-141">Add-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="13c2a-141">Add-AzApplicationGatewaySslProfilePolicy</span></span>](./Add-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="13c2a-142">New-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="13c2a-142">New-AzApplicationGatewaySslProfilePolicy</span></span>](./New-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="13c2a-143">Get-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="13c2a-143">Get-AzApplicationGatewaySslProfilePolicy</span></span>](./Get-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="13c2a-144">Remove-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="13c2a-144">Remove-AzApplicationGatewaySslProfilePolicy</span></span>](./Remove-AzApplicationGatewaySslProfilePolicy.md)
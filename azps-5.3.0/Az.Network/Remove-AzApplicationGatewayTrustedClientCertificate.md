---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: 40f31fc2c8cc4d0cb3a9637b39d8c3fcbd18ee42
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525824"
---
# <span data-ttu-id="8bd99-101">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="8bd99-101">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="8bd99-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8bd99-102">SYNOPSIS</span></span>
<span data-ttu-id="8bd99-103">Tar bort kedje objekt för Trusted client-certifikatutfärdare från en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="8bd99-103">Removes the trusted client CA certificate chain object from an application gateway.</span></span>

## <span data-ttu-id="8bd99-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8bd99-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayTrustedClientCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8bd99-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8bd99-105">DESCRIPTION</span></span>
<span data-ttu-id="8bd99-106">Cmdleten **Remove-AzApplicationGatewayTrustedClientCertificate** tar bort kedje objekt för Trusted client-certifikatutfärdare från en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="8bd99-106">The **Remove-AzApplicationGatewayTrustedClientCertificate** cmdlet removes the trusted client CA certificate chain object from an application gateway.</span></span>

## <span data-ttu-id="8bd99-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8bd99-107">EXAMPLES</span></span>

### <span data-ttu-id="8bd99-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8bd99-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Remove-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway $gw -Name "TrustedClientCertificate01"
```

<span data-ttu-id="8bd99-109">Det första kommandot får en Programgateway och lagrar den i $gw variabeln.</span><span class="sxs-lookup"><span data-stu-id="8bd99-109">The first command gets an application gateway and stores it in the $gw variable.</span></span> <span data-ttu-id="8bd99-110">Det andra kommandot tar bort den betrodda klient certifikat utfärdarens certifikat kedja med namnet "TrustedClientCertificate01" från Application Gateway som lagras i $gw.</span><span class="sxs-lookup"><span data-stu-id="8bd99-110">The second command removes the trusted client CA certificate chain named "TrustedClientCertificate01" from the application gateway stored in $gw.</span></span>

## <span data-ttu-id="8bd99-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8bd99-111">PARAMETERS</span></span>

### <span data-ttu-id="8bd99-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8bd99-112">-ApplicationGateway</span></span>
<span data-ttu-id="8bd99-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8bd99-113">The applicationGateway</span></span>

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

### <span data-ttu-id="8bd99-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bd99-114">-DefaultProfile</span></span>
<span data-ttu-id="8bd99-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8bd99-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8bd99-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="8bd99-116">-Name</span></span>
<span data-ttu-id="8bd99-117">Namnet på den betrodda klient certifikat utfärdarens certifikat kedja</span><span class="sxs-lookup"><span data-stu-id="8bd99-117">The name of the trusted client CA certificate chain</span></span>

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

### <span data-ttu-id="8bd99-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8bd99-118">-Confirm</span></span>
<span data-ttu-id="8bd99-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8bd99-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8bd99-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8bd99-120">-WhatIf</span></span>
<span data-ttu-id="8bd99-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8bd99-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8bd99-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8bd99-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8bd99-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bd99-123">CommonParameters</span></span>
<span data-ttu-id="8bd99-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bd99-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bd99-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8bd99-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bd99-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8bd99-126">INPUTS</span></span>

### <span data-ttu-id="8bd99-127">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8bd99-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8bd99-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8bd99-128">OUTPUTS</span></span>

### <span data-ttu-id="8bd99-129">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8bd99-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8bd99-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8bd99-130">NOTES</span></span>

## <span data-ttu-id="8bd99-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8bd99-131">RELATED LINKS</span></span>

[<span data-ttu-id="8bd99-132">New-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="8bd99-132">New-AzApplicationGatewayTrustedClientCertificate</span></span>](./New-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="8bd99-133">Add-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="8bd99-133">Add-AzApplicationGatewayTrustedClientCertificate</span></span>](./Add-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="8bd99-134">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="8bd99-134">Get-AzApplicationGatewayTrustedClientCertificate</span></span>](./Get-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="8bd99-135">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="8bd99-135">Set-AzApplicationGatewayTrustedClientCertificate</span></span>](./Set-AzApplicationGatewayTrustedClientCertificate.md)
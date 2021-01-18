---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: 5f52b68e538072e6ff6aecde99f59337b532130c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525804"
---
# <span data-ttu-id="e74bf-101">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="e74bf-101">Set-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="e74bf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e74bf-102">SYNOPSIS</span></span>
<span data-ttu-id="e74bf-103">Ändrar den betrodda klient certifikat utfärdarens certifikat kedja för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="e74bf-103">Modifies the trusted client CA certificate chain of an application gateway.</span></span>

## <span data-ttu-id="e74bf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e74bf-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e74bf-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e74bf-105">DESCRIPTION</span></span>
<span data-ttu-id="e74bf-106">Cmdleten **set-AzApplicationGatewayTrustedClientCertificate** ändrar den betrodda klient certifikat utfärdarens certifikat kedja för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="e74bf-106">The **Set-AzApplicationGatewayTrustedClientCertificate** cmdlet modifies the trusted client CA certificate chain of an application gateway.</span></span>

## <span data-ttu-id="e74bf-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e74bf-107">EXAMPLES</span></span>

### <span data-ttu-id="e74bf-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e74bf-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\clientCAUpdated.cer"
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="e74bf-109">Ovan i scenario visar vi hur du uppdaterar ett befintligt kedje objekt för en betrodd klient certifikat utfärdare.</span><span class="sxs-lookup"><span data-stu-id="e74bf-109">Above example scenarios shows how to update an existing trusted client CA certificate chain object.</span></span> <span data-ttu-id="e74bf-110">Det första kommandot får en Programgateway och lagrar den i $gw variabeln.</span><span class="sxs-lookup"><span data-stu-id="e74bf-110">The first command gets an application gateway and stores it in the $gw variable.</span></span> <span data-ttu-id="e74bf-111">Det andra kommandot ändrar det befintliga betrodda klient certifikat utfärdarens certifikat för certifikatutfärdarcertifikatet med en ny kedje fil för CA-certifikat.</span><span class="sxs-lookup"><span data-stu-id="e74bf-111">The second command modifies the existing trusted client CA certificate chain object with a new CA certificate chain file.</span></span> <span data-ttu-id="e74bf-112">Det tredje kommandot uppdaterar programgatewayen på Azure.</span><span class="sxs-lookup"><span data-stu-id="e74bf-112">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="e74bf-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e74bf-113">PARAMETERS</span></span>

### <span data-ttu-id="e74bf-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e74bf-114">-ApplicationGateway</span></span>
<span data-ttu-id="e74bf-115">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e74bf-115">The applicationGateway</span></span>

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

### <span data-ttu-id="e74bf-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="e74bf-116">-CertificateFile</span></span>
<span data-ttu-id="e74bf-117">Sökväg till den betrodda klient certifikat utfärdarens certifikats kedja</span><span class="sxs-lookup"><span data-stu-id="e74bf-117">Path of the trusted client CA certificate chain file</span></span>

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

### <span data-ttu-id="e74bf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e74bf-118">-DefaultProfile</span></span>
<span data-ttu-id="e74bf-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e74bf-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e74bf-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="e74bf-120">-Name</span></span>
<span data-ttu-id="e74bf-121">Namnet på den betrodda klient certifikat utfärdarens certifikat kedja</span><span class="sxs-lookup"><span data-stu-id="e74bf-121">The name of the trusted client CA certificate chain</span></span>

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

### <span data-ttu-id="e74bf-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e74bf-122">-Confirm</span></span>
<span data-ttu-id="e74bf-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e74bf-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e74bf-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e74bf-124">-WhatIf</span></span>
<span data-ttu-id="e74bf-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e74bf-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e74bf-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e74bf-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e74bf-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e74bf-127">CommonParameters</span></span>
<span data-ttu-id="e74bf-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e74bf-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e74bf-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e74bf-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e74bf-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e74bf-130">INPUTS</span></span>

### <span data-ttu-id="e74bf-131">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e74bf-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e74bf-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e74bf-132">OUTPUTS</span></span>

### <span data-ttu-id="e74bf-133">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e74bf-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e74bf-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e74bf-134">NOTES</span></span>

## <span data-ttu-id="e74bf-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e74bf-135">RELATED LINKS</span></span>

[<span data-ttu-id="e74bf-136">Add-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="e74bf-136">Add-AzApplicationGatewayTrustedClientCertificate</span></span>](./Add-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="e74bf-137">New-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="e74bf-137">New-AzApplicationGatewayTrustedClientCertificate</span></span>](./New-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="e74bf-138">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="e74bf-138">Get-AzApplicationGatewayTrustedClientCertificate</span></span>](./Get-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="e74bf-139">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="e74bf-139">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>](./Remove-AzApplicationGatewayTrustedClientCertificate.md)
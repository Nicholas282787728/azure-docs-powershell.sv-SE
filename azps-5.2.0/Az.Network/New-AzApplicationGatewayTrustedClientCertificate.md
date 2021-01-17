---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: 285e9c343ed18d4aa21c328344b7be82319f0d3b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98411344"
---
# <span data-ttu-id="5ede4-101">New-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="5ede4-101">New-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="5ede4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5ede4-102">SYNOPSIS</span></span>
<span data-ttu-id="5ede4-103">Skapar en betrodd klient certifikat utfärdares certifikat kedja för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="5ede4-103">Creates a trusted client CA certificate chain for an application gateway.</span></span>

## <span data-ttu-id="5ede4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5ede4-104">SYNTAX</span></span>

```
New-AzApplicationGatewayTrustedClientCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ede4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5ede4-105">DESCRIPTION</span></span>
<span data-ttu-id="5ede4-106">New-AzApplicationGatewayTrustedClientCertificate-cmdleten skapar en betrodd klient certifikat utfärdares certifikat kedja för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="5ede4-106">The New-AzApplicationGatewayTrustedClientCertificate cmdlet creates a trusted client CA certificate chain for an application gateway.</span></span>

## <span data-ttu-id="5ede4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5ede4-107">EXAMPLES</span></span>

### <span data-ttu-id="5ede4-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5ede4-108">Example 1</span></span>
```powershell
PS C:\> $trustedClient = New-AzApplicationGatewayTrustedClientCertificate -Name "ClientCert" -CertificateFile "C:\clientCAChain.cer"
```
<span data-ttu-id="5ede4-109">Kommandot skapar en ny betrodd klient certifikat utfärdarens certifikatutfärdarcertifikat som tar vägen till klient certifikat utfärdarens certifikat som indata.</span><span class="sxs-lookup"><span data-stu-id="5ede4-109">The command creates a new trusted client CA certificate chain object taking path of the client CA certificate as input.</span></span>

## <span data-ttu-id="5ede4-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5ede4-110">PARAMETERS</span></span>

### <span data-ttu-id="5ede4-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="5ede4-111">-CertificateFile</span></span>
<span data-ttu-id="5ede4-112">Sökväg till den betrodda klient certifikat utfärdarens certifikats kedja</span><span class="sxs-lookup"><span data-stu-id="5ede4-112">Path of the trusted client CA certificate chain file</span></span>

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

### <span data-ttu-id="5ede4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ede4-113">-DefaultProfile</span></span>
<span data-ttu-id="5ede4-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5ede4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ede4-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="5ede4-115">-Name</span></span>
<span data-ttu-id="5ede4-116">Namnet på den betrodda klient certifikat utfärdarens certifikat kedja</span><span class="sxs-lookup"><span data-stu-id="5ede4-116">The name of the trusted client CA certificate chain</span></span>

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

### <span data-ttu-id="5ede4-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5ede4-117">-Confirm</span></span>
<span data-ttu-id="5ede4-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5ede4-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ede4-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ede4-119">-WhatIf</span></span>
<span data-ttu-id="5ede4-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5ede4-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ede4-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5ede4-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ede4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ede4-122">CommonParameters</span></span>
<span data-ttu-id="5ede4-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ede4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ede4-124">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5ede4-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ede4-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5ede4-125">INPUTS</span></span>

### <span data-ttu-id="5ede4-126">Ingen</span><span class="sxs-lookup"><span data-stu-id="5ede4-126">None</span></span>

## <span data-ttu-id="5ede4-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5ede4-127">OUTPUTS</span></span>

### <span data-ttu-id="5ede4-128">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="5ede4-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="5ede4-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5ede4-129">NOTES</span></span>

## <span data-ttu-id="5ede4-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5ede4-130">RELATED LINKS</span></span>

[<span data-ttu-id="5ede4-131">Add-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="5ede4-131">Add-AzApplicationGatewayTrustedClientCertificate</span></span>](./Add-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="5ede4-132">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="5ede4-132">Get-AzApplicationGatewayTrustedClientCertificate</span></span>](./Get-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="5ede4-133">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="5ede4-133">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>](./Remove-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="5ede4-134">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="5ede4-134">Set-AzApplicationGatewayTrustedClientCertificate</span></span>](./Set-AzApplicationGatewayTrustedClientCertificate.md)
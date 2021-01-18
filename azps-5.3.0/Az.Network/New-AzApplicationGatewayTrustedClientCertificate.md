---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: 285e9c343ed18d4aa21c328344b7be82319f0d3b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98521885"
---
# <span data-ttu-id="54561-101">New-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="54561-101">New-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="54561-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="54561-102">SYNOPSIS</span></span>
<span data-ttu-id="54561-103">Skapar en betrodd klient certifikat utfärdares certifikat kedja för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="54561-103">Creates a trusted client CA certificate chain for an application gateway.</span></span>

## <span data-ttu-id="54561-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="54561-104">SYNTAX</span></span>

```
New-AzApplicationGatewayTrustedClientCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54561-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="54561-105">DESCRIPTION</span></span>
<span data-ttu-id="54561-106">New-AzApplicationGatewayTrustedClientCertificate-cmdleten skapar en betrodd klient certifikat utfärdares certifikat kedja för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="54561-106">The New-AzApplicationGatewayTrustedClientCertificate cmdlet creates a trusted client CA certificate chain for an application gateway.</span></span>

## <span data-ttu-id="54561-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="54561-107">EXAMPLES</span></span>

### <span data-ttu-id="54561-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="54561-108">Example 1</span></span>
```powershell
PS C:\> $trustedClient = New-AzApplicationGatewayTrustedClientCertificate -Name "ClientCert" -CertificateFile "C:\clientCAChain.cer"
```
<span data-ttu-id="54561-109">Kommandot skapar en ny betrodd klient certifikat utfärdarens certifikatutfärdarcertifikat som tar vägen till klient certifikat utfärdarens certifikat som indata.</span><span class="sxs-lookup"><span data-stu-id="54561-109">The command creates a new trusted client CA certificate chain object taking path of the client CA certificate as input.</span></span>

## <span data-ttu-id="54561-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="54561-110">PARAMETERS</span></span>

### <span data-ttu-id="54561-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="54561-111">-CertificateFile</span></span>
<span data-ttu-id="54561-112">Sökväg till den betrodda klient certifikat utfärdarens certifikats kedja</span><span class="sxs-lookup"><span data-stu-id="54561-112">Path of the trusted client CA certificate chain file</span></span>

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

### <span data-ttu-id="54561-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54561-113">-DefaultProfile</span></span>
<span data-ttu-id="54561-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="54561-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54561-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="54561-115">-Name</span></span>
<span data-ttu-id="54561-116">Namnet på den betrodda klient certifikat utfärdarens certifikat kedja</span><span class="sxs-lookup"><span data-stu-id="54561-116">The name of the trusted client CA certificate chain</span></span>

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

### <span data-ttu-id="54561-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="54561-117">-Confirm</span></span>
<span data-ttu-id="54561-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="54561-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54561-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54561-119">-WhatIf</span></span>
<span data-ttu-id="54561-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="54561-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54561-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="54561-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54561-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54561-122">CommonParameters</span></span>
<span data-ttu-id="54561-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54561-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54561-124">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="54561-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54561-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="54561-125">INPUTS</span></span>

### <span data-ttu-id="54561-126">Ingen</span><span class="sxs-lookup"><span data-stu-id="54561-126">None</span></span>

## <span data-ttu-id="54561-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="54561-127">OUTPUTS</span></span>

### <span data-ttu-id="54561-128">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="54561-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="54561-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="54561-129">NOTES</span></span>

## <span data-ttu-id="54561-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="54561-130">RELATED LINKS</span></span>

[<span data-ttu-id="54561-131">Add-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="54561-131">Add-AzApplicationGatewayTrustedClientCertificate</span></span>](./Add-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="54561-132">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="54561-132">Get-AzApplicationGatewayTrustedClientCertificate</span></span>](./Get-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="54561-133">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="54561-133">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>](./Remove-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="54561-134">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="54561-134">Set-AzApplicationGatewayTrustedClientCertificate</span></span>](./Set-AzApplicationGatewayTrustedClientCertificate.md)
---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 482c289922d6b8a905bee901a34568050a52c2c7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98421779"
---
# <span data-ttu-id="33f53-101">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="33f53-101">New-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="33f53-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="33f53-102">SYNOPSIS</span></span>
<span data-ttu-id="33f53-103">Skapar ett betrott rot certifikat för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="33f53-103">Creates a Trusted Root Certificate for an application gateway.</span></span>

## <span data-ttu-id="33f53-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="33f53-104">SYNTAX</span></span>

```
New-AzApplicationGatewayTrustedRootCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33f53-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="33f53-105">DESCRIPTION</span></span>
<span data-ttu-id="33f53-106">Cmdleten **New-AzApplicationGatewayTrustedRootCertificate** skapar ett betrott rot certifikat för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="33f53-106">The **New-AzApplicationGatewayTrustedRootCertificate** cmdlet creates a Trusted Root Certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="33f53-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="33f53-107">EXAMPLES</span></span>

### <span data-ttu-id="33f53-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="33f53-108">Example 1</span></span>
```powershell
PS C:\> $certFilePath = ".\rootCA.cer"
PS C:\> $trc = New-AzApplicationGatewayTrustedRootCertificate -Name "trc1" -CertificateFile $certFilePath
```

<span data-ttu-id="33f53-109">Det här kommandot skapar ett betrott rot certifikat med listan "trc1" och lagrar resultatet i variabeln som heter $trc.</span><span class="sxs-lookup"><span data-stu-id="33f53-109">This command creates a Trusted Root Certificate named List "trc1" and stores the result in the variable named $trc.</span></span>

## <span data-ttu-id="33f53-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="33f53-110">PARAMETERS</span></span>

### <span data-ttu-id="33f53-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="33f53-111">-CertificateFile</span></span>
<span data-ttu-id="33f53-112">Sökväg till certifikat-CER-fil</span><span class="sxs-lookup"><span data-stu-id="33f53-112">Path of certificate CER file</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33f53-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33f53-113">-DefaultProfile</span></span>
<span data-ttu-id="33f53-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="33f53-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33f53-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="33f53-115">-Name</span></span>
<span data-ttu-id="33f53-116">Namnet på TrustedRoot-certifikatet</span><span class="sxs-lookup"><span data-stu-id="33f53-116">The name of the TrustedRoot certificate</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33f53-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="33f53-117">-Confirm</span></span>
<span data-ttu-id="33f53-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="33f53-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33f53-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33f53-119">-WhatIf</span></span>
<span data-ttu-id="33f53-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="33f53-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33f53-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="33f53-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33f53-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33f53-122">CommonParameters</span></span>
<span data-ttu-id="33f53-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33f53-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33f53-124">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33f53-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33f53-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="33f53-125">INPUTS</span></span>

### <span data-ttu-id="33f53-126">Ingen</span><span class="sxs-lookup"><span data-stu-id="33f53-126">None</span></span>

## <span data-ttu-id="33f53-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="33f53-127">OUTPUTS</span></span>

### <span data-ttu-id="33f53-128">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="33f53-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="33f53-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="33f53-129">NOTES</span></span>

## <span data-ttu-id="33f53-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="33f53-130">RELATED LINKS</span></span>

[<span data-ttu-id="33f53-131">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="33f53-131">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="33f53-132">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="33f53-132">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="33f53-133">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="33f53-133">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="33f53-134">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="33f53-134">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)

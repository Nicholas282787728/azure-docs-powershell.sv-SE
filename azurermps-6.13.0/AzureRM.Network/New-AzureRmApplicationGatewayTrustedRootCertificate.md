---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 5f71f9a28eb1daae1bee070907675c87002241f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585931"
---
# <span data-ttu-id="3330e-101">New-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="3330e-101">New-AzureRmApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="3330e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3330e-102">SYNOPSIS</span></span>
<span data-ttu-id="3330e-103">Skapar ett betrott rot certifikat för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="3330e-103">Creates a Trusted Root Certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3330e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3330e-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayTrustedRootCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3330e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3330e-105">DESCRIPTION</span></span>
<span data-ttu-id="3330e-106">Cmdleten **New-AzureRmApplicationGatewayTrustedRootCertificate** skapar ett betrott rot certifikat för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="3330e-106">The **New-AzureRmApplicationGatewayTrustedRootCertificate** cmdlet creates a Trusted Root Certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="3330e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3330e-107">EXAMPLES</span></span>

### <span data-ttu-id="3330e-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3330e-108">Example 1</span></span>
```powershell
PS C:\> $certFilePath = ".\rootCA.cer"
PS C:\> $trc = New-AzureRmApplicationGatewayTrustedRootCertificate -Name "trc1" --CertificateFile $certFilePath
```

<span data-ttu-id="3330e-109">Det här kommandot skapar ett betrott rot certifikat med listan "trc1" och lagrar resultatet i variabeln som heter $trc.</span><span class="sxs-lookup"><span data-stu-id="3330e-109">This command creates a Trusted Root Certificate named List "trc1" and stores the result in the variable named $trc.</span></span>

## <span data-ttu-id="3330e-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3330e-110">PARAMETERS</span></span>

### <span data-ttu-id="3330e-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="3330e-111">-CertificateFile</span></span>
<span data-ttu-id="3330e-112">Sökväg till certifikat-CER-fil</span><span class="sxs-lookup"><span data-stu-id="3330e-112">Path of certificate CER file</span></span>

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

### <span data-ttu-id="3330e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3330e-113">-DefaultProfile</span></span>
<span data-ttu-id="3330e-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3330e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3330e-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="3330e-115">-Name</span></span>
<span data-ttu-id="3330e-116">Namnet på TrustedRoot-certifikatet</span><span class="sxs-lookup"><span data-stu-id="3330e-116">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="3330e-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3330e-117">-Confirm</span></span>
<span data-ttu-id="3330e-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3330e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3330e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3330e-119">-WhatIf</span></span>
<span data-ttu-id="3330e-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3330e-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3330e-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3330e-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3330e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3330e-122">CommonParameters</span></span>
<span data-ttu-id="3330e-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3330e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3330e-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3330e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3330e-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3330e-125">INPUTS</span></span>

### <span data-ttu-id="3330e-126">Ingen</span><span class="sxs-lookup"><span data-stu-id="3330e-126">None</span></span>

## <span data-ttu-id="3330e-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3330e-127">OUTPUTS</span></span>

### <span data-ttu-id="3330e-128">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="3330e-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="3330e-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3330e-129">NOTES</span></span>

## <span data-ttu-id="3330e-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3330e-130">RELATED LINKS</span></span>

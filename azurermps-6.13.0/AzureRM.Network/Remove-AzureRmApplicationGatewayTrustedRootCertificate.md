---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: eecce510632e7eef3fc61cf53127777b93c81e51
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576182"
---
# <span data-ttu-id="e9b34-101">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="e9b34-101">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="e9b34-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e9b34-102">SYNOPSIS</span></span>
<span data-ttu-id="e9b34-103">Tar bort ett betrott rot certifikat från en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="e9b34-103">Removes a Trusted Root Certificate from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e9b34-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e9b34-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayTrustedRootCertificate -Name <String>
 -ApplicationGateway <PSApplicationGateway> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e9b34-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e9b34-105">DESCRIPTION</span></span>
<span data-ttu-id="e9b34-106">Cmdleten **Remove-AzureRmApplicationGatewayTrustedRootCertificate** tar bort ett betrott rot certifikat från en befintlig Programgateway.</span><span class="sxs-lookup"><span data-stu-id="e9b34-106">The **Remove-AzureRmApplicationGatewayTrustedRootCertificate** cmdlet removes a Trusted Root Certificate from an existing Application Gateway.</span></span>

## <span data-ttu-id="e9b34-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e9b34-107">EXAMPLES</span></span>

### <span data-ttu-id="e9b34-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e9b34-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzureRmApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Remove-AzureRmApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name "myRootCA"
PS C:\> $gw = Set-AzureRmApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="e9b34-109">Det första kommandot får en Programgateway och lagrar den i $gw variabeln.</span><span class="sxs-lookup"><span data-stu-id="e9b34-109">The first command gets an application gateway and stores it in the $gw variable.</span></span>
<span data-ttu-id="e9b34-110">Det andra kommandot tar bort det betrodda rot certifikatet med namnet myRootCA från Application Gateway som lagras i $gw.</span><span class="sxs-lookup"><span data-stu-id="e9b34-110">The second command removes the trusted root certificate named myRootCA from the application gateway stored in $gw.</span></span>
<span data-ttu-id="e9b34-111">Det tredje kommandot uppdaterar programgatewayen på Azure.</span><span class="sxs-lookup"><span data-stu-id="e9b34-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="e9b34-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e9b34-112">PARAMETERS</span></span>

### <span data-ttu-id="e9b34-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e9b34-113">-ApplicationGateway</span></span>
<span data-ttu-id="e9b34-114">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e9b34-114">The applicationGateway</span></span>

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

### <span data-ttu-id="e9b34-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9b34-115">-DefaultProfile</span></span>
<span data-ttu-id="e9b34-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e9b34-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9b34-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="e9b34-117">-Name</span></span>
<span data-ttu-id="e9b34-118">Namnet på TrustedRoot-certifikatet</span><span class="sxs-lookup"><span data-stu-id="e9b34-118">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="e9b34-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e9b34-119">-Confirm</span></span>
<span data-ttu-id="e9b34-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e9b34-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9b34-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9b34-121">-WhatIf</span></span>
<span data-ttu-id="e9b34-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e9b34-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9b34-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e9b34-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9b34-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9b34-124">CommonParameters</span></span>
<span data-ttu-id="e9b34-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9b34-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9b34-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9b34-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9b34-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e9b34-127">INPUTS</span></span>

### <span data-ttu-id="e9b34-128">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e9b34-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e9b34-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e9b34-129">OUTPUTS</span></span>

### <span data-ttu-id="e9b34-130">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e9b34-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e9b34-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e9b34-131">NOTES</span></span>

## <span data-ttu-id="e9b34-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e9b34-132">RELATED LINKS</span></span>
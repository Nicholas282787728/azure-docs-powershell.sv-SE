---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3C046A0A-A2B6-413C-8D3B-8991A1FC4926
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: dc5a0fb99ca3ce41447cc95ebb42490b88379f83
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98398331"
---
# <span data-ttu-id="c4bb5-101">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="c4bb5-101">New-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="c4bb5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c4bb5-102">SYNOPSIS</span></span>
<span data-ttu-id="c4bb5-103">Skapar en front port för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="c4bb5-103">Creates a front-end port for an application gateway.</span></span>

## <span data-ttu-id="c4bb5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c4bb5-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFrontendPort -Name <String> -Port <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c4bb5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c4bb5-105">DESCRIPTION</span></span>
<span data-ttu-id="c4bb5-106">Cmdleten **New-AzApplicationGatewayFrontendPort** skapar en front port för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="c4bb5-106">The **New-AzApplicationGatewayFrontendPort** cmdlet creates a front-end port for an Azure application gateway.</span></span>

## <span data-ttu-id="c4bb5-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c4bb5-107">EXAMPLES</span></span>

### <span data-ttu-id="c4bb5-108">Exempel 1: Example1: skapa en front port</span><span class="sxs-lookup"><span data-stu-id="c4bb5-108">Example 1: Example1: Create a front-end port</span></span>
```powershell
PS C:\>$FrontEndPort = New-AzApplicationGatewayFrontendPort -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="c4bb5-109">Det här kommandot skapar en frontend-port med namnet FrontEndPort01 på port 80 och lagrar resultatet i variabeln som heter $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="c4bb5-109">This command creates a front-end port named FrontEndPort01 on port 80 and stores the result in the variable named $FrontEndPort.</span></span>

## <span data-ttu-id="c4bb5-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c4bb5-110">PARAMETERS</span></span>

### <span data-ttu-id="c4bb5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4bb5-111">-DefaultProfile</span></span>
<span data-ttu-id="c4bb5-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c4bb5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4bb5-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="c4bb5-113">-Name</span></span>
<span data-ttu-id="c4bb5-114">Anger namnet på front porten som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="c4bb5-114">Specifies the name of the front-end port that this cmdlet creates.</span></span>

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

### <span data-ttu-id="c4bb5-115">-Port</span><span class="sxs-lookup"><span data-stu-id="c4bb5-115">-Port</span></span>
<span data-ttu-id="c4bb5-116">Anger port numret för front porten.</span><span class="sxs-lookup"><span data-stu-id="c4bb5-116">Specifies the port number of the front-end port.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4bb5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4bb5-117">CommonParameters</span></span>
<span data-ttu-id="c4bb5-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4bb5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4bb5-119">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4bb5-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4bb5-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c4bb5-120">INPUTS</span></span>

### <span data-ttu-id="c4bb5-121">Ingen</span><span class="sxs-lookup"><span data-stu-id="c4bb5-121">None</span></span>

## <span data-ttu-id="c4bb5-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c4bb5-122">OUTPUTS</span></span>

### <span data-ttu-id="c4bb5-123">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="c4bb5-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="c4bb5-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c4bb5-124">NOTES</span></span>

## <span data-ttu-id="c4bb5-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c4bb5-125">RELATED LINKS</span></span>

[<span data-ttu-id="c4bb5-126">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="c4bb5-126">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="c4bb5-127">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="c4bb5-127">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="c4bb5-128">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="c4bb5-128">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="c4bb5-129">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="c4bb5-129">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)



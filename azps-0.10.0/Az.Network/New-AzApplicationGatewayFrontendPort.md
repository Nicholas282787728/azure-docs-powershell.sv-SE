---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3C046A0A-A2B6-413C-8D3B-8991A1FC4926
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: ddfe8b1736ef6c037522815dc81019fadc5b6c1f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922166"
---
# <span data-ttu-id="d730c-101">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="d730c-101">New-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="d730c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d730c-102">SYNOPSIS</span></span>
<span data-ttu-id="d730c-103">Skapar en front port för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="d730c-103">Creates a front-end port for an application gateway.</span></span>

## <span data-ttu-id="d730c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d730c-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFrontendPort -Name <String> -Port <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d730c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d730c-105">DESCRIPTION</span></span>
<span data-ttu-id="d730c-106">Cmdleten **New-AzApplicationGatewayFrontendPort** skapar en front port för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="d730c-106">The **New-AzApplicationGatewayFrontendPort** cmdlet creates a front-end port for an Azure application gateway.</span></span>

## <span data-ttu-id="d730c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d730c-107">EXAMPLES</span></span>

### <span data-ttu-id="d730c-108">Example1: skapa en front port</span><span class="sxs-lookup"><span data-stu-id="d730c-108">Example1: Create a front-end port</span></span>
```
PS C:\>$FrontEndPort = New-AzApplicationGatewayFrontendPort -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="d730c-109">Det här kommandot skapar en frontend-port med namnet FrontEndPort01 på port 80 och lagrar resultatet i variabeln som heter $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="d730c-109">This command creates a front-end port named FrontEndPort01 on port 80 and stores the result in the variable named $FrontEndPort.</span></span>

## <span data-ttu-id="d730c-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d730c-110">PARAMETERS</span></span>

### <span data-ttu-id="d730c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d730c-111">-DefaultProfile</span></span>
<span data-ttu-id="d730c-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d730c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d730c-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="d730c-113">-Name</span></span>
<span data-ttu-id="d730c-114">Anger namnet på front porten som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="d730c-114">Specifies the name of the front-end port that this cmdlet creates.</span></span>

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

### <span data-ttu-id="d730c-115">-Port</span><span class="sxs-lookup"><span data-stu-id="d730c-115">-Port</span></span>
<span data-ttu-id="d730c-116">Anger port numret för front porten.</span><span class="sxs-lookup"><span data-stu-id="d730c-116">Specifies the port number of the front-end port.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d730c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d730c-117">CommonParameters</span></span>
<span data-ttu-id="d730c-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d730c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d730c-119">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d730c-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d730c-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d730c-120">INPUTS</span></span>

### <span data-ttu-id="d730c-121">System. String</span><span class="sxs-lookup"><span data-stu-id="d730c-121">System.String</span></span>

## <span data-ttu-id="d730c-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d730c-122">OUTPUTS</span></span>

### <span data-ttu-id="d730c-123">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="d730c-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="d730c-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d730c-124">NOTES</span></span>

## <span data-ttu-id="d730c-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d730c-125">RELATED LINKS</span></span>

[<span data-ttu-id="d730c-126">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="d730c-126">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="d730c-127">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="d730c-127">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="d730c-128">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="d730c-128">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="d730c-129">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="d730c-129">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


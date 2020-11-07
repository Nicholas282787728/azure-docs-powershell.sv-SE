---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 3C046A0A-A2B6-413C-8D3B-8991A1FC4926
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayFrontendPort.md
ms.openlocfilehash: bccdcb5f94cc90dca04229ca643fd23f29a276e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755860"
---
# <span data-ttu-id="36212-101">New-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="36212-101">New-AzureRmApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="36212-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="36212-102">SYNOPSIS</span></span>
<span data-ttu-id="36212-103">Skapar en front port för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="36212-103">Creates a front-end port for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36212-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="36212-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayFrontendPort -Name <String> -Port <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36212-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="36212-105">DESCRIPTION</span></span>
<span data-ttu-id="36212-106">Cmdleten **New-AzureRmApplicationGatewayFrontendPort** skapar en front port för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="36212-106">The **New-AzureRmApplicationGatewayFrontendPort** cmdlet creates a front-end port for an Azure application gateway.</span></span>

## <span data-ttu-id="36212-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="36212-107">EXAMPLES</span></span>

### <span data-ttu-id="36212-108">Example1: skapa en front port</span><span class="sxs-lookup"><span data-stu-id="36212-108">Example1: Create a front-end port</span></span>
```
PS C:\>$FrontEndPort = New-AzureRmApplicationGatewayFrontendPort -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="36212-109">Det här kommandot skapar en frontend-port med namnet FrontEndPort01 på port 80 och lagrar resultatet i variabeln som heter $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="36212-109">This command creates a front-end port named FrontEndPort01 on port 80 and stores the result in the variable named $FrontEndPort.</span></span>

## <span data-ttu-id="36212-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="36212-110">PARAMETERS</span></span>

### <span data-ttu-id="36212-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36212-111">-DefaultProfile</span></span>
<span data-ttu-id="36212-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="36212-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36212-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="36212-113">-Name</span></span>
<span data-ttu-id="36212-114">Anger namnet på front porten som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="36212-114">Specifies the name of the front-end port that this cmdlet creates.</span></span>

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

### <span data-ttu-id="36212-115">-Port</span><span class="sxs-lookup"><span data-stu-id="36212-115">-Port</span></span>
<span data-ttu-id="36212-116">Anger port numret för front porten.</span><span class="sxs-lookup"><span data-stu-id="36212-116">Specifies the port number of the front-end port.</span></span>

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

### <span data-ttu-id="36212-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36212-117">CommonParameters</span></span>
<span data-ttu-id="36212-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36212-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36212-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36212-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36212-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="36212-120">INPUTS</span></span>

### <span data-ttu-id="36212-121">System. String</span><span class="sxs-lookup"><span data-stu-id="36212-121">System.String</span></span>

## <span data-ttu-id="36212-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="36212-122">OUTPUTS</span></span>

### <span data-ttu-id="36212-123">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="36212-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="36212-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="36212-124">NOTES</span></span>

## <span data-ttu-id="36212-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="36212-125">RELATED LINKS</span></span>

[<span data-ttu-id="36212-126">Add-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="36212-126">Add-AzureRmApplicationGatewayFrontendPort</span></span>](./Add-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="36212-127">Get-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="36212-127">Get-AzureRmApplicationGatewayFrontendPort</span></span>](./Get-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="36212-128">Remove-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="36212-128">Remove-AzureRmApplicationGatewayFrontendPort</span></span>](./Remove-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="36212-129">Set-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="36212-129">Set-AzureRmApplicationGatewayFrontendPort</span></span>](./Set-AzureRmApplicationGatewayFrontendPort.md)



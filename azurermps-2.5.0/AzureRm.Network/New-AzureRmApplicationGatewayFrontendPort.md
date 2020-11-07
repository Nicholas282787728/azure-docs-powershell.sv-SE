---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 3C046A0A-A2B6-413C-8D3B-8991A1FC4926
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayfrontendport
schema: 2.0.0
ms.openlocfilehash: f8b9d6b981300c32badbe69ec153865c04814dd6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930541"
---
# <span data-ttu-id="ace05-101">New-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="ace05-101">New-AzureRmApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="ace05-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ace05-102">SYNOPSIS</span></span>
<span data-ttu-id="ace05-103">Skapar en front port för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="ace05-103">Creates a front-end port for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ace05-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ace05-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayFrontendPort -Name <String> -Port <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ace05-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ace05-105">DESCRIPTION</span></span>
<span data-ttu-id="ace05-106">Cmdleten **New-AzureRmApplicationGatewayFrontendPort** skapar en front port för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="ace05-106">The **New-AzureRmApplicationGatewayFrontendPort** cmdlet creates a front-end port for an Azure application gateway.</span></span>

## <span data-ttu-id="ace05-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ace05-107">EXAMPLES</span></span>

### <span data-ttu-id="ace05-108">Example1: skapa en front port</span><span class="sxs-lookup"><span data-stu-id="ace05-108">Example1: Create a front-end port</span></span>
```
PS C:\>$FrontEndPort = New-AzureRmApplicationGatewayFrontendPort -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="ace05-109">Det här kommandot skapar en frontend-port med namnet FrontEndPort01 på port 80 och lagrar resultatet i variabeln som heter $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="ace05-109">This command creates a front-end port named FrontEndPort01 on port 80 and stores the result in the variable named $FrontEndPort.</span></span>

## <span data-ttu-id="ace05-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ace05-110">PARAMETERS</span></span>

### <span data-ttu-id="ace05-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ace05-111">-DefaultProfile</span></span>
<span data-ttu-id="ace05-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ace05-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ace05-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="ace05-113">-Name</span></span>
<span data-ttu-id="ace05-114">Anger namnet på front porten som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="ace05-114">Specifies the name of the front-end port that this cmdlet creates.</span></span>

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

### <span data-ttu-id="ace05-115">-Port</span><span class="sxs-lookup"><span data-stu-id="ace05-115">-Port</span></span>
<span data-ttu-id="ace05-116">Anger port numret för front porten.</span><span class="sxs-lookup"><span data-stu-id="ace05-116">Specifies the port number of the front-end port.</span></span>

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

### <span data-ttu-id="ace05-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ace05-117">CommonParameters</span></span>
<span data-ttu-id="ace05-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ace05-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ace05-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ace05-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ace05-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ace05-120">INPUTS</span></span>

### <span data-ttu-id="ace05-121">System. String</span><span class="sxs-lookup"><span data-stu-id="ace05-121">System.String</span></span>

## <span data-ttu-id="ace05-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ace05-122">OUTPUTS</span></span>

### <span data-ttu-id="ace05-123">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="ace05-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="ace05-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ace05-124">NOTES</span></span>

## <span data-ttu-id="ace05-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ace05-125">RELATED LINKS</span></span>

[<span data-ttu-id="ace05-126">Add-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="ace05-126">Add-AzureRmApplicationGatewayFrontendPort</span></span>](./Add-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="ace05-127">Get-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="ace05-127">Get-AzureRmApplicationGatewayFrontendPort</span></span>](./Get-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="ace05-128">Remove-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="ace05-128">Remove-AzureRmApplicationGatewayFrontendPort</span></span>](./Remove-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="ace05-129">Set-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="ace05-129">Set-AzureRmApplicationGatewayFrontendPort</span></span>](./Set-AzureRmApplicationGatewayFrontendPort.md)



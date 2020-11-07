---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewaybackendhttpsettings
schema: 2.0.0
ms.openlocfilehash: 71ce0dd8d4c5988dfc5cd4226ee76dcec46042ff
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929697"
---
# <span data-ttu-id="4198f-101">Remove-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="4198f-101">Remove-AzureRmApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="4198f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4198f-102">SYNOPSIS</span></span>
<span data-ttu-id="4198f-103">Tar bort backend-HTTP-inställningar från en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="4198f-103">Removes back-end HTTP settings from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4198f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4198f-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayBackendHttpSettings -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4198f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4198f-105">DESCRIPTION</span></span>
<span data-ttu-id="4198f-106">Remove-AzureRmApplicationGatewayBackendHttpSettings cmdlet tar bort backend-inställningarna från en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="4198f-106">The Remove-AzureRmApplicationGatewayBackendHttpSettings cmdlet removes back-end Hypertext Transfer Protocol (HTTP) settings from an Azure application gateway.</span></span>

## <span data-ttu-id="4198f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4198f-107">EXAMPLES</span></span>

### <span data-ttu-id="4198f-108">Exempel 1: ta bort backend-HTTP-inställningar från en Programgateway</span><span class="sxs-lookup"><span data-stu-id="4198f-108">Example 1: Remove back-end HTTP settings from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayBackendHttpSettings -ApplicationGateway $AppGw -Name "BackEndSetting02"
```

<span data-ttu-id="4198f-109">Det första kommandot får en Programgateway som heter ApplicationGateway01 som tillhör resurs gruppen med namnet ResourceGroup01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="4198f-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="4198f-110">Med det andra kommandot tas backend-HTTP-inställningen bort med namnet BackEndSetting02 från Application Gateway som lagras i $AppGw.</span><span class="sxs-lookup"><span data-stu-id="4198f-110">The second command removes the back-end HTTP setting named BackEndSetting02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="4198f-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4198f-111">PARAMETERS</span></span>

### <span data-ttu-id="4198f-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4198f-112">-ApplicationGateway</span></span>
<span data-ttu-id="4198f-113">Anger den Programgateway från vilken denna cmdlet tar bort backend HTTP-inställningar.</span><span class="sxs-lookup"><span data-stu-id="4198f-113">Specifies the application gateway from which this cmdlet removes back-end HTTP settings.</span></span>

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

### <span data-ttu-id="4198f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4198f-114">-DefaultProfile</span></span>
<span data-ttu-id="4198f-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4198f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4198f-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="4198f-116">-Name</span></span>
<span data-ttu-id="4198f-117">Anger namnet på de HTTP-inställningar för backend som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="4198f-117">Specifies the name of the back-end HTTP settings that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4198f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4198f-118">CommonParameters</span></span>
<span data-ttu-id="4198f-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4198f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4198f-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4198f-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4198f-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4198f-121">INPUTS</span></span>

### <span data-ttu-id="4198f-122">System. String</span><span class="sxs-lookup"><span data-stu-id="4198f-122">System.String</span></span>

## <span data-ttu-id="4198f-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4198f-123">OUTPUTS</span></span>

### <span data-ttu-id="4198f-124">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4198f-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4198f-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4198f-125">NOTES</span></span>

## <span data-ttu-id="4198f-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4198f-126">RELATED LINKS</span></span>

[<span data-ttu-id="4198f-127">Add-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="4198f-127">Add-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="4198f-128">New-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="4198f-128">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="4198f-129">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="4198f-129">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="4198f-130">Set-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="4198f-130">Set-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()


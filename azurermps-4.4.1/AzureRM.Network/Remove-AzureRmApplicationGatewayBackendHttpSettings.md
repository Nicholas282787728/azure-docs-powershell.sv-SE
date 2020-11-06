---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayBackendHttpSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayBackendHttpSettings.md
ms.openlocfilehash: 2481fa04c8c31e9537fcb53801edad181b3812d0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574577"
---
# <span data-ttu-id="4002c-101">Remove-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="4002c-101">Remove-AzureRmApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="4002c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4002c-102">SYNOPSIS</span></span>
<span data-ttu-id="4002c-103">Tar bort backend-HTTP-inställningar från en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="4002c-103">Removes back-end HTTP settings from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4002c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4002c-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayBackendHttpSettings -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4002c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4002c-105">DESCRIPTION</span></span>
<span data-ttu-id="4002c-106">Remove-AzureRmApplicationGatewayBackendHttpSettings cmdlet tar bort backend-inställningarna från en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="4002c-106">The Remove-AzureRmApplicationGatewayBackendHttpSettings cmdlet removes back-end Hypertext Transfer Protocol (HTTP) settings from an Azure application gateway.</span></span>

## <span data-ttu-id="4002c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4002c-107">EXAMPLES</span></span>

### <span data-ttu-id="4002c-108">Exempel 1: ta bort backend-HTTP-inställningar från en Programgateway</span><span class="sxs-lookup"><span data-stu-id="4002c-108">Example 1: Remove back-end HTTP settings from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayBackendHttpSettings -ApplicationGateway $AppGw -Name "BackEndSetting02"
```

<span data-ttu-id="4002c-109">Det första kommandot får en Programgateway som heter ApplicationGateway01 som tillhör resurs gruppen med namnet ResourceGroup01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="4002c-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="4002c-110">Med det andra kommandot tas backend-HTTP-inställningen bort med namnet BackEndSetting02 från Application Gateway som lagras i $AppGw.</span><span class="sxs-lookup"><span data-stu-id="4002c-110">The second command removes the back-end HTTP setting named BackEndSetting02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="4002c-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4002c-111">PARAMETERS</span></span>

### <span data-ttu-id="4002c-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4002c-112">-ApplicationGateway</span></span>
<span data-ttu-id="4002c-113">Anger den Programgateway från vilken denna cmdlet tar bort backend HTTP-inställningar.</span><span class="sxs-lookup"><span data-stu-id="4002c-113">Specifies the application gateway from which this cmdlet removes back-end HTTP settings.</span></span>

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

### <span data-ttu-id="4002c-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="4002c-114">-Name</span></span>
<span data-ttu-id="4002c-115">Anger namnet på de HTTP-inställningar för backend som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="4002c-115">Specifies the name of the back-end HTTP settings that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4002c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4002c-116">-DefaultProfile</span></span>
<span data-ttu-id="4002c-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4002c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4002c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4002c-118">CommonParameters</span></span>
<span data-ttu-id="4002c-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4002c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4002c-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4002c-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4002c-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4002c-121">INPUTS</span></span>

### <span data-ttu-id="4002c-122">System. String</span><span class="sxs-lookup"><span data-stu-id="4002c-122">System.String</span></span>

## <span data-ttu-id="4002c-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4002c-123">OUTPUTS</span></span>

### <span data-ttu-id="4002c-124">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4002c-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4002c-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4002c-125">NOTES</span></span>

## <span data-ttu-id="4002c-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4002c-126">RELATED LINKS</span></span>

[<span data-ttu-id="4002c-127">Add-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="4002c-127">Add-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="4002c-128">New-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="4002c-128">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="4002c-129">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="4002c-129">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="4002c-130">Set-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="4002c-130">Set-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()


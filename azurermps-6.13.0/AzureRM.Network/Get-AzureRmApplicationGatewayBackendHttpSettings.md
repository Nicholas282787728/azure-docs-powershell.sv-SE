---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaybackendhttpsettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayBackendHttpSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayBackendHttpSettings.md
ms.openlocfilehash: d7dc38e25ffda43eae3c29bc0e3db83f1a27c9f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576246"
---
# <span data-ttu-id="8e6cf-101">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="8e6cf-101">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="8e6cf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8e6cf-102">SYNOPSIS</span></span>
<span data-ttu-id="8e6cf-103">Hämtar dina backend HTTP-inställningar för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="8e6cf-103">Gets the back-end HTTP settings of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e6cf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8e6cf-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayBackendHttpSettings [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e6cf-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8e6cf-105">DESCRIPTION</span></span>
<span data-ttu-id="8e6cf-106">Med cmdleten Get-AzureRmApplicationGatewayBackendHttpSettings får du backend-HTTP-inställningarna för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="8e6cf-106">The Get-AzureRmApplicationGatewayBackendHttpSettings cmdlet gets the back-end HTTP settings of an application gateway.</span></span>

## <span data-ttu-id="8e6cf-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8e6cf-107">EXAMPLES</span></span>

### <span data-ttu-id="8e6cf-108">Exempel 1: kom tillbaka-HTTP-inställningar efter namn</span><span class="sxs-lookup"><span data-stu-id="8e6cf-108">Example 1: Get back-end HTTP settings by name</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzureRmApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
```

<span data-ttu-id="8e6cf-109">Det första kommandot får den Programgateway som heter ApplicationGateway01 i resurs gruppen som heter ResourceGroup01 och lagrar den i $AppGw variabel. Det andra kommandot får HTTP-inställningarna "Settings01" för $AppGw och lagrar inställningarna i $Settings-variabeln.</span><span class="sxs-lookup"><span data-stu-id="8e6cf-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>

### <span data-ttu-id="8e6cf-110">Exempel 2: få en samling backend-HTTP-inställningar</span><span class="sxs-lookup"><span data-stu-id="8e6cf-110">Example 2: Get a collection of back-end HTTP settings</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SettingsList  = Get-AzureRmApplicationGatewayBackendHttpSettings -ApplicationGateway $AppGw
```

<span data-ttu-id="8e6cf-111">Det första kommandot får den Programgateway som heter ApplicationGateway01 i resurs gruppen som heter ResourceGroup01 och lagrar den i $AppGw variabel. Det andra kommandot hämtar HTTP-inställningarna för $AppGw och lagrar inställningarna i $SettingsList-variabeln.</span><span class="sxs-lookup"><span data-stu-id="8e6cf-111">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the collection of HTTP settings for $AppGw and stores the settings in the $SettingsList variable.</span></span>

## <span data-ttu-id="8e6cf-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8e6cf-112">PARAMETERS</span></span>

### <span data-ttu-id="8e6cf-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8e6cf-113">-ApplicationGateway</span></span>
<span data-ttu-id="8e6cf-114">Anger ett objekt för Application Gateway som innehåller backend HTTP-inställningar.</span><span class="sxs-lookup"><span data-stu-id="8e6cf-114">Specifies an application gateway object that contains back-end HTTP settings.</span></span>

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

### <span data-ttu-id="8e6cf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e6cf-115">-DefaultProfile</span></span>
<span data-ttu-id="8e6cf-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8e6cf-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e6cf-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="8e6cf-117">-Name</span></span>
<span data-ttu-id="8e6cf-118">Anger namnet på Server delens HTTP-inställningar som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="8e6cf-118">Specifies the name of the backend HTTP settings that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e6cf-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e6cf-119">CommonParameters</span></span>
<span data-ttu-id="8e6cf-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e6cf-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e6cf-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e6cf-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e6cf-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8e6cf-122">INPUTS</span></span>

### <span data-ttu-id="8e6cf-123">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8e6cf-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="8e6cf-124">Parametrar: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8e6cf-124">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="8e6cf-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8e6cf-125">OUTPUTS</span></span>

### <span data-ttu-id="8e6cf-126">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="8e6cf-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="8e6cf-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8e6cf-127">NOTES</span></span>

## <span data-ttu-id="8e6cf-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8e6cf-128">RELATED LINKS</span></span>

[<span data-ttu-id="8e6cf-129">Add-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="8e6cf-129">Add-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="8e6cf-130">New-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="8e6cf-130">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="8e6cf-131">Remove-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="8e6cf-131">Remove-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="8e6cf-132">Set-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="8e6cf-132">Set-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()


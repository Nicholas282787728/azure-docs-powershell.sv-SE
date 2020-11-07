---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaybackendhttpsettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayBackendHttpSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayBackendHttpSettings.md
ms.openlocfilehash: f0fa24fd6a7d8ed9cf1a9806ca0a419da8c3deb8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578152"
---
# <span data-ttu-id="65858-101">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="65858-101">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="65858-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="65858-102">SYNOPSIS</span></span>
<span data-ttu-id="65858-103">Hämtar dina backend HTTP-inställningar för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="65858-103">Gets the back-end HTTP settings of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65858-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="65858-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayBackendHttpSettings [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65858-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="65858-105">DESCRIPTION</span></span>
<span data-ttu-id="65858-106">Med cmdleten Get-AzureRmApplicationGatewayBackendHttpSettings får du backend-HTTP-inställningarna för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="65858-106">The Get-AzureRmApplicationGatewayBackendHttpSettings cmdlet gets the back-end HTTP settings of an application gateway.</span></span>

## <span data-ttu-id="65858-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="65858-107">EXAMPLES</span></span>

### <span data-ttu-id="65858-108">Exempel 1: kom tillbaka-HTTP-inställningar efter namn</span><span class="sxs-lookup"><span data-stu-id="65858-108">Example 1: Get back-end HTTP settings by name</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzureRmApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
```

<span data-ttu-id="65858-109">Det första kommandot får den Programgateway som heter ApplicationGateway01 i resurs gruppen som heter ResourceGroup01 och lagrar den i $AppGw variabel. Det andra kommandot får HTTP-inställningarna "Settings01" för $AppGw och lagrar inställningarna i $Settings-variabeln.</span><span class="sxs-lookup"><span data-stu-id="65858-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>

### <span data-ttu-id="65858-110">Exempel 2: få en samling backend-HTTP-inställningar</span><span class="sxs-lookup"><span data-stu-id="65858-110">Example 2: Get a collection of back-end HTTP settings</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SettingsList  = Get-AzureRmApplicationGatewayBackendHttpSettings -ApplicationGateway $AppGw
```

<span data-ttu-id="65858-111">Det första kommandot får den Programgateway som heter ApplicationGateway01 i resurs gruppen som heter ResourceGroup01 och lagrar den i $AppGw variabel. Det andra kommandot hämtar HTTP-inställningarna för $AppGw och lagrar inställningarna i $SettingsList-variabeln.</span><span class="sxs-lookup"><span data-stu-id="65858-111">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the collection of HTTP settings for $AppGw and stores the settings in the $SettingsList variable.</span></span>

## <span data-ttu-id="65858-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="65858-112">PARAMETERS</span></span>

### <span data-ttu-id="65858-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="65858-113">-ApplicationGateway</span></span>
<span data-ttu-id="65858-114">Anger ett objekt för Application Gateway som innehåller backend HTTP-inställningar.</span><span class="sxs-lookup"><span data-stu-id="65858-114">Specifies an application gateway object that contains back-end HTTP settings.</span></span>

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

### <span data-ttu-id="65858-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65858-115">-DefaultProfile</span></span>
<span data-ttu-id="65858-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="65858-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65858-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="65858-117">-Name</span></span>
<span data-ttu-id="65858-118">Anger namnet på Server delens HTTP-inställningar som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="65858-118">Specifies the name of the backend HTTP settings that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65858-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65858-119">CommonParameters</span></span>
<span data-ttu-id="65858-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65858-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65858-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65858-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65858-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="65858-122">INPUTS</span></span>

### <span data-ttu-id="65858-123">System. String</span><span class="sxs-lookup"><span data-stu-id="65858-123">System.String</span></span>

## <span data-ttu-id="65858-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="65858-124">OUTPUTS</span></span>

### <span data-ttu-id="65858-125">Microsoft. Azure. commands. Networks. Models. AzureApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="65858-125">Microsoft.Azure.Commands.Network.Models.AzureApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="65858-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="65858-126">NOTES</span></span>

## <span data-ttu-id="65858-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="65858-127">RELATED LINKS</span></span>

[<span data-ttu-id="65858-128">Add-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="65858-128">Add-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="65858-129">New-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="65858-129">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="65858-130">Remove-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="65858-130">Remove-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="65858-131">Set-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="65858-131">Set-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

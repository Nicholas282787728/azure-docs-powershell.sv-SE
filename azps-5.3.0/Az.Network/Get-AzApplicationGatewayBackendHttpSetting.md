---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaybackendhttpsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 5aeae0fe7a3efe4513869991d1e53ac429f52401
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522866"
---
# <span data-ttu-id="ccdc0-101">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="ccdc0-101">Get-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="ccdc0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ccdc0-102">SYNOPSIS</span></span>
<span data-ttu-id="ccdc0-103">Hämtar dina backend HTTP-inställningar för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="ccdc0-103">Gets the back-end HTTP settings of an application gateway.</span></span>

## <span data-ttu-id="ccdc0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ccdc0-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayBackendHttpSetting [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ccdc0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ccdc0-105">DESCRIPTION</span></span>
<span data-ttu-id="ccdc0-106">Med cmdleten Get-AzApplicationGatewayBackendHttpSetting får du backend-HTTP-inställningarna för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="ccdc0-106">The Get-AzApplicationGatewayBackendHttpSetting cmdlet gets the back-end HTTP settings of an application gateway.</span></span>

## <span data-ttu-id="ccdc0-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ccdc0-107">EXAMPLES</span></span>

### <span data-ttu-id="ccdc0-108">Exempel 1: kom tillbaka-HTTP-inställningar efter namn</span><span class="sxs-lookup"><span data-stu-id="ccdc0-108">Example 1: Get back-end HTTP settings by name</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSetting -Name "Settings01" -ApplicationGateway $AppGw
```

<span data-ttu-id="ccdc0-109">Det första kommandot får den Programgateway som heter ApplicationGateway01 i resurs gruppen som heter ResourceGroup01 och lagrar den i $AppGw variabel. Det andra kommandot får HTTP-inställningarna "Settings01" för $AppGw och lagrar inställningarna i $Settings-variabeln.</span><span class="sxs-lookup"><span data-stu-id="ccdc0-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>

### <span data-ttu-id="ccdc0-110">Exempel 2: få en samling backend-HTTP-inställningar</span><span class="sxs-lookup"><span data-stu-id="ccdc0-110">Example 2: Get a collection of back-end HTTP settings</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SettingsList  = Get-AzApplicationGatewayBackendHttpSetting -ApplicationGateway $AppGw
```

<span data-ttu-id="ccdc0-111">Det första kommandot får den Programgateway som heter ApplicationGateway01 i resurs gruppen som heter ResourceGroup01 och lagrar den i $AppGw variabel. Det andra kommandot hämtar HTTP-inställningarna för $AppGw och lagrar inställningarna i $SettingsList-variabeln.</span><span class="sxs-lookup"><span data-stu-id="ccdc0-111">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the collection of HTTP settings for $AppGw and stores the settings in the $SettingsList variable.</span></span>

## <span data-ttu-id="ccdc0-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ccdc0-112">PARAMETERS</span></span>

### <span data-ttu-id="ccdc0-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ccdc0-113">-ApplicationGateway</span></span>
<span data-ttu-id="ccdc0-114">Anger ett objekt för Application Gateway som innehåller backend HTTP-inställningar.</span><span class="sxs-lookup"><span data-stu-id="ccdc0-114">Specifies an application gateway object that contains back-end HTTP settings.</span></span>

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

### <span data-ttu-id="ccdc0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccdc0-115">-DefaultProfile</span></span>
<span data-ttu-id="ccdc0-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ccdc0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ccdc0-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="ccdc0-117">-Name</span></span>
<span data-ttu-id="ccdc0-118">Anger namnet på Server delens HTTP-inställningar som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="ccdc0-118">Specifies the name of the backend HTTP settings that this cmdlet gets.</span></span>

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

### <span data-ttu-id="ccdc0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccdc0-119">CommonParameters</span></span>
<span data-ttu-id="ccdc0-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ccdc0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccdc0-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ccdc0-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccdc0-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ccdc0-122">INPUTS</span></span>

### <span data-ttu-id="ccdc0-123">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ccdc0-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ccdc0-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ccdc0-124">OUTPUTS</span></span>

### <span data-ttu-id="ccdc0-125">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="ccdc0-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="ccdc0-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ccdc0-126">NOTES</span></span>

## <span data-ttu-id="ccdc0-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ccdc0-127">RELATED LINKS</span></span>

[<span data-ttu-id="ccdc0-128">Add-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="ccdc0-128">Add-AzApplicationGatewayBackendHttpSetting</span></span>](./Add-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="ccdc0-129">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="ccdc0-129">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="ccdc0-130">Remove-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="ccdc0-130">Remove-AzApplicationGatewayBackendHttpSetting</span></span>](./Remove-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="ccdc0-131">Set-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="ccdc0-131">Set-AzApplicationGatewayBackendHttpSetting</span></span>](./Set-AzApplicationGatewayBackendHttpSetting.md)


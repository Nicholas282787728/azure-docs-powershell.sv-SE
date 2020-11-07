---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayredirectconfiguration
schema: 2.0.0
ms.openlocfilehash: ba979a12584d526ba7e3a36d13c44b51704b44f6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929334"
---
# <span data-ttu-id="5549d-101">Remove-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="5549d-101">Remove-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="5549d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5549d-102">SYNOPSIS</span></span>
<span data-ttu-id="5549d-103">Tar bort en omdirigeringsinställningar från en befintlig Programgateway.</span><span class="sxs-lookup"><span data-stu-id="5549d-103">Removes a redirect configuration from an existing Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5549d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5549d-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5549d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5549d-105">DESCRIPTION</span></span>
<span data-ttu-id="5549d-106">Cmdleten **Remove-AzureRmApplicationGatewayRedirectConfiguration** tar bort en omdirigeringsinställningar från en befintlig Programgateway.</span><span class="sxs-lookup"><span data-stu-id="5549d-106">The **Remove-AzureRmApplicationGatewayRedirectConfiguration** cmdlet removes a redirect configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="5549d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5549d-107">EXAMPLES</span></span>

### <span data-ttu-id="5549d-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5549d-108">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$AppGw = Remove-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01"
```

<span data-ttu-id="5549d-109">Det första kommandot får en Programgateway och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="5549d-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="5549d-110">Det andra kommandot tar bort den omdirigerings konfiguration som heter Redirect01 från Application Gateway som lagras i $AppGw.</span><span class="sxs-lookup"><span data-stu-id="5549d-110">The second command removes the redirect configuration named Redirect01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="5549d-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5549d-111">PARAMETERS</span></span>

### <span data-ttu-id="5549d-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5549d-112">-ApplicationGateway</span></span>
<span data-ttu-id="5549d-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5549d-113">The applicationGateway</span></span>

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

### <span data-ttu-id="5549d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5549d-114">-DefaultProfile</span></span>
<span data-ttu-id="5549d-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5549d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5549d-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="5549d-116">-Name</span></span>
<span data-ttu-id="5549d-117">Namnet på omdirigerings konfigurationen</span><span class="sxs-lookup"><span data-stu-id="5549d-117">The name of the redirect configuration</span></span>

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

### <span data-ttu-id="5549d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5549d-118">CommonParameters</span></span>
<span data-ttu-id="5549d-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5549d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5549d-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5549d-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5549d-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5549d-121">INPUTS</span></span>

### <span data-ttu-id="5549d-122">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5549d-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5549d-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5549d-123">OUTPUTS</span></span>

### <span data-ttu-id="5549d-124">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5549d-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5549d-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5549d-125">NOTES</span></span>

## <span data-ttu-id="5549d-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5549d-126">RELATED LINKS</span></span>


---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7C8B47B4-2F6A-45EF-A351-88C8C3F9D0D3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGateway.md
ms.openlocfilehash: d9eb7f4783f950ba001be5b173fca9614422ce9d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584056"
---
# <span data-ttu-id="79728-101">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="79728-101">Set-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="79728-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="79728-102">SYNOPSIS</span></span>
<span data-ttu-id="79728-103">Uppdaterar en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="79728-103">Updates an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79728-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="79728-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79728-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="79728-105">DESCRIPTION</span></span>
<span data-ttu-id="79728-106">Cmdleten **set-AzureRmApplicationGateway** uppdaterar en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="79728-106">The **Set-AzureRmApplicationGateway** cmdlet updates an Azure application gateway.</span></span>

## <span data-ttu-id="79728-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="79728-107">EXAMPLES</span></span>

### <span data-ttu-id="79728-108">Exempel 1: uppdatera en Programgateway</span><span class="sxs-lookup"><span data-stu-id="79728-108">Example 1: Update an application gateway</span></span>
```
PS C:\>$UpdatedAppGw = Set-AzureRmApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="79728-109">Det här kommandot uppdaterar programgatewayen med inställningarna i $AppGw variabel och lagrar den uppdaterade gatewayen i $UpdatedAppGw-variabeln.</span><span class="sxs-lookup"><span data-stu-id="79728-109">This command updates the application gateway with settings in the $AppGw variable and stores the updated gateway in the $UpdatedAppGw variable.</span></span>

## <span data-ttu-id="79728-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="79728-110">PARAMETERS</span></span>

### <span data-ttu-id="79728-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="79728-111">-ApplicationGateway</span></span>
<span data-ttu-id="79728-112">Anger ett objekt för Application Gateway som representerar det tillstånd som Application Gateway ska anges för.</span><span class="sxs-lookup"><span data-stu-id="79728-112">Specifies an application gateway object representing the state to which the application gateway should be set.</span></span>

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

### <span data-ttu-id="79728-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="79728-113">-AsJob</span></span>
<span data-ttu-id="79728-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="79728-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79728-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79728-115">-DefaultProfile</span></span>
<span data-ttu-id="79728-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="79728-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79728-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79728-117">CommonParameters</span></span>
<span data-ttu-id="79728-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79728-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79728-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79728-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79728-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="79728-120">INPUTS</span></span>

### <span data-ttu-id="79728-121">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="79728-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="79728-122">Parametrar: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="79728-122">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="79728-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="79728-123">OUTPUTS</span></span>

### <span data-ttu-id="79728-124">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="79728-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="79728-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="79728-125">NOTES</span></span>

## <span data-ttu-id="79728-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="79728-126">RELATED LINKS</span></span>

[<span data-ttu-id="79728-127">Start-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="79728-127">Start-AzureRmApplicationGateway</span></span>](./Start-AzureRmApplicationGateway.md)


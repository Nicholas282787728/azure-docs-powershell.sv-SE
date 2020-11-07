---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7C8B47B4-2F6A-45EF-A351-88C8C3F9D0D3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGateway.md
ms.openlocfilehash: f755c08b880a9ec97315931843d6dca6f5fc3229
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586464"
---
# <span data-ttu-id="71e42-101">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="71e42-101">Set-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="71e42-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="71e42-102">SYNOPSIS</span></span>
<span data-ttu-id="71e42-103">Uppdaterar en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="71e42-103">Updates an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71e42-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="71e42-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGateway -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71e42-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="71e42-105">DESCRIPTION</span></span>
<span data-ttu-id="71e42-106">Cmdleten **set-AzureRmApplicationGateway** uppdaterar en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="71e42-106">The **Set-AzureRmApplicationGateway** cmdlet updates an Azure application gateway.</span></span>

## <span data-ttu-id="71e42-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="71e42-107">EXAMPLES</span></span>

### <span data-ttu-id="71e42-108">Exempel 1: uppdatera en Programgateway</span><span class="sxs-lookup"><span data-stu-id="71e42-108">Example 1: Update an application gateway</span></span>
```
PS C:\>$UpdatedAppGw = Set-AzureRmApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="71e42-109">Det här kommandot uppdaterar programgatewayen med inställningarna i $AppGw variabel och lagrar den uppdaterade gatewayen i $UpdatedAppGw-variabeln.</span><span class="sxs-lookup"><span data-stu-id="71e42-109">This command updates the application gateway with settings in the $AppGw variable and stores the updated gateway in the $UpdatedAppGw variable.</span></span>

## <span data-ttu-id="71e42-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="71e42-110">PARAMETERS</span></span>

### <span data-ttu-id="71e42-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="71e42-111">-ApplicationGateway</span></span>
<span data-ttu-id="71e42-112">Anger ett objekt för Application Gateway som representerar det tillstånd som Application Gateway ska anges för.</span><span class="sxs-lookup"><span data-stu-id="71e42-112">Specifies an application gateway object representing the state to which the application gateway should be set.</span></span>

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

### <span data-ttu-id="71e42-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71e42-113">-DefaultProfile</span></span>
<span data-ttu-id="71e42-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="71e42-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71e42-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71e42-115">CommonParameters</span></span>
<span data-ttu-id="71e42-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71e42-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71e42-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71e42-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71e42-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="71e42-118">INPUTS</span></span>

### <span data-ttu-id="71e42-119">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="71e42-119">PSApplicationGateway</span></span>
<span data-ttu-id="71e42-120">Parametern ' ApplicationGateway ' godkänner värdet av typen ' PSApplicationGateway ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="71e42-120">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="71e42-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="71e42-121">OUTPUTS</span></span>

### <span data-ttu-id="71e42-122">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="71e42-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="71e42-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="71e42-123">NOTES</span></span>

## <span data-ttu-id="71e42-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="71e42-124">RELATED LINKS</span></span>

[<span data-ttu-id="71e42-125">Start-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="71e42-125">Start-AzureRmApplicationGateway</span></span>](./Start-AzureRmApplicationGateway.md)


---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7C8B47B4-2F6A-45EF-A351-88C8C3F9D0D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGateway.md
ms.openlocfilehash: b62a41c2c97055f0ef090ed5def3dc771ae3c1ed
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924305"
---
# <span data-ttu-id="a13e4-101">Set-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a13e4-101">Set-AzApplicationGateway</span></span>

## <span data-ttu-id="a13e4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a13e4-102">SYNOPSIS</span></span>
<span data-ttu-id="a13e4-103">Uppdaterar en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="a13e4-103">Updates an application gateway.</span></span>

## <span data-ttu-id="a13e4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a13e4-104">SYNTAX</span></span>

```
Set-AzApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a13e4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a13e4-105">DESCRIPTION</span></span>
<span data-ttu-id="a13e4-106">Cmdleten **set-AzApplicationGateway** uppdaterar en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="a13e4-106">The **Set-AzApplicationGateway** cmdlet updates an Azure application gateway.</span></span>

## <span data-ttu-id="a13e4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a13e4-107">EXAMPLES</span></span>

### <span data-ttu-id="a13e4-108">Exempel 1: uppdatera en Programgateway</span><span class="sxs-lookup"><span data-stu-id="a13e4-108">Example 1: Update an application gateway</span></span>
```
PS C:\>$UpdatedAppGw = Set-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="a13e4-109">Det här kommandot uppdaterar programgatewayen med inställningarna i $AppGw variabel och lagrar den uppdaterade gatewayen i $UpdatedAppGw-variabeln.</span><span class="sxs-lookup"><span data-stu-id="a13e4-109">This command updates the application gateway with settings in the $AppGw variable and stores the updated gateway in the $UpdatedAppGw variable.</span></span>

## <span data-ttu-id="a13e4-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a13e4-110">PARAMETERS</span></span>

### <span data-ttu-id="a13e4-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a13e4-111">-ApplicationGateway</span></span>
<span data-ttu-id="a13e4-112">Anger ett objekt för Application Gateway som representerar det tillstånd som Application Gateway ska anges för.</span><span class="sxs-lookup"><span data-stu-id="a13e4-112">Specifies an application gateway object representing the state to which the application gateway should be set.</span></span>

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

### <span data-ttu-id="a13e4-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a13e4-113">-AsJob</span></span>
<span data-ttu-id="a13e4-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="a13e4-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a13e4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a13e4-115">-DefaultProfile</span></span>
<span data-ttu-id="a13e4-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a13e4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a13e4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a13e4-117">CommonParameters</span></span>
<span data-ttu-id="a13e4-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a13e4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a13e4-119">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a13e4-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a13e4-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a13e4-120">INPUTS</span></span>

### <span data-ttu-id="a13e4-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a13e4-121">PSApplicationGateway</span></span>
<span data-ttu-id="a13e4-122">Parametern ' ApplicationGateway ' godkänner värdet av typen ' PSApplicationGateway ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="a13e4-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="a13e4-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a13e4-123">OUTPUTS</span></span>

### <span data-ttu-id="a13e4-124">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a13e4-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a13e4-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a13e4-125">NOTES</span></span>

## <span data-ttu-id="a13e4-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a13e4-126">RELATED LINKS</span></span>

[<span data-ttu-id="a13e4-127">Start-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a13e4-127">Start-AzApplicationGateway</span></span>](./Start-AzApplicationGateway.md)


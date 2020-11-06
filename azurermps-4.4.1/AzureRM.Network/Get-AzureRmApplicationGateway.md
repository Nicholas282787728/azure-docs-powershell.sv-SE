---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 77CDEE77-FD5D-4C2D-B027-FF1F6FF6618E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGateway.md
ms.openlocfilehash: 6c15f0dce8102acb609b2e7dcfb9ca4c17626906
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574618"
---
# <span data-ttu-id="8e16b-101">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8e16b-101">Get-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="8e16b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8e16b-102">SYNOPSIS</span></span>
<span data-ttu-id="8e16b-103">Hämtar en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="8e16b-103">Gets an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e16b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8e16b-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGateway [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e16b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8e16b-105">DESCRIPTION</span></span>
<span data-ttu-id="8e16b-106">Cmdleten **Get-AzureRmApplicationGateway** hämtar en programport.</span><span class="sxs-lookup"><span data-stu-id="8e16b-106">The **Get-AzureRmApplicationGateway** cmdlet gets an application gateway.</span></span>

## <span data-ttu-id="8e16b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8e16b-107">EXAMPLES</span></span>

### <span data-ttu-id="8e16b-108">Exempel 1: skaffa en angiven Programgateway</span><span class="sxs-lookup"><span data-stu-id="8e16b-108">Example 1: Get a specified application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="8e16b-109">Det här kommandot hämtar den Programgateway som heter ApplicationGateway01 som tillhör resurs gruppen som heter ResourceGroup01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="8e16b-109">This command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

### <span data-ttu-id="8e16b-110">Exempel 2: Hämta en lista med program gateways i en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="8e16b-110">Example 2: Get a list of application gateways in a resource group</span></span>
```
PS C:\>$AppGwList = Get-AzureRmApplicationGateway -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="8e16b-111">Det här kommandot får en lista över alla programgateways i resurs gruppen som heter ResourceGroup01 och lagrar den i $AppGwList variabeln.</span><span class="sxs-lookup"><span data-stu-id="8e16b-111">This command gets a list of all the application gateways in the resource group named ResourceGroup01 and stores it in the $AppGwList variable.</span></span>

### <span data-ttu-id="8e16b-112">Exempel 3: Hämta en lista med programgateways i ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="8e16b-112">Example 3: Get a list of application gateways in a subscription</span></span>
```
PS C:\>$AppGwList = Get-AzureRmApplicationGateway
```

<span data-ttu-id="8e16b-113">Det här kommandot får en lista över alla programgateways i prenumerationen och lagrar dem i $AppGwList variabel.</span><span class="sxs-lookup"><span data-stu-id="8e16b-113">This command gets a list of all the application gateways in the subscription and stores it in the $AppGwList variable.</span></span>

## <span data-ttu-id="8e16b-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8e16b-114">PARAMETERS</span></span>

### <span data-ttu-id="8e16b-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="8e16b-115">-Name</span></span>
<span data-ttu-id="8e16b-116">Anger namnet på den Application Gateway som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="8e16b-116">Specifies the name of the application gateway that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e16b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e16b-117">-ResourceGroupName</span></span>
<span data-ttu-id="8e16b-118">Anger namnet på den resurs grupp som innehåller programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="8e16b-118">Specifies the name of the resource group that contains the application gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e16b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e16b-119">-DefaultProfile</span></span>
<span data-ttu-id="8e16b-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8e16b-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e16b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e16b-121">CommonParameters</span></span>
<span data-ttu-id="8e16b-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e16b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e16b-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e16b-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e16b-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8e16b-124">INPUTS</span></span>

### <span data-ttu-id="8e16b-125">System. String</span><span class="sxs-lookup"><span data-stu-id="8e16b-125">System.String</span></span>

## <span data-ttu-id="8e16b-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8e16b-126">OUTPUTS</span></span>

### <span data-ttu-id="8e16b-127">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8e16b-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8e16b-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8e16b-128">NOTES</span></span>

## <span data-ttu-id="8e16b-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8e16b-129">RELATED LINKS</span></span>

[<span data-ttu-id="8e16b-130">Stopp-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8e16b-130">Stop-AzureRmApplicationGateway</span></span>](./Stop-AzureRmApplicationGateway.md)



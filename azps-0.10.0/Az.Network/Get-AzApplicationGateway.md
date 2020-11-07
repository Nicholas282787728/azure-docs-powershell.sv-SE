---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 77CDEE77-FD5D-4C2D-B027-FF1F6FF6618E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGateway.md
ms.openlocfilehash: 61547a4ee5f60fccc371ca7b2c426ca1a4bbb005
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922353"
---
# <span data-ttu-id="58261-101">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="58261-101">Get-AzApplicationGateway</span></span>

## <span data-ttu-id="58261-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="58261-102">SYNOPSIS</span></span>
<span data-ttu-id="58261-103">Hämtar en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="58261-103">Gets an application gateway.</span></span>

## <span data-ttu-id="58261-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="58261-104">SYNTAX</span></span>

```
Get-AzApplicationGateway [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58261-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="58261-105">DESCRIPTION</span></span>
<span data-ttu-id="58261-106">Cmdleten **Get-AzApplicationGateway** hämtar en programport.</span><span class="sxs-lookup"><span data-stu-id="58261-106">The **Get-AzApplicationGateway** cmdlet gets an application gateway.</span></span>

## <span data-ttu-id="58261-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="58261-107">EXAMPLES</span></span>

### <span data-ttu-id="58261-108">Exempel 1: skaffa en angiven Programgateway</span><span class="sxs-lookup"><span data-stu-id="58261-108">Example 1: Get a specified application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="58261-109">Det här kommandot hämtar den Programgateway som heter ApplicationGateway01 som tillhör resurs gruppen som heter ResourceGroup01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="58261-109">This command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

### <span data-ttu-id="58261-110">Exempel 2: Hämta en lista med program gateways i en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="58261-110">Example 2: Get a list of application gateways in a resource group</span></span>
```
PS C:\>$AppGwList = Get-AzApplicationGateway -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="58261-111">Det här kommandot får en lista över alla programgateways i resurs gruppen som heter ResourceGroup01 och lagrar den i $AppGwList variabeln.</span><span class="sxs-lookup"><span data-stu-id="58261-111">This command gets a list of all the application gateways in the resource group named ResourceGroup01 and stores it in the $AppGwList variable.</span></span>

### <span data-ttu-id="58261-112">Exempel 3: Hämta en lista med programgateways i ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="58261-112">Example 3: Get a list of application gateways in a subscription</span></span>
```
PS C:\>$AppGwList = Get-AzApplicationGateway
```

<span data-ttu-id="58261-113">Det här kommandot får en lista över alla programgateways i prenumerationen och lagrar dem i $AppGwList variabel.</span><span class="sxs-lookup"><span data-stu-id="58261-113">This command gets a list of all the application gateways in the subscription and stores it in the $AppGwList variable.</span></span>

## <span data-ttu-id="58261-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="58261-114">PARAMETERS</span></span>

### <span data-ttu-id="58261-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58261-115">-DefaultProfile</span></span>
<span data-ttu-id="58261-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="58261-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58261-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="58261-117">-Name</span></span>
<span data-ttu-id="58261-118">Anger namnet på den Application Gateway som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="58261-118">Specifies the name of the application gateway that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58261-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58261-119">-ResourceGroupName</span></span>
<span data-ttu-id="58261-120">Anger namnet på den resurs grupp som innehåller programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="58261-120">Specifies the name of the resource group that contains the application gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58261-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58261-121">CommonParameters</span></span>
<span data-ttu-id="58261-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58261-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58261-123">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58261-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58261-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="58261-124">INPUTS</span></span>

### <span data-ttu-id="58261-125">System. String</span><span class="sxs-lookup"><span data-stu-id="58261-125">System.String</span></span>

## <span data-ttu-id="58261-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="58261-126">OUTPUTS</span></span>

### <span data-ttu-id="58261-127">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="58261-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="58261-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="58261-128">NOTES</span></span>

## <span data-ttu-id="58261-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="58261-129">RELATED LINKS</span></span>

[<span data-ttu-id="58261-130">Stopp-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="58261-130">Stop-AzApplicationGateway</span></span>](./Stop-AzApplicationGateway.md)



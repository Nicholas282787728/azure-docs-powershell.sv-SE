---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 17BA2ED5-E347-45C0-AF20-CDD288469514
online version: ''
schema: 2.0.0
ms.openlocfilehash: a07afcadb2207f2e4377601abfa6094bc3293328
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099638"
---
# <span data-ttu-id="708cc-101">Stop-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="708cc-101">Stop-AzureApplicationGateway</span></span>

## <span data-ttu-id="708cc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="708cc-102">SYNOPSIS</span></span>
<span data-ttu-id="708cc-103">Stoppar en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="708cc-103">Stops an application gateway.</span></span>

## <span data-ttu-id="708cc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="708cc-104">SYNTAX</span></span>

```
Stop-AzureApplicationGateway -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="708cc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="708cc-105">DESCRIPTION</span></span>
<span data-ttu-id="708cc-106">Cmdleten **Stop-AzureApplicationGateway** stoppar en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="708cc-106">The **Stop-AzureApplicationGateway** cmdlet stops an application gateway.</span></span>

## <span data-ttu-id="708cc-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="708cc-107">EXAMPLES</span></span>

### <span data-ttu-id="708cc-108">Exempel 1: stoppa en Programgateway</span><span class="sxs-lookup"><span data-stu-id="708cc-108">Example 1: Stop an application gateway</span></span>
```
PS C:\> Stop-AzureApplicationGateway -Name "ApplicationGateway06"
```

<span data-ttu-id="708cc-109">Det här kommandot stoppar programgatewayen med namnet ApplicationGateway06.</span><span class="sxs-lookup"><span data-stu-id="708cc-109">This command stops the application gateway named ApplicationGateway06.</span></span>

## <span data-ttu-id="708cc-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="708cc-110">PARAMETERS</span></span>

### <span data-ttu-id="708cc-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="708cc-111">-Name</span></span>
<span data-ttu-id="708cc-112">Anger namnet på den Programgateway som denna cmdlet slutar.</span><span class="sxs-lookup"><span data-stu-id="708cc-112">Specifies the name of the application gateway that this cmdlet stops.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="708cc-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="708cc-113">-Profile</span></span>
<span data-ttu-id="708cc-114">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="708cc-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="708cc-115">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="708cc-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="708cc-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="708cc-116">CommonParameters</span></span>
<span data-ttu-id="708cc-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="708cc-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="708cc-118">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="708cc-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="708cc-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="708cc-119">INPUTS</span></span>

### <span data-ttu-id="708cc-120">System. String</span><span class="sxs-lookup"><span data-stu-id="708cc-120">System.String</span></span>

## <span data-ttu-id="708cc-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="708cc-121">OUTPUTS</span></span>

### <span data-ttu-id="708cc-122">Microsoft. WindowsAzure. Management. ApplicationGateway. Models. ApplicationGatewayOperationResponse</span><span class="sxs-lookup"><span data-stu-id="708cc-122">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="708cc-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="708cc-123">NOTES</span></span>

## <span data-ttu-id="708cc-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="708cc-124">RELATED LINKS</span></span>

[<span data-ttu-id="708cc-125">Get-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="708cc-125">Get-AzureApplicationGateway</span></span>](./Get-AzureApplicationGateway.md)

[<span data-ttu-id="708cc-126">New-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="708cc-126">New-AzureApplicationGateway</span></span>](./New-AzureApplicationGateway.md)

[<span data-ttu-id="708cc-127">Remove-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="708cc-127">Remove-AzureApplicationGateway</span></span>](./Remove-AzureApplicationGateway.md)

[<span data-ttu-id="708cc-128">Start-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="708cc-128">Start-AzureApplicationGateway</span></span>](./Start-AzureApplicationGateway.md)

[<span data-ttu-id="708cc-129">Update-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="708cc-129">Update-AzureApplicationGateway</span></span>](./Update-AzureApplicationGateway.md)

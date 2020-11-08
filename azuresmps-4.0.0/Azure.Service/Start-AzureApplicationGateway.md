---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: D50984B7-FD97-4713-8E56-1C06D2B008E3
online version: ''
schema: 2.0.0
ms.openlocfilehash: a01d59d6a0755b3763eaef9b7532326ca0ffd402
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099009"
---
# <span data-ttu-id="86c42-101">Start-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="86c42-101">Start-AzureApplicationGateway</span></span>

## <span data-ttu-id="86c42-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="86c42-102">SYNOPSIS</span></span>
<span data-ttu-id="86c42-103">Startar en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="86c42-103">Starts an application gateway.</span></span>

## <span data-ttu-id="86c42-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="86c42-104">SYNTAX</span></span>

```
Start-AzureApplicationGateway -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="86c42-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="86c42-105">DESCRIPTION</span></span>
<span data-ttu-id="86c42-106">Cmdleten **Start-AzureApplicationGateway** startar en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="86c42-106">The **Start-AzureApplicationGateway** cmdlet starts an application gateway.</span></span>

## <span data-ttu-id="86c42-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="86c42-107">EXAMPLES</span></span>

### <span data-ttu-id="86c42-108">Exempel 1: starta en Programgateway</span><span class="sxs-lookup"><span data-stu-id="86c42-108">Example 1: Start an application gateway</span></span>
```
PS C:\> Start-AzureApplicationGateway -Name "ApplicationGateway06"
```

<span data-ttu-id="86c42-109">Det här kommandot startar den Programgateway som heter ApplicationGateway06.</span><span class="sxs-lookup"><span data-stu-id="86c42-109">This command starts the application gateway named ApplicationGateway06.</span></span>

## <span data-ttu-id="86c42-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="86c42-110">PARAMETERS</span></span>

### <span data-ttu-id="86c42-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="86c42-111">-Name</span></span>
<span data-ttu-id="86c42-112">Anger namnet på den Programgateway som den här cmdleten startar.</span><span class="sxs-lookup"><span data-stu-id="86c42-112">Specifies the name of the application gateway that this cmdlet starts.</span></span>

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

### <span data-ttu-id="86c42-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="86c42-113">-Profile</span></span>
<span data-ttu-id="86c42-114">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="86c42-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="86c42-115">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="86c42-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="86c42-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86c42-116">CommonParameters</span></span>
<span data-ttu-id="86c42-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86c42-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86c42-118">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86c42-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86c42-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="86c42-119">INPUTS</span></span>

### <span data-ttu-id="86c42-120">System. String</span><span class="sxs-lookup"><span data-stu-id="86c42-120">System.String</span></span>

## <span data-ttu-id="86c42-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="86c42-121">OUTPUTS</span></span>

### <span data-ttu-id="86c42-122">Microsoft. WindowsAzure. Management. ApplicationGateway. Models. ApplicationGatewayOperationResponse</span><span class="sxs-lookup"><span data-stu-id="86c42-122">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="86c42-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="86c42-123">NOTES</span></span>

## <span data-ttu-id="86c42-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="86c42-124">RELATED LINKS</span></span>

[<span data-ttu-id="86c42-125">Get-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="86c42-125">Get-AzureApplicationGateway</span></span>](./Get-AzureApplicationGateway.md)

[<span data-ttu-id="86c42-126">New-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="86c42-126">New-AzureApplicationGateway</span></span>](./New-AzureApplicationGateway.md)

[<span data-ttu-id="86c42-127">Remove-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="86c42-127">Remove-AzureApplicationGateway</span></span>](./Remove-AzureApplicationGateway.md)

[<span data-ttu-id="86c42-128">Stopp-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="86c42-128">Stop-AzureApplicationGateway</span></span>](./Stop-AzureApplicationGateway.md)

[<span data-ttu-id="86c42-129">Update-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="86c42-129">Update-AzureApplicationGateway</span></span>](./Update-AzureApplicationGateway.md)



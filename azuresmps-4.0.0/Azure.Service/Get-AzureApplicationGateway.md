---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 0AED21E8-A638-4019-9B23-447472E56C7A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 202066cfc2649b0f56810123e211bbeb5d69720f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093396"
---
# <span data-ttu-id="558ac-101">Get-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="558ac-101">Get-AzureApplicationGateway</span></span>

## <span data-ttu-id="558ac-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="558ac-102">SYNOPSIS</span></span>
<span data-ttu-id="558ac-103">Hämtar en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="558ac-103">Gets an Application Gateway.</span></span>

## <span data-ttu-id="558ac-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="558ac-104">SYNTAX</span></span>

```
Get-AzureApplicationGateway [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="558ac-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="558ac-105">DESCRIPTION</span></span>
<span data-ttu-id="558ac-106">Cmdleten **Get-AzureApplicationGateway** hämtar en befintlig Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="558ac-106">The **Get-AzureApplicationGateway** cmdlet gets an existing Azure Application Gateway.</span></span>

## <span data-ttu-id="558ac-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="558ac-107">EXAMPLES</span></span>

### <span data-ttu-id="558ac-108">Exempel 1: skaffa en Programgateway</span><span class="sxs-lookup"><span data-stu-id="558ac-108">Example 1: Get an Application Gateway</span></span>
```
PS C:\> Get-AzureApplicationGateway -Name "ApplicationGateway06"
```

<span data-ttu-id="558ac-109">Det här kommandot hämtar programgatewayen med namnet ApplicationGateway06.</span><span class="sxs-lookup"><span data-stu-id="558ac-109">This command gets the Application Gateway named ApplicationGateway06.</span></span>

### <span data-ttu-id="558ac-110">Exempel 2: Hämta alla programgateways</span><span class="sxs-lookup"><span data-stu-id="558ac-110">Example 2: Get all Application Gateways</span></span>
```
PS C:\> Get-AzureApplicationGateway
```

<span data-ttu-id="558ac-111">Det här kommandot får alla programgateways under din prenumeration.</span><span class="sxs-lookup"><span data-stu-id="558ac-111">This command gets all the Application Gateways under your subscription.</span></span>

## <span data-ttu-id="558ac-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="558ac-112">PARAMETERS</span></span>

### <span data-ttu-id="558ac-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="558ac-113">-Name</span></span>
<span data-ttu-id="558ac-114">Anger namnet på den Application Gateway som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="558ac-114">Specifies the name of the Application Gateway that this cmdlet gets.</span></span>

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

### <span data-ttu-id="558ac-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="558ac-115">-Profile</span></span>
<span data-ttu-id="558ac-116">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="558ac-116">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="558ac-117">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="558ac-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="558ac-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="558ac-118">CommonParameters</span></span>
<span data-ttu-id="558ac-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="558ac-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="558ac-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="558ac-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="558ac-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="558ac-121">INPUTS</span></span>

### <span data-ttu-id="558ac-122">System. String</span><span class="sxs-lookup"><span data-stu-id="558ac-122">System.String</span></span>

## <span data-ttu-id="558ac-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="558ac-123">OUTPUTS</span></span>

### <span data-ttu-id="558ac-124">Microsoft. Azure. Networking. ApplicationGatewayObjectModel. ApplicationGateway, IEnumerable<Microsoft. Azure. Networking. ApplicationGatewayObjectModel. ApplicationGateway></span><span class="sxs-lookup"><span data-stu-id="558ac-124">Microsoft.Azure.Networking.ApplicationGatewayObjectModel.ApplicationGateway, IEnumerable<Microsoft.Azure.Networking.ApplicationGatewayObjectModel.ApplicationGateway></span></span>

## <span data-ttu-id="558ac-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="558ac-125">NOTES</span></span>

## <span data-ttu-id="558ac-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="558ac-126">RELATED LINKS</span></span>

[<span data-ttu-id="558ac-127">New-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="558ac-127">New-AzureApplicationGateway</span></span>](./New-AzureApplicationGateway.md)

[<span data-ttu-id="558ac-128">Remove-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="558ac-128">Remove-AzureApplicationGateway</span></span>](./Remove-AzureApplicationGateway.md)

[<span data-ttu-id="558ac-129">Start-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="558ac-129">Start-AzureApplicationGateway</span></span>](./Start-AzureApplicationGateway.md)

[<span data-ttu-id="558ac-130">Stopp-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="558ac-130">Stop-AzureApplicationGateway</span></span>](./Stop-AzureApplicationGateway.md)

[<span data-ttu-id="558ac-131">Update-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="558ac-131">Update-AzureApplicationGateway</span></span>](./Update-AzureApplicationGateway.md)



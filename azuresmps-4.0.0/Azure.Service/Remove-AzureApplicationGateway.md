---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 128AD64D-709A-4B59-B233-4221A9120AE1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4803fd24952066c4dcea72daaf0c999b64ae4c5d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099727"
---
# <span data-ttu-id="334ca-101">Remove-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="334ca-101">Remove-AzureApplicationGateway</span></span>

## <span data-ttu-id="334ca-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="334ca-102">SYNOPSIS</span></span>
<span data-ttu-id="334ca-103">Tar bort en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="334ca-103">Removes an application gateway.</span></span>

## <span data-ttu-id="334ca-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="334ca-104">SYNTAX</span></span>

```
Remove-AzureApplicationGateway -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="334ca-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="334ca-105">DESCRIPTION</span></span>
<span data-ttu-id="334ca-106">Cmdleten **Remove-AzureApplicationGateway** tar bort en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="334ca-106">The **Remove-AzureApplicationGateway** cmdlet removes an application gateway.</span></span>

## <span data-ttu-id="334ca-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="334ca-107">EXAMPLES</span></span>

### <span data-ttu-id="334ca-108">Exempel 1: ta bort en Programgateway</span><span class="sxs-lookup"><span data-stu-id="334ca-108">Example 1: Remove an application gateway</span></span>
```
PS C:\> Remove-AzureApplicationGateway -Name "ApplicationGateway06"
```

<span data-ttu-id="334ca-109">Det här kommandot tar bort programgatewayen med namnet ApplicationGateway06.</span><span class="sxs-lookup"><span data-stu-id="334ca-109">This command removes the application gateway named ApplicationGateway06.</span></span>

## <span data-ttu-id="334ca-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="334ca-110">PARAMETERS</span></span>

### <span data-ttu-id="334ca-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="334ca-111">-Name</span></span>
<span data-ttu-id="334ca-112">Anger namnet på den Programgateway som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="334ca-112">Specifies the name of the application gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="334ca-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="334ca-113">-Profile</span></span>
<span data-ttu-id="334ca-114">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="334ca-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="334ca-115">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="334ca-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="334ca-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="334ca-116">CommonParameters</span></span>
<span data-ttu-id="334ca-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="334ca-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="334ca-118">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="334ca-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="334ca-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="334ca-119">INPUTS</span></span>

### <span data-ttu-id="334ca-120">System. String</span><span class="sxs-lookup"><span data-stu-id="334ca-120">System.String</span></span>

## <span data-ttu-id="334ca-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="334ca-121">OUTPUTS</span></span>

### <span data-ttu-id="334ca-122">Microsoft. WindowsAzure. Management. ApplicationGateway. Models. ApplicationGatewayOperationResponse</span><span class="sxs-lookup"><span data-stu-id="334ca-122">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="334ca-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="334ca-123">NOTES</span></span>

## <span data-ttu-id="334ca-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="334ca-124">RELATED LINKS</span></span>

[<span data-ttu-id="334ca-125">Get-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="334ca-125">Get-AzureApplicationGateway</span></span>](./Get-AzureApplicationGateway.md)

[<span data-ttu-id="334ca-126">New-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="334ca-126">New-AzureApplicationGateway</span></span>](./New-AzureApplicationGateway.md)

[<span data-ttu-id="334ca-127">Start-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="334ca-127">Start-AzureApplicationGateway</span></span>](./Start-AzureApplicationGateway.md)

[<span data-ttu-id="334ca-128">Stopp-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="334ca-128">Stop-AzureApplicationGateway</span></span>](./Stop-AzureApplicationGateway.md)

[<span data-ttu-id="334ca-129">Update-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="334ca-129">Update-AzureApplicationGateway</span></span>](./Update-AzureApplicationGateway.md)



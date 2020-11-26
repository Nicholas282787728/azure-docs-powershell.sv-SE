---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azautoapprovedprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAutoApprovedPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAutoApprovedPrivateLinkService.md
ms.openlocfilehash: b03aad1f76c5151746d50e69bc48ccf10e60842f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258323"
---
# <span data-ttu-id="d6005-101">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d6005-101">Get-AzAutoApprovedPrivateLinkService</span></span>

## <span data-ttu-id="d6005-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d6005-102">SYNOPSIS</span></span>
<span data-ttu-id="d6005-103">Hämtar en matris med privata länk tjänst-ID som kan länkas till en privat slut punkt med automatisk godkänd.</span><span class="sxs-lookup"><span data-stu-id="d6005-103">Gets an array of private link service id that can be linked to a private end point with auto approved.</span></span>

## <span data-ttu-id="d6005-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d6005-104">SYNTAX</span></span>

```
Get-AzAutoApprovedPrivateLinkService -Location <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6005-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d6005-105">DESCRIPTION</span></span>
<span data-ttu-id="d6005-106">**Get-AzAutoApprovedPrivateLinkService** hämtar en matris med privata länk tjänst-ID som kan länkas till en privat slut punkt med automatisk godkänd.</span><span class="sxs-lookup"><span data-stu-id="d6005-106">The **Get-AzAutoApprovedPrivateLinkService** gets an array of private link service id that can be linked to a private end point with auto approved.</span></span>

## <span data-ttu-id="d6005-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d6005-107">EXAMPLES</span></span>

### <span data-ttu-id="d6005-108">Exempel</span><span class="sxs-lookup"><span data-stu-id="d6005-108">Example</span></span>
```
Get-AzAutoApprovedPrivateLinkService -Location westus -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="d6005-109">I det här exemplet returneras en matris av Private Link service-ID som kan länkas till en privat slut punkt med automatisk godkänd.</span><span class="sxs-lookup"><span data-stu-id="d6005-109">This example return an array of private link service id that can be linked to a private end point with auto approved.</span></span>

## <span data-ttu-id="d6005-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d6005-110">PARAMETERS</span></span>

### <span data-ttu-id="d6005-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6005-111">-DefaultProfile</span></span>
<span data-ttu-id="d6005-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d6005-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6005-113">-Plats</span><span class="sxs-lookup"><span data-stu-id="d6005-113">-Location</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6005-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6005-114">-ResourceGroupName</span></span>
<span data-ttu-id="d6005-115">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="d6005-115">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="d6005-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6005-116">CommonParameters</span></span>
<span data-ttu-id="d6005-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6005-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6005-118">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d6005-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6005-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d6005-119">INPUTS</span></span>

### <span data-ttu-id="d6005-120">Ingen</span><span class="sxs-lookup"><span data-stu-id="d6005-120">None</span></span>

## <span data-ttu-id="d6005-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d6005-121">OUTPUTS</span></span>

### <span data-ttu-id="d6005-122">Microsoft. Azure. commands. Networks. Models. PSAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d6005-122">Microsoft.Azure.Commands.Network.Models.PSAutoApprovedPrivateLinkService</span></span>

## <span data-ttu-id="d6005-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d6005-123">NOTES</span></span>

## <span data-ttu-id="d6005-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d6005-124">RELATED LINKS</span></span>
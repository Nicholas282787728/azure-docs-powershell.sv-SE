---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 2099938F-5325-416C-AE10-6813546A1055
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/get-azmediaservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceKey.md
ms.openlocfilehash: a01aeaa5868ece4f376dd5be934ba1029379958b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092262"
---
# <span data-ttu-id="b2fd5-101">Get-AzMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="b2fd5-101">Get-AzMediaServiceKey</span></span>

## <span data-ttu-id="b2fd5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b2fd5-102">SYNOPSIS</span></span>
<span data-ttu-id="b2fd5-103">Hämtar viktig information för åtkomst till den REST-slutpunkt som är associerad med medie tjänsten.</span><span class="sxs-lookup"><span data-stu-id="b2fd5-103">Gets key information for accessing the REST endpoint associated with the media service.</span></span>

## <span data-ttu-id="b2fd5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b2fd5-104">SYNTAX</span></span>

```
Get-AzMediaServiceKey [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2fd5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b2fd5-105">DESCRIPTION</span></span>
<span data-ttu-id="b2fd5-106">Cmdleten **Get-AzMediaServiceKey** hämtar viktig information för att få åtkomst till den ompresentations status överföring (rest) som är associerad med Azure Media-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="b2fd5-106">The **Get-AzMediaServiceKey** cmdlet gets key information for accessing the Representational State Transfer (REST) endpoint associated with the Azure media service.</span></span>

## <span data-ttu-id="b2fd5-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b2fd5-107">EXAMPLES</span></span>

### <span data-ttu-id="b2fd5-108">Exempel 1: Hämta viktig information för att komma åt medie tjänsten</span><span class="sxs-lookup"><span data-stu-id="b2fd5-108">Example 1: Get the key information for accessing the media service</span></span>
```
PS C:\>Get-AzMediaServiceKey -ResourceGroupName "ResourceGroup001" -AccountName "MediaService001"
```

<span data-ttu-id="b2fd5-109">Det här kommandot får viktig information för åtkomst till medie tjänsten med namnet MediaService001 som tillhör resurs gruppen med namnet ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="b2fd5-109">This command gets the key information for accessing the media service named MediaService001 that belongs to the resource group named ResourceGroup001.</span></span>

## <span data-ttu-id="b2fd5-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b2fd5-110">PARAMETERS</span></span>

### <span data-ttu-id="b2fd5-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b2fd5-111">-AccountName</span></span>
<span data-ttu-id="b2fd5-112">Anger namnet på den medie tjänst som denna cmdlet hämtar medie tjänstens nycklar från.</span><span class="sxs-lookup"><span data-stu-id="b2fd5-112">Specifies the name of the media service that this cmdlet gets the media service keys from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2fd5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2fd5-113">-DefaultProfile</span></span>
<span data-ttu-id="b2fd5-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="b2fd5-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b2fd5-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2fd5-115">-ResourceGroupName</span></span>
<span data-ttu-id="b2fd5-116">Anger namnet på den resurs grupp som innehåller medie tjänsten.</span><span class="sxs-lookup"><span data-stu-id="b2fd5-116">Specifies the name of the resource group that contains the media service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2fd5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2fd5-117">CommonParameters</span></span>
<span data-ttu-id="b2fd5-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2fd5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2fd5-119">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2fd5-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2fd5-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b2fd5-120">INPUTS</span></span>

### <span data-ttu-id="b2fd5-121">System. String</span><span class="sxs-lookup"><span data-stu-id="b2fd5-121">System.String</span></span>

## <span data-ttu-id="b2fd5-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b2fd5-122">OUTPUTS</span></span>

### <span data-ttu-id="b2fd5-123">Microsoft. Azure. commands. Media. Models. PSServiceKeys</span><span class="sxs-lookup"><span data-stu-id="b2fd5-123">Microsoft.Azure.Commands.Media.Models.PSServiceKeys</span></span>

## <span data-ttu-id="b2fd5-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b2fd5-124">NOTES</span></span>

## <span data-ttu-id="b2fd5-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b2fd5-125">RELATED LINKS</span></span>

[<span data-ttu-id="b2fd5-126">Set-AzMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="b2fd5-126">Set-AzMediaServiceKey</span></span>](./Set-AzMediaServiceKey.md)



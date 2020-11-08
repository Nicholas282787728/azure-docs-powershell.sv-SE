---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 23C6C9D3-A745-46C8-AB2C-B874223FBFFF
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/get-azmediaservicenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceNameAvailability.md
ms.openlocfilehash: d7718ffafd6383e0873e61955cd231ca8b6a409d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261228"
---
# <span data-ttu-id="55911-101">Get-AzMediaServiceNameAvailability</span><span class="sxs-lookup"><span data-stu-id="55911-101">Get-AzMediaServiceNameAvailability</span></span>

## <span data-ttu-id="55911-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="55911-102">SYNOPSIS</span></span>
<span data-ttu-id="55911-103">Kontrollerar om medie tjänstens namn är tillgängligt.</span><span class="sxs-lookup"><span data-stu-id="55911-103">Checks whether a media service name is available.</span></span>
<span data-ttu-id="55911-104">Medie tjänstens namn är globalt unika.</span><span class="sxs-lookup"><span data-stu-id="55911-104">Media service names are globally unique.</span></span>

## <span data-ttu-id="55911-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="55911-105">SYNTAX</span></span>

```
Get-AzMediaServiceNameAvailability [-DefaultProfile <IAzureContextContainer>] [-AccountName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="55911-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="55911-106">DESCRIPTION</span></span>
<span data-ttu-id="55911-107">Cmdleten **Get-AzMediaServiceNameAvailability** kontrollerar om medie tjänstens namn är tillgängligt.</span><span class="sxs-lookup"><span data-stu-id="55911-107">The **Get-AzMediaServiceNameAvailability** cmdlet checks whether a media service name is available.</span></span>
<span data-ttu-id="55911-108">Medie tjänstens namn är globalt unika.</span><span class="sxs-lookup"><span data-stu-id="55911-108">Media service names are globally unique.</span></span>

## <span data-ttu-id="55911-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="55911-109">EXAMPLES</span></span>

### <span data-ttu-id="55911-110">Exempel 1: kontrol lera om medie tjänstens namn är tillgängligt</span><span class="sxs-lookup"><span data-stu-id="55911-110">Example 1: Check whether a Media Service name is available</span></span>
```
PS C:\>Get-AzMediaServiceNameAvailability -AccountName "MediaService1"
```

<span data-ttu-id="55911-111">Det här kommandot kontrollerar om namnet MediaService1 är tillgängligt.</span><span class="sxs-lookup"><span data-stu-id="55911-111">This command checks if the name MediaService1 is available.</span></span>

## <span data-ttu-id="55911-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="55911-112">PARAMETERS</span></span>

### <span data-ttu-id="55911-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="55911-113">-AccountName</span></span>
<span data-ttu-id="55911-114">Anger namnet på den medie tjänst som cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="55911-114">Specifies the name of the media service that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55911-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55911-115">-DefaultProfile</span></span>
<span data-ttu-id="55911-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="55911-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="55911-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55911-117">CommonParameters</span></span>
<span data-ttu-id="55911-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55911-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55911-119">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55911-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55911-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="55911-120">INPUTS</span></span>

### <span data-ttu-id="55911-121">Ingen</span><span class="sxs-lookup"><span data-stu-id="55911-121">None</span></span>

## <span data-ttu-id="55911-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="55911-122">OUTPUTS</span></span>

### <span data-ttu-id="55911-123">Microsoft. Azure. commands. Media. Models. PSCheckNameAvailabilityOutput</span><span class="sxs-lookup"><span data-stu-id="55911-123">Microsoft.Azure.Commands.Media.Models.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="55911-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="55911-124">NOTES</span></span>

## <span data-ttu-id="55911-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="55911-125">RELATED LINKS</span></span>

[<span data-ttu-id="55911-126">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="55911-126">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="55911-127">New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="55911-127">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="55911-128">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="55911-128">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)

[<span data-ttu-id="55911-129">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="55911-129">Set-AzMediaService</span></span>](./Set-AzMediaService.md)



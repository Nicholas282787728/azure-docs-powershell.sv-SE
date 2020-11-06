---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 23C6C9D3-A745-46C8-AB2C-B874223FBFFF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.media/get-azurermmediaservicenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaServiceNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaServiceNameAvailability.md
ms.openlocfilehash: 8de8b9f389f8d57d844c17d92dd492390fbf1884
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574823"
---
# <span data-ttu-id="56d39-101">Get-AzureRmMediaServiceNameAvailability</span><span class="sxs-lookup"><span data-stu-id="56d39-101">Get-AzureRmMediaServiceNameAvailability</span></span>

## <span data-ttu-id="56d39-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="56d39-102">SYNOPSIS</span></span>
<span data-ttu-id="56d39-103">Kontrollerar om medie tjänstens namn är tillgängligt.</span><span class="sxs-lookup"><span data-stu-id="56d39-103">Checks whether a media service name is available.</span></span>
<span data-ttu-id="56d39-104">Medie tjänstens namn är globalt unika.</span><span class="sxs-lookup"><span data-stu-id="56d39-104">Media service names are globally unique.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56d39-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="56d39-105">SYNTAX</span></span>

```
Get-AzureRmMediaServiceNameAvailability [-DefaultProfile <IAzureContextContainer>] [-AccountName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="56d39-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="56d39-106">DESCRIPTION</span></span>
<span data-ttu-id="56d39-107">Cmdleten **Get-AzureRmMediaServiceNameAvailability** kontrollerar om medie tjänstens namn är tillgängligt.</span><span class="sxs-lookup"><span data-stu-id="56d39-107">The **Get-AzureRmMediaServiceNameAvailability** cmdlet checks whether a media service name is available.</span></span>
<span data-ttu-id="56d39-108">Medie tjänstens namn är globalt unika.</span><span class="sxs-lookup"><span data-stu-id="56d39-108">Media service names are globally unique.</span></span>

## <span data-ttu-id="56d39-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="56d39-109">EXAMPLES</span></span>

### <span data-ttu-id="56d39-110">Exempel 1: kontrol lera om medie tjänstens namn är tillgängligt</span><span class="sxs-lookup"><span data-stu-id="56d39-110">Example 1: Check whether a Media Service name is available</span></span>
```
PS C:\>Get-AzureRmMediaServiceNameAvailability -AccountName "MediaService1"
```

<span data-ttu-id="56d39-111">Det här kommandot kontrollerar om namnet MediaService1 är tillgängligt.</span><span class="sxs-lookup"><span data-stu-id="56d39-111">This command checks if the name MediaService1 is available.</span></span>

## <span data-ttu-id="56d39-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="56d39-112">PARAMETERS</span></span>

### <span data-ttu-id="56d39-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="56d39-113">-AccountName</span></span>
<span data-ttu-id="56d39-114">Anger namnet på den medie tjänst som cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="56d39-114">Specifies the name of the media service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="56d39-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56d39-115">-DefaultProfile</span></span>
<span data-ttu-id="56d39-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="56d39-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="56d39-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56d39-117">CommonParameters</span></span>
<span data-ttu-id="56d39-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56d39-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56d39-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56d39-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56d39-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="56d39-120">INPUTS</span></span>

### <span data-ttu-id="56d39-121">Ingen</span><span class="sxs-lookup"><span data-stu-id="56d39-121">None</span></span>

## <span data-ttu-id="56d39-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="56d39-122">OUTPUTS</span></span>

### <span data-ttu-id="56d39-123">Microsoft. Azure. commands. Media. Models. PSCheckNameAvailabilityOutput</span><span class="sxs-lookup"><span data-stu-id="56d39-123">Microsoft.Azure.Commands.Media.Models.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="56d39-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="56d39-124">NOTES</span></span>

## <span data-ttu-id="56d39-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="56d39-125">RELATED LINKS</span></span>

[<span data-ttu-id="56d39-126">Get-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="56d39-126">Get-AzureRmMediaService</span></span>](./Get-AzureRmMediaService.md)

[<span data-ttu-id="56d39-127">New-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="56d39-127">New-AzureRmMediaService</span></span>](./New-AzureRmMediaService.md)

[<span data-ttu-id="56d39-128">Remove-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="56d39-128">Remove-AzureRmMediaService</span></span>](./Remove-AzureRmMediaService.md)

[<span data-ttu-id="56d39-129">Set-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="56d39-129">Set-AzureRmMediaService</span></span>](./Set-AzureRmMediaService.md)



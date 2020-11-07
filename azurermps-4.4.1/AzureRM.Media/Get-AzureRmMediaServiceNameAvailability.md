---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 23C6C9D3-A745-46C8-AB2C-B874223FBFFF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaServiceNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaServiceNameAvailability.md
ms.openlocfilehash: be459183e47982fef8dbd2376ddd5110251bb001
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756931"
---
# <span data-ttu-id="1116d-101">Get-AzureRmMediaServiceNameAvailability</span><span class="sxs-lookup"><span data-stu-id="1116d-101">Get-AzureRmMediaServiceNameAvailability</span></span>

## <span data-ttu-id="1116d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1116d-102">SYNOPSIS</span></span>
<span data-ttu-id="1116d-103">Kontrollerar om medie tjänstens namn är tillgängligt.</span><span class="sxs-lookup"><span data-stu-id="1116d-103">Checks whether a media service name is available.</span></span>
<span data-ttu-id="1116d-104">Medie tjänstens namn är globalt unika.</span><span class="sxs-lookup"><span data-stu-id="1116d-104">Media service names are globally unique.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1116d-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1116d-105">SYNTAX</span></span>

```
Get-AzureRmMediaServiceNameAvailability [-DefaultProfile <IAzureContextContainer>] [-AccountName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="1116d-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1116d-106">DESCRIPTION</span></span>
<span data-ttu-id="1116d-107">Cmdleten **Get-AzureRmMediaServiceNameAvailability** kontrollerar om medie tjänstens namn är tillgängligt.</span><span class="sxs-lookup"><span data-stu-id="1116d-107">The **Get-AzureRmMediaServiceNameAvailability** cmdlet checks whether a media service name is available.</span></span>
<span data-ttu-id="1116d-108">Medie tjänstens namn är globalt unika.</span><span class="sxs-lookup"><span data-stu-id="1116d-108">Media service names are globally unique.</span></span>

## <span data-ttu-id="1116d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1116d-109">EXAMPLES</span></span>

### <span data-ttu-id="1116d-110">Exempel 1: kontrol lera om medie tjänstens namn är tillgängligt</span><span class="sxs-lookup"><span data-stu-id="1116d-110">Example 1: Check whether a Media Service name is available</span></span>
```
PS C:\>Get-AzureRmMediaServiceNameAvailability -AccountName "MediaService1"
```

<span data-ttu-id="1116d-111">Det här kommandot kontrollerar om namnet MediaService1 är tillgängligt.</span><span class="sxs-lookup"><span data-stu-id="1116d-111">This command checks if the name MediaService1 is available.</span></span>

## <span data-ttu-id="1116d-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1116d-112">PARAMETERS</span></span>

### <span data-ttu-id="1116d-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1116d-113">-AccountName</span></span>
<span data-ttu-id="1116d-114">Anger namnet på den medie tjänst som cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="1116d-114">Specifies the name of the media service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="1116d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1116d-115">-DefaultProfile</span></span>
<span data-ttu-id="1116d-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1116d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1116d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1116d-117">CommonParameters</span></span>
<span data-ttu-id="1116d-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1116d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1116d-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1116d-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1116d-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1116d-120">INPUTS</span></span>

## <span data-ttu-id="1116d-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1116d-121">OUTPUTS</span></span>

### <span data-ttu-id="1116d-122">Microsoft. Azure. commands. Media. Models. PSCheckNameAvailabilityOutput</span><span class="sxs-lookup"><span data-stu-id="1116d-122">Microsoft.Azure.Commands.Media.Models.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="1116d-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1116d-123">NOTES</span></span>

## <span data-ttu-id="1116d-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1116d-124">RELATED LINKS</span></span>

[<span data-ttu-id="1116d-125">Get-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="1116d-125">Get-AzureRmMediaService</span></span>](./Get-AzureRmMediaService.md)

[<span data-ttu-id="1116d-126">New-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="1116d-126">New-AzureRmMediaService</span></span>](./New-AzureRmMediaService.md)

[<span data-ttu-id="1116d-127">Remove-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="1116d-127">Remove-AzureRmMediaService</span></span>](./Remove-AzureRmMediaService.md)

[<span data-ttu-id="1116d-128">Set-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="1116d-128">Set-AzureRmMediaService</span></span>](./Set-AzureRmMediaService.md)



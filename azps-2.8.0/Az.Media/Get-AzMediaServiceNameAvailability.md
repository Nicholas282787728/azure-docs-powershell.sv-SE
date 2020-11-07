---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 23C6C9D3-A745-46C8-AB2C-B874223FBFFF
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/get-azmediaservicenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceNameAvailability.md
ms.openlocfilehash: 8c62bf114feee8f9b87e2b7ca35b4c67b423ed66
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93743630"
---
# <span data-ttu-id="c3d1e-101">Get-AzMediaServiceNameAvailability</span><span class="sxs-lookup"><span data-stu-id="c3d1e-101">Get-AzMediaServiceNameAvailability</span></span>

## <span data-ttu-id="c3d1e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c3d1e-102">SYNOPSIS</span></span>
<span data-ttu-id="c3d1e-103">Kontrollerar om medie tjänstens namn är tillgängligt.</span><span class="sxs-lookup"><span data-stu-id="c3d1e-103">Checks whether a media service name is available.</span></span>
<span data-ttu-id="c3d1e-104">Medie tjänstens namn är globalt unika.</span><span class="sxs-lookup"><span data-stu-id="c3d1e-104">Media service names are globally unique.</span></span>

## <span data-ttu-id="c3d1e-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c3d1e-105">SYNTAX</span></span>

```
Get-AzMediaServiceNameAvailability [-DefaultProfile <IAzureContextContainer>] [-AccountName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="c3d1e-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c3d1e-106">DESCRIPTION</span></span>
<span data-ttu-id="c3d1e-107">Cmdleten **Get-AzMediaServiceNameAvailability** kontrollerar om medie tjänstens namn är tillgängligt.</span><span class="sxs-lookup"><span data-stu-id="c3d1e-107">The **Get-AzMediaServiceNameAvailability** cmdlet checks whether a media service name is available.</span></span>
<span data-ttu-id="c3d1e-108">Medie tjänstens namn är globalt unika.</span><span class="sxs-lookup"><span data-stu-id="c3d1e-108">Media service names are globally unique.</span></span>

## <span data-ttu-id="c3d1e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c3d1e-109">EXAMPLES</span></span>

### <span data-ttu-id="c3d1e-110">Exempel 1: kontrol lera om medie tjänstens namn är tillgängligt</span><span class="sxs-lookup"><span data-stu-id="c3d1e-110">Example 1: Check whether a Media Service name is available</span></span>
```
PS C:\>Get-AzMediaServiceNameAvailability -AccountName "MediaService1"
```

<span data-ttu-id="c3d1e-111">Det här kommandot kontrollerar om namnet MediaService1 är tillgängligt.</span><span class="sxs-lookup"><span data-stu-id="c3d1e-111">This command checks if the name MediaService1 is available.</span></span>

## <span data-ttu-id="c3d1e-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c3d1e-112">PARAMETERS</span></span>

### <span data-ttu-id="c3d1e-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c3d1e-113">-AccountName</span></span>
<span data-ttu-id="c3d1e-114">Anger namnet på den medie tjänst som cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="c3d1e-114">Specifies the name of the media service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="c3d1e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3d1e-115">-DefaultProfile</span></span>
<span data-ttu-id="c3d1e-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="c3d1e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c3d1e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3d1e-117">CommonParameters</span></span>
<span data-ttu-id="c3d1e-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3d1e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3d1e-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3d1e-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3d1e-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c3d1e-120">INPUTS</span></span>

### <span data-ttu-id="c3d1e-121">Ingen</span><span class="sxs-lookup"><span data-stu-id="c3d1e-121">None</span></span>

## <span data-ttu-id="c3d1e-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c3d1e-122">OUTPUTS</span></span>

### <span data-ttu-id="c3d1e-123">Microsoft. Azure. commands. Media. Models. PSCheckNameAvailabilityOutput</span><span class="sxs-lookup"><span data-stu-id="c3d1e-123">Microsoft.Azure.Commands.Media.Models.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="c3d1e-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c3d1e-124">NOTES</span></span>

## <span data-ttu-id="c3d1e-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c3d1e-125">RELATED LINKS</span></span>

[<span data-ttu-id="c3d1e-126">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="c3d1e-126">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="c3d1e-127">New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="c3d1e-127">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="c3d1e-128">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="c3d1e-128">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)

[<span data-ttu-id="c3d1e-129">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="c3d1e-129">Set-AzMediaService</span></span>](./Set-AzMediaService.md)



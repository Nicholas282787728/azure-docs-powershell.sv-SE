---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: D0336AB5-019F-4EFD-88D2-63E12BA1ED95
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoverySite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoverySite.md
ms.openlocfilehash: 7f8dfed861abd9d426a72c5d66f7c41b4efc947e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574512"
---
# <span data-ttu-id="6de30-101">New-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="6de30-101">New-AzureRmSiteRecoverySite</span></span>

## <span data-ttu-id="6de30-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6de30-102">SYNOPSIS</span></span>
<span data-ttu-id="6de30-103">Skapar en webbplats återställnings webbplats.</span><span class="sxs-lookup"><span data-stu-id="6de30-103">Creates a Site Recovery site.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6de30-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6de30-104">SYNTAX</span></span>

```
New-AzureRmSiteRecoverySite -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6de30-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6de30-105">DESCRIPTION</span></span>
<span data-ttu-id="6de30-106">Cmdleten **New-AzureRmSiteRecoverySite** skapar en Azure Site Recovery-webbplats i det aktuella valvet.</span><span class="sxs-lookup"><span data-stu-id="6de30-106">The **New-AzureRmSiteRecoverySite** cmdlet creates an Azure Site Recovery site in the current vault.</span></span>

## <span data-ttu-id="6de30-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6de30-107">EXAMPLES</span></span>

## <span data-ttu-id="6de30-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6de30-108">PARAMETERS</span></span>

### <span data-ttu-id="6de30-109">-Namn</span><span class="sxs-lookup"><span data-stu-id="6de30-109">-Name</span></span>
<span data-ttu-id="6de30-110">Anger namnet på webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="6de30-110">Specifies the name of the site.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6de30-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6de30-111">-DefaultProfile</span></span>
<span data-ttu-id="6de30-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6de30-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6de30-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6de30-113">CommonParameters</span></span>
<span data-ttu-id="6de30-114">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6de30-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6de30-115">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6de30-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6de30-116">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6de30-116">INPUTS</span></span>

## <span data-ttu-id="6de30-117">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6de30-117">OUTPUTS</span></span>

## <span data-ttu-id="6de30-118">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6de30-118">NOTES</span></span>

## <span data-ttu-id="6de30-119">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6de30-119">RELATED LINKS</span></span>

[<span data-ttu-id="6de30-120">Get-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="6de30-120">Get-AzureRmSiteRecoverySite</span></span>](./Get-AzureRmSiteRecoverySite.md)

[<span data-ttu-id="6de30-121">Remove-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="6de30-121">Remove-AzureRmSiteRecoverySite</span></span>](./Remove-AzureRmSiteRecoverySite.md)

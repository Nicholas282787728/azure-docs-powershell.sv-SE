---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: D0336AB5-019F-4EFD-88D2-63E12BA1ED95
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/new-azurermsiterecoverysite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoverySite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoverySite.md
ms.openlocfilehash: 053cd7695768be44cf3cecc5964e037f12f0b84e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579363"
---
# <span data-ttu-id="871de-101">New-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="871de-101">New-AzureRmSiteRecoverySite</span></span>

## <span data-ttu-id="871de-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="871de-102">SYNOPSIS</span></span>
<span data-ttu-id="871de-103">Skapar en webbplats återställnings webbplats.</span><span class="sxs-lookup"><span data-stu-id="871de-103">Creates a Site Recovery site.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="871de-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="871de-104">SYNTAX</span></span>

```
New-AzureRmSiteRecoverySite -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="871de-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="871de-105">DESCRIPTION</span></span>
<span data-ttu-id="871de-106">Cmdleten **New-AzureRmSiteRecoverySite** skapar en Azure Site Recovery-webbplats i det aktuella valvet.</span><span class="sxs-lookup"><span data-stu-id="871de-106">The **New-AzureRmSiteRecoverySite** cmdlet creates an Azure Site Recovery site in the current vault.</span></span>

## <span data-ttu-id="871de-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="871de-107">EXAMPLES</span></span>

## <span data-ttu-id="871de-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="871de-108">PARAMETERS</span></span>

### <span data-ttu-id="871de-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="871de-109">-DefaultProfile</span></span>
<span data-ttu-id="871de-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="871de-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="871de-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="871de-111">-Name</span></span>
<span data-ttu-id="871de-112">Anger namnet på webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="871de-112">Specifies the name of the site.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="871de-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="871de-113">CommonParameters</span></span>
<span data-ttu-id="871de-114">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="871de-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="871de-115">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="871de-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="871de-116">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="871de-116">INPUTS</span></span>

### <span data-ttu-id="871de-117">Ingen</span><span class="sxs-lookup"><span data-stu-id="871de-117">None</span></span>
<span data-ttu-id="871de-118">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="871de-118">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="871de-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="871de-119">OUTPUTS</span></span>

## <span data-ttu-id="871de-120">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="871de-120">NOTES</span></span>

## <span data-ttu-id="871de-121">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="871de-121">RELATED LINKS</span></span>

[<span data-ttu-id="871de-122">Get-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="871de-122">Get-AzureRmSiteRecoverySite</span></span>](./Get-AzureRmSiteRecoverySite.md)

[<span data-ttu-id="871de-123">Remove-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="871de-123">Remove-AzureRmSiteRecoverySite</span></span>](./Remove-AzureRmSiteRecoverySite.md)

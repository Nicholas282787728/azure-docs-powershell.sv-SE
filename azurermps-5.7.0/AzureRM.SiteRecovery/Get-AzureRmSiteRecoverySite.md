---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: F9A652D0-26D9-4F3F-A365-285B05AA7C0B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoverysite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoverySite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoverySite.md
ms.openlocfilehash: 4a710507321d2f4eb2a605846928f66c5bdb6a4a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757206"
---
# <span data-ttu-id="0f779-101">Get-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="0f779-101">Get-AzureRmSiteRecoverySite</span></span>

## <span data-ttu-id="0f779-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0f779-102">SYNOPSIS</span></span>
<span data-ttu-id="0f779-103">Hämtar Hyper-V-webbplatserna från Site Recovery-valvet.</span><span class="sxs-lookup"><span data-stu-id="0f779-103">Gets the Hyper-V sites from the Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f779-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0f779-104">SYNTAX</span></span>

### <span data-ttu-id="0f779-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="0f779-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoverySite [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0f779-106">ByName</span><span class="sxs-lookup"><span data-stu-id="0f779-106">ByName</span></span>
```
Get-AzureRmSiteRecoverySite -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0f779-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="0f779-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoverySite -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0f779-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0f779-108">DESCRIPTION</span></span>
<span data-ttu-id="0f779-109">Cmdleten **Get-AzureRmSiteRecoverySite** hämtar Hyper-V-webbplatserna i Azure Site Recovery-valvet.</span><span class="sxs-lookup"><span data-stu-id="0f779-109">The **Get-AzureRmSiteRecoverySite** cmdlet gets the Hyper-V sites in the Azure Site Recovery vault.</span></span>

## <span data-ttu-id="0f779-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0f779-110">EXAMPLES</span></span>

## <span data-ttu-id="0f779-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0f779-111">PARAMETERS</span></span>

### <span data-ttu-id="0f779-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f779-112">-DefaultProfile</span></span>
<span data-ttu-id="0f779-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0f779-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f779-114">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="0f779-114">-FriendlyName</span></span>
<span data-ttu-id="0f779-115">Anger webbplatsens egna namn.</span><span class="sxs-lookup"><span data-stu-id="0f779-115">Specifies the friendly name of the site.</span></span>

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f779-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="0f779-116">-Name</span></span>
<span data-ttu-id="0f779-117">Anger namnet på webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="0f779-117">Specifies the name of the site.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f779-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f779-118">CommonParameters</span></span>
<span data-ttu-id="0f779-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f779-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f779-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f779-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f779-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0f779-121">INPUTS</span></span>

### <span data-ttu-id="0f779-122">Ingen</span><span class="sxs-lookup"><span data-stu-id="0f779-122">None</span></span>
<span data-ttu-id="0f779-123">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="0f779-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0f779-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0f779-124">OUTPUTS</span></span>

### <span data-ttu-id="0f779-125">System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. SiteRecovery. ASRSite]</span><span class="sxs-lookup"><span data-stu-id="0f779-125">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.SiteRecovery.ASRSite]</span></span>

## <span data-ttu-id="0f779-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0f779-126">NOTES</span></span>

## <span data-ttu-id="0f779-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0f779-127">RELATED LINKS</span></span>

[<span data-ttu-id="0f779-128">New-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="0f779-128">New-AzureRmSiteRecoverySite</span></span>](./New-AzureRmSiteRecoverySite.md)

[<span data-ttu-id="0f779-129">Remove-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="0f779-129">Remove-AzureRmSiteRecoverySite</span></span>](./Remove-AzureRmSiteRecoverySite.md)

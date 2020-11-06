---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: F9A652D0-26D9-4F3F-A365-285B05AA7C0B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoverySite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoverySite.md
ms.openlocfilehash: e41b491611ebc5dda1da56ac26827c5fa547dd4a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575808"
---
# <span data-ttu-id="05efd-101">Get-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="05efd-101">Get-AzureRmSiteRecoverySite</span></span>

## <span data-ttu-id="05efd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="05efd-102">SYNOPSIS</span></span>
<span data-ttu-id="05efd-103">Hämtar Hyper-V-webbplatserna från Site Recovery-valvet.</span><span class="sxs-lookup"><span data-stu-id="05efd-103">Gets the Hyper-V sites from the Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05efd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="05efd-104">SYNTAX</span></span>

### <span data-ttu-id="05efd-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="05efd-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoverySite [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="05efd-106">ByName</span><span class="sxs-lookup"><span data-stu-id="05efd-106">ByName</span></span>
```
Get-AzureRmSiteRecoverySite -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="05efd-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="05efd-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoverySite -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="05efd-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="05efd-108">DESCRIPTION</span></span>
<span data-ttu-id="05efd-109">Cmdleten **Get-AzureRmSiteRecoverySite** hämtar Hyper-V-webbplatserna i Azure Site Recovery-valvet.</span><span class="sxs-lookup"><span data-stu-id="05efd-109">The **Get-AzureRmSiteRecoverySite** cmdlet gets the Hyper-V sites in the Azure Site Recovery vault.</span></span>

## <span data-ttu-id="05efd-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="05efd-110">EXAMPLES</span></span>

## <span data-ttu-id="05efd-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="05efd-111">PARAMETERS</span></span>

### <span data-ttu-id="05efd-112">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="05efd-112">-FriendlyName</span></span>
<span data-ttu-id="05efd-113">Anger webbplatsens egna namn.</span><span class="sxs-lookup"><span data-stu-id="05efd-113">Specifies the friendly name of the site.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05efd-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="05efd-114">-Name</span></span>
<span data-ttu-id="05efd-115">Anger namnet på webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="05efd-115">Specifies the name of the site.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05efd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05efd-116">-DefaultProfile</span></span>
<span data-ttu-id="05efd-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="05efd-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="05efd-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05efd-118">CommonParameters</span></span>
<span data-ttu-id="05efd-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05efd-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05efd-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05efd-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05efd-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="05efd-121">INPUTS</span></span>

## <span data-ttu-id="05efd-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="05efd-122">OUTPUTS</span></span>

### <span data-ttu-id="05efd-123">System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. SiteRecovery. ASRSite]</span><span class="sxs-lookup"><span data-stu-id="05efd-123">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.SiteRecovery.ASRSite]</span></span>

## <span data-ttu-id="05efd-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="05efd-124">NOTES</span></span>

## <span data-ttu-id="05efd-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="05efd-125">RELATED LINKS</span></span>

[<span data-ttu-id="05efd-126">New-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="05efd-126">New-AzureRmSiteRecoverySite</span></span>](./New-AzureRmSiteRecoverySite.md)

[<span data-ttu-id="05efd-127">Remove-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="05efd-127">Remove-AzureRmSiteRecoverySite</span></span>](./Remove-AzureRmSiteRecoverySite.md)

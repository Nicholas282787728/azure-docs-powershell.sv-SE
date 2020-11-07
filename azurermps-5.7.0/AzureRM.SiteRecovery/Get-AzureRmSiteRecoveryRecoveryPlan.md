---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 3B879056-5BF3-4262-8BAA-E79589149370
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryRecoveryPlan.md
ms.openlocfilehash: ae5a1d5a70064b3849bc8f38cab46ecfabaf4968
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757211"
---
# <span data-ttu-id="5cb62-101">Get-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="5cb62-101">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="5cb62-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5cb62-102">SYNOPSIS</span></span>
<span data-ttu-id="5cb62-103">Hämtar en återställnings plan i webbplats återställning.</span><span class="sxs-lookup"><span data-stu-id="5cb62-103">Gets a recovery plan in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5cb62-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5cb62-104">SYNTAX</span></span>

### <span data-ttu-id="5cb62-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="5cb62-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryRecoveryPlan [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5cb62-106">ByName</span><span class="sxs-lookup"><span data-stu-id="5cb62-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryRecoveryPlan -Name <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5cb62-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="5cb62-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryRecoveryPlan -FriendlyName <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5cb62-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5cb62-108">DESCRIPTION</span></span>
<span data-ttu-id="5cb62-109">Cmdleten **Get-AzureRmSiteRecoveryRecoveryPlan** hämtar en återställnings plan i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="5cb62-109">The **Get-AzureRmSiteRecoveryRecoveryPlan** cmdlet gets a recovery plan in Azure Site Recovery.</span></span>

## <span data-ttu-id="5cb62-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5cb62-110">EXAMPLES</span></span>

## <span data-ttu-id="5cb62-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5cb62-111">PARAMETERS</span></span>

### <span data-ttu-id="5cb62-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cb62-112">-DefaultProfile</span></span>
<span data-ttu-id="5cb62-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5cb62-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5cb62-114">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="5cb62-114">-FriendlyName</span></span>
<span data-ttu-id="5cb62-115">Anger det egna namnet på återställnings planen som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="5cb62-115">Specifies the friendly name of the recovery plan that this cmdlet gets.</span></span>

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

### <span data-ttu-id="5cb62-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="5cb62-116">-Name</span></span>
<span data-ttu-id="5cb62-117">Anger namnet på den återställnings plan som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="5cb62-117">Specifies the name of the recovery plan that this cmdlet gets.</span></span>

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

### <span data-ttu-id="5cb62-118">-Path</span><span class="sxs-lookup"><span data-stu-id="5cb62-118">-Path</span></span>
<span data-ttu-id="5cb62-119">Anger sökvägen till den plats där denna cmdlet sparar återställnings planen.</span><span class="sxs-lookup"><span data-stu-id="5cb62-119">Specifies the file path to which this cmdlet saves the recovery plan.</span></span>

```yaml
Type: String
Parameter Sets: ByName, ByFriendlyName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cb62-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cb62-120">CommonParameters</span></span>
<span data-ttu-id="5cb62-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cb62-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cb62-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cb62-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cb62-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5cb62-123">INPUTS</span></span>

### <span data-ttu-id="5cb62-124">Ingen</span><span class="sxs-lookup"><span data-stu-id="5cb62-124">None</span></span>
<span data-ttu-id="5cb62-125">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="5cb62-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5cb62-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5cb62-126">OUTPUTS</span></span>

### <span data-ttu-id="5cb62-127">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. commands. SiteRecovery. ASRRecoveryPlan]</span><span class="sxs-lookup"><span data-stu-id="5cb62-127">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlan]</span></span>

## <span data-ttu-id="5cb62-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5cb62-128">NOTES</span></span>

## <span data-ttu-id="5cb62-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5cb62-129">RELATED LINKS</span></span>

[<span data-ttu-id="5cb62-130">New-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="5cb62-130">New-AzureRmSiteRecoveryRecoveryPlan</span></span>](./New-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="5cb62-131">Remove-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="5cb62-131">Remove-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="5cb62-132">Update-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="5cb62-132">Update-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Update-AzureRmSiteRecoveryRecoveryPlan.md)

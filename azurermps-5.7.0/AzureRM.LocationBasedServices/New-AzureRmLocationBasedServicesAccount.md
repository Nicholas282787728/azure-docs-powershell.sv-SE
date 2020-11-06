---
external help file: Microsoft.Azure.Commands.LocationBasedServices.dll-Help.xml
Module Name: AzureRM.LocationBasedServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.locationbasedservices/new-azurermlocationbasedservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/New-AzureRmLocationBasedServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/New-AzureRmLocationBasedServicesAccount.md
ms.openlocfilehash: 739ce121e26f1010c5c13ff3330dadffa02053af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574941"
---
# <span data-ttu-id="bf116-101">New-AzureRmLocationBasedServicesAccount</span><span class="sxs-lookup"><span data-stu-id="bf116-101">New-AzureRmLocationBasedServicesAccount</span></span>

## <span data-ttu-id="bf116-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bf116-102">SYNOPSIS</span></span>
<span data-ttu-id="bf116-103">Skapar ett konto för platsbaserade tjänster.</span><span class="sxs-lookup"><span data-stu-id="bf116-103">Creates a Location Based Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf116-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bf116-104">SYNTAX</span></span>

```
New-AzureRmLocationBasedServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String>
 [-Tag <Hashtable[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bf116-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bf116-105">DESCRIPTION</span></span>
<span data-ttu-id="bf116-106">Cmdleten **New-AzureRmLocationBasedServicesAccount** skapar ett konto för platsbaserade tjänster med angiven SKU.</span><span class="sxs-lookup"><span data-stu-id="bf116-106">The **New-AzureRmLocationBasedServicesAccount** cmdlet creates a Location Based Services account with the specified SKU.</span></span>

## <span data-ttu-id="bf116-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bf116-107">EXAMPLES</span></span>

### <span data-ttu-id="bf116-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="bf116-108">Example 1</span></span>
```
PS C:\> New-AzureRmLocationBasedServicesAccount -ResourceGroupName MyResourceGroup -Name MyAccount -SkuName S0 -Tags @{Name="test";Value="true"}

Notice
By creating a Location Based Account, you are consenting to the terms of use (see https://azure.microsoft.com/en-us/support/legal/preview-supplemental-terms/).
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"): y

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount
```

<span data-ttu-id="bf116-109">Skapar ett nytt platsbaserade tjänst konto med namnet mitt konto i resurs gruppen MyResourceGroup med SKU-S0 och en-etikett.</span><span class="sxs-lookup"><span data-stu-id="bf116-109">Creates a new Location Based Services account named MyAccount in the resource group MyResourceGroup with the SKU S0 and a tag.</span></span>

## <span data-ttu-id="bf116-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bf116-110">PARAMETERS</span></span>

### <span data-ttu-id="bf116-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf116-111">-DefaultProfile</span></span>
<span data-ttu-id="bf116-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bf116-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bf116-113">-Force</span><span class="sxs-lookup"><span data-stu-id="bf116-113">-Force</span></span>
<span data-ttu-id="bf116-114">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="bf116-114">Don't ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf116-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="bf116-115">-Name</span></span>
<span data-ttu-id="bf116-116">Konto namn för platsbaserade tjänster.</span><span class="sxs-lookup"><span data-stu-id="bf116-116">Location Based Services Account Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: LocationBasedServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf116-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf116-117">-ResourceGroupName</span></span>
<span data-ttu-id="bf116-118">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="bf116-118">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf116-119">-SkuName</span><span class="sxs-lookup"><span data-stu-id="bf116-119">-SkuName</span></span>
<span data-ttu-id="bf116-120">SKU-namn på platsbaserade tjänster.</span><span class="sxs-lookup"><span data-stu-id="bf116-120">Location Based Services Account Sku Name.</span></span>

<span data-ttu-id="bf116-121">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="bf116-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="bf116-122">S0</span><span class="sxs-lookup"><span data-stu-id="bf116-122">S0</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: S0

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf116-123">-Tagg</span><span class="sxs-lookup"><span data-stu-id="bf116-123">-Tag</span></span>
<span data-ttu-id="bf116-124">Taggar för platsbaserade tjänster.</span><span class="sxs-lookup"><span data-stu-id="bf116-124">Location Based Services Account Tags.</span></span>

```yaml
Type: Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf116-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bf116-125">-Confirm</span></span>
<span data-ttu-id="bf116-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bf116-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf116-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf116-127">-WhatIf</span></span>
<span data-ttu-id="bf116-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bf116-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf116-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bf116-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf116-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf116-130">CommonParameters</span></span>
<span data-ttu-id="bf116-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf116-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf116-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf116-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf116-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bf116-133">INPUTS</span></span>

### <span data-ttu-id="bf116-134">System. String</span><span class="sxs-lookup"><span data-stu-id="bf116-134">System.String</span></span>

## <span data-ttu-id="bf116-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bf116-135">OUTPUTS</span></span>

### <span data-ttu-id="bf116-136">Microsoft. Azure. commands. LocationBasedServices. Models. PSLocationBasedServicesAccount</span><span class="sxs-lookup"><span data-stu-id="bf116-136">Microsoft.Azure.Commands.LocationBasedServices.Models.PSLocationBasedServicesAccount</span></span>

## <span data-ttu-id="bf116-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bf116-137">NOTES</span></span>

<span data-ttu-id="bf116-138">Om du skapar ett konto för platsbaserade tjänster måste du besvara en uppmaning om att acceptera villkoren (mer information finns i https://azure.microsoft.com/en-us/support/legal/preview-supplemental-terms/) .</span><span class="sxs-lookup"><span data-stu-id="bf116-138">Creating a Location Based Services account requires answering a prompt to accept terms (see https://azure.microsoft.com/en-us/support/legal/preview-supplemental-terms/).</span></span>  <span data-ttu-id="bf116-139">Parametern-Force kan användas för att ange godkännande av villkoren.</span><span class="sxs-lookup"><span data-stu-id="bf116-139">The -Force parameter can be used to indicate acceptance of the terms.</span></span>

## <span data-ttu-id="bf116-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bf116-140">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatasharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSubscription.md
ms.openlocfilehash: 64309b77801646e61e3a144bc4a7405e4e978aa6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744429"
---
# <span data-ttu-id="e8236-101">New-AzDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="e8236-101">New-AzDataShareSubscription</span></span>

## <span data-ttu-id="e8236-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e8236-102">SYNOPSIS</span></span>
<span data-ttu-id="e8236-103">Skapar en ny resurs prenumeration.</span><span class="sxs-lookup"><span data-stu-id="e8236-103">Creates a new share subscription.</span></span>

## <span data-ttu-id="e8236-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e8236-104">SYNTAX</span></span>

```
New-AzDataShareSubscription -ResourceGroupName <String> -AccountName <String> -Name <String>
 -InvitationId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8236-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e8236-105">DESCRIPTION</span></span>
<span data-ttu-id="e8236-106">Cmdleten **New-AzDataShareSubscription** skapar en resurs prenumeration i angivet data resurs konto och inbjudan-ID.</span><span class="sxs-lookup"><span data-stu-id="e8236-106">The **New-AzDataShareSubscription** cmdlet creates a share subscription in specified data share account and invitation id.</span></span>

## <span data-ttu-id="e8236-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e8236-107">EXAMPLES</span></span>

### <span data-ttu-id="e8236-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e8236-108">Example 1</span></span>
```
PS C:\> New-AzDataShareSubscription -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShareSubscription" -InvitationId "167e06ff-567f-4bc7-be0c-645a6de710f3"
CreatedAt               : 6/30/2019 12:42:12 AM
CreatedBy               : adstest@microsoft.com
InvitationId            : 167e06ff-567f-4bc7-be0c-645a6de710f3
ProvisioningState       : Succeeded
ShareName               : AdsShare
ShareSender             : adsprovider@microsoft.com
ShareSenderCompanyName  : ADS Company
ShareDescription        : Test description  
ShareTerms              : Test terms of use
ShareSubscriptionStatus : Active
ShareKind               : CopyBased
Id                      : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shareSubscriptions/AdsShareSubscription
Name                    : AdsShareSubscription
Type                    : Microsoft.DataShare/ShareSubscriptions
```

<span data-ttu-id="e8236-109">Med de här kommandona skapas en ny AdsShareSubscription för Share-abonnemang för invitaionId under data Share Account WikiAds.</span><span class="sxs-lookup"><span data-stu-id="e8236-109">This commands creates a new share subscription AdsShareSubscription for invitaionId under data share account WikiAds.</span></span>

## <span data-ttu-id="e8236-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e8236-110">PARAMETERS</span></span>

### <span data-ttu-id="e8236-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e8236-111">-AccountName</span></span>
<span data-ttu-id="e8236-112">Namn på Azure Data Share-konto</span><span class="sxs-lookup"><span data-stu-id="e8236-112">Azure data share account name</span></span>

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

### <span data-ttu-id="e8236-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8236-113">-DefaultProfile</span></span>
<span data-ttu-id="e8236-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e8236-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8236-115">-InvitationId</span><span class="sxs-lookup"><span data-stu-id="e8236-115">-InvitationId</span></span>
<span data-ttu-id="e8236-116">Azure Data Share-invitationId</span><span class="sxs-lookup"><span data-stu-id="e8236-116">Azure data share invitationId</span></span>

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

### <span data-ttu-id="e8236-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="e8236-117">-Name</span></span>
<span data-ttu-id="e8236-118">Namn på Azure Data Share-prenumeration</span><span class="sxs-lookup"><span data-stu-id="e8236-118">Azure data share subscription name</span></span>

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

### <span data-ttu-id="e8236-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8236-119">-ResourceGroupName</span></span>
<span data-ttu-id="e8236-120">Resurs grupp namnet för Azure Data Share-kontot</span><span class="sxs-lookup"><span data-stu-id="e8236-120">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="e8236-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e8236-121">-Confirm</span></span>
<span data-ttu-id="e8236-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e8236-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8236-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8236-123">-WhatIf</span></span>
<span data-ttu-id="e8236-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e8236-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8236-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e8236-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8236-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8236-126">CommonParameters</span></span>
<span data-ttu-id="e8236-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8236-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8236-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8236-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8236-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e8236-129">INPUTS</span></span>

### <span data-ttu-id="e8236-130">Ingen</span><span class="sxs-lookup"><span data-stu-id="e8236-130">None</span></span>

## <span data-ttu-id="e8236-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e8236-131">OUTPUTS</span></span>

### <span data-ttu-id="e8236-132">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="e8236-132">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="e8236-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e8236-133">NOTES</span></span>

## <span data-ttu-id="e8236-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e8236-134">RELATED LINKS</span></span>

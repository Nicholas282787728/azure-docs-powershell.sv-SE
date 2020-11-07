---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/grant-azdatasharesubscriptionaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Grant-AzDataShareSubscriptionAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Grant-AzDataShareSubscriptionAccess.md
ms.openlocfilehash: befe472f3340ae41e669ffa584e500051a7728d4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744446"
---
# <span data-ttu-id="8b920-101">Grant-AzDataShareSubscriptionAccess</span><span class="sxs-lookup"><span data-stu-id="8b920-101">Grant-AzDataShareSubscriptionAccess</span></span>

## <span data-ttu-id="8b920-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8b920-102">SYNOPSIS</span></span>
<span data-ttu-id="8b920-103">Ger åtkomst till en återkallad dela-prenumeration till käll resursen</span><span class="sxs-lookup"><span data-stu-id="8b920-103">Grants a revoked share subscription access to source share</span></span>

## <span data-ttu-id="8b920-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8b920-104">SYNTAX</span></span>

### <span data-ttu-id="8b920-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="8b920-105">ByFieldsParameterSet (Default)</span></span>
```
Grant-AzDataShareSubscriptionAccess -ResourceGroupName <String> -AccountName <String> [-ShareName <String>]
 -ShareSubscriptionId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8b920-106">ByProviderShareSubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b920-106">ByProviderShareSubscriptionIdParameterSet</span></span>
```
Grant-AzDataShareSubscriptionAccess -ShareSubscriptionId <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b920-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8b920-107">DESCRIPTION</span></span>
<span data-ttu-id="8b920-108">Cmdleten **Grant-AzDataShareSubscriptionAccess** tilldelar en åtkomst till käll delning för Share-prenumeration</span><span class="sxs-lookup"><span data-stu-id="8b920-108">The **Grant-AzDataShareSubscriptionAccess** cmdlet grants a share subscription access to source share</span></span>

## <span data-ttu-id="8b920-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8b920-109">EXAMPLES</span></span>

### <span data-ttu-id="8b920-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8b920-110">Example 1</span></span>
```
PS C:\> Grant-AzDataShareSubscriptionAccess -ResourceGroupName "ADS" -AccountName "WikiAdsAccount" -ShareName "AdsShare" -ShareSubscriptionId 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12

Company                   : ADS
CreatedAt                 : 6/15/2019 1:02:28 AM
CreatedBy                 : abc@microsoft.com
SharedAt                  : 6/15/2019 12:08:48 AM
SharedBy                  : abc@microsoft.com
ShareSubscriptionObjectId : 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12
ShareSubscriptionStatus   : Active
Id                        : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shares/AdsShare/shareSubscriptions/8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12
Name                      : AdsShare
Type                      : Microsoft.DataShare/ShareSubscriptions
```

<span data-ttu-id="8b920-111">Beviljar åtkomst till Share-prenumeration som identifieras av ID 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12</span><span class="sxs-lookup"><span data-stu-id="8b920-111">Grants access to share subscription identified by id 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12</span></span>

## <span data-ttu-id="8b920-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8b920-112">PARAMETERS</span></span>

### <span data-ttu-id="8b920-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8b920-113">-AccountName</span></span>
<span data-ttu-id="8b920-114">Namn på Azure Data Share-konto</span><span class="sxs-lookup"><span data-stu-id="8b920-114">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b920-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b920-115">-DefaultProfile</span></span>
<span data-ttu-id="8b920-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8b920-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b920-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b920-117">-ResourceGroupName</span></span>
<span data-ttu-id="8b920-118">Resurs grupp namnet för Azure Data Share-kontot</span><span class="sxs-lookup"><span data-stu-id="8b920-118">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b920-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8b920-119">-ResourceId</span></span>
<span data-ttu-id="8b920-120">Resurs-ID för Azure Data-resursen</span><span class="sxs-lookup"><span data-stu-id="8b920-120">The resource id of the azure data share</span></span>

```yaml
Type: System.String
Parameter Sets: ByProviderShareSubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b920-121">-ShareName</span><span class="sxs-lookup"><span data-stu-id="8b920-121">-ShareName</span></span>
<span data-ttu-id="8b920-122">Azure Data Share-namn</span><span class="sxs-lookup"><span data-stu-id="8b920-122">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b920-123">-ShareSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8b920-123">-ShareSubscriptionId</span></span>
<span data-ttu-id="8b920-124">ID för Share-Subscription för leverantörens delnings abonnemang</span><span class="sxs-lookup"><span data-stu-id="8b920-124">The share subscription id of the provider share subscription</span></span>

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

### <span data-ttu-id="8b920-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8b920-125">-Confirm</span></span>
<span data-ttu-id="8b920-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8b920-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b920-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b920-127">-WhatIf</span></span>
<span data-ttu-id="8b920-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8b920-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8b920-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8b920-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b920-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b920-130">CommonParameters</span></span>
<span data-ttu-id="8b920-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b920-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b920-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b920-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b920-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8b920-133">INPUTS</span></span>

### <span data-ttu-id="8b920-134">System. String</span><span class="sxs-lookup"><span data-stu-id="8b920-134">System.String</span></span>

## <span data-ttu-id="8b920-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8b920-135">OUTPUTS</span></span>

### <span data-ttu-id="8b920-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span><span class="sxs-lookup"><span data-stu-id="8b920-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span></span>

## <span data-ttu-id="8b920-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8b920-137">NOTES</span></span>

## <span data-ttu-id="8b920-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8b920-138">RELATED LINKS</span></span>
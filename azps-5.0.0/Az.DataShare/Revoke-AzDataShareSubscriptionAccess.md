---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/revoke-azdatasharesubscriptionaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Revoke-AzDataShareSubscriptionAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Revoke-AzDataShareSubscriptionAccess.md
ms.openlocfilehash: 540426cc8612f4cee7364a7875bb9a142bca07ef
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320244"
---
# <span data-ttu-id="9027d-101">Revoke-AzDataShareSubscriptionAccess</span><span class="sxs-lookup"><span data-stu-id="9027d-101">Revoke-AzDataShareSubscriptionAccess</span></span>

## <span data-ttu-id="9027d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9027d-102">SYNOPSIS</span></span>
<span data-ttu-id="9027d-103">Återkalla åtkomst till käll delning för abonnemang</span><span class="sxs-lookup"><span data-stu-id="9027d-103">Revokes share subscription access to source share</span></span>

## <span data-ttu-id="9027d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9027d-104">SYNTAX</span></span>

### <span data-ttu-id="9027d-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="9027d-105">ByFieldsParameterSet (Default)</span></span>
```
Revoke-AzDataShareSubscriptionAccess -ResourceGroupName <String> -AccountName <String> [-ShareName <String>]
 -ShareSubscriptionId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9027d-106">ByProviderShareSubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9027d-106">ByProviderShareSubscriptionIdParameterSet</span></span>
```
Revoke-AzDataShareSubscriptionAccess -ShareSubscriptionId <String> -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9027d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9027d-107">DESCRIPTION</span></span>
<span data-ttu-id="9027d-108">Med cmdleten **REVOKE-AzDataShareSubscriptionAccess** tilldelas en åtkomst till käll resursen för dela prenumeration</span><span class="sxs-lookup"><span data-stu-id="9027d-108">The **Revoke-AzDataShareSubscriptionAccess** cmdlet grants a share subscription access to source share</span></span>

## <span data-ttu-id="9027d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9027d-109">EXAMPLES</span></span>

### <span data-ttu-id="9027d-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9027d-110">Example 1</span></span>
```
PS C:\> Revoke-AzDataShareSubscriptionAccess -ResourceGroupName "ADS" -AccountName "WikiAdsAccount" -ShareName "AdsShare" -ShareSubscriptionId 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12

Company                   : ADS
CreatedAt                 : 6/15/2019 1:02:28 AM
CreatedBy                 : abc@microsoft.com
SharedAt                  : 6/15/2019 12:08:48 AM
SharedBy                  : abc@microsoft.com
ShareSubscriptionObjectId : 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12
ShareSubscriptionStatus   : Revoked
Id                        : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shares/AdsShare/shareSubscriptions/8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12
Name                      : AdsShare
Type                      : Microsoft.DataShare/ShareSubscriptions
```

<span data-ttu-id="9027d-111">Återkalla åtkomsten till Share-prenumerationen som identifieras av ID 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12</span><span class="sxs-lookup"><span data-stu-id="9027d-111">Revokes access of share subscription identified by id 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12</span></span>

## <span data-ttu-id="9027d-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9027d-112">PARAMETERS</span></span>

### <span data-ttu-id="9027d-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9027d-113">-AccountName</span></span>
<span data-ttu-id="9027d-114">Namn på Azure Data Share-konto</span><span class="sxs-lookup"><span data-stu-id="9027d-114">Azure data share account name</span></span>

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

### <span data-ttu-id="9027d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9027d-115">-AsJob</span></span>
<span data-ttu-id="9027d-116">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="9027d-116">{{Fill AsJob Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9027d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9027d-117">-DefaultProfile</span></span>
<span data-ttu-id="9027d-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9027d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9027d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9027d-119">-ResourceGroupName</span></span>
<span data-ttu-id="9027d-120">Resurs grupp namnet för Azure Data Share-kontot</span><span class="sxs-lookup"><span data-stu-id="9027d-120">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="9027d-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9027d-121">-ResourceId</span></span>
<span data-ttu-id="9027d-122">Resurs-ID för Azure Data-resursen</span><span class="sxs-lookup"><span data-stu-id="9027d-122">The resource id of the azure data share</span></span>

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

### <span data-ttu-id="9027d-123">-ShareName</span><span class="sxs-lookup"><span data-stu-id="9027d-123">-ShareName</span></span>
<span data-ttu-id="9027d-124">Azure Data Share-namn</span><span class="sxs-lookup"><span data-stu-id="9027d-124">Azure data share name</span></span>

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

### <span data-ttu-id="9027d-125">-ShareSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9027d-125">-ShareSubscriptionId</span></span>
<span data-ttu-id="9027d-126">ID för Share-Subscription för leverantörens delnings abonnemang</span><span class="sxs-lookup"><span data-stu-id="9027d-126">The share subscription id of the provider share subscription</span></span>

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

### <span data-ttu-id="9027d-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9027d-127">-Confirm</span></span>
<span data-ttu-id="9027d-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9027d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9027d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9027d-129">-WhatIf</span></span>
<span data-ttu-id="9027d-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9027d-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9027d-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9027d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9027d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9027d-132">CommonParameters</span></span>
<span data-ttu-id="9027d-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9027d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9027d-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9027d-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9027d-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9027d-135">INPUTS</span></span>

### <span data-ttu-id="9027d-136">System. String</span><span class="sxs-lookup"><span data-stu-id="9027d-136">System.String</span></span>

## <span data-ttu-id="9027d-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9027d-137">OUTPUTS</span></span>

### <span data-ttu-id="9027d-138">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span><span class="sxs-lookup"><span data-stu-id="9027d-138">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span></span>

## <span data-ttu-id="9027d-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9027d-139">NOTES</span></span>

## <span data-ttu-id="9027d-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9027d-140">RELATED LINKS</span></span>
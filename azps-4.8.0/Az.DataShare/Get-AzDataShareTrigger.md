---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareTrigger.md
ms.openlocfilehash: 23554c4de23062fa44a690843232dbc6337e3c9e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102908"
---
# <span data-ttu-id="6f7e4-101">Get-AzDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="6f7e4-101">Get-AzDataShareTrigger</span></span>

## <span data-ttu-id="6f7e4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6f7e4-102">SYNOPSIS</span></span>
<span data-ttu-id="6f7e4-103">Hämtar information om en utlösare i dela prenumeration.</span><span class="sxs-lookup"><span data-stu-id="6f7e4-103">Gets information about a trigger in share subscription.</span></span>

## <span data-ttu-id="6f7e4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6f7e4-104">SYNTAX</span></span>

### <span data-ttu-id="6f7e4-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="6f7e4-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareTrigger -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f7e4-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f7e4-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareTrigger -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f7e4-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6f7e4-107">DESCRIPTION</span></span>
<span data-ttu-id="6f7e4-108">Cmdleten **Get-AzDataShareTrigger** hämtar information om trigger för Share-prenumeration under data delnings konto.</span><span class="sxs-lookup"><span data-stu-id="6f7e4-108">The **Get-AzDataShareTrigger** cmdlet gets information about trigger for share subscription under data share account.</span></span>

## <span data-ttu-id="6f7e4-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6f7e4-109">EXAMPLES</span></span>

### <span data-ttu-id="6f7e4-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6f7e4-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareTrigger -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -Name "AdsTrigger"

CreatedAt           : 7/10/2019 12:16:34 AM
CreatedBy           : Ads test
ProvisioningState   : Succeeded
RecurrenceInterval  : Day
SynchronizationMode : Incremental
SynchronizationTime : 7/9/2019 9:00:00 AM
TriggerStatus       : Active
Id                  : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shareSubscriptions/AdsShareSubscription/triggers/AdsTrigger
Name                : AdsTrigger
Type                : Microsoft.DataShare/Triggers
```

<span data-ttu-id="6f7e4-111">Det här kommandot får information om trigger AdsTrigger för Share Subscription AdsShareSubscription under data Share Account WikiAds.</span><span class="sxs-lookup"><span data-stu-id="6f7e4-111">This command gets information about trigger AdsTrigger for share subscription AdsShareSubscription under data share account WikiAds.</span></span>

## <span data-ttu-id="6f7e4-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6f7e4-112">PARAMETERS</span></span>

### <span data-ttu-id="6f7e4-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6f7e4-113">-AccountName</span></span>
<span data-ttu-id="6f7e4-114">Namn på Azure Data Share-konto</span><span class="sxs-lookup"><span data-stu-id="6f7e4-114">Azure data share account name</span></span>

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

### <span data-ttu-id="6f7e4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f7e4-115">-DefaultProfile</span></span>
<span data-ttu-id="6f7e4-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6f7e4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f7e4-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="6f7e4-117">-Name</span></span>
<span data-ttu-id="6f7e4-118">Namn på Azure Data Share-avtryckare</span><span class="sxs-lookup"><span data-stu-id="6f7e4-118">Azure data share trigger name</span></span>

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

### <span data-ttu-id="6f7e4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f7e4-119">-ResourceGroupName</span></span>
<span data-ttu-id="6f7e4-120">Resurs grupp namnet för Azure Data Share-kontot</span><span class="sxs-lookup"><span data-stu-id="6f7e4-120">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="6f7e4-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6f7e4-121">-ResourceId</span></span>
<span data-ttu-id="6f7e4-122">Resurs-ID för utlösaren</span><span class="sxs-lookup"><span data-stu-id="6f7e4-122">The resource id of the trigger</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f7e4-123">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="6f7e4-123">-ShareSubscriptionName</span></span>
<span data-ttu-id="6f7e4-124">Namn på Azure Data Share-prenumeration</span><span class="sxs-lookup"><span data-stu-id="6f7e4-124">Azure data share subscription name</span></span>

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

### <span data-ttu-id="6f7e4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f7e4-125">CommonParameters</span></span>
<span data-ttu-id="6f7e4-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f7e4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f7e4-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6f7e4-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f7e4-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6f7e4-128">INPUTS</span></span>

### <span data-ttu-id="6f7e4-129">System. String</span><span class="sxs-lookup"><span data-stu-id="6f7e4-129">System.String</span></span>

## <span data-ttu-id="6f7e4-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6f7e4-130">OUTPUTS</span></span>

### <span data-ttu-id="6f7e4-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="6f7e4-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span></span>

## <span data-ttu-id="6f7e4-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6f7e4-132">NOTES</span></span>

## <span data-ttu-id="6f7e4-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6f7e4-133">RELATED LINKS</span></span>

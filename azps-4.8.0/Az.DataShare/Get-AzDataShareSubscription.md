---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscription.md
ms.openlocfilehash: 910afff2a9c5524d452c5a5f4bec48a3f18359a3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262295"
---
# <span data-ttu-id="a08e2-101">Get-AzDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="a08e2-101">Get-AzDataShareSubscription</span></span>

## <span data-ttu-id="a08e2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a08e2-102">SYNOPSIS</span></span>
<span data-ttu-id="a08e2-103">Hämtar information om hur du delar abonnemang i data resurs konto.</span><span class="sxs-lookup"><span data-stu-id="a08e2-103">Gets information about share subscription in data share account.</span></span>

## <span data-ttu-id="a08e2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a08e2-104">SYNTAX</span></span>

### <span data-ttu-id="a08e2-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="a08e2-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSubscription -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a08e2-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a08e2-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSubscription -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a08e2-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a08e2-107">DESCRIPTION</span></span>
<span data-ttu-id="a08e2-108">Cmdleten **Get-AzDataShareSubscription** innehåller information om hur du delar abonnemang i ett data delnings konto.</span><span class="sxs-lookup"><span data-stu-id="a08e2-108">The **Get-AzDataShareSubscription** cmdlet provides information about share subscription in a data share account.</span></span> <span data-ttu-id="a08e2-109">Om Share-prenumerationens namn anges ger cmdleten information om det specifika abonnemanget för resursen.</span><span class="sxs-lookup"><span data-stu-id="a08e2-109">If share subscription name is provided, the cmdlet gives information about the particular share subscription.</span></span> <span data-ttu-id="a08e2-110">Annars tillhandahåller cmdleten en lista med resurs prenumerationer i data resurs kontot.</span><span class="sxs-lookup"><span data-stu-id="a08e2-110">Otherwise, the cmdlet provides a list of share subscriptions in the data share account.</span></span>

## <span data-ttu-id="a08e2-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a08e2-111">EXAMPLES</span></span>

### <span data-ttu-id="a08e2-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a08e2-112">Example 1</span></span>
```
PS C:\> Get-AzDataShareSubscription -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShareSubscription"

CreatedAt               : 7/9/2019 12:32:53 AM
CreatedBy               : adstest@microsoft.com
InvitationId            : 0c14f5b6-0e22-49ab-8043-d6edad51db13
ProvisioningState       : Succeeded
ShareName               : AdsShare
ShareSender             : adsprovider@microsoft.com
ShareSenderCompanyName  : ADS Test
ShareDescription        : Ads description
ShareTerms              : Ads terms of use
ShareSubscriptionStatus : Active
ShareKind               : CopyBased
Id                      : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shareSubscriptions/AdsShareSubscription
Name                    : AdsShareSubscription
Type                    : Microsoft.DataShare/ShareSubscriptions
```

<span data-ttu-id="a08e2-113">Det här kommandot innehåller information om hur du delar abonnemangs AdsShareSubscription i WikiAds för data delning.</span><span class="sxs-lookup"><span data-stu-id="a08e2-113">This command provides information about share subscription AdsShareSubscription in data share account WikiAds.</span></span>

## <span data-ttu-id="a08e2-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a08e2-114">PARAMETERS</span></span>

### <span data-ttu-id="a08e2-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a08e2-115">-AccountName</span></span>
<span data-ttu-id="a08e2-116">Namn på Azure Data Share-konto</span><span class="sxs-lookup"><span data-stu-id="a08e2-116">Azure data share account name</span></span>

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

### <span data-ttu-id="a08e2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a08e2-117">-DefaultProfile</span></span>
<span data-ttu-id="a08e2-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a08e2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a08e2-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="a08e2-119">-Name</span></span>
<span data-ttu-id="a08e2-120">Namn på Azure Data Share-prenumeration</span><span class="sxs-lookup"><span data-stu-id="a08e2-120">Azure data share subscription name</span></span>

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

### <span data-ttu-id="a08e2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a08e2-121">-ResourceGroupName</span></span>
<span data-ttu-id="a08e2-122">Resurs grupp namnet för Azure Data Share-kontot</span><span class="sxs-lookup"><span data-stu-id="a08e2-122">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="a08e2-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a08e2-123">-ResourceId</span></span>
<span data-ttu-id="a08e2-124">Resurs-ID för Azure Data Share-prenumerationen</span><span class="sxs-lookup"><span data-stu-id="a08e2-124">The resource id of the azure data share subscription</span></span>

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

### <span data-ttu-id="a08e2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a08e2-125">CommonParameters</span></span>
<span data-ttu-id="a08e2-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a08e2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a08e2-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a08e2-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a08e2-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a08e2-128">INPUTS</span></span>

### <span data-ttu-id="a08e2-129">System. String</span><span class="sxs-lookup"><span data-stu-id="a08e2-129">System.String</span></span>

## <span data-ttu-id="a08e2-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a08e2-130">OUTPUTS</span></span>

### <span data-ttu-id="a08e2-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="a08e2-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="a08e2-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a08e2-132">NOTES</span></span>

## <span data-ttu-id="a08e2-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a08e2-133">RELATED LINKS</span></span>

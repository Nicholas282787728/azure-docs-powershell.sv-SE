---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatashareprovidersharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareProviderShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareProviderShareSubscription.md
ms.openlocfilehash: 5422b43019b7b667ba7ea787663e91e2b6beb118
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320355"
---
# <span data-ttu-id="f4745-101">Get-AzDataShareProviderShareSubscription</span><span class="sxs-lookup"><span data-stu-id="f4745-101">Get-AzDataShareProviderShareSubscription</span></span>

## <span data-ttu-id="f4745-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f4745-102">SYNOPSIS</span></span>
<span data-ttu-id="f4745-103">Hämtar information om klient prenumerations abonnemang på leverantörens sida.</span><span class="sxs-lookup"><span data-stu-id="f4745-103">Gets information about consumer share subscriptions on provider side.</span></span>

## <span data-ttu-id="f4745-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f4745-104">SYNTAX</span></span>

### <span data-ttu-id="f4745-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="f4745-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareProviderShareSubscription -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 [-ShareSubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4745-106">ByProviderShareSubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4745-106">ByProviderShareSubscriptionIdParameterSet</span></span>
```
Get-AzDataShareProviderShareSubscription [-ShareSubscriptionId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4745-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f4745-107">DESCRIPTION</span></span>
<span data-ttu-id="f4745-108">Cmdleten **Get-AzDataShareProviderSubscription** hämtar information om klient prenumerationer på leverantörens sida.</span><span class="sxs-lookup"><span data-stu-id="f4745-108">The **Get-AzDataShareProviderSubscription** cmdlet gets information about consumer share subscriptions on provider side.</span></span> <span data-ttu-id="f4745-109">Om du anger Share abonnemang ID får denna cmdlet information om Share-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="f4745-109">If you specify the share subscrption id, this cmdlet gets information about the share subscription.</span></span> <span data-ttu-id="f4745-110">Om du inte anger ID för delad prenumeration får denna cmdlet information om alla klient prenumerationer för konsument delning som är associerade med resursen.</span><span class="sxs-lookup"><span data-stu-id="f4745-110">If you do not specify the share subscription id, this cmdlet gets information about all the consumer share subscriptions in associated with the share.</span></span>

## <span data-ttu-id="f4745-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f4745-111">EXAMPLES</span></span>

### <span data-ttu-id="f4745-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f4745-112">Example 1</span></span>
```
PS C:\> Get-AzDataShareProviderShareSubscription -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -ShareSubscriptionId "/subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shares/AdsShare/shareSubscriptions/505c3500-b2ff-46ab-96bf-50f5ec89d75a"

Company                   : ADS Test
CreatedAt                 : 6/30/2019 12:42:12 AM
CreatedBy                 : adstest@microsoft.com
SharedAt                  : 6/30/2019 12:41:37 AM
SharedBy                  : adsprovider@microsoft.com
ShareSubscriptionObjectId : 505c3500-b2ff-46ab-96bf-50f5ec89d75a
ShareSubscriptionStatus   : Active
Id                        : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shares/AdsShare/shareSubscriptions/505c3500-b2ff-46ab-96bf-50f5ec89d75a
Name                      : AdsShareSubscription
Type                      : Microsoft.DataShare/ShareSubscriptions
```

<span data-ttu-id="f4745-113">Det här kommandot innehåller information om klient prenumerationen för resurser som är kopplad till Share AdsShare i WikiAds för data delning.</span><span class="sxs-lookup"><span data-stu-id="f4745-113">This commands provides information about consumer share subscription associated with share AdsShare in data share account WikiAds.</span></span>

## <span data-ttu-id="f4745-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f4745-114">PARAMETERS</span></span>

### <span data-ttu-id="f4745-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f4745-115">-AccountName</span></span>
<span data-ttu-id="f4745-116">Namn på Azure DataShare.</span><span class="sxs-lookup"><span data-stu-id="f4745-116">Azure DataShare Account name.</span></span>

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

### <span data-ttu-id="f4745-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4745-117">-DefaultProfile</span></span>
<span data-ttu-id="f4745-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f4745-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4745-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4745-119">-ResourceGroupName</span></span>
<span data-ttu-id="f4745-120">Resurs gruppen för Azure DataShare-kontot.</span><span class="sxs-lookup"><span data-stu-id="f4745-120">The resource group of the Azure DataShare Account.</span></span>

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

### <span data-ttu-id="f4745-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f4745-121">-ResourceId</span></span>
<span data-ttu-id="f4745-122">Resurs-ID för resursen</span><span class="sxs-lookup"><span data-stu-id="f4745-122">The resource id of the share</span></span>

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

### <span data-ttu-id="f4745-123">-ShareName</span><span class="sxs-lookup"><span data-stu-id="f4745-123">-ShareName</span></span>
<span data-ttu-id="f4745-124">Namn på Azure DataShare.</span><span class="sxs-lookup"><span data-stu-id="f4745-124">Azure DataShare name.</span></span>

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

### <span data-ttu-id="f4745-125">-ShareSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f4745-125">-ShareSubscriptionId</span></span>
<span data-ttu-id="f4745-126">ID för konsument delnings abonnemang</span><span class="sxs-lookup"><span data-stu-id="f4745-126">The id of consumer share subscription</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4745-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4745-127">CommonParameters</span></span>
<span data-ttu-id="f4745-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4745-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4745-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f4745-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4745-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f4745-130">INPUTS</span></span>

### <span data-ttu-id="f4745-131">System. String</span><span class="sxs-lookup"><span data-stu-id="f4745-131">System.String</span></span>

## <span data-ttu-id="f4745-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f4745-132">OUTPUTS</span></span>

### <span data-ttu-id="f4745-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span><span class="sxs-lookup"><span data-stu-id="f4745-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span></span>

## <span data-ttu-id="f4745-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f4745-134">NOTES</span></span>

## <span data-ttu-id="f4745-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f4745-135">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 6E84E26F-8150-41F8-8823-CEED05619A75
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountPartner.md
ms.openlocfilehash: 7063fb81705a14f1c1d8f0d02a2dc51d8a5617ac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756500"
---
# <span data-ttu-id="b2ee8-101">Get-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="b2ee8-101">Get-AzureRmIntegrationAccountPartner</span></span>

## <span data-ttu-id="b2ee8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b2ee8-102">SYNOPSIS</span></span>
<span data-ttu-id="b2ee8-103">Får integrerings konto partners.</span><span class="sxs-lookup"><span data-stu-id="b2ee8-103">Gets integration account partners.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b2ee8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b2ee8-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccountPartner [-ResourceGroupName <String>] [-Name <String>] [-PartnerName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2ee8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b2ee8-105">DESCRIPTION</span></span>
<span data-ttu-id="b2ee8-106">Cmdleten **Get-AzureRmIntegrationAccountPartner** får integrerings konto partner från en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="b2ee8-106">The **Get-AzureRmIntegrationAccountPartner** cmdlet gets integration account partners from a resource group.</span></span>
<span data-ttu-id="b2ee8-107">Ange integrerings konto namn, resurs grupps namn och partner namn.</span><span class="sxs-lookup"><span data-stu-id="b2ee8-107">Specify the integration account name, resource group name, and partner name.</span></span>

<span data-ttu-id="b2ee8-108">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="b2ee8-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="b2ee8-109">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="b2ee8-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="b2ee8-110">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="b2ee8-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="b2ee8-111">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="b2ee8-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="b2ee8-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b2ee8-112">EXAMPLES</span></span>

### <span data-ttu-id="b2ee8-113">Exempel 1: skaffa en integrations konto partner</span><span class="sxs-lookup"><span data-stu-id="b2ee8-113">Example 1: Get an integration account partner</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner22"
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/TestIntegrationAccount/partners/IntegrationAccountPartner31
Name               : IntegrationAccountPartner31
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/24/2016 8:46:05 PM
ChangedTime        : 3/24/2016 8:47:47 PM
BusinessIdentities : {"Qualifier":"CC","Value":"FF"}
Metadata           :
```

<span data-ttu-id="b2ee8-114">Det här kommandot får integrerings konto partnern med namnet IntegrationAccountPartner22.</span><span class="sxs-lookup"><span data-stu-id="b2ee8-114">This command gets the integration account partner named IntegrationAccountPartner22.</span></span>

### <span data-ttu-id="b2ee8-115">Exempel 2: skaffa ett integrerings konto partner med hjälp av ett integrations konto namn</span><span class="sxs-lookup"><span data-stu-id="b2ee8-115">Example 2: Get an integration account partners by using an integration account name</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/TestIntegrationAccount/partners/IntegrationAccountPartner31
Name               : IntegrationAccountPartner31
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/24/2016 8:46:05 PM
ChangedTime        : 3/24/2016 8:47:47 PM
BusinessIdentities : {"Qualifier":"CC","Value":"FF"}
Metadata           :
```

<span data-ttu-id="b2ee8-116">Det här kommandot får integrerings konto partners för integrations kontot med namnet IntegrationAccount31.</span><span class="sxs-lookup"><span data-stu-id="b2ee8-116">This command gets the integration account partners for the integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="b2ee8-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b2ee8-117">PARAMETERS</span></span>

### <span data-ttu-id="b2ee8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2ee8-118">-DefaultProfile</span></span>
<span data-ttu-id="b2ee8-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="b2ee8-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b2ee8-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="b2ee8-120">-Name</span></span>
<span data-ttu-id="b2ee8-121">Anger namnet på ett integrations konto.</span><span class="sxs-lookup"><span data-stu-id="b2ee8-121">Specifies the name of an integration account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2ee8-122">-PartnerName</span><span class="sxs-lookup"><span data-stu-id="b2ee8-122">-PartnerName</span></span>
<span data-ttu-id="b2ee8-123">Anger namnet på integrations konto partnern.</span><span class="sxs-lookup"><span data-stu-id="b2ee8-123">Specifies the name of the integration account partner.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2ee8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2ee8-124">-ResourceGroupName</span></span>
<span data-ttu-id="b2ee8-125">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="b2ee8-125">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2ee8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2ee8-126">CommonParameters</span></span>
<span data-ttu-id="b2ee8-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2ee8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2ee8-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2ee8-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2ee8-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b2ee8-129">INPUTS</span></span>

### <span data-ttu-id="b2ee8-130">Ingen</span><span class="sxs-lookup"><span data-stu-id="b2ee8-130">None</span></span>
<span data-ttu-id="b2ee8-131">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="b2ee8-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b2ee8-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b2ee8-132">OUTPUTS</span></span>

### <span data-ttu-id="b2ee8-133">Microsoft. Azure. Management. Logic. Models. IntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="b2ee8-133">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span></span>

## <span data-ttu-id="b2ee8-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b2ee8-134">NOTES</span></span>

## <span data-ttu-id="b2ee8-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b2ee8-135">RELATED LINKS</span></span>

[<span data-ttu-id="b2ee8-136">New-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="b2ee8-136">New-AzureRmIntegrationAccountPartner</span></span>](./New-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="b2ee8-137">Remove-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="b2ee8-137">Remove-AzureRmIntegrationAccountPartner</span></span>](./Remove-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="b2ee8-138">Set-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="b2ee8-138">Set-AzureRmIntegrationAccountPartner</span></span>](./Set-AzureRmIntegrationAccountPartner.md)



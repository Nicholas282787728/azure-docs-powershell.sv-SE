---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 6E84E26F-8150-41F8-8823-CEED05619A75
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountPartner.md
ms.openlocfilehash: cf6d2f4da1803e5c9403803ea7231b55c13d7243
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525934"
---
# <span data-ttu-id="f624a-101">Get-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="f624a-101">Get-AzIntegrationAccountPartner</span></span>

## <span data-ttu-id="f624a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f624a-102">SYNOPSIS</span></span>
<span data-ttu-id="f624a-103">Får integrerings konto partners.</span><span class="sxs-lookup"><span data-stu-id="f624a-103">Gets integration account partners.</span></span>

## <span data-ttu-id="f624a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f624a-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountPartner [-ResourceGroupName <String>] [-Name <String>] [-PartnerName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f624a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f624a-105">DESCRIPTION</span></span>
<span data-ttu-id="f624a-106">Cmdleten **Get-AzIntegrationAccountPartner** får integrerings konto partner från en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="f624a-106">The **Get-AzIntegrationAccountPartner** cmdlet gets integration account partners from a resource group.</span></span>
<span data-ttu-id="f624a-107">Ange integrerings konto namn, resurs grupps namn och partner namn.</span><span class="sxs-lookup"><span data-stu-id="f624a-107">Specify the integration account name, resource group name, and partner name.</span></span>
<span data-ttu-id="f624a-108">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="f624a-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="f624a-109">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="f624a-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="f624a-110">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="f624a-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="f624a-111">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="f624a-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="f624a-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f624a-112">EXAMPLES</span></span>

### <span data-ttu-id="f624a-113">Exempel 1: skaffa en integrations konto partner</span><span class="sxs-lookup"><span data-stu-id="f624a-113">Example 1: Get an integration account partner</span></span>
```
PS C:\>Get-AzIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner22"
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/TestIntegrationAccount/partners/IntegrationAccountPartner31
Name               : IntegrationAccountPartner31
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/24/2016 8:46:05 PM
ChangedTime        : 3/24/2016 8:47:47 PM
BusinessIdentities : {"Qualifier":"CC","Value":"FF"}
Metadata           :
```

<span data-ttu-id="f624a-114">Det här kommandot får integrerings konto partnern med namnet IntegrationAccountPartner22.</span><span class="sxs-lookup"><span data-stu-id="f624a-114">This command gets the integration account partner named IntegrationAccountPartner22.</span></span>

### <span data-ttu-id="f624a-115">Exempel 2: skaffa ett integrerings konto partner med hjälp av ett integrations konto namn</span><span class="sxs-lookup"><span data-stu-id="f624a-115">Example 2: Get an integration account partners by using an integration account name</span></span>
```
PS C:\>Get-AzIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/TestIntegrationAccount/partners/IntegrationAccountPartner31
Name               : IntegrationAccountPartner31
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/24/2016 8:46:05 PM
ChangedTime        : 3/24/2016 8:47:47 PM
BusinessIdentities : {"Qualifier":"CC","Value":"FF"}
Metadata           :
```

<span data-ttu-id="f624a-116">Det här kommandot får integrerings konto partners för integrations kontot med namnet IntegrationAccount31.</span><span class="sxs-lookup"><span data-stu-id="f624a-116">This command gets the integration account partners for the integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="f624a-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f624a-117">PARAMETERS</span></span>

### <span data-ttu-id="f624a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f624a-118">-DefaultProfile</span></span>
<span data-ttu-id="f624a-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="f624a-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f624a-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="f624a-120">-Name</span></span>
<span data-ttu-id="f624a-121">Anger namnet på ett integrations konto.</span><span class="sxs-lookup"><span data-stu-id="f624a-121">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f624a-122">-PartnerName</span><span class="sxs-lookup"><span data-stu-id="f624a-122">-PartnerName</span></span>
<span data-ttu-id="f624a-123">Anger namnet på integrations konto partnern.</span><span class="sxs-lookup"><span data-stu-id="f624a-123">Specifies the name of the integration account partner.</span></span>

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

### <span data-ttu-id="f624a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f624a-124">-ResourceGroupName</span></span>
<span data-ttu-id="f624a-125">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="f624a-125">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f624a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f624a-126">CommonParameters</span></span>
<span data-ttu-id="f624a-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f624a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f624a-128">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f624a-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f624a-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f624a-129">INPUTS</span></span>

### <span data-ttu-id="f624a-130">System. String</span><span class="sxs-lookup"><span data-stu-id="f624a-130">System.String</span></span>

## <span data-ttu-id="f624a-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f624a-131">OUTPUTS</span></span>

### <span data-ttu-id="f624a-132">Microsoft. Azure. Management. Logic. Models. IntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="f624a-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span></span>

## <span data-ttu-id="f624a-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f624a-133">NOTES</span></span>

## <span data-ttu-id="f624a-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f624a-134">RELATED LINKS</span></span>

[<span data-ttu-id="f624a-135">New-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="f624a-135">New-AzIntegrationAccountPartner</span></span>](./New-AzIntegrationAccountPartner.md)

[<span data-ttu-id="f624a-136">Remove-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="f624a-136">Remove-AzIntegrationAccountPartner</span></span>](./Remove-AzIntegrationAccountPartner.md)

[<span data-ttu-id="f624a-137">Set-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="f624a-137">Set-AzIntegrationAccountPartner</span></span>](./Set-AzIntegrationAccountPartner.md)



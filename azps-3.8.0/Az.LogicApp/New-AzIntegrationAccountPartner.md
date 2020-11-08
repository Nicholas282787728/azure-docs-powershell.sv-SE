---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 2B5FC268-4888-4AEB-B125-7263CF2E4DCD
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountPartner.md
ms.openlocfilehash: bbd64f1e6df016efe0bdd22bb0ae848c79566edf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93925833"
---
# <span data-ttu-id="f330c-101">New-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="f330c-101">New-AzIntegrationAccountPartner</span></span>

## <span data-ttu-id="f330c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f330c-102">SYNOPSIS</span></span>
<span data-ttu-id="f330c-103">Skapar en integrerings konto partner.</span><span class="sxs-lookup"><span data-stu-id="f330c-103">Creates an integration account partner.</span></span>

## <span data-ttu-id="f330c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f330c-104">SYNTAX</span></span>

```
New-AzIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String>
 [-PartnerType <String>] -BusinessIdentities <Object> [-Metadata <Object>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f330c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f330c-105">DESCRIPTION</span></span>
<span data-ttu-id="f330c-106">Cmdleten **New-AzIntegrationAccountPartner** skapar en integrerings konto partner.</span><span class="sxs-lookup"><span data-stu-id="f330c-106">The **New-AzIntegrationAccountPartner** cmdlet creates an integration account partner.</span></span>
<span data-ttu-id="f330c-107">Denna cmdlet returnerar ett objekt som representerar integrerings konto partnern.</span><span class="sxs-lookup"><span data-stu-id="f330c-107">This cmdlet returns an object that represents the integration account partner.</span></span>
<span data-ttu-id="f330c-108">Ange integrerings konto namn, resurs grupps namn, partner namn och partner identiteter.</span><span class="sxs-lookup"><span data-stu-id="f330c-108">Specify the integration account name, resource group name, partner name, and partner identities.</span></span>
<span data-ttu-id="f330c-109">De fil värden för mallfiler som du anger i kommando raden har högre prioritet än värden för Mallkategorier i ett Template parameter-objekt.</span><span class="sxs-lookup"><span data-stu-id="f330c-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="f330c-110">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="f330c-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="f330c-111">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="f330c-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="f330c-112">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="f330c-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="f330c-113">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="f330c-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="f330c-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f330c-114">EXAMPLES</span></span>

### <span data-ttu-id="f330c-115">Exempel 1: skapa en integrations konto partner</span><span class="sxs-lookup"><span data-stu-id="f330c-115">Example 1: Create an integration account partner</span></span>
```
PS C:\>New-AzIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner22" -PartnerType "B2B" -BusinessIdentities $BusinessIdentities
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/partners/IntegrationAccountPartner1
Name               : IntegrationAccountPartner1
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/26/2016 7:29:30 PM
ChangedTime        : 3/26/2016 7:29:30 PM
BusinessIdentities : [{"Qualifier":"ZZ","Value":"AA"},{"Qualifier":"XX","Value":"GG"}]
Metadata           :
```

<span data-ttu-id="f330c-116">Det här kommandot skapar integrerings konto partnern med namnet IntegrationAccountPartner22 i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="f330c-116">This command creates the integration account partner named IntegrationAccountPartner22 in the specified resource group.</span></span>

## <span data-ttu-id="f330c-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f330c-117">PARAMETERS</span></span>

### <span data-ttu-id="f330c-118">-BusinessIdentities</span><span class="sxs-lookup"><span data-stu-id="f330c-118">-BusinessIdentities</span></span>
<span data-ttu-id="f330c-119">Anger företags identitet för integrerings konto partnern.</span><span class="sxs-lookup"><span data-stu-id="f330c-119">Specifies business identities for the integration account partner.</span></span>
<span data-ttu-id="f330c-120">Ange en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="f330c-120">Specify a hash table.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f330c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f330c-121">-DefaultProfile</span></span>
<span data-ttu-id="f330c-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="f330c-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f330c-123">-Metadata</span><span class="sxs-lookup"><span data-stu-id="f330c-123">-Metadata</span></span>
<span data-ttu-id="f330c-124">Anger ett metadataobjekt för partnern.</span><span class="sxs-lookup"><span data-stu-id="f330c-124">Specifies a metadata object for the partner.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f330c-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="f330c-125">-Name</span></span>
<span data-ttu-id="f330c-126">Anger namnet på ett integrations konto.</span><span class="sxs-lookup"><span data-stu-id="f330c-126">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f330c-127">-PartnerName</span><span class="sxs-lookup"><span data-stu-id="f330c-127">-PartnerName</span></span>
<span data-ttu-id="f330c-128">Anger ett namn på integrations konto partnern.</span><span class="sxs-lookup"><span data-stu-id="f330c-128">Specifies a name for the integration account partner.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f330c-129">-PartnerType</span><span class="sxs-lookup"><span data-stu-id="f330c-129">-PartnerType</span></span>
<span data-ttu-id="f330c-130">Anger typen av integrations konto.</span><span class="sxs-lookup"><span data-stu-id="f330c-130">Specifies the type of the integration account.</span></span>
<span data-ttu-id="f330c-131">Den här parametern har stöd för typen B2B.</span><span class="sxs-lookup"><span data-stu-id="f330c-131">This parameter supports the type B2B.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: B2B

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f330c-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f330c-132">-ResourceGroupName</span></span>
<span data-ttu-id="f330c-133">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="f330c-133">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f330c-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f330c-134">-Confirm</span></span>
<span data-ttu-id="f330c-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f330c-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f330c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f330c-136">-WhatIf</span></span>
<span data-ttu-id="f330c-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f330c-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f330c-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f330c-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f330c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f330c-139">CommonParameters</span></span>
<span data-ttu-id="f330c-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f330c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f330c-141">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f330c-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f330c-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f330c-142">INPUTS</span></span>

### <span data-ttu-id="f330c-143">System. String</span><span class="sxs-lookup"><span data-stu-id="f330c-143">System.String</span></span>

## <span data-ttu-id="f330c-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f330c-144">OUTPUTS</span></span>

### <span data-ttu-id="f330c-145">Microsoft. Azure. Management. Logic. Models. IntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="f330c-145">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span></span>

## <span data-ttu-id="f330c-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f330c-146">NOTES</span></span>

## <span data-ttu-id="f330c-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f330c-147">RELATED LINKS</span></span>

[<span data-ttu-id="f330c-148">Get-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="f330c-148">Get-AzIntegrationAccountPartner</span></span>](./Get-AzIntegrationAccountPartner.md)

[<span data-ttu-id="f330c-149">Remove-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="f330c-149">Remove-AzIntegrationAccountPartner</span></span>](./Remove-AzIntegrationAccountPartner.md)

[<span data-ttu-id="f330c-150">Set-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="f330c-150">Set-AzIntegrationAccountPartner</span></span>](./Set-AzIntegrationAccountPartner.md)


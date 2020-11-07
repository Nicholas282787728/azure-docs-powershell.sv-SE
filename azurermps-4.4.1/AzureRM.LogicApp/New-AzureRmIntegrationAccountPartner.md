---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 2B5FC268-4888-4AEB-B125-7263CF2E4DCD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccountPartner.md
ms.openlocfilehash: da4ea8acd09fadbead53d54618f04597795c45c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758395"
---
# <span data-ttu-id="8b891-101">New-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="8b891-101">New-AzureRmIntegrationAccountPartner</span></span>

## <span data-ttu-id="8b891-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8b891-102">SYNOPSIS</span></span>
<span data-ttu-id="8b891-103">Skapar en integrerings konto partner.</span><span class="sxs-lookup"><span data-stu-id="8b891-103">Creates an integration account partner.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b891-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8b891-104">SYNTAX</span></span>

```
New-AzureRmIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String>
 [-PartnerType <String>] -BusinessIdentities <Object> [-Metadata <Object>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b891-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8b891-105">DESCRIPTION</span></span>
<span data-ttu-id="8b891-106">Cmdleten **New-AzureRmIntegrationAccountPartner** skapar en integrerings konto partner.</span><span class="sxs-lookup"><span data-stu-id="8b891-106">The **New-AzureRmIntegrationAccountPartner** cmdlet creates an integration account partner.</span></span>
<span data-ttu-id="8b891-107">Denna cmdlet returnerar ett objekt som representerar integrerings konto partnern.</span><span class="sxs-lookup"><span data-stu-id="8b891-107">This cmdlet returns an object that represents the integration account partner.</span></span>
<span data-ttu-id="8b891-108">Ange integrerings konto namn, resurs grupps namn, partner namn och partner identiteter.</span><span class="sxs-lookup"><span data-stu-id="8b891-108">Specify the integration account name, resource group name, partner name, and partner identities.</span></span>

<span data-ttu-id="8b891-109">De fil värden för mallfiler som du anger i kommando raden har högre prioritet än värden för Mallkategorier i ett Template parameter-objekt.</span><span class="sxs-lookup"><span data-stu-id="8b891-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

<span data-ttu-id="8b891-110">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="8b891-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="8b891-111">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="8b891-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="8b891-112">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="8b891-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="8b891-113">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="8b891-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="8b891-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8b891-114">EXAMPLES</span></span>

### <span data-ttu-id="8b891-115">Exempel 1: skapa en integrations konto partner</span><span class="sxs-lookup"><span data-stu-id="8b891-115">Example 1: Create an integration account partner</span></span>
```
PS C:\>New-AzureRmIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner22" -PartnerType "B2B" -BusinessIdentities $BusinessIdentities
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/partners/IntegrationAccountPartner1
Name               : IntegrationAccountPartner1
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/26/2016 7:29:30 PM
ChangedTime        : 3/26/2016 7:29:30 PM
BusinessIdentities : [{"Qualifier":"ZZ","Value":"AA"},{"Qualifier":"XX","Value":"GG"}]
Metadata           :
```

<span data-ttu-id="8b891-116">Det här kommandot skapar integrerings konto partnern med namnet IntegrationAccountPartner22 i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="8b891-116">This command creates the integration account partner named IntegrationAccountPartner22 in the specified resource group.</span></span>

## <span data-ttu-id="8b891-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8b891-117">PARAMETERS</span></span>

### <span data-ttu-id="8b891-118">-BusinessIdentities</span><span class="sxs-lookup"><span data-stu-id="8b891-118">-BusinessIdentities</span></span>
<span data-ttu-id="8b891-119">Anger företags identitet för integrerings konto partnern.</span><span class="sxs-lookup"><span data-stu-id="8b891-119">Specifies business identities for the integration account partner.</span></span>
<span data-ttu-id="8b891-120">Ange en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="8b891-120">Specify a hash table.</span></span>

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

### <span data-ttu-id="8b891-121">-Metadata</span><span class="sxs-lookup"><span data-stu-id="8b891-121">-Metadata</span></span>
<span data-ttu-id="8b891-122">Anger ett metadataobjekt för partnern.</span><span class="sxs-lookup"><span data-stu-id="8b891-122">Specifies a metadata object for the partner.</span></span>

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

### <span data-ttu-id="8b891-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="8b891-123">-Name</span></span>
<span data-ttu-id="8b891-124">Anger namnet på ett integrations konto.</span><span class="sxs-lookup"><span data-stu-id="8b891-124">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="8b891-125">-PartnerName</span><span class="sxs-lookup"><span data-stu-id="8b891-125">-PartnerName</span></span>
<span data-ttu-id="8b891-126">Anger ett namn på integrations konto partnern.</span><span class="sxs-lookup"><span data-stu-id="8b891-126">Specifies a name for the integration account partner.</span></span>

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

### <span data-ttu-id="8b891-127">-PartnerType</span><span class="sxs-lookup"><span data-stu-id="8b891-127">-PartnerType</span></span>
<span data-ttu-id="8b891-128">Anger typen av integrations konto.</span><span class="sxs-lookup"><span data-stu-id="8b891-128">Specifies the type of the integration account.</span></span>
<span data-ttu-id="8b891-129">Den här parametern har stöd för typen B2B.</span><span class="sxs-lookup"><span data-stu-id="8b891-129">This parameter supports the type B2B.</span></span>

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

### <span data-ttu-id="8b891-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b891-130">-ResourceGroupName</span></span>
<span data-ttu-id="8b891-131">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="8b891-131">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="8b891-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8b891-132">-Confirm</span></span>
<span data-ttu-id="8b891-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8b891-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b891-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b891-134">-WhatIf</span></span>
<span data-ttu-id="8b891-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8b891-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b891-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8b891-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b891-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b891-137">-DefaultProfile</span></span>
<span data-ttu-id="8b891-138">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8b891-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b891-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b891-139">CommonParameters</span></span>
<span data-ttu-id="8b891-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b891-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b891-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b891-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b891-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8b891-142">INPUTS</span></span>

## <span data-ttu-id="8b891-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8b891-143">OUTPUTS</span></span>

### <span data-ttu-id="8b891-144">Microsoft. Azure. Management. Logic. Models. IntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="8b891-144">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span></span>

## <span data-ttu-id="8b891-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8b891-145">NOTES</span></span>

## <span data-ttu-id="8b891-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8b891-146">RELATED LINKS</span></span>

[<span data-ttu-id="8b891-147">Get-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="8b891-147">Get-AzureRmIntegrationAccountPartner</span></span>](./Get-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="8b891-148">Remove-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="8b891-148">Remove-AzureRmIntegrationAccountPartner</span></span>](./Remove-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="8b891-149">Set-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="8b891-149">Set-AzureRmIntegrationAccountPartner</span></span>](./Set-AzureRmIntegrationAccountPartner.md)



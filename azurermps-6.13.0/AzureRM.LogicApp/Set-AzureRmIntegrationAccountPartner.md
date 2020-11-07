---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 9B3B6AD4-C37C-4877-9864-9FB2E3B0BDAB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/set-azurermintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountPartner.md
ms.openlocfilehash: ca7e043d8205800322469a59cea6c17ceb96eff6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757596"
---
# <span data-ttu-id="22475-101">Set-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="22475-101">Set-AzureRmIntegrationAccountPartner</span></span>

## <span data-ttu-id="22475-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="22475-102">SYNOPSIS</span></span>
<span data-ttu-id="22475-103">Ändrar en integrerings konto partner.</span><span class="sxs-lookup"><span data-stu-id="22475-103">Modifies an integration account partner.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22475-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="22475-104">SYNTAX</span></span>

```
Set-AzureRmIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String>
 [-PartnerType <String>] [-BusinessIdentities <Object>] [-Metadata <Object>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22475-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="22475-105">DESCRIPTION</span></span>
<span data-ttu-id="22475-106">Cmdleten **set-AzureRmIntegrationAccountPartner** ändrar en integrations konto partner.</span><span class="sxs-lookup"><span data-stu-id="22475-106">The **Set-AzureRmIntegrationAccountPartner** cmdlet modifies an integration account partner.</span></span>
<span data-ttu-id="22475-107">Denna cmdlet returnerar ett objekt som representerar integrerings konto partnern.</span><span class="sxs-lookup"><span data-stu-id="22475-107">This cmdlet returns an object that represents the integration account partner.</span></span>
<span data-ttu-id="22475-108">Ange integrerings konto namn, resurs grupps namn och partner namn.</span><span class="sxs-lookup"><span data-stu-id="22475-108">Specify the integration account name, resource group name, and partner name.</span></span>
<span data-ttu-id="22475-109">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="22475-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="22475-110">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="22475-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="22475-111">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="22475-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="22475-112">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="22475-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="22475-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="22475-113">EXAMPLES</span></span>

### <span data-ttu-id="22475-114">Exempel 1: ändra en integrations konto partner</span><span class="sxs-lookup"><span data-stu-id="22475-114">Example 1: Modify an integration account partner</span></span>
```
PS C:\>Set-AzureRmIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner22" -PartnerType "B2B" -BusinessIdentities $BusinessIdentities
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/partners/IntegrationAccountPartner1
Name               : IntegrationAccountPartner1
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/26/2016 7:29:30 PM
ChangedTime        : 3/26/2016 7:29:30 PM
BusinessIdentities : [{"Qualifier":"ZZ","Value":"AA"},{"Qualifier":"XX","Value":"GG"}]
Metadata
```

<span data-ttu-id="22475-115">Det här kommandot ändra integrerings konto partnern med namnet IntegrationAccountPartner22 i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="22475-115">This command modify the integration account partner named IntegrationAccountPartner22 in the specified resource group.</span></span>

## <span data-ttu-id="22475-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="22475-116">PARAMETERS</span></span>

### <span data-ttu-id="22475-117">-BusinessIdentities</span><span class="sxs-lookup"><span data-stu-id="22475-117">-BusinessIdentities</span></span>
<span data-ttu-id="22475-118">Anger företags identitet för integrerings konto partnern.</span><span class="sxs-lookup"><span data-stu-id="22475-118">Specifies business identities for the integration account partner.</span></span>
<span data-ttu-id="22475-119">Ange en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="22475-119">Specify a hash table.</span></span>

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

### <span data-ttu-id="22475-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22475-120">-DefaultProfile</span></span>
<span data-ttu-id="22475-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="22475-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="22475-122">-Force</span><span class="sxs-lookup"><span data-stu-id="22475-122">-Force</span></span>
<span data-ttu-id="22475-123">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="22475-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="22475-124">-Metadata</span><span class="sxs-lookup"><span data-stu-id="22475-124">-Metadata</span></span>
<span data-ttu-id="22475-125">Anger ett metadataobjekt för partnern.</span><span class="sxs-lookup"><span data-stu-id="22475-125">Specifies a metadata object for the partner.</span></span>

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

### <span data-ttu-id="22475-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="22475-126">-Name</span></span>
<span data-ttu-id="22475-127">Anger namnet på ett integrations konto.</span><span class="sxs-lookup"><span data-stu-id="22475-127">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="22475-128">-PartnerName</span><span class="sxs-lookup"><span data-stu-id="22475-128">-PartnerName</span></span>
<span data-ttu-id="22475-129">Anger namnet på integrations konto partnern.</span><span class="sxs-lookup"><span data-stu-id="22475-129">Specifies the name of the integration account partner.</span></span>

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

### <span data-ttu-id="22475-130">-PartnerType</span><span class="sxs-lookup"><span data-stu-id="22475-130">-PartnerType</span></span>
<span data-ttu-id="22475-131">Anger typen av integrations konto.</span><span class="sxs-lookup"><span data-stu-id="22475-131">Specifies the type of the integration account.</span></span>
<span data-ttu-id="22475-132">Den här parametern har stöd för typen B2B.</span><span class="sxs-lookup"><span data-stu-id="22475-132">This parameter supports the type B2B.</span></span>

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

### <span data-ttu-id="22475-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22475-133">-ResourceGroupName</span></span>
<span data-ttu-id="22475-134">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="22475-134">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="22475-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="22475-135">-Confirm</span></span>
<span data-ttu-id="22475-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="22475-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22475-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22475-137">-WhatIf</span></span>
<span data-ttu-id="22475-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="22475-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22475-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="22475-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22475-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22475-140">CommonParameters</span></span>
<span data-ttu-id="22475-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22475-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22475-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22475-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22475-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="22475-143">INPUTS</span></span>

### <span data-ttu-id="22475-144">System. String</span><span class="sxs-lookup"><span data-stu-id="22475-144">System.String</span></span>

## <span data-ttu-id="22475-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="22475-145">OUTPUTS</span></span>

### <span data-ttu-id="22475-146">Microsoft. Azure. Management. Logic. Models. IntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="22475-146">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span></span>

## <span data-ttu-id="22475-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="22475-147">NOTES</span></span>

## <span data-ttu-id="22475-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="22475-148">RELATED LINKS</span></span>

[<span data-ttu-id="22475-149">Get-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="22475-149">Get-AzureRmIntegrationAccountPartner</span></span>](./Get-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="22475-150">New-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="22475-150">New-AzureRmIntegrationAccountPartner</span></span>](./New-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="22475-151">Remove-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="22475-151">Remove-AzureRmIntegrationAccountPartner</span></span>](./Remove-AzureRmIntegrationAccountPartner.md)

